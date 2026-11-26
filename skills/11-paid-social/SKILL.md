---
name: 11-paid-social
description: Plan and audit creative-led paid social. Use for Meta, Instagram, TikTok, LinkedIn, Pinterest or Reddit ads, campaign structure, audiences, budget, or clicks without calls.
metadata:
  section: "11 Distribution"
  covers: "Paid social"
---
# Paid social

Paid social is interruption: the buyer did not search for you, so the creative does the targeting and the platform's delivery system learns who responds. The plan's job is to give that system the right signal (an event that stands for the real business outcome), enough distinct creative to learn from, and rules for when to keep, change or stop. A plan that optimises for clicks, or scales the ad with the most likes, buys the wrong people faster.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present and the commercial terms are confirmed. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Core offer**, from `07-offer-design`.
- `context/awareness.md` → **Awareness map**, from `03-awareness-map`.
- If present, also read `context/message.md` → **Promise** (from `08-message-doc`), Proof stack and Objection map; `context/customer.md` → ICP and personas, Segments and Voice of customer; `context/awareness.md` → Traffic temperature; `context/offer.md` → Price and model, Guarantee, Urgency and scarcity, Value ladder; any ad exports, ad logs, CRM outcomes or budget notes in `inputs/`; any work in `work/09-creative-strategy/09-angle-matrix-*.md`, `work/09-creative-strategy/09-ad-creative-*.md`, `work/11-distribution/11-channel-selection-*.md`, `work/12-funnel/12-landing-page-*.md`, `work/17-measurement/17-unit-economics-*.md` or `work/17-measurement/17-tracking-plan-*.md`.
- If `customer.md#Segments`, `message.md#Promise`, unit economics, landing page QA or conversion tracking are missing while Core offer and Awareness map exist, still write the draft plan and flag each missing item as a pre-launch gate to close before spending.
- If a required section is missing:
  - **The upstream evidence exists** (for example interview notes in `inputs/` but no Awareness map): run the skill that fills it first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Core offer → `07-offer-design`; Awareness map → `03-awareness-map`), and ask for evidence, not a description of the buyer. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Budget, price, discounts, promo codes, free trials, guarantees, deadlines and capacity are the owner's commitments. If the campaign must carry one that `offer.md` and `inputs/` don't hold (a first-box discount, a launch date, a new bonus), stop before writing, ask the owner for the exact terms, and write no plan on assumed terms. An unknown budget is not a stop: plan the test in spend units and ask for the figure.
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.
- If `03-awareness-map` is not loaded, stop and say: enable mkt-q1-audience.

## Process

Use [references/paid-social-guide.md](references/paid-social-guide.md) for the decision rules, the results read and the platform-claims rule; [references/meta-performance-five-and-delivery.md](references/meta-performance-five-and-delivery.md) for the Performance 5 review, 11-field alignment row and compatible results arithmetic; [references/meta-learning-leads-and-specs.md](references/meta-learning-leads-and-specs.md) for learning-phase isolation, Conversion Leads setup, budgeting/underdelivery triage, regulated checks, placement specs and Ads Manager pulls; and [references/pinterest-and-reddit-ads.md](references/pinterest-and-reddit-ads.md) for Pinterest Ads (visual search, Pin vs. Outbound clicks, catalog pins, longer conversion lag) and Reddit Ads (subreddit targeting, community-native copy, comments policy and CAPI checks).

1. **Outcome, economics, and conversion event.** Name the primary business outcome (a qualified call, a paying subscriber who stays past the second box), the nearest tracked optimization event that stands for it, and the allowable cost per business outcome from price, margin, and retention in context or `inputs/` (otherwise give the formula and mark *to set by the owner*). Clicks, CTR, likes, comments and platform-reported leads are delivery signals, never the outcome.
2. **Read what already ran,** when `inputs/` holds results. Total spend, platform-reported results and business outcomes per concept with [scripts/sum_by.py](scripts/sum_by.py) (`python3 <this skill's folder>/scripts/sum_by.py <file> concept --ratio spend_usd/<outcome column>`), never by eye. Rank by cost per business outcome, show each sample size, and label each figure *observed* (from the export), *calculated* or *inferred*. A pattern (frequency rising while CTR falls) is not a cause; say what would confirm it.
3. **Pre-launch readiness gates (before spending $1).** Check four go-live gates before any campaign launches: (a) offer, target segment/exclusions, and message/proof locked (`07-offer-design`, `02-segmentation`, `08-message-doc`); (b) destination landing page live, fast, and matched to the campaign's awareness level (`12-landing-page`); (c) conversion tracking wired and verified in Events Manager (Pixel + CAPI deduplication, dataset/domain checks, CRM offline / Conversion Leads join where applicable, and UTM convention via `17-tracking-plan`); (d) ad policy, Special Ad Category, consent, and billing checks (`20-compliance`). A missing gate blocks go-live, not drafting the plan.
4. **Choose platforms** where the evidence puts the buyer (customer.md, lead sources, any channel-selection output) and where the buyer can be reached at the size that matters (B2B company size, consumer interest). One or two platforms done well, not five. Name what each platform is for in this plan.
5. **Structure by temperature.** Pick one cold awareness level to start (or separate cold campaigns with strictly one awareness level per campaign; never combine levels such as *unaware and problem-aware*). Every concept inside a campaign must match that campaign's exact awareness level, entry message and offer (if `Awareness map` and `Traffic temperature` differ on the cold level or an asset is a gap, reconcile the choice explicitly). Warm audiences go to `12-retargeting`, which owns the retargeting ladder. Name the audience approach (broad, interest, lookalike, job-title or company filters) as a hypothesis with the reason, and exclude existing buyers from acquisition.
6. **Creative is the targeting.** Set 3 to 5 distinct concepts to test, each from a real angle (awareness entry, evidenced pain or objection, proof that exists), each naming the one thing it tests. Production goes to `09-ad-creative` (or `09-ugc-brief`, `09-image-video`, `10-ad-copy`); this plan sets the slots, the offer each points to (only offers in `offer.md`) and the destination.
7. **Budget, learning and stop rules.** Size the test from the owner's budget and economics: the allowable cost per business outcome from price and margin when context holds them, otherwise *to set by the owner*. Give each concept a minimum spend or outcome count before any call (labelled heuristic), a stop rule, and a keep rule, all in cost per business outcome. Scaling a winner is not this skill's call: hand budget increases to `19-scale-paid`, which owns the readiness, economics, marginal-evidence and guardrail gates. Never state a universal budget-increase rule.
8. **Hands-on Ads Manager build order (draft to publish).** Follow this execution sequence inside Meta Ads Manager or social ad platforms:
   1. Verify Business Portfolio / ad account, billing, Special Ad Category, and policy/consent rules (`20-compliance`).
   2. Publish and QA the destination landing page on mobile and desktop (`12-landing-page`).
   3. Wire and test Pixel, Conversions API deduplication, conversion event, CRM join, and UTMs (`17-tracking-plan`).
   4. Produce creative concepts and copy verified against placement safe zones (`09-ad-creative`, `09-image-video`, `10-ad-copy`).
   5. Build in draft from top to bottom: Campaign (objective, CBO/ABO) -> Ad Set (conversion event, audience/exclusions, placements, schedule, budget) -> Ads (concepts, copy, UTMs, verified destination URL).
   6. Run pre-publish QA and obtain explicit owner approval.
   7. Publish and confirm active delivery and live event firing in Events Manager.
9. **Platform facts.** Formats, specs, audience options and size limits, optimisation events, learning-phase rules, special ad categories and policies change. Verify each in the platform's current official documentation (URL and date checked) or the ad account, or mark it *to confirm*. Never state one from memory as current.
10. **Approval and check before saving.** The plan is a draft. Launching, pausing, changing budgets, audiences or conversion events needs the owner's explicit approval, and each change is verified in the account afterwards. Re-read the draft against the Checks and fix any failure before saving.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features, benchmarks, platform capabilities or delivery terms that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Describe each source only as it reads. Third-party benchmarks (a "typical" CPM, CTR or cost per lead) are not evidence about this account; leave them out. Competitor claims need a dated source or an `(assumption)` label.

For current platform capabilities specifically, official documentation actually consulted during this run is also a source: cite the URL and access date next to the claim, keep its documented scope, and separate documented behaviour from what this account can use. This exception never supplies the business's prices, offers, customer evidence or performance.

## Output

Write `work/11-distribution/11-paid-social-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Paid social plan: <business, platforms, period>
Skill: 11-paid-social · Date: <YYYY-MM-DD> · Framework: Paid social (creative-led, broad targeting, algorithm learning) with traffic temperature
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing launched or changed
## Outcome that decides
## What has run so far (if any)
| Concept | Spend | Platform-reported | Business outcome | Cost per outcome | n | Label |
| --- | --- | --- | --- | --- | --- | --- |
## Platforms and their job
## Pre-launch build order (gate before spend)
## Campaign structure
| Campaign | Temperature and awareness level | Audience (hypothesis) | Optimisation event | Offer and destination | Exclusions |
| --- | --- | --- | --- | --- | --- |
## Creative concepts to test
| Concept | Angle and evidence | The one thing it tests | Offer | Production owner |
| --- | --- | --- | --- | --- |
## Budget, learning and stop rules
## Tracking and attribution prerequisites
## Platform facts
| Fact the plan relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a review, an interview, an ad log), with the source named. Write your own lines, concepts and hooks in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the outcome that decides, the key keep, change or stop calls, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The plan is judged on a named business outcome; clicks, CTR, engagement and platform leads are never treated as the outcome.
- [ ] Any results read are totalled with `sum_by.py`, ranked by cost per business outcome with sample sizes, and labelled observed, calculated or inferred.
- [ ] Each cold campaign targets strictly one awareness level (never two combined), all concepts inside it match that level's entry message and offer, and any difference between `Awareness map` and `Traffic temperature` is reconciled; warm audiences go to `12-retargeting`; buyers are excluded from acquisition.
- [ ] Concepts are distinct, each names the one thing it tests, and every offer, price and term exists in `offer.md` or `inputs/`.
- [ ] Budget increases are handed to `19-scale-paid`; no universal scaling rule; stop and keep rules are in cost per business outcome.
- [ ] Pre-launch readiness gates (offer/message/segment alignment, landing page QA, Pixel/CAPI/UTM tracking verification, compliance) and the hands-on build order are explicitly gated before live spend.
- [ ] Every platform fact is cited with a dated official URL or marked *to confirm*; no benchmark is used as evidence.
- [ ] The plan says nothing is launched or changed without the owner's approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

On paid social the creative finds the buyer, so give the platform an event that stands for the real business outcome, distinct concepts to learn from, and rules for when to stop, and judge every ad on cost per business outcome, not clicks. Paid social (creative-led, broad targeting, algorithm learning) and traffic temperature, The Complete Marketing System, section 11 Distribution (Servidad, 2026); Traffic Secrets (Russell Brunson); Traction (Weinberg & Mares).
