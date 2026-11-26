# Paid scaling readiness gates (Meta & Google), pacing and guardrails

Use alongside [scale-paid-guide.md](scale-paid-guide.md) whenever an owner asks whether to raise spend on Meta or Google Ads, expand placements/campaigns, or diagnose why efficiency collapses as budgets climb. Never endorse a universal percentage-jump formula (such as raising budgets every few days regardless of signal); every scaling move requires owner approval and source-of-truth guardrails.

## 1. Six readiness gates and the proof standard

Verify all six gates before approving higher ad spend:
1. **Unit economics:** Allowable CAC from contribution margin and observed cohort payback (`17-unit-economics`) supports higher **marginal** acquisition cost.
2. **Measurement integrity:** Store/CRM customer counts reconcile with ad-platform conversions; any double-firing pixel or offline-import lag is repaired (`17-tracking-plan`).
3. **Primary constraint:** Acquisition capacity is truly the bottleneck, not onboarding stalls, churn (`15-churn-prevention`), stockout risk, or fulfilment SLA (`19-constraint-finder`).
4. **Operational capacity:** Team, onboarding slots, sales calendar, and inventory can absorb higher volume without breaking delivery quality (`context/offer.md`).
5. **Creative supply capacity:** Creative pipeline can feed net-new distinct concepts as frequency and spend climb (`09-ad-creative`, `18-creative-testing`).
6. **Causal proof standard:** Platform ROAS alone is `C0` evidence (`17-incrementality`); sustained budget jumps or channel-mix shifts warrant `C3` quasi-experimental or `C4` randomized lift proof alongside marginal blended MER checks.

## 2. Controlled budget steps, pacing and recovery

- Replace overnight doubling with **owner-approved incremental steps**, held long enough to capture full conversion/sales-cycle lag before evaluating marginal cost per new customer (`marginal spend delta / marginal new customers`).
- Pre-write explicit **hold, guardrail, and rollback triggers** before increasing spend (e.g., roll back if blended MER or verified marginal CAC breaches the ceiling across a full decision window after accounting for lag).

## 3. Meta Ads scaling modes (*to confirm* against live Meta controls)

- **Controlled budget steps:** Scale consolidated winning campaigns gradually rather than duplicating ad sets into fragmented auctions without a distinct country, margin, or offer hypothesis.
- **Creative diversity and format expansion:** Supply structurally diverse concepts (`09-ad-creative`) and valid placements rather than forcing extra spend into one fatigued asset (`11-paid-social`). Keep winning entity/creative IDs intact where practical.
- **Catalog, qualified-event and value scaling:** Upgrade optimization events from raw leads to CRM-qualified Conversion Leads or Purchase Value (`17-tracking-plan`) when signal volume confirms; inspect Advantage+ Sales Product Sets rather than blinding spend onto thin-margin SKUs.
- Rising frequency alone never proves creative fatigue; verify falling response on stable audiences before swapping winners out.

## 4. Google Ads scaling modes (*to confirm* against live Google Ads controls)

- **Separate Brand vs. Non-Brand completely:** Never justify higher non-brand spend on blended Search averages inflated by cheap Brand clicks (`11-paid-search`).
- **Search scaling paths:** Capture lost impression share on proven exact/phrase profit winners -> expand adjacent high-intent commercial themes with dedicated landing pages (`12-landing-page`) -> test Search automation / AI Max with tight URL and brand exclusions only when offline conversion imports are clean.
- **Shopping and Performance Max:** Segment SKUs by contribution margin and stock (`11-shopping-feeds`), exclude money-losing SKUs hidden inside campaign averages, add asset groups only for distinct offers/categories, and inspect PMax channel/search-term reports carefully.
- Treat Google Performance Planner, bid simulators, and automated Recommendations as hypotheses, never proof of incremental lift; disable auto-apply recommendations that conflict with controlled experiment design (`17-incrementality`).

## Sources

Meta Media Buying study guide (Feb 2026); Google Ads Search/PMax/Shopping optimization principles; The Complete Marketing System, section 19 Growth (Servidad, 2026).
