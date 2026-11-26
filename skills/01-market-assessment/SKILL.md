---
name: 01-market-assessment
description: Judge whether a market is worth entering from evidence on demand, size, forces, timing and ability to pay. Use for TAM/SAM/SOM, market sizing, should we enter. Not for search demand (01-demand-check).
metadata:
  section: "01 Market"
  covers: "Blue Ocean; Five Forces (Porter); PESTLE; Starving crowd; TAM / SAM / SOM"
---
# Market assessment

A starving crowd beats a great product: a market with real pain, money to pay, buyers you can reach and growth will forgive weak marketing, and a market without them won't reward strong marketing. This skill decides, from evidence, whether this market is worth it: who exactly the market is, how big it really is for this business, and what forces make money easy or hard to earn in it. Sizing in three rings keeps ambition (the total market) apart from reach (what this business can actually win).

## Needs (read before writing)

- **Evidence about the market**, in `inputs/`, elsewhere in the project, or pasted by the user. Any of these counts:
  - industry or census data, trade-association reports, published surveys, with publisher and date;
  - the business's own numbers: customers, average revenue per customer, delivery cost or margin, capacity, sales data;
  - demand evidence (search or ad data), competitor notes, customer research.
- If present, also read:
  - `context/customer.md` → ICP and personas, from `02-icp-persona`: who the market is made of. Also Segments, Pains, desires and fears, Current alternatives, and Buying triggers and process.
  - `context/market.md` → Demand (`01-demand-check`) and Competitors and alternatives (`01-competitor-profiling`). Reuse them; don't redo them.
  - `context/offer.md` → Core offer and Price and model: what is being sold, at what price.
- Nothing upstream is required. If there is no market evidence at all (no data, no customers, no research), the material is missing, so stop before writing any context section. Write the research plan described under Output instead.
  - Never state a market size, growth rate, share or industry figure from memory or as a "typical" number.
  - The user's description of their market and their goal are hypotheses and targets, not evidence.
  - Look up public sources only when the user asks you to and a web tool is available. Then open each one, and record the publisher, the figure, the URL and the date you saw it.

## Process

Use [references/frameworks.md](references/frameworks.md) for the detail of each test.

1. **Define the market.** One line each: who buys (from the ICP if present), what job they hire it for, where (geography), and what is in and out of scope. Name the category as buyers search for and compare it.
2. **Run the Starving Crowd test.** Score each of the four, with evidence, as strong, mixed, weak or unknown:
   - **Pain:** is the problem urgent and costly? (Customer research, lost-deal reasons, triggers.)
   - **Purchasing power:** can they pay what the offer costs? (Their revenue, what they pay alternatives now.)
   - **Easy to target:** can you find and reach them? (Associations, lists, communities, search terms, referral paths.)
   - **Growing:** is the buyer group growing or shrinking? (Dated counts or trends.)
3. **Size it in three rings.** For each ring, show the inputs, the formula and the result, and label it *calculated from* its sources. Compute with `python3`, not by hand.
   - **TAM:** every buyer who could have this job, times annual value per buyer.
   - **SAM:** the part this business can serve with this offer: the ICP's size band, geography, channel and fit.
   - **SOM:** what it can realistically win in a stated period. Bound it by capacity and by evidence of win rates, not by a hopeful percentage.

   Use the business's own price for value per buyer when it exists, and say which. When an input is missing, write the range or *unknown*, and say what would fill it. Never fill a ring with an invented number.
4. **Check the goal against the rings.** If the user has a revenue goal, translate it into customers needed (goal ÷ annual revenue per customer). Compare that with SOM and with delivery capacity. Say plainly if the goal needs a bigger market, a higher price or more capacity.
5. **Rate the forces.** Use Porter's Five Forces: rivalry, threat of new entrants, substitutes, buyer power and supplier power. Rate each high, medium or low, with evidence. Then add the PESTLE forces that change the decision (political, economic, social, technological, legal, environmental), each with its source or marked `(assumption)` or *unverified*. Leave out the forces with no bearing; don't pad all six.
   - A regulation or legal change the business has not verified is a question to check, not a fact.
6. **Timing.** Say whether the market is early, growing, mature or declining, on the evidence, and what that means for entering or expanding now.
7. **Verdict.** One of: *worth pursuing*, *worth pursuing with conditions* (name them), *not yet: evidence missing* (name it), or *not worth it* (why). Name the evidence that would change it. If a less-contested space shows up (a Blue Ocean move, by changing the factors the category competes on), note it as an opening for `06-positioning`, not as a decision.
8. **Check before saving.** Re-read the draft against every item under Checks, and run `scripts/check_quotes.py` on it. Fix any failure before you save.

**Calculations and labels.** Every number is either copied from a named source, *calculated* from named inputs (show the formula), or marked `(assumption)`. Survey answers are stated preference (*62% say…*), not behaviour. A trade body's figure is that body's estimate, not a fact about this business. No unmarked inference: a motive, trend or frequency the evidence does not state carries `(assumption)`.

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from a source. Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py context/market.md`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches. Count items with [scripts/tally.py](scripts/tally.py) when the material is a file.

## Output

**With evidence**, write three sections of `context/market.md`, replacing each section's body and leaving every other section exactly as it was:

```markdown
## Market definition
Status: draft (<YYYY-MM-DD>, 01-market-assessment)
Written by: 01-market-assessment, <YYYY-MM-DD>
Market: <who buys> · <job> · <where> · in scope <…> · out of scope <…>
Starving Crowd test: pain <rating, evidence> · purchasing power <…> · easy to target <…> · growing <…>
Verdict: <worth pursuing | with conditions | not yet: evidence missing | not worth it> — <why, and what would change it>
Evidence: <sources>
Method: Starving Crowd test, $100M Offers / $100M Leads (Hormozi)

## Size
Status: draft (<YYYY-MM-DD>, 01-market-assessment)
Written by: 01-market-assessment, <YYYY-MM-DD>
| Ring | Buyers | Value per buyer per year | Size | Inputs and formula | Kind |
| --- | --- | --- | --- | --- | --- |
Goal check: <goal → customers needed → vs SOM and capacity>
Gaps: <missing inputs and how to get them>
Evidence: <sources>
Method: TAM / SAM / SOM, bottom-up

## Forces and timing
Status: draft (<YYYY-MM-DD>, 01-market-assessment)
Written by: 01-market-assessment, <YYYY-MM-DD>
| Force | Rating | Evidence |
| --- | --- | --- |
PESTLE forces that matter: <force — effect — source, (assumption) or unverified>
Timing: <early | growing | mature | declining> — <evidence and what it means now>
Evidence: <sources>
Method: Porter's Five Forces; PESTLE
```

Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/market.md` does not exist, create it with frontmatter, these sections and a change log.

**Without evidence**, write `work/01-market/01-market-assessment-<YYYY-MM-DD>-plan.md`: the market hypothesis, the questions for each Starving Crowd test, the inputs each ring needs and where to find them (census or trade data, the business's own price and capacity, demand data, competitor notes), and the hypotheses to test. Leave `context/` unchanged.

Reply with:
- the verdict in one line, with the deciding evidence;
- the ring sizes and the goal check;
- the gaps;
- the next skill: `01-demand-check`, `01-competitor-profiling` or `01-sophistication-stage`.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The market is defined by buyer, job, geography and scope, not just a category name.
- [ ] Each Starving Crowd test is rated with evidence or marked unknown.
- [ ] Every ring shows its inputs, formula and kind. No size, growth rate or share is invented or taken from memory.
- [ ] SOM is bounded by capacity and evidence of win rates, and a stated goal is checked against it.
- [ ] Survey answers are labelled as stated, and third-party figures name their publisher and date.
- [ ] Each force is rated with evidence. Unverified regulation is a question to check, not a fact.
- [ ] The verdict names the evidence that would change it.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] Without evidence, no context section was written.
- [ ] Only the three owned sections changed. Each has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

A starving crowd beats a great product: choose a market with urgent pain, money to pay, buyers you can reach and growth, size it from reach rather than ambition, and know the forces that decide whether money can be made in it. Starving Crowd test, $100M Offers (Alex Hormozi) and the starving crowd (Gary Halbert); TAM / SAM / SOM; Five Forces (Michael Porter, Competitive Strategy); PESTLE; The Complete Marketing System, section 1 Market (Servidad, 2026).
