# Meta Ads Platform Registry

**Last verified:** 2026-11-12  
**Freshness class:** High-change; recheck within 30 days or whenever current behavior affects a decision.

Read this reference for current Meta AI, automation, audience, placement, objective, or interface terminology. Apply the root `library/contracts/PLATFORM-CURRENCY.md` contract.

## Current mappings

| Stable concept | Current official product label or capability | Verified scope |
|---|---|---|
| AI-assisted audience expansion | **Advantage+ audience** | Expands the eligible audience pool the delivery system can search. Documented non-negotiable constraints that are not expanded: location, minimum age, language, and Custom Audience exclusions. Confirm availability, defaults, and control behavior in the current ad account. |
| Automated inventory selection | **Advantage+ placements** | Allocates delivery across eligible Meta placements and is documented as the default setting in the Marketing API. Availability and placement inventory can vary by objective, format, market, and account. |
| Automated shopping campaign | **Advantage+ Sales** | Current documented name; formerly Advantage+ Shopping Campaigns (ASC). Treat older ASC naming and its legacy API path as outdated. |
| Automated app campaign | **Advantage+ App** | Current documented name; formerly Advantage+ App Campaigns (AAC). |
| Prior-relationship audience | **Custom Audience** plus an exact source, membership window, and exclusions | “Retargeting” remains a strategy label, not a complete Meta configuration. Carried forward from 2026-08-22; not reverified against Meta help since. |
| Delivery outcome selection | **Performance goal** and selected optimization event | Record separately from campaign objective, conversion location, dataset/Meta Pixel, and attribution setting. Carried forward from 2026-08-22; not reverified against Meta help since. |

## First-party sources

- [Advantage+ audience](https://www.facebook.com/business/ads/meta-advantage-plus/audience) — audience suggestions, expansion, and documented controls.
- [Advantage+ placements](https://www.facebook.com/business/ads/meta-advantage-plus/placements) — automated placement scope and product framing.
- [Advantage+ audience, Marketing API reference](https://developers.facebook.com/documentation/ads-commerce/marketing-api/audiences/reference/targeting-expansion/advantage-audience) — expansion behavior and non-negotiable constraints.
- [Advantage+ campaigns, Marketing API](https://developers.facebook.com/documentation/ads-commerce/marketing-api/advantage-campaigns) — current campaign naming for Sales, App and Leads, placements default, and version deprecations.

Meta help content and account creation flows can be login-, market-, and rollout-dependent. If a precise creation default, eligibility rule, objective, performance goal, conversion location, dataset, event, attribution option, or Advantage+ control affects the decision, verify it in first-party help and then in the actual account.

## Verification record

**2026-11-12 — recheck against Meta first-party developer documentation.** The header date covers the four developer-documented rows only.

Verified unchanged: **Advantage+ audience** (expands the eligible pool; location, minimum age, language and Custom Audience exclusions are not expanded), **Advantage+ placements** as the Marketing API default, and **Advantage+ Sales** and **Advantage+ App** as the current names for the former ASC and AAC. The placements clause on availability by objective, format, market and account was not reverified.

Seen on the same Advantage+ campaigns page and not yet added as mappings: the page now covers **Advantage+ leads** campaigns for the leads objective; and it states that creating ASC through `smart_promotion_type` already fails on v24.0, fails on every version from v25.0, and that legacy ASC and AAC campaigns are blocked from edits from v26.0. Confirm against the page before relying on a version number.

**Not verified this cycle:** `www.facebook.com/business` pages are still disallowed to automated fetching, so the two help-surface sources, the **Custom Audience** row and the **Performance goal** row remain carried forward from 2026-08-22, as their table cells now say. The developer pages were read through an automated fetch that returns extracted text, and no ad account was inspected: evidence state is *officially documented*, not account-visible.

**2026-09-22 — recheck against Meta first-party developer documentation.**

Verified unchanged: **Advantage+ audience** and **Advantage+ placements** remain the current official labels. The audience reference documents expansion of the eligible pool while location, minimum age, language and Custom Audience exclusions are explicitly not expanded; placements is documented as the API default.

**Changed since the 2026-08-22 registry:** Meta's documented campaign naming has moved to **Advantage+ Sales** (formerly Advantage+ Shopping Campaigns / ASC) and **Advantage+ App** (formerly Advantage+ App Campaigns / AAC). The documentation also records that the legacy `smart_promotion_type` API path for ASC stops working from v25.0. These rows are new to this registry; no existing skill decision rule referenced the old names, so no rule change was required.

**Not verified this cycle:** `www.facebook.com/business` help pages are disallowed to automated fetching by Meta's robots rules, so the Custom Audience and Performance goal rows were not re-confirmed against the Ads Manager help surface in this cycle. Both remain carried forward from the 2026-08-22 verification and are unchanged in the developer documentation reviewed. Evidence state: *officially documented* for the Advantage+ rows; the two carried-forward rows should be treated as documented-but-not-reverified until an account or help-surface check is possible. No Meta ad account was inspected, so nothing here is account-visible.

## Watchlist

Reverify Advantage+ campaign/audience naming and defaults, strict controls versus suggestions, placement inventory, creative automation, objective and performance-goal options, attribution settings, event/dataset terminology, Conversions API and deduplication guidance, reporting breakdown availability, and experiment/lift tooling.

Do not call delivery volatility an “algorithm change” without official evidence. Diagnose auction, audience, creative, destination, offer, measurement, and business demand separately; label causal explanations as observed, experimentally observed, inferred, or unknown.
