---
name: 11-paid-search
description: Plan and audit Google or Bing search ads with keywords, search terms reports, match types and bidding. Use for search ad plans, wasted search spend, search terms reports, negative keywords.
metadata:
  section: "11 Distribution"
  covers: "Paid search"
---
# Paid search

Paid search captures intent: the buyer has already typed the problem or the solution, and the ad meets them at that moment. The plan's job is to buy only the searches whose intent the offer serves, send each to the page that answers it, tell the platform which outcome counts (a qualified call or a paying customer, not a form fill from anyone), and read the search terms often enough to stop paying for the wrong ones. A plan judged on clicks or platform conversions, or one that buys a big generic term the buyer never uses, spends fast and teaches nothing.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present and the commercial terms are confirmed. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Core offer**, from `07-offer-design`: what the searcher is offered.
- `context/awareness.md` → **Awareness map**, from `03-awareness-map`: which searches belong to which level and what each level needs to see.
- If present, also read `context/offer.md` → Price and model, Guarantee, Urgency and scarcity (capacity), Value ladder (free assets for informational searches); `context/customer.md` → ICP and personas, Segments and Voice of customer; `context/awareness.md` → Journey and Traffic temperature; `context/message.md` → Promise, Proof stack; `context/market.md` → Competitors and alternatives; keyword-tool exports, search terms reports, campaign exports, CRM outcomes, margin and budget notes in `inputs/`; any work in `work/11-distribution/11-seo-*.md`, `work/11-distribution/11-channel-selection-*.md`, `work/12-funnel/12-landing-page-*.md`, `work/17-measurement/17-unit-economics-*.md` or `work/17-measurement/17-tracking-plan-*.md`.
- If `customer.md#Segments`, `message.md#Promise`, unit economics, dedicated landing pages or conversion tracking are missing while Core offer and Awareness map exist, still write the draft plan and flag each missing item as a pre-launch gate before live spend.
- If a required section is missing:
  - **The upstream evidence exists** (for example interview notes in `inputs/` but no Awareness map): run the skill that fills it first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Core offer → `07-offer-design`; Awareness map → `03-awareness-map`), and ask for evidence, not a description of the buyer. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Budget, price, discounts, free trials, free items, guarantees, deadlines and capacity are the owner's commitments. If the ads must carry one that `offer.md` and `inputs/` don't hold (a free first bag, a percentage off, a launch date), stop before writing, ask the owner for the exact terms, and write no plan on assumed terms. An unknown budget is not a stop: plan the test in spend units and ask for the figure.
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.
- If `03-awareness-map` is not loaded, stop and say: enable mkt-q1-audience.

## Process

Use [references/paid-search-guide.md](references/paid-search-guide.md) for match types, negatives, bidding, the results read and the platform-claims rule; [references/gaql-and-account-diagnostics.md](references/gaql-and-account-diagnostics.md) for read-only GAQL pulls, call/GA4 rules, competitor ad-library logs, consent and regulated checks; [references/search-pmax-and-asset-validation.md](references/search-pmax-and-asset-validation.md) for the Search alignment chain, Performance Max / AI Max inspection, and RSA/DKI asset validation; and [references/google-ads-power-pack-and-vbb.md](references/google-ads-power-pack-and-vbb.md) for the AI Power Pack (Demand Gen channel controls, AI Max for Search, PMax channel reporting), Value-Based Bidding for lead gen and AI-qualified calls, daily/monthly spending limit hygiene, and clean Google Ads Experiments.

1. **The outcome that decides.** Name the primary business outcome (a qualified call, a client, a paying subscriber who stays) and the conversion action the campaign will optimise for: the nearest tracked event that stands for that outcome. Clicks, CTR, quality score and platform-counted conversions are signals, never the outcome. If the account counts any form fill as a conversion, say what it gets wrong and what to import instead (CRM-qualified outcomes), handing tracking gaps to `17-tracking-plan`.
2. **Economics.** The allowable cost per business outcome, from price, margin and retention in context or `inputs/`, with the calculation shown; otherwise the formula and *to set by the owner*. Never a benchmark CPC, CPA or conversion rate.
3. **Read what already ran,** when `inputs/` holds a search terms report or campaign export. Total spend, clicks, platform conversions and business outcomes by search term or theme with [scripts/sum_by.py](scripts/sum_by.py) (`python3 <this skill's folder>/scripts/sum_by.py <file> search_term --ratio cost_usd/<outcome column>`), never by eye. Rank by cost per business outcome with sample sizes, label each figure *observed*, *calculated* or *inferred*, and call small counts directional. Separate irrelevant intent (jobs, free, other industries, cheap or local generic) from relevant intent that has not converted yet.
4. **Pre-launch readiness gates (before spending $1).** Gate four items before live spend: (a) offer, target segment/exclusions, and message/proof locked (`07-offer-design`, `02-segmentation`, `08-message-doc`); (b) dedicated intent-matched landing pages live and matching ad promises (`12-landing-page`); (c) conversion tracking wired and verified (Primary vs. Secondary conversion goals, Enhanced Conversions or CRM offline conversion imports rather than raw form fills, auto-tagging and UTM convention via `17-tracking-plan`); (d) billing, location presence settings, network defaults (Display expansion and Search Partners off unless explicitly tested), and trademark/policy compliance (`20-compliance`). Missing gates block go-live, not drafting the plan.
5. **Keywords by intent and awareness.** Sort candidate searches (from the export, the keyword tool, Voice of customer, sales-call questions) by intent and awareness level: solution-aware and product-aware searches (the category for this buyer, comparisons, pricing, the brand) usually come first; problem-aware searches go to a free asset only when one exists in the value ladder; generic terms the ICP doesn't use, or whose searchers the offer can't serve at its price, are excluded whatever their volume. Tool volumes and bid ranges are estimates; label them.
6. **Structure.** Campaigns and ad groups by intent theme (one theme per ad group, each with its own landing page that answers that search). Match types per keyword with the reason (tighter where intent is narrow and budget small, broader only with a reliable conversion signal and negatives), the negative keyword list with the evidence for each, geography, schedule and networks as hypotheses. Protect brand and proven terms.
7. **Ads and landing pages.** For each ad group, the message for its awareness level from the awareness map and the promise, using only offers, prices and proof in context. Ad copy goes to `10-ad-copy`; the page to `12-landing-page` or the existing page that matches. No ad promises what the page doesn't show.
8. **Bidding, budget, learning and stop rules.** Start with the bidding approach the conversion signal can support (manual or click-based caps while signal is thin, outcome-based bidding once the business outcome is imported and frequent enough; the thresholds are platform rules to confirm). Size the test from the owner's budget and the allowable cost. Set a review rhythm for search terms, a minimum spend or outcome count before a call (labelled heuristic), keep rules and stop rules in cost per business outcome. Scaling is not this skill's call: budget increases and coverage expansion go to `19-scale-paid`. Never state a universal budget rule.
9. **Hands-on Google Ads build order (draft to publish).** Follow this execution sequence inside Google Ads:
   1. Verify billing, auto-tagging, and Conversion Actions (Primary vs. Secondary goals, Enhanced Conversions / offline CRM import verified via `17-tracking-plan`).
   2. Publish and QA each intent-matched destination landing page (`12-landing-page`).
   3. Load starter account and campaign negative keyword lists before enabling spend.
   4. Build in draft from top to bottom: Campaign (goal, Search network only unless tested, location presence, schedule, budget, initial bidding) -> Ad Groups (one intent theme each, exact/phrase keywords) -> RSAs and extensions/assets (`10-ad-copy`) with verified final URLs.
   5. Run pre-publish QA and obtain explicit owner approval.
   6. Publish, verify live conversion firing, and schedule the first search-terms review.
10. **Platform facts, approval, and check before saving.** Match-type behaviour, close variants, bidding strategies and their data needs, conversion imports, quality score, ad formats and policies change. Verify each in the platform's current official documentation (URL and date checked) or the ad account, or mark *to confirm*. Never state one from memory as current. Creating or changing campaigns, keywords, negatives, bids, budgets or conversion actions, and pausing or enabling anything, needs the owner's explicit approval; each change is verified in the account afterwards. Re-read the draft against the Checks and fix any failure before saving.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features, benchmarks, platform capabilities or delivery terms that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Describe each source only as it reads. Third-party benchmarks (a "typical" CPC, CTR, conversion rate or cost per lead) are not evidence about this account; leave them out. Competitor claims need a dated source or an `(assumption)` label.

For current platform capabilities specifically, official documentation actually consulted during this run is also a source: cite the URL and access date next to the claim, keep its documented scope, and separate documented behaviour from what this account can use. This exception never supplies the business's prices, offers, customer evidence or performance.

## Output

Write `work/11-distribution/11-paid-search-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Paid search plan: <business, platform, period>
Skill: 11-paid-search · Date: <YYYY-MM-DD> · Framework: Paid search intent capture (keywords by intent, match types, negatives, ad groups, bidding)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing launched or changed
## Outcome that decides and conversion action
## Economics
## What has run so far (if any)
| Search term or theme | Clicks | Cost | Platform conversions | Business outcome | Cost per outcome | n | Label |
| --- | --- | --- | --- | --- | --- | --- | --- |
## Keywords by intent and awareness
| Keyword or theme | Intent | Awareness level | Match type and why | Volume and bid (tool estimate) | Decision |
| --- | --- | --- | --- | --- | --- |
## Negative keywords
| Negative | Match | Evidence |
| --- | --- | --- |
## Pre-launch build order (gate before spend)
## Campaign and ad group structure
| Campaign | Ad group (one theme) | Keywords | Message for its level | Offer (from offer.md) | Landing page |
| --- | --- | --- | --- | --- | --- |
## Bidding, budget, learning and stop rules
## Tracking prerequisites
## Platform facts
| Fact the plan relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/` and nothing in any ad account. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a search term in an export, a review, an interview), with the source named. Write your own keywords, headlines and proposals in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the outcome that decides, the key keep, change or stop calls, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The plan is judged on a named business outcome; clicks, CTR, quality score and platform-counted conversions are never treated as the outcome, and any form-fill conversion action is flagged.
- [ ] Any results read are totalled with `sum_by.py`, ranked by cost per business outcome with sample sizes, labelled, and small counts called directional.
- [ ] Every keyword has an intent and awareness level; generic terms the ICP doesn't use are excluded whatever their volume; tool volumes and bids are labelled estimates.
- [ ] Each ad group has one theme, a matching landing page, and only offers, prices and proof that exist in context.
- [ ] Negatives cite their evidence; brand and proven terms are protected; budget increases go to `19-scale-paid` with no universal rule.
- [ ] Pre-launch readiness gates (offer/message/segment alignment, intent-matched landing page QA, Primary/Secondary conversion tracking and offline imports, network/location hygiene) and the hands-on build order are explicitly gated before live spend.
- [ ] Every platform fact is cited with a dated official URL or marked *to confirm*; no benchmark is used; nothing is launched or changed without the owner's approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Paid search buys intent that already exists: pay only for the searches your offer serves, send each to the page that answers it, optimise for the outcome the business is paid for, and read the search terms before spending more. Paid search intent capture (keywords, match types, quality score, bidding), The Complete Marketing System, section 11 Distribution (Servidad, 2026); Breakthrough Advertising (Eugene Schwartz) for awareness levels; Google Ads and Microsoft Advertising documentation (verify current).
