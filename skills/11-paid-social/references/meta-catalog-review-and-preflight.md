# Meta Catalog Readiness, Audience Controls, 6-Step Review and Launch Preflight

Distilled from official 2026 Meta Blueprint study guides (Digital Marketing Associate Jan 2026, Media Buying Feb 2026, Media Planning Feb 2026). Confirm all current Ads Manager labels, Advantage+ defaults, and Commerce Manager eligibility against live Meta documentation and the ad account (*to confirm*).

## 1. Catalog and Product Set readiness

Before launching Advantage+ Sales catalog campaigns or Dynamic Product Ads:
1. **Product truth:** Reconcile SKU/variant IDs, price, currency, stock availability, imagery, and destination URLs against the store catalog. Avoid multiple feed integrations overwriting the same items simultaneously.
2. **Product Sets over duplicate catalogs:** Express commercial inclusion and exclusion rules (margin tiers, in-stock hero SKUs, country/currency filters) using clean Product Sets (`11-shopping-feeds` for feed taxonomy; `12-retargeting` for dynamic product retargeting).
3. **Catalog Match Rate vs. Event Match Quality (EMQ):** Confirm `ViewContent`, `AddToCart`, and `Purchase` event `content_ids` match actual catalog variant IDs (`17-tracking-plan`), separate from customer PII hashing quality (EMQ). Never pad sets with out-of-stock or unshippable variants to hit arbitrary catalog size heuristics.

## 2. Audience controls vs. suggestions

Record every audience input with: `business reason | source and window | proposed audience | hard control or suggestion | account evidence`.
- **Hard Controls** restrict delivery boundaries where supported (country/region, minimum age, language, Special Ad Category limits, Custom Audience exclusions for buyers or disqualified segments).
- **Audience Suggestions** (such as Advantage+ Audience inputs *to confirm* in current ad set UI) only guide initial exploration and can expand beyond the suggested group when the system predicts conversions elsewhere. Never present an audience suggestion as a strict retargeting or ICP guarantee.
- **Reach and overlap arithmetic:** Never sum daily reach into unique campaign reach. Compare overlapping ad sets on incremental business outcomes and distinct margin/offer reasons before consolidating; overlap alone does not automatically prove harmful auction self-competition.

## 3. Meta 6-step account results review and the breakdown-effect trap

Audit existing Meta campaigns in this exact order (Meta Media Buying Study Guide 2026):
1. Inspect goal-aligned **Results** and **Cost per result** against the exact counting definition (never pool purchases, raw leads, and qualified SQLs into one blended total).
2. Inspect supporting delivery, response, visit, and conversion measures (`CPM`, `Reach`, `Frequency`, `Outbound CTR`, `Landing page views`).
3. Inspect campaign and ad-set configuration (objective, conversion location, performance goal, attribution setting, exclusions).
4. Evaluate results and setup together across matched date ranges and unchanged attribution windows.
5. Repeat across sibling ad sets to isolate structural differences.
6. Rank bounded optimization opportunities (`09-ad-creative`, `17-tracking-plan`, `19-scale-paid`).

**The breakdown-effect trap:** Ads Manager demographic, placement, and dynamic-creative breakdowns show **marginal algorithmic allocation**, not average profitability per cell. The delivery system shifts budget toward pockets with cheaper marginal conversions; turning off "higher CPA" placements or age brackets from breakdown averages alone frequently hurts total ad-set efficiency and pushes overall CPA up. Form hypotheses from breakdowns, then test cleanly rather than knee-jerk pruning.

## 4. Launch access and brand suitability preflight

Before pressing publish:
- **Business Portfolio least-privilege map:** Verify owner and task-level access for Ad Account, Facebook Page, Instagram identity, Dataset/Pixel, Catalog, and Domain without ever collecting passwords, cookies, or personal tokens.
- **Brand suitability and exclusions:** Match account requirements to supported placement controls, inventory filters, and block lists (*to confirm* in Brand Safety controls), noting reach/CPM tradeoffs.
- **Rejected-ad discipline:** Preserve the rejected ad ID, exact policy reason, and affected asset/URL (`20-compliance`); fix the root claim/asset or appeal via the official flow rather than duplicating accounts or cloaking URLs. Verify whether post-publish review delays impact timed launches.

## Sources

Meta Certified Digital Marketing Associate (Jan 2026), Media Buying (Feb 2026), and Media Planning (Feb 2026) study guides; Meta Ads Manager documentation (to confirm current UI controls).
