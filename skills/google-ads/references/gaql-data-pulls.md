# Google Ads Data Pulls (GAQL)

**Last verified:** 2026-11-18  
**Freshness class:** High-change; recheck within 30 days or whenever current behavior affects a decision.  
**Source:** The 2026 Google Ads and Meta Ads Playbooks (Vince Servidad), condensed; their platform sections were read against Google's and Meta's help pages on 2026-11-18.

Read this reference before pulling Google Ads account data with the search tool. Apply the root `library/contracts/PLATFORM-CURRENCY.md` contract before treating any rule here as current in a specific account. "Google says" and "Meta says" mark platform claims, not expected account results. Not legal advice.

## Defaults

- Range: `LAST_30_DAYS`, compared with the 30 days before.
- Report exact figures. Label estimates "projected".

## Queries

1. Campaign health:
```
SELECT campaign.name, campaign.status, campaign.advertising_channel_type, campaign.bidding_strategy_type, campaign.primary_status, campaign.primary_status_reasons, campaign_budget.amount_micros, metrics.cost_micros, metrics.conversions, metrics.conversions_value, metrics.cost_per_conversion, metrics.search_budget_lost_impression_share, metrics.search_rank_lost_impression_share
FROM campaign WHERE campaign.status = 'ENABLED' AND segments.date DURING LAST_30_DAYS
```

2. Conversion actions, setup. No date range. A blank last conversion date means the action never recorded one; `phone_call_duration_seconds` is the minimum call length on call actions.
```
SELECT conversion_action.name, conversion_action.category, conversion_action.primary_for_goal, conversion_action.counting_type, conversion_action.type, conversion_action.phone_call_duration_seconds, metrics.conversion_last_conversion_date
FROM conversion_action WHERE conversion_action.status = 'ENABLED'
```

3. Conversion actions, last 30 days. `metrics.conversion_last_conversion_date` fails with a date range, so it stays in query 2.
```
SELECT conversion_action.name, conversion_action.primary_for_goal, metrics.all_conversions, metrics.all_conversions_value
FROM conversion_action WHERE conversion_action.status = 'ENABLED' AND segments.date DURING LAST_30_DAYS
```

4. Search terms with spend and no conversions:
```
SELECT search_term_view.search_term, campaign.name, metrics.cost_micros, metrics.clicks, metrics.conversions
FROM search_term_view WHERE segments.date DURING LAST_30_DAYS AND metrics.conversions = 0 ORDER BY metrics.cost_micros DESC LIMIT 50
```
A zero-conversion term is not a negative by itself; apply the `google-ads` negative-keyword rule.

5. Recent changes to campaigns, budgets and ad groups:
```
SELECT change_event.change_date_time, change_event.change_resource_type, change_event.resource_change_operation, change_event.changed_fields, change_event.client_type, change_event.user_email, campaign.name
FROM change_event WHERE change_event.change_date_time DURING LAST_14_DAYS AND change_event.change_resource_type IN ('CAMPAIGN', 'CAMPAIGN_BUDGET', 'AD_GROUP') ORDER BY change_event.change_date_time DESC LIMIT 200
```
- Rerun with `('AD_GROUP_AD', 'AD_GROUP_CRITERION', 'CAMPAIGN_CRITERION')` for ads, keywords and negatives.
- `client_type` `GOOGLE_ADS_RECOMMENDATIONS` = applied from Recommendations; `GOOGLE_ADS_RECOMMENDATIONS_SUBSCRIPTION` = auto-applied.
- `change_event` needs a `LIMIT` (10,000 at most) and reaches back 30 days only. Check that the oldest row reaches the start of the range.
- Google Ads Editor changes are not returned; check Change history in Google Ads.
- Never propose reversing a change the user or their team made on purpose.

6. EU political ads declaration (`UNSPECIFIED` = not declared):
```
SELECT campaign.name, campaign.status, campaign.contains_eu_political_advertising
FROM campaign WHERE campaign.status != 'REMOVED'
```

## Units

- `cost_micros`, `cost_per_conversion` and `amount_micros` are micros: divide by 1,000,000.
- Impression share fields are fractions (0.51 = 51%).

## Error rules

- `primary_status_reasons` can return `UNKNOWN` when the API cannot name the reason; check the Status column in Google Ads.
- If a field errors, check it with the metadata tool before retrying. Never guess field names.
- If a pull fails or is refused, report it as missing evidence; do not fill the gap with estimates.
