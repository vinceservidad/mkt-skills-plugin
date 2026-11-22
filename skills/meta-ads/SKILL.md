---
name: meta-ads
description: Audit, diagnose, or plan Meta Ads delivery, structure, audiences, placements, and ads using funnel and business evidence; not for concept, hook, or angle development, or for automatic publishing or spend changes.
---

# Meta Ads

Classify each audit, strategy, process, tactic, technique, best practice, or heuristic with [`KNOWLEDGE-TAXONOMY.md`](../../library/contracts/KNOWLEDGE-TAXONOMY.md). Name the primary type and keep documented platform capability separate from expected business impact.

## Required inputs

Collect campaign objective, conversion location, performance goal, dataset or Meta Pixel, selected optimization event, Conversions API status, attribution setting, market, dates and comparison, spend, campaign/ad-set/ad results, creative IDs, destinations, business revenue or lead-quality data, and constraints. Do not collapse those configuration fields into one “optimization” setting.

## Method

1. Confirm event quality and deduplication before treating platform results as business truth.
2. Decompose delivery (CPM, reach, frequency), response (outbound CTR or relevant attention signal), visit quality, conversion rate, value/lead quality, and profit (name the profit level and the costs included).
3. Use breakdowns only when sample sizes support them; account for aggregation and attribution bias.
4. Diagnose at the right layer: auction, objective, audience, creative, destination, offer, or measurement.
5. Treat rising frequency plus worsening response as suggestive of fatigue, not conclusive without audience and delivery context.

For substantial funnel-mode work, read [new-customer acquisition / prospecting](references/prospecting.md) or [retargeting / remarketing](references/retargeting.md) as relevant. These are strategic categories; also state the current Meta implementation such as Advantage+ audience, audience suggestions, Custom Audiences, exclusions, or other controls. For current AI, automation, audience, placement, objective, or interface claims, read [Platform Registry](references/platform-current.md) and apply the root `library/contracts/PLATFORM-CURRENCY.md` freshness gate.

For an objective-led account review, use [Meta Performance 5 decision review](references/meta-performance-five-review.md). For source-to-event gaps, use [Google/Meta signal validation](../tracking-measurement/references/google-meta-signal-validation.md) with `$tracking-measurement`.

For the supplied July 2026 guide's campaign-side creative decisions, use [Creative delivery alignment](references/meta-creative-delivery-alignment.md). Coordinate [partnership versus retailer-catalog planning](../influencer-marketing/references/meta-partnership-collaborative-planning.md) and the [creative learning agenda](../tracking-measurement/references/meta-creative-learning-agenda.md) only when required; source recommendations do not authorize account changes.

For the supplied January/February 2026 Blueprint guides, read the [source and catalog access record](references/meta-2026-guides-source-notes.md) when provenance or source conflicts matter. Use [budget and bid planning](references/meta-budget-bid-planning.md), [catalog and audience readiness](references/meta-catalog-audience-readiness.md), [launch/access preflight](references/meta-launch-access-preflight.md), or [results review](references/meta-results-review.md) only for the relevant task. These extend existing decisions; dated recommendations do not authorize account changes or establish current controls.

Use [Learning, lead quality, account health and specs](references/meta-leads-health-specs.md) when the question involves learning and significant edits, lead quality, restrictions or rejected ads, data-source or consent rules, regulated categories, ad specs, or a Meta data pull.

## Rules

- Do not fragment budgets into many ad sets without a distinct hypothesis or constraint.
- Judge broad targeting, automated placements, and automation by incremental business outcome and control needs, not ideology.
- Do not pause an ad for low CTR when it produces profitable or high-quality outcomes.
- Do not decide scaling here: route a budget increase or coverage expansion of an existing Meta system to `$optimization-scaling` and its full gate set, implement only what that decision and its authorization cover, and never treat a short window or platform ROAS alone as a reason to scale.
- Publishing, budget, bid, audience, and status changes require explicit approval.
- Do not call performance volatility an undocumented “Meta algorithm change.” Separate officially documented capability, account-visible behavior, experimentally observed impact, inference, and unknowns. Confirm account availability before recommending a current control.

## Output

Audit: measurement status; funnel decomposition; entity-level and creative findings; ranked actions; test plan; risks and unknowns.

Build plan: objective; architecture; optimization event; audience logic; creative matrix; budget logic; measurement; launch checklist; approval status.

## Library references

Owned shared library artifacts, read when their scope applies:

- [meta-ads-full-stack.md](../../library/frameworks/meta-ads-full-stack.md) — full-account decision model beyond a single audit or diagnosis.
- [meta-ads-audit.md](../../library/playbooks/meta-ads-audit.md) — step-by-step audit workflow.
- [meta-ads-optimization.md](../../library/workflows/meta-ads-optimization.md) — recurring optimization cadence.
- [campaign-brief.md](../../library/templates/campaign-brief.md) — campaign brief format, owned by $google-ads and also loaded here.

## QA

Verify attribution and event definitions, distinguish link clicks from landing-page views, connect creative IDs to results, account for frequency and spend distribution, label platform-only conclusions, check platform-registry freshness, and confirm account-visible availability for current controls.
