---
name: google-ads
description: Audit, diagnose, or plan Google Ads Search, Shopping, and Performance Max work using business outcomes and query or product evidence; not for YouTube video campaigns, scaling-readiness or budget-expansion decisions, or unsupported live changes.
---

# Google Ads

Covers Search, Shopping, and Performance Max structure, bidding, and account mechanics. YouTube video advertising is a distinct discipline with different attention economics, format constraints, and measurement norms — route to `$youtube-ads` for format selection, video-specific targeting, and view-through measurement fit; this skill covers the shared Google Ads account and bidding layer YouTube campaigns also run through. Raising the budget or expanding the coverage (new campaigns, asset groups, products, keywords, or markets) of an existing account to grow volume is a scaling decision owned by `$optimization-scaling`; this skill supplies the account mechanics, plans a first build or launch, and scopes settings changes inside an already-approved plan.

Classify each audit, model, methodology, process, tactic, technique, best practice, or heuristic with [`KNOWLEDGE-TAXONOMY.md`](../../library/contracts/KNOWLEDGE-TAXONOMY.md). Name the primary type and keep platform evidence separate from recommendations.

## Required inputs

Collect business goal, account and market scope, date range and comparison, budget, bidding strategy, campaign type, conversion goals, conversion actions, action-optimization status, revenue or qualified-lead definition, and available exports. For ecommerce profitability, request price, COGS, variable fulfillment, payment fees, discounts, refunds, revenue basis, and feed status.

## Method

1. Verify conversion goals, their included conversion actions, each action's Primary/Secondary status, campaign goal selection, counting, values, attribution windows, consent gaps, and agreement with the business source of truth. A Primary action influences bidding only when the campaign uses its containing goal.
2. Decompose demand and eligibility → auctions and spend → clicks → site behavior → conversions → revenue, margin, or lead quality.
3. Inspect the correct unit:
   - Search: queries, match type, intent, ad relevance, landing alignment, geography, device, and schedule.
   - Shopping/PMax: item ID, product type, price, feed quality, availability, asset-group segmentation, and available channel-mix evidence.
4. Compare like-for-like periods and separate volume, efficiency, mix, and measurement effects.
5. Rank actions by expected business impact, confidence, reversibility, and learning value.

For substantial mode-specific work, read only the relevant reference: [Search](references/search.md), [Shopping](references/shopping.md), or [Performance Max](references/pmax.md). For current AI, automation, control, reporting, or interface claims, read [Platform Registry](references/platform-current.md) and apply the root `library/contracts/PLATFORM-CURRENCY.md` freshness gate.

For a Search configuration or experiment decision, use [Google Search outcome alignment](references/google-search-outcome-alignment.md). When event quality blocks that decision, use [Google/Meta signal validation](../tracking-measurement/references/google-meta-signal-validation.md) with the measurement owner.

For an RSA draft, mandatory-text, insertion or ad-to-page fit decision, use [Search asset validation](references/search-asset-validation.md) with [Search ad drafting](../creative-strategy/references/search-ad-drafting.md); Creative Strategy owns the finished paid wording. Read the [Shopify Google/ad-copy source review](references/shopify-google-ad-copy-source-review.md) when article provenance, coverage or a source conflict matters, not as current platform instructions.

For a prior-relationship audience, suppression or targeting-versus-observation question, use [Audience relationship and delivery readiness](references/audience-readiness.md) to populate the membership, consent and actual delivery-use record; do not assume every campaign's audience settings restrict reach.

Use [GAQL data pulls](references/gaql-data-pulls.md) when pulling account data through the Google Ads search tool. Use [Merchant Center, calls, Local Services Ads and GA4](references/calls-local-ga4.md) when the work involves feed rules, call conversions, Local Services Ads or GA4 imports. Use [Competitor research, consent and risk](references/competitor-consent-risk.md) when researching competitor ads, checking consent, handling a suspension or appeal, or working in a regulated industry.

## Rules

- Never add a negative solely because a query did not convert in a small sample; consider intent, spend against allowable CPA, assisted value, and protected brand/product coverage.
- Do not recommend or make a budget increase or coverage expansion of an existing account here; route it to `$optimization-scaling`, whose gates include measurement integrity and unit economics, and implement only what that decision and its authorization cover.
- Avoid structural rebuilds when the issue is isolated to measurement, feed eligibility, landing experience, or a small set of queries/items.
- Do not infer unseen PMax channel allocation.
- Use profit (name the level and the costs included) or qualified-lead economics when available. Label ROAS/CPA conclusions provisional otherwise.
- Use “conversion goal” for the Google Ads grouping and “conversion action” for the measured action. Do not call the main commercial result a Primary conversion action; call it the primary business outcome.
- Do not claim an undocumented “Google algorithm change.” Separate officially documented capability, account-visible behavior, experimentally observed impact, inference, and unknowns. Confirm account availability before recommending a current control.

## Output

Audit: scope; measurement status; findings with evidence, impact, and confidence; protected coverage; prioritized actions; tests; unknowns.

Change plan: exact entity; current and proposed state; rationale; risk; rollback/stop rule; approval required.

## Library references

Owned shared library artifacts, read when their scope applies:

- [google-ads-full-stack.md](../../library/frameworks/google-ads-full-stack.md) — full-account decision model beyond a single audit or diagnosis.
- [google-ads-audit.md](../../library/playbooks/google-ads-audit.md) — step-by-step audit workflow.
- [google-ads-optimization.md](../../library/workflows/google-ads-optimization.md) — recurring optimization cadence.
- [campaign-brief.md](../../library/templates/campaign-brief.md) — campaign brief format; also loaded by $meta-ads.

## QA

Check date and attribution consistency, conversion scope, sample size, query/item evidence, margin or lead-quality caveats, preservation of valuable coverage, platform-registry freshness, and account-visible availability for current controls.
