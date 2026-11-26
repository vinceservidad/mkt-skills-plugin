---
name: 06-positioning-statement
description: Position the product against the real alternatives with unique attributes, value, best-fit customers and category. Use for positioning, positioning statement, how we're different, April Dunford.
metadata:
  section: "06 Positioning"
  covers: "22 Immutable Laws of Marketing (Ries & Trout); Competitive alternatives; Obviously Awesome (Dunford); Only-ness statement; Perceptual map; Positioning (Ries & Trout); Positioning statement (Moore); USP; Value proposition (canvas)"
---
# Positioning statement

Positioning is not what you do to the product; it is what you do to the buyer's mind. A buyer understands a product only against something they already know: the alternatives they would use instead, the category they file it under. Good positioning starts from those alternatives, finds what the business has that they lack, turns that into value a specific customer cares about, and picks the category frame that makes that value obvious. It is a trade-off: who the business is *not* for is part of it. This skill decides the position from evidence and writes it as a statement every downstream skill can use.

## Needs (read before writing)

- Required (drafted or confirmed, with content):
  - `context/customer.md` → **ICP and personas**, written by `02-icp-persona`: who the best-fit customer is.
  - The alternatives, from either:
    - `context/customer.md` → **Current alternatives**, written by `02-customer-research`; or
    - `context/market.md` → **Competitors and alternatives**, written by `01-competitor-profiling`.
    Read both when both exist; the market section has dated competitor claims, the customer section has what buyers actually used.
- If present, also read:
  - `context/customer.md` → Jobs to be done, Segments, Pains desires and fears, Beliefs objections and drivers, Voice of customer;
  - `context/offer.md` → Core offer and Guarantee (`07-offer-design`): the capabilities the business actually has, and which are only proposed;
  - `context/market.md` → Market sophistication and Demand;
  - `context/positioning.md`: any earlier draft, to revise rather than ignore;
  - `inputs/`: competitor notes, sales-call notes, win/loss reasons, interviews.
- `context/message.md` and `context/brand.md` are downstream or parallel: you may read them, but they are not evidence of a difference.
- If a required section is missing:
  - **Raw customer or competitor evidence exists** (interviews, call notes, reviews or competitor notes in `inputs/` or the conversation): run the skill that fills the missing section first (`02-icp-persona`, with `02-customer-research` behind it; or `01-competitor-profiling`), then continue.
  - **It doesn't:** stop. Name each missing section with the skill that fills it (ICP and personas → `02-icp-persona`; Current alternatives → `02-customer-research`, or Competitors and alternatives → `01-competitor-profiling`). Ask for customer interviews, sales-call notes or reviews and dated competitor observations, not a description of the buyer. Don't suggest competitors or alternatives by name from memory, even as examples. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.
- If `02-customer-research` is not loaded, stop and say: enable mkt-q1-audience.
- If `01-competitor-profiling` is not loaded, stop and say: enable mkt-q1-audience.

## Process

Follow Dunford's order. Each step uses the one before it. Detail and traps: [references/obviously-awesome.md](references/obviously-awesome.md). Test the final frame and USP against the Ries & Trout laws and Reeves's 3-part USP check in [references/positioning-classics.md](references/positioning-classics.md).

1. **Competitive alternatives.** What would the best-fit customers do if the business did not exist? Take the list from the context, including DIY, an in-house hire and doing nothing wherever evidence shows them. Rank them by how often buyers actually choose them (lost deals, switch stories, counts), not by how much they worry you, and sort the table rows in that order, highest count first. Count with `scripts/tally.py` when you count from files.
2. **Unique attributes.** List what the business has that the alternatives lack: capabilities, delivery, expertise, terms. Use only what is confirmed to exist across the product today: any `offer.md` item marked *proposed*, *planned*, *unknown*, or only seen once / *confirm it is standard* is NOT a current attribute and must appear only under Future differentiators — never as a current attribute, a current "Where we beat it" edge in the Alternatives table, or a claim in the Positioning statement. For each attribute, check the alternatives' dated claims:
   - **Unique:** no alternative claims it, as far as the evidence shows (say *as observed on <date>*).
   - **Shared:** an alternative claims it too (name who); it can't carry the position alone.
   - **Better, with proof:** both have it, and evidence shows the business's version is better for this buyer (a number, a buyer's reason).
   - **Unproven:** the business says it, but no evidence shows buyers value or notice it.
   - **Unknown against competitors:** there is no dated evidence about the alternatives on this point. *Shared* needs a named source; never assume what *any* or *most* competitors in the category offer.
3. **Value.** For each unique or better attribute, write what it enables for the customer and the evidence that customers care (their words, a struggling moment, a lost-deal reason). An attribute nobody values is not a differentiator. Group the values into one to three themes.
4. **Best-fit customers.** Who cares most about that value? Take them from the ICP and segments, and name who the position is *not* for, with evidence (disqualifiers, churn reasons, wrong-fit losses).
5. **Market category.** Choose the frame of reference that makes the value obvious to those customers, and say why, with evidence of how buyers describe their search (the questions they ask, the terms they use). Weigh three options:
   - **Head-on in an existing category**, when the business can win it as buyers define it;
   - **A subsegment of an existing category** (*X for Y*), when it wins only for a specific customer;
   - **A new category**, only when no existing frame fits. That is a separate decision with a high cost: record it as an option and hand it to `06-category-design`.
6. **Write the statements.**
   - **Positioning statement (Moore):** *For [target customer] who [need], [product] is a [category] that [key benefit]. Unlike [primary alternative], it [key difference].* Every slot comes from steps 1–5.
   - **Only-ness statement (Neumeier)**, only when step 2 found a unique attribute: *[Brand] is the only [category] that [difference] for [customer] in [market] who [need] during [era].* Do not claim *only* if the evidence shows an alternative claims the same thing; say what would have to be verified.
   - **Perceptual map**, only when two axes buyers care about are evidenced (for example speed of numbers and depth of advice), placing each alternative from evidence; unplaced alternatives say *unknown*.
   - **USP and value proposition:** the one benefit the alternatives cannot or do not claim, and the jobs, pains and gains it serves (Value Proposition Canvas), in a line each.
7. **Proof and test.** For each claim in the statement, name its proof or mark the gap. Propose how to test the position: sales-call framing, win rate against the primary alternative over a stated number of calls, the questions buyers stop asking.
8. **Check before saving.** Re-read the draft against every item under Checks, and run `scripts/check_quotes.py` on the file. Fix every failure before you save.

**Nothing the context doesn't support.** No capability, result, price, customer count, competitor fact or buyer motive that is not in `context/` or `inputs/`. Competitor claims are their claims, with the date seen. A competitor's visible tactic is not proof that it works. Inferences carry `(assumption)`. A proposed capability is never written as if it exists.

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from a source (a customer, a competitor's page as recorded), with the source named. The statements and your summaries are your own words: write them in italics or plain text. Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py context/positioning.md`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches.

## Output

Write five sections of `context/positioning.md`, replacing each section's body and leaving every other section (`## Unique mechanism`, `## Category design`, and every other file) exactly as it was:

```markdown
## Category
Status: draft (<YYYY-MM-DD>, 06-positioning-statement)
Written by: 06-positioning-statement, <YYYY-MM-DD>
Category: <frame of reference> — <head-on / subsegment / new-category option handed to category-design>
Why this frame: <how buyers describe their search, with evidence>
Evidence: <sources>
Method: Market category, Obviously Awesome (Dunford)

## Target customer
Status: draft (<YYYY-MM-DD>, 06-positioning-statement)
Written by: 06-positioning-statement, <YYYY-MM-DD>
Best fit: <who cares most about the value, from the ICP, with evidence>
Not for: <who the position excludes, with evidence>
Evidence: <sources>
Method: Best-fit customers, Obviously Awesome (Dunford)

## Competitive alternatives
Status: draft (<YYYY-MM-DD>, 06-positioning-statement)
Written by: 06-positioning-statement, <YYYY-MM-DD>
| Alternative | What buyers use it for | How often chosen (evidence) | Where it beats us | Where we beat it |
| --- | --- | --- | --- | --- |
Primary alternative: <the one the statement names, and why>
Evidence: <sources>
Method: Competitive alternatives analysis, Obviously Awesome (Dunford)

## Differentiation
Status: draft (<YYYY-MM-DD>, 06-positioning-statement)
Written by: 06-positioning-statement, <YYYY-MM-DD>
| Attribute (exists today) | Unique / shared / better / unproven / unknown | Value to the customer | Evidence customers care | Proof |
| --- | --- | --- | --- | --- |
Value themes: <one to three>
Future differentiators (not yet true): <proposed items, with their status>
USP: <one line>
Value proposition: <jobs, pains, gains served, one line>
Evidence: <sources>
Method: Unique attributes and value, Obviously Awesome (Dunford); USP (Reeves); Value Proposition Canvas (Osterwalder)

## Positioning statement
Status: draft (<YYYY-MM-DD>, 06-positioning-statement)
Written by: 06-positioning-statement, <YYYY-MM-DD>
Statement: *For … who …, … is a … that … . Unlike …, it … .*
Only-ness: *<statement>* or not claimed — <why>
Perceptual map: <axes and placements from evidence> or not drawn — <why>
Proof per claim: <claim → proof or gap>
Test: <how, over how many calls or weeks, what would change it>
Evidence: <sources>
Method: Positioning statement (Moore, Crossing the Chasm); Obviously Awesome (Dunford); Positioning (Ries & Trout)
```

- In table cells, paraphrase without quotation marks unless you copy a source exactly.
- Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/positioning.md` does not exist, create it with frontmatter, all seven positioning sections (the two you don't own `Status: empty`) and a change log.

Reply with:
- the positioning statement in one line, and the primary alternative it is set against;
- the weakest link (an unproven claim, a shared attribute, thin evidence) and what would fix it;
- the next skill: `06-unique-mechanism` (why it works), `06-category-design` if a new category is on the table, `06-competitor-pages`, or `08-message-doc`.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The alternatives include DIY, in-house and doing nothing wherever evidence shows them, ranked by how often buyers choose them, with the table rows sorted highest count first.
- [ ] Every differentiator exists today; proposed or unknown capabilities are listed only as future differentiators.
- [ ] Each attribute is labelled unique, shared (naming who also claims it, with a source), better with proof, unproven, or unknown against competitors. No *only* or *better* claim without evidence, and nothing assumed about what competitors in general offer.
- [ ] Every value has evidence that customers care; the target customer and who it is *not* for both cite evidence.
- [ ] The category choice gives a reason from how buyers describe their search; a new category is only an option handed to `06-category-design`.
- [ ] The Moore statement fills every slot from steps 1–5 and claims nothing the proof line doesn't support.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean. No unmarked inference.
- [ ] Only the five owned sections changed. Each has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

A position is a place in the buyer's mind relative to the alternatives they already know, built from what you have that they lack, the value it creates for the customers who care most, and the category frame that makes that value obvious; who you are not for is part of it. Obviously Awesome (April Dunford); Crossing the Chasm (Geoffrey Moore); Positioning: The Battle for Your Mind and The 22 Immutable Laws of Marketing (Al Ries and Jack Trout); Reality in Advertising (Rosser Reeves); The Complete Marketing System, section 6 Positioning (Servidad, 2026).
