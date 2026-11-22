# Google Ads Platform Registry

**Last verified:** 2026-11-12  
**Freshness class:** High-change; recheck within 30 days or whenever current behavior affects a decision.

Read this reference for current Google Ads AI, automation, controls, reporting, or interface terminology. Apply the root `library/contracts/PLATFORM-CURRENCY.md` contract.

## Current mappings

| Stable concept | Current official product label or capability | Verified scope |
|---|---|---|
| Search automation layer | **AI Max for Search campaigns** | An optimization layer activated inside existing eligible Search campaigns, not a separate campaign type. Its documented core features include search term matching and asset optimization. |
| Automated text adaptation | **Text customization** | Google documents this as the current name for the capability formerly called automatically created assets within AI Max. |
| Dynamic landing-page selection | **Final URL expansion** | A documented asset-optimization feature; dependencies and URL controls must be checked in the current account. |
| AI Max targeting and URL controls | **Locations of interest**, **brand settings**, **URL inclusions and URL exclusions** | Documented AI Max campaign-level controls alongside asset optimization. Confirm availability and defaults in the current account. |
| Cross-inventory automated campaign | **Performance Max** | Campaign type using Google inventory and automated optimization toward configured conversion goals. |
| PMax channel visibility | **Channel performance report** | Google documents campaign-level channel and ad-format reporting across Search, Display, YouTube, Discover, Maps, Gmail and Search partners. Documented date-range availability covers dates after 2025-06-06. Confirm account availability and metric scope before claiming visibility. |
| PMax query exclusion | **Performance Max campaign negative keywords** | Google documents campaign- and account-level negative-keyword controls for Search and Shopping inventory only. Brand exclusions remain a separate control. |

## First-party sources

- [Set up AI Max for Search campaigns](https://support.google.com/google-ads/answer/15909989?hl=en) — product type, settings, dependencies, and setup.
- [How AI Max for Search campaigns works](https://support.google.com/google-ads/answer/15910187?hl=en) — feature composition and renamed controls.
- [About AI Max experiments](https://support.google.com/google-ads/answer/16450159?hl=en) — controlled trial capability and limitations.
- [About the channel performance report for Performance Max](https://support.google.com/google-ads/answer/16260130?hl=en) — documented channel-reporting scope.
- [Negative keywords in Performance Max campaigns](https://support.google.com/google-ads/answer/15726455?hl=en) — campaign/account control and inventory scope.
- [Search targeting and controls for Performance Max](https://support.google.com/google-ads/answer/16672776) — current control family.

## Verification record

**2026-11-12 — recheck of the seven mappings against the first-party sources listed above.** No mapping changed. Six were confirmed from the fetched help pages: AI Max as an optimization layer, text customization as the rename of automatically created assets, final URL expansion, the AI Max control family, the channel performance report and Performance Max negative keywords. The channel performance report wording now follows the page ("any date range after June 6, 2025"); the page also covers Demand Gen. The Performance Max campaign-type row was not reverified, because none of the listed sources defines the campaign type; it is carried forward from 2026-09-22. Google's AI Max experiments page currently excludes campaigns with text customization enabled from that setup flow. The Quality Score note in the watchlist was confirmed against its page on the same date. The pages were read through an automated fetch that returns extracted text, and no Google Ads account was inspected, so every row stays *officially documented*, not account-visible.

**2026-09-22 — recheck of all six mappings against the first-party sources listed above.** No mapping changed; every previously recorded label and scope remains officially documented.

Confirmed unchanged: AI Max is explicitly documented as an optimization layer and not a new campaign type; text customization is the documented rename of automatically created assets; negative keywords apply to Search and Shopping inventory at campaign and account level; brand exclusions are documented separately from negative keywords.

Added from the same recheck: the AI Max control family (locations of interest, brand settings, URL inclusions and exclusions), the channel performance report's channel list, and its documented date-range availability from 2025-06-06. Evidence state for every row above is *officially documented*; none of it is account-visible here, because no Google Ads account was inspected.

## Watchlist

### Search asset and offline-outcome addition, 2026-09-30

The core mappings above were last rechecked on the date in the header. [Search asset validation](search-asset-validation.md) separately records the 2026-09-30 first-party check for RSA assembly/input constraints and keyword insertion. [Google offline outcome validation](../../tracking-measurement/references/google-offline-outcome-validation.md) records current method/migration checks for offline lead outcomes. These additions are officially documented checks, not account-visible availability or client effectiveness evidence.

Google's [Quality Score guidance](https://support.google.com/google-ads/answer/6167123?hl=en), checked 2026-11-12, treats the displayed Quality Score as a diagnostic rather than an auction input or a business KPI. Do not import Shopify tutorials' simple bid-times-displayed-score auction formula or optimize that score instead of the actual business outcome.

Reverify AI Max defaults and eligibility, feature dependencies, DSA migration timelines, PMax reporting columns and availability, negative-keyword limits/scope, search-theme behavior, brand controls, conversion-goal behavior, bidding strategies, attribution options, and policy/consent requirements.

Do not convert Google product claims into expected client impact. Confirm the current account, measurement integrity, economics, and a reversible test design.
