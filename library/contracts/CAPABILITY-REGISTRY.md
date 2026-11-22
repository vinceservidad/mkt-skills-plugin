# Capability Registry

Declares what the Marketing OS governs, what it partially covers, and what it does not cover. The Marketing Router applies this registry before routing. A capability absent from the `Governed` table has no governed specialist, regardless of any framework, playbook, template, or export file that discusses the topic.

Status definitions:

- **Governed** — a canonical skill in `.agents/skills/` owns the capability end to end.
- **Partially covered** — a canonical skill owns a defined portion. Work outside that boundary has no specialist and must be labeled.
- **Planned** — accepted on `docs/ROADMAP.md`, not yet built. Not available.
- **Unsupported** — no governed specialist and none currently scheduled.

Existence of a document is not coverage. A capability is governed only when a skill owns it, declares its evidence requirements, states its authorization boundary, and defines its output contract.

## Governed

| Capability | Owner |
|---|---|
| Request routing and owner appointment | `$marketing-router` |
| Business-level growth strategy and integrated marketing planning: objective, constraint structure (binding, co-limiting, independent, or unresolved), opportunity portfolio, priorities, non-priorities, sequencing, specialist orchestration, learning roadmap, and review governance | `$growth-strategy` |
| Marketing operations: recurring cross-skill loops, trigger/cadence governance, run state, idempotency, approval gates, execution handoffs, verification, escalation, and retirement | `$marketing-operations` |
| Engagement intake: scope, evidence grading, metric definitions, access, authorization, reusable Marketing Context | `$marketing-intake` |
| Offer strategy: commercial proposition, promised outcome, core deliverable, value architecture, bundle, risk reversal, real urgency/scarcity | `$offer-strategy` |
| Pricing and monetization: base price, value metric, package/tier architecture, payment model, discount architecture, willingness-to-pay evidence, price-change testing and migration | `$pricing-monetization` |
| Activation: first meaningful value definition, post-conversion path-to-value, time-to-value, activation friction diagnosis, interventions, and validation | `$activation` |
| Retention strategy: churn/lapse reason diagnosis, cause-matched retention/save/recovery/repeat/renewal/win-back intervention design and validation | `$retention-strategy` |
| Google Ads: Search, Shopping, Performance Max structure, queries, bidding, first build or launch planning, and settings changes inside an already-approved plan — with budget or coverage expansion of an existing account under `$optimization-scaling` | `$google-ads` |
| Meta Ads: structure, audiences, delivery, placements | `$meta-ads` |
| Creative strategy: angles, hooks, concepts, briefs, tests | `$creative-strategy` |
| Conversion Rate Optimization: conversion diagnosis of landing/product pages, forms, checkout, and pre-conversion friction; copy evaluated as a conversion variable (message scent, clarity, objection handling); test hypothesis and design — with final copy handed to `$copywriting` | `$cro` |
| Performance diagnosis: metric change, anomaly, causal triage | `$performance-diagnostics` |
| Tracking and measurement: event integrity, platform-versus-business attribution reconciliation | `$tracking-measurement` |
| Measurement validity: causal evidence grading, incrementality method selection, holdouts, geo experiments, lift studies, Marketing Mix Modeling, triangulation | `$tracking-measurement` |
| Experiment learning: test validity classification, scoped learning records, transfer status, contradiction preservation, decision-relevant experiment backlog | `$tracking-measurement` |
| Customer research: interviews, reviews, surveys, evidence synthesis | `$customer-research` |
| Ideal Customer Profile, Jobs-to-be-Done, and competitive intelligence for buyer/positioning decisions | `$icp-jtbd` |
| Optimization and scaling: paid-media readiness, marginal economics, paid-media portfolio allocation, de-scaling, recovery, budget/outcome pacing | `$optimization-scaling` |
| Retention economics: lifetime value, payback period, cohort retention, churn, lead-to-revenue cohorts | `$retention-economics` |
| Search Engine Optimization: visibility audit, technical health, content and topic strategy, ranking-change diagnosis, AI-search visibility and AI-crawler access | `$seo` |
| Copywriting: all page copy (landing-page, product-page, sales-page, and website headlines, body, offer wording, CTAs, microcopy), email, lifecycle, long-form, brand — written from supplied customer evidence, with paid-ad hooks, angles, and concepts under `$creative-strategy` and conversion diagnosis and test design under `$cro` | `$copywriting` |
| Email and lifecycle program strategy: segmentation, trigger logic, cadence, deliverability | `$lifecycle-marketing` |
| YouTube video advertising: format selection, targeting, view-through measurement fit | `$youtube-ads` |
| TikTok advertising: native creative fit, Spark Ads vs in-feed, targeting breadth, creative-fatigue cadence | `$tiktok-ads` |
| LinkedIn advertising: account/firmographic targeting, format selection, Lead Gen Forms, B2B cost-structure economics | `$linkedin-ads` |
| Influencer and creator marketing: audience authenticity/fit vetting, compensation structure, usage rights, disclosure compliance | `$influencer-marketing` |
| Affiliate and partner marketing: commission structure, attribution integrity, fraud/brand-bidding screening | `$affiliate-marketing` |
| Organic social: content strategy, cadence, algorithm-distribution fit, community management | `$organic-social` |
| Programmatic: supply-path optimization, inventory verification, fraud screening | `$programmatic` |
| Public relations: media relations, pitch strategy, crisis communications | `$public-relations` |
| Cross-channel executive reporting, recurring cadence, stakeholder scorecards | `$marketing-reporting` |
| Marketing analytics engineering: source data contracts, warehouse/pipeline design, conformed models, semantic metric layers, data-quality controls, BI/dashboard implementation, refresh/backfill governance, and pipeline source-to-model data reconciliation | `$marketing-analytics` |

## Partially covered

None currently. Requests outside the governed table must fail closed through the uncovered-request rules below rather than being silently absorbed by a neighboring skill.

Analytics engineering and BI implementation are governed by $marketing-analytics. Tracking architecture and causal measurement remain with $tracking-measurement; diagnostic interpretation remains with $performance-diagnostics; stakeholder narrative remains with $marketing-reporting.

## Planned

None currently.

## Unsupported

The capabilities below have no governed specialist. The connector's `find_marketing_method` tool names them as not covered (`UNCOVERED` in `apps/web/lib/mcp/router.ts`) instead of substituting a neighbouring skill.

| Capability | Boundary |
|---|---|
| Marketplace selling (Amazon, Etsy, Walmart, eBay and similar) | No governed specialist. Named as a gap instead of answered. |
| Pinterest, Snapchat, Reddit, X and Microsoft Advertising | No governed channel owner. Named as a gap; platform-agnostic methods apply only to a distinct covered part of the request. |
| Local search and Google Business Profile | Not owned by `$seo` today. Named as a gap. |
| App store optimization and app install campaigns | No governed specialist. Named as a gap. |

Standalone forecasting — a forecast outside a `$growth-strategy` scenario or an `$optimization-scaling` pacing reforecast — is also ungoverned. `$marketing-router` declares that gap when it routes; the app's `UNCOVERED` list does not detect it.

## Handling an uncovered request

1. Do not silently substitute the nearest channel skill.
2. Name the capability gap explicitly in the response.
3. Apply platform-agnostic frameworks only where they genuinely address a distinct part of the request.
4. Label any platform-specific guidance as ungoverned and unverified by this system.
5. Do not invent a skill name that does not exist.
6. State the gap in the response's exact-status line.
