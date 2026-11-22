# Meta Ads: Learning, Lead Quality, Account Health, Regulated Industries, Specs and Data Pulls

**Last verified:** 2026-11-18  
**Freshness class:** High-change; recheck within 30 days or whenever current behavior affects a decision.  
**Source:** The 2026 Google Ads and Meta Ads Playbooks (Vince Servidad), condensed; their platform sections were read against Google's and Meta's help pages on 2026-11-18.

Read this reference for learning-phase and significant-edit questions, lead quality, restrictions and rejected ads, data-source and consent rules, regulated categories, ad specs, or a Meta data pull. Apply the root `library/contracts/PLATFORM-CURRENCY.md` contract before treating any rule here as current in a specific account. "Google says" and "Meta says" mark platform claims, not expected account results. Not legal advice.

## Learning and significant edits

- Objectives: Awareness, Traffic, Engagement, Leads, App promotion, Sales. Sales, Leads and App promotion start in Advantage+ setup; Advantage+ stays on with campaign budget, Advantage+ audience (settings as suggestions) and Advantage+ placements. Multiple ad sets with ad set budgets turn it off.
- Advantage+ shopping campaigns are now Advantage+ sales campaigns; legacy shopping and app campaigns cannot be created or updated through the API after 2026-05-19.
- An ad set usually exits learning after about 50 results in the week after its last significant edit. Shops ads need 17 website purchases and 5 through Meta.
- Significant edits (restart learning): targeting, creative or optimization event changes; adding an ad; pausing 7 days or longer; changing bid strategy. Budget, bid, cost-per-result goal, ROAS goal and spending-limit changes count only if large (Meta's example: $100 to $1,000 may reset; $100 to $101 will not).
- With campaign budget: budget shifts between ad sets, an ad set-level edit, or adding an ad set do not reset other ad sets. Changing campaign bid strategy or budget can reset several.
- Learning limited is not a penalty: the ad set is unlikely to reach about 50 events in a week. Options, in order: combine ad sets and campaigns, expand the audience, raise budget, raise bid or cost control, or choose a more frequent optimization event. Budget raises on an existing system route to `$optimization-scaling`.
- Fewer ad sets and ads, up to 10 creative assets per ad. Use breakdowns instead of splitting ad sets by age, placement, language or small regions.
- Judge an ad set after it exits learning. One significant edit at a time.

## Lead quality

- Connect the CRM, then send lead stages back through the Conversions API (Conversion Leads integration). Keep the Meta Lead ID (15 to 17 digits) on every lead.
- Then use the Conversion leads performance goal; gains come after Meta's training period. It works with Instant forms; website forms need Pixel plus Conversions API with a qualified-lead event.
- Advantage+ leads campaigns support Instant forms, website forms, calls and click-to-message. Meta says Advantage+ leads campaigns had 14% lower cost per lead and 10% lower cost per qualified lead in early tests.
- When volume is fine but quality is poor, add qualifying questions to Instant forms.

## Account health and data rules

- Restrictions can hit the business portfolio, ad account, Page or person. Causes: policy breaches, hacked accounts, missing two-factor authentication, unusual or failed payments. Limits can include a daily spend cap, fewer payment features or no advertising.
- Fix in Business Support Home > Account Overview > the restricted account > What you can do (admins only). A policy-disabled ad account not reinstated within 6 months cannot be restored.
- Rejected ad: edit it (reviewed again) or request another review. Meta aims to decide within 48 hours; one re-review per ad. Do not delete an ad you want reviewed. Editing or deleting does not remove the violation; repeats lead to restrictions.
- Data source categories (Events Manager): health and wellness and some others get Core Setup (no custom parameters or URL parts after the domain), restricted standard events, or full restrictions. 60 days to categorize each source; uncategorized sources take the dataset's main category. Custom events are blocked until reviewed. Under full restrictions, use Awareness, Engagement or Traffic.
- GDPR consent: `fbq('consent', 'revoke')` before init on every page, `fbq('consent', 'grant')` after agreement. Safe rule: send Conversions API events only for people who agreed. Meta says each company is responsible for its own GDPR compliance.
- US states: the Limited Data Use flag covers 14 states (November 2026) on Pixel and Conversions API, for people who opted out, with legal advice. Retargeting and measurement weaken.

## Regulated industries

- Special Ad Categories: Financial products and services (replaced Credit; required since 2025-01-21 for advertisers in or reaching the US), Employment, Housing. For the US, and some Canada and European reach, age, gender, ZIP or postal code, exclusions, lookalikes and saved audiences are limited or unavailable. Social issues, elections or politics: authorization and a "Paid for by" disclaimer; not allowed in the EU.
- Health and wellness: no claims to cure the incurable diseases Meta lists (including diabetes, cancer, HIV); symptom-management claims allowed. Weight loss and cosmetic procedures: 18+ only. No negative statements about a person's looks; no timed result promises without qualifiers.
- Point the user to the full policy for the product and country.

## Ad specs (Meta Ads Guide, November 2026)

Images: JPG or PNG, max 30MB. Video: MP4 or MOV, H.264, max 4GB; captions and sound recommended.

| Placement | Shape | Size | Text limits |
|---|---|---|---|
| Facebook Feed (image) | 4:5 | 1440 x 1800 | Primary 50-150, headline 27 |
| Instagram Feed (image) | 4:5 | 1440 x 1800 | Primary 125, headline 40, 30 hashtags max |
| Instagram Feed (video) | 9:16 recommended | 1080 x 1920 | Primary 125; 1 second to 60 minutes |
| Stories (FB and IG) | 9:16 | 1440 x 2560 | Primary 125, headline 40 (FB); video to 3 min (FB), 60 min (IG) |
| Facebook Reels | 9:16 | 1440 x 2560 | Primary 40, headline 55 |
| Instagram Reels | 9:16 | 1440 x 2560 | Primary 44; video to 15 minutes |
| Ads on Facebook Reels (overlay) | 1:1 | 1080 x 1080 min | Primary 60, headline 10; video 4-15 seconds |
| Marketplace, Search Results, In-Stream | 1:1 (1.91:1 on some) | 1080 x 1080 min | Primary 125, headline 40, description 30 |
| Right Column | 1:1 | 1080 x 1080 min | Headline 40, no text on image |
| Carousel | 1:1 (IG image-only 4:5) | 1080 x 1080 min | 2-10 cards; FB Feed primary 80, headline 20, description 18 |
| Collection | 1.91:1 to 1:1 (FB Reels 9:16 to 1:1) | 1080 x 1080 min | Primary 125, headline 40; Instant Experience required |

9:16 safe zones: top 14%, bottom 35%, 6% each side. Aspect-ratio tolerance: 1% on Instagram and Stories, 3% on most Facebook placements.

## Data pulls

Use the Meta ads MCP server or an Ads Manager export. Last 30 days vs the 30 before; one attribution setting for the whole pull, stated.

- Campaign and ad set: name, Delivery, Objective, Performance goal, Bid strategy, Budget, Amount spent, Results, Cost per result, Purchase ROAS (sales), Frequency, Reach, Last significant edit, Attribution setting.
- Creative: Ad name, Format, Amount spent, Results, Cost per result, link CTR, 3-second video plays and Impressions (hook rate), ThruPlays, Creative diversity, Delivery status (Creative limited / Creative fatigue).
- Breakdowns: Placement, Age, Gender, Platform; audience segments (new, engaged, existing) for Advantage+ sales.
- Events Manager: events by source (browser, server), deduplication, Event Match Quality per event, Diagnostics.
- Activity history: last 14 days, all changes, by whom.
- If a column is missing, say so. Never invent columns.
