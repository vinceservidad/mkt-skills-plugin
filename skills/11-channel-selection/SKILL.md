---
name: 11-channel-selection
description: Choose one or two channels to win with the Bullseye method across paid, owned and earned. Use for which channels, where to advertise, marketing mix, where to find customers.
metadata:
  section: "11 Distribution"
  covers: "Bullseye Framework (Traction); Demand generation; Direct mail; Localization; Marketplaces (Amazon, app stores); Omnichannel sequencing; OOH, TV, radio, print; POEM (paid, owned, earned)"
---
# Channel selection

Most companies grow on one or two channels, and most waste effort spreading thin across five (Weinberg & Mares). The job is to look at every channel once, honestly, then put the business's limited time and money into the few where its buyers already are, at a cost its economics can carry. A channel is chosen from evidence about this business (where its buyers came from, what they closed at, what a customer is worth), never from what is fashionable or what a benchmark says works elsewhere.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: who the channel must reach.
- `context/offer.md` → **Core offer** (from `07-offer-design`) or **Price and model** (from `07-pricing`): what a customer buys and is worth.
- If present, also read `context/awareness.md` → Traffic temperature, Journey, Buying triggers and process, Segments; `context/offer.md` → Price and model, Urgency and scarcity (capacity), Value ladder; `context/market.md` → Competitors and alternatives; any lead-source, CRM, sales-call, billing, margin, ad or analytics data in `inputs/`; any work in `work/` from channel skills.
- If a required section is missing:
  - **The upstream evidence exists** (for example interview notes in `inputs/` but no ICP): run the skill that fills it first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (ICP and personas → `02-icp-persona`; Core offer → `07-offer-design`; Price and model → `07-pricing`), and ask for evidence (customer interviews, sales notes, where current customers came from), not a description of the buyer. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Budget, price, discounts, referral rewards, free boxes or trials, capacity and partner fees are the owner's. An unknown budget is not a stop: size tests in hours and spend units and ask for the figure. Never invent one. When a channel idea would need an incentive or offer that `offer.md` does not hold, describe the need generically (*a referral reward, terms to be set by the owner via `16-referral-program`*) and never name its terms or a specific mechanic such as a free box or a percentage.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.
- If `07-pricing` is not loaded, stop and say: enable mkt-q2-offer.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/channel-guide.md](references/channel-guide.md) for the 19 channels, the scoring rules and the economics.

1. **The outcome and the economics.** Name the primary business outcome a channel must produce (a qualified call that can close, a paying subscriber who stays). Work out what a customer is worth from context: price, gross margin, retention or tenure. Then the allowable acquisition cost, as a calculation with its inputs shown. If margin or retention is missing, write the formula and mark the figure *unknown, owner to supply*. Never use a benchmark CAC, LTV or conversion rate.
2. **What already works.** Count where current customers and leads came from, and what each source closed at, from `inputs/` or context. Use [scripts/sum_by.py](scripts/sum_by.py) or count line by line; never by eye. Label each figure *observed*, *calculated* or *inferred*, with its sample size. Small counts are directional.
3. **Outer ring: brainstorm all 19.** Give every Traction channel one line: a concrete idea for this business, its POEM class (paid, owned, earned; partnerships count as borrowed), and why it is or is not promising, citing evidence or marking `(assumption)`. Add offline and marketplace channels where they could fit. No channel is dismissed without a reason, and none is promoted without one.
4. **Middle ring: pick about three to test.** Rank on evidence that the buyer is reachable there, fit with the offer's price and buying process, cost against the allowable acquisition cost, time to a readable result, the owner's capacity (hours, skills, budget) and delivery capacity (how many new customers the business can take). Prefer borrowing an audience that already gathers the buyer (partners, podcasts, communities: Dream 100) before building one.
5. **Design each test.** For each: the smallest version that gives a readable answer, its cost in money and hours, the time window, the success metric in the business outcome (not clicks, followers or opens), a keep rule and a stop rule. Label any threshold a heuristic. Name the skill that would run the channel (`11-seo`, `paid-search`, `paid-social`, `cold-email`, `pr`, `affiliate-jv`, `co-marketing`, `events`, `podcast-video`, `social`, `content-strategy`, `16-referral-program`...).
6. **Inner ring: the focus.** Name the one channel to focus on now (two at most when one is a referral or partner engine the business already has), why, what it needs, and the explicit non-priorities: the channels not worked on this period and what would change that. Say how attention from paid or borrowed channels becomes owned (email list, community).
7. **Sequencing and limits.** Say which channel introduces, which converts and which keeps, when the evidence supports it. Capacity in context caps growth whatever the channel does. Scaling a channel that works is not this skill's call: budget increases go to `19-scale-paid`; broader growth strategy to `19-growth`.
8. **Platform facts.** Any current claim about a platform (ad formats, targeting options, costs, policies, marketplace fees) is checked in the platform's own current documentation with URL and date, or marked *to confirm*. Never state one from memory as current.
9. **Approval.** This is a recommendation. Spending money, signing partner or commission deals, or launching any channel needs the owner's explicit approval.
10. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features, benchmarks, platform capabilities or delivery terms that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Describe each source only as it reads. Third-party benchmarks (a "typical" cost per lead or conversion rate for a channel) are not evidence about this business; leave them out. Competitor claims need a dated source or an `(assumption)` label.

## Output

Write `work/11-distribution/11-channel-selection-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Channel selection: <business, period>
Skill: 11-channel-selection · Date: <YYYY-MM-DD> · Framework: Bullseye (Traction) with POEM
Built from: <context sections and inputs used, with their status>
Status: recommendation for the owner's approval; no channel launched or money committed
## Outcome and economics
<primary business outcome; value of a customer and allowable acquisition cost, with the calculation and its inputs, or the formula and what is missing>
## What already works
| Source | Leads or customers | Closed or kept | Rate | n | Label |
| --- | --- | --- | --- | --- | --- |
## Outer ring: all channels
| Channel | POEM | Idea for this business | Promising? Why (evidence or assumption) |
| --- | --- | --- | --- |
## Middle ring: tests
| Channel | Smallest test | Cost (money, hours) | Window | Success metric (business outcome) | Keep rule | Stop rule | Run by |
| --- | --- | --- | --- | --- | --- | --- | --- |
## Inner ring: focus now
## Not now, and what would change that
## Sequencing and capacity
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a review, an interview, a sales note), with the source named. Write your own ideas and labels in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the focus channel and the tests, the economics (or what is missing to compute them), and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] All 19 Traction channels appear in the outer ring, each with a POEM class and a reason tied to evidence or marked `(assumption)`.
- [ ] Lead-source and close-rate figures are counted from the material with sample sizes and labelled observed, calculated or inferred; small counts are called directional.
- [ ] The allowable acquisition cost is calculated from context with its inputs shown, or left as a formula with the missing inputs named; no benchmark is used.
- [ ] About three tests, each with cost, window, a success metric in the business outcome, keep and stop rules, and the skill that runs it.
- [ ] One focus channel (two at most), explicit non-priorities, and delivery capacity respected; scaling is handed to `19-scale-paid`.
- [ ] Every platform fact is cited with a dated official URL or marked *to confirm*; nothing is launched or committed without the owner's approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Look at every channel once, test the few where your buyers already gather at a cost your economics can carry, and focus on the one that works: most companies grow on one or two channels. Bullseye Framework, Traction (Gabriel Weinberg and Justin Mares); Paid–Owned–Earned media (POEM); Dream 100 (Dan Kennedy, Russell Brunson); The Complete Marketing System, section 11 Distribution (Servidad, 2026).
