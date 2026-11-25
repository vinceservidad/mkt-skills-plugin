# Google Ads GAQL Diagnostics, Calls, GA4 and Compliance

Use when `inputs/` holds Google Ads exports, GAQL results, conversion-setup notes, call tracking details, GA4 linking questions, or regulated/competitor checks. Platform rules and API fields are high-change: cite official docs with URL and date checked, verify in the live account, or mark *to confirm*. Not legal advice.

## 1. Core GAQL diagnostic pulls (read-only)

Default window: `LAST_30_DAYS` compared against the prior 30 days. Never fill missing or refused pulls with estimates.

1. **Campaign health and lost impression share:**
   ```sql
   SELECT campaign.name, campaign.status, campaign.advertising_channel_type, campaign.bidding_strategy_type, campaign.primary_status, campaign.primary_status_reasons, campaign_budget.amount_micros, metrics.cost_micros, metrics.conversions, metrics.conversions_value, metrics.cost_per_conversion, metrics.search_budget_lost_impression_share, metrics.search_rank_lost_impression_share
   FROM campaign WHERE campaign.status = 'ENABLED' AND segments.date DURING LAST_30_DAYS
   ```
2. **Conversion action setup (no date range; checks `phone_call_duration_seconds` and `metrics.conversion_last_conversion_date`):**
   ```sql
   SELECT conversion_action.name, conversion_action.category, conversion_action.primary_for_goal, conversion_action.counting_type, conversion_action.type, conversion_action.phone_call_duration_seconds, metrics.conversion_last_conversion_date
   FROM conversion_action WHERE conversion_action.status = 'ENABLED'
   ```
3. **Conversion action counts (last 30 days):**
   ```sql
   SELECT conversion_action.name, conversion_action.primary_for_goal, metrics.all_conversions, metrics.all_conversions_value
   FROM conversion_action WHERE conversion_action.status = 'ENABLED' AND segments.date DURING LAST_30_DAYS
   ```
4. **Zero-conversion search terms by spend:**
   ```sql
   SELECT search_term_view.search_term, campaign.name, metrics.cost_micros, metrics.clicks, metrics.conversions
   FROM search_term_view WHERE segments.date DURING LAST_30_DAYS AND metrics.conversions = 0 ORDER BY metrics.cost_micros DESC LIMIT 50
   ```
   A zero-conversion query is not automatically a negative keyword without intent and spend-sample analysis.
5. **Recent 14-day changes (`change_event` reaches back 30 days only; Editor changes are omitted):**
   ```sql
   SELECT change_event.change_date_time, change_event.change_resource_type, change_event.resource_change_operation, change_event.changed_fields, change_event.client_type, change_event.user_email, campaign.name
   FROM change_event WHERE change_event.change_date_time DURING LAST_14_DAYS AND change_event.change_resource_type IN ('CAMPAIGN', 'CAMPAIGN_BUDGET', 'AD_GROUP') ORDER BY change_event.change_date_time DESC LIMIT 200
   ```
   Check `('AD_GROUP_AD', 'AD_GROUP_CRITERION', 'CAMPAIGN_CRITERION')` for ads, keywords, and negatives. Distinguish `GOOGLE_ADS_RECOMMENDATIONS` from `GOOGLE_ADS_RECOMMENDATIONS_SUBSCRIPTION` (auto-apply).
6. **EU political ads declaration:**
   ```sql
   SELECT campaign.name, campaign.status, campaign.contains_eu_political_advertising
   FROM campaign WHERE campaign.status != 'REMOVED'
   ```

**Unit rules:** divide `cost_micros`, `cost_per_conversion`, and `amount_micros` by `1,000,000`. Impression share values are fractions (`0.51` = `51%`). If `primary_status_reasons` returns `UNKNOWN`, inspect the live Status column.

## 2. Calls, GA4 imports and Local Services Ads (*to confirm* in account)

| Call conversion source | What is actually counted |
| --- | --- |
| Calls from ads | Call and location assets or call ads |
| Calls to a website number | Google forwarding number replaces site number for ad clickers |
| Clicks on mobile site numbers | Button click only, not answered call |
| Clicks on call assets without forwarding | Estimated calls from clicks |
| Imported CRM calls | Only calls verified as qualified leads or sales with value |

- Match minimum call duration to real enquiry length; set count to *one* per call for lead generation and bid toward CRM-qualified calls when tracked.
- **GA4 rule:** keep one Primary conversion source per commercial event (never count both a native Google tag purchase/lead and an imported GA4 event for the same goal as Primary).
- For tracking fixes and offline CRM imports, hand off to `17-tracking-plan`.

## 3. Competitor ad logs, consent and regulated policies (*to confirm*)

- **Ad libraries (Google Ads Transparency Center / Meta Ad Library):** log advertiser, market, date, format, offer, angle, CTA, landing page, source URL, and check date. Ad longevity hints at continuity, never profit or conversion rate; treat competitor logs as market observations, never customer evidence.
- **EEA/UK/Switzerland Consent Mode v2:** Google says `ad_user_data` and `ad_personalization` signals affect conversion tracking, Customer Match, and remarketing eligibility (*to confirm* against current Google EU user consent docs).
- **Regulated categories & account health:** flag healthcare, pharmaceuticals, financial services, gambling, sensitive-interest personalization bans, housing/employment/credit restrictions, EU political declarations, advertiser verification deadlines, and repeated disapprovals for compliance review (`20-compliance`) before launch.
