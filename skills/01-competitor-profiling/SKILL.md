---
name: 01-competitor-profiling
description: Profile competitors and the real alternatives, including doing nothing or a spreadsheet, from dated evidence. Use for competitor analysis, who we compete with, comparing rivals' prices and claims.
metadata:
  section: "01 Market"
---
# Competitor profiling

Buyers don't compare you with the competitors you worry about; they compare you with what they would do instead. That includes the rival with the bigger ad budget, but also the spreadsheet, the office manager, the tax accountant they already have, and doing nothing. This skill builds the real alternative set from dated evidence and says where each alternative wins and loses. Positioning, pricing, sophistication and sales all read it.

## Needs (read before writing)

- **Raw evidence**, in `inputs/`, elsewhere in the project, or pasted by the user. Any of these counts:
  - notes or screenshots of competitor websites, pricing pages, ads or search results, with the date seen;
  - lost-deal reasons, sales-call notes or win/loss interviews;
  - reviews of the business or of competitors;
  - competitor names the user gives (record them as *named by the user*; their details are still unknown).
- If present, also read:
  - `context/market.md` → Market definition, from `01-market-assessment`: whose alternatives you are listing;
  - `context/customer.md` → Current alternatives, from `02-customer-research`: what customers used before or instead. Reuse it and cite it; don't contradict it silently.
  - `context/customer.md` → Beliefs, objections and drivers, and Voice of customer: why buyers left or chose an alternative.
  - `context/offer.md` → Core offer and Price and model: what we are being compared on.
- Nothing upstream is required. If there is no evidence at all, the material is missing, so stop before writing any context section. Write the collection plan described under Output instead, and ask the user to bring it back.
  - Never name competitors, prices, features or claims from memory or from "typical" players in the category.
  - Look up public sources only when the user asks you to and a web tool is available. Then open each page, and record its URL, what it showed and the date you saw it. Never use a figure you did not see.

## Process

1. **Build the alternative set.** List every option the buyer weighs, in four groups, using [references/alternatives.md](references/alternatives.md):
   - **Direct:** the same kind of solution for the same buyer.
   - **Indirect:** a different solution to the same job (a fractional executive, software, a marketplace).
   - **DIY or in-house:** the owner, an employee, a spreadsheet.
   - **Status quo:** doing nothing, waiting, leaving it to someone who already serves them.

   Include an alternative only where evidence shows buyers weigh it or the user names it. Write anything else as a gap.
2. **Profile each alternative** from the evidence:
   - who it is for, and its promise as they state it;
   - price, as observed, with date and source, or *not shown*;
   - the proof it shows (reviews, case studies, counts), described as *claimed by the company* unless independently verified;
   - where it wins and where it loses for our buyer, from buyer evidence (lost deals, interviews, reviews), not from our opinion of it.
3. **Count wins and losses.** Use lost-deal reasons, churn reasons and switch stories, with counts. Count with `scripts/tally.py`, never by eye.
4. **Label every claim by kind:**
   - **Observed:** seen on a dated page, ad or search result.
   - **Reported:** what a buyer or the user said about it.
   - **Inferred:** your reading, marked `(assumption)`.
   - **Unknown:** the gap, and how to fill it.

   A competitor's claim is what they say, not a fact about the market. A competitor's visible tactic (an ad, a price, a headline) is evidence about that competitor, not proof that it works or that we should copy it.
5. **Name the threats and openings.** Which alternative takes the most deals today, which is growing (with evidence), and where buyers' unmet needs leave room. Keep this to what the evidence shows; positioning decisions belong to `06-positioning-statement`.
6. **Check before saving.** Re-read the draft against every item under Checks, and run `scripts/check_quotes.py` on it. Fix any failure before you save.

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from a source: a competitor's page as recorded in the notes, a review, an interview. Your summaries, labels and readings go without quotation marks. Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py context/market.md`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches.

## Output

**With evidence**, write `context/market.md` → `## Competitors and alternatives`, replacing that section's body and leaving every other section (in this file and in `context/positioning.md`) exactly as it was:

```markdown
## Competitors and alternatives
Status: draft (<YYYY-MM-DD>, 01-competitor-profiling)
Written by: 01-competitor-profiling, <YYYY-MM-DD>
| Alternative | Group | Who it's for · promise (as stated) | Price (observed, date) | Proof shown | Wins when | Loses when | Evidence (kind, source, date) |
| --- | --- | --- | --- | --- | --- | --- | --- |
Deals and switches: <lost-deal and churn counts by alternative, with source>
Biggest threat now: <alternative and why, with evidence>
Openings: <unmet needs the evidence shows, or "none evidenced">
Gaps: <what is unknown and how to find out>
Evidence: <files, IDs and dates>
Method: Competitive alternatives analysis (Dunford, Obviously Awesome); dated competitor profiles
```

- In table cells, paraphrase without quotation marks unless you copy a source exactly.
- Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/market.md` does not exist, first copy [assets/market.md](assets/market.md) to `context/market.md`, then write your section into it.

**Without evidence**, write `work/01-market/01-competitor-profiling-<YYYY-MM-DD>-plan.md`: the alternatives to look for in all four groups, what to capture for each (promise, price, proof, date seen), where to look (their sites and pricing pages, search results, ad libraries, review sites, lost-deal notes), and how to log it. Leave `context/` unchanged.

Reply with:
- the alternative that takes the most deals and the biggest gap in the evidence;
- the next skill: `01-sophistication-stage` (how worn the claims are), `06-positioning-statement`, or `07-pricing`.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Ad counts and ad-library presence are dated observations only; the file and the reply never call them spend, budget, reach or success (write *spend unknown*).
- [ ] The set includes DIY or in-house and the status quo wherever evidence shows them, not only named companies.
- [ ] Every competitor, price, claim and count traces to a dated source or the user's words. Nothing comes from memory, and unknown fields say *not shown* or *unknown*.
- [ ] Each claim is labelled observed, reported, inferred `(assumption)` or unknown. Competitor claims are stated as their claims, not as facts.
- [ ] Wins and losses come from buyer evidence (lost deals, interviews, reviews), with counts recounted by `tally.py`.
- [ ] No visible competitor tactic is presented as proof that it works or as something to copy.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] Without evidence, no context section was written and no competitor was named from memory.
- [ ] Only `## Competitors and alternatives` changed (not `positioning.md`). It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

Buyers compare you with what they would otherwise do, including nothing, so the real competition is the full set of alternatives, profiled from dated evidence of what they promise, charge and lose on. Competitive alternatives, Obviously Awesome (April Dunford); The Complete Marketing System, section 1 Market (Servidad, 2026).
