---
name: 04-plg-audit
description: Audit a free, freemium, trial or self-serve product as the growth engine, from signup to value, habit and paid. Use for product-led growth, habit loops, free users who don't upgrade. Not for pricing.
metadata:
  section: "04 Product"
  covers: "Hook Model (Eyal); Product-led growth"
---
# PLG audit

In product-led growth the product does the work a salesperson would: people find it, start free, get real value on their own, come back, and pay or ask to talk when the value is proven. The engine works only if the free product reaches the right people, gets them to first meaningful value fast, brings them back, and leads to a paid step those people can buy. This skill audits each link from evidence, says where it leaks and for whom, and hands the fixes to their owners. It changes nothing live.

## Needs (read before writing)

- **Product evidence**, in `inputs/`, elsewhere in the project, or pasted by the user. Any of these counts:
  - a funnel or product-analytics export (signups, setup, first value, return, upgrade or call, paid), with its event definitions and export date, ideally by cohort and segment;
  - notes on what the free product is, what is free and what is paid, how a user moves to paid;
  - in-product feedback, support tickets, usage or retention by cohort;
  - costs of serving free users (infrastructure, vendor fees, support time).
- If present, also read:
  - `context/customer.md` → Jobs to be done (`02-jobs-to-be-done`), Segments and ICP and personas: what value means and who the engine should bring in;
  - `context/offer.md` → Price and model (`07-pricing`), Core offer and Value ladder: what the paid step is, and whether the free product is listed;
  - any `work/04-product/04-pmf-check-*.md` file.
- Nothing upstream is required. If there is no product evidence and no free or self-serve product exists, say whether a product-led model could fit (step 1) from what the user and the context say, mark it `(assumption)`, and write the audit plan described under Output. Never state a conversion rate, activation rate, benchmark or "typical freemium" figure from memory.

## Process

Use [references/plg-engine.md](references/plg-engine.md) for the fit test, the funnel links, the Hook Model and the owners of each fix.

1. **Test the fit first.** Is a free or self-serve product the right engine for this business? Use Bush's MOAT questions (market strategy, ocean conditions, audience, time-to-value): can a buyer reach real value alone, quickly, without a salesperson; is the user also the buyer or an influencer of the buyer; does free use cost little to serve? Name the model it fits: *freemium*, *free trial*, *free tool feeding a sales or service motion* (product-led sales), or *not product-led* (then say what the nearest honest equivalent is, such as a sample or a demo, and who owns it).
2. **Map the engine** from the export, link by link: signup → setup → first meaningful value → return (habit) → paid step (upgrade, call, purchase) → expansion or referral. Copy the event definitions from the source. Sum and rate every step with [scripts/funnel.py](scripts/funnel.py) (`python3 <this skill's folder>/scripts/funnel.py <export.csv> <segment column>`), never by eye, overall, by segment and by cohort. Exclude or flag cohorts too young for a later step (`--exclude <value>`).
3. **Define first meaningful value** (activation). It is the first moment the user gets the result they came for, not a setup step and not an event the system fires on its own. Name the candidate event, why it represents value, and how strong the evidence is. Do not call signup, connection, an automatic event or a tutorial *activation*. Fix the denominator and window before reading the rate.
4. **Read habit with the Hook Model.** Trigger (external, such as an email, and internal, such as a worry), action (the smallest thing the user does), variable reward (what changes each time), investment (data, setup, history that makes the product better with use). Which link is weak, from the evidence?
5. **Check who the engine brings in.** Split every step by segment. A free product that mostly attracts buyers who cannot or will not buy the paid step is an acquisition leak, not a conversion leak. Compare with the ICP and the owner's stated goal.
6. **Check the paid step.** What exactly does a user pay for or move to; is it visible at the moment of value; does it fit the segments that get value? A price a user *says* they would pay is stated preference, not evidence of willingness to pay: hand price and packaging to `07-pricing`, and the step itself to `13-paywalls` or `13-signup`.
7. **Check the economics and the measurement.** Cost to serve free users (from the source, or *unknown*), paid outcomes and their value. Check how conversions are attributed (a call booked in the product may already be counted under another lead source) so the product is not credited twice or not at all. A connection error or defect is a product failure to fix before blaming onboarding.
8. **Diagnose the leak.** Name the link or links where the evidence says the engine loses the most of the *right* users, with counts, and what else could explain it (fit, a defect, measurement). Say if leaks are co-limiting or the evidence cannot separate them.
9. **Recommend tests, not changes.** Each fix is a hypothesis with its owner skill, metric, window and stopping rule (experiments → `18-hypothesis`; onboarding → `15-onboarding`; invites and sharing → `16-viral-loop`; the in-product prompts' wording → `10-page-copy`). Any change to the live product, its price or its signup needs the owner's approval and a check afterwards.
10. **Check before saving.** Re-read the draft against the Checks and run `scripts/check_quotes.py`; fix any failure.

**Labels.** Every number is copied from a named export or note (with its date), *calculated* by `funnel.py` or `python3` (show numerator and denominator), or marked `(assumption)`. No unmarked inference.

**Platform facts.** Do not state how an analytics tool, app store, payment provider or integrated platform (for example an accounting app's connection) currently works unless you cite its own documentation as `(first-party: <URL>, checked YYYY-MM-DD)`. Otherwise describe only what the export and notes show, and mark anything else *unverified*.

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from a source, with the source ID. Your own proposed prompts and lines go in italics. Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py <file>`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches. Row counts come from [scripts/tally.py](scripts/tally.py).

## Output

**With evidence**, write `work/04-product/04-plg-audit-<YYYY-MM-DD>-plg-audit.md`:

```markdown
# PLG audit: <product> (<date>)
Skill: 04-plg-audit · Framework: Product-Led Growth (Bush); Hook Model (Eyal)
Built from: <exports, notes and context sections used, with dates and status>
## Fit: is product-led the right engine?
<MOAT answers; model it fits; or not product-led and the nearest honest equivalent>
## The engine, link by link
| Link | Event (source definition) | Count | Rate (calculation) | By segment | Reading |
| --- | --- | --- | --- | --- | --- |
## First meaningful value
<candidate event, why, evidence strength; events that are not value>
## Habit (Hook Model)
## Who it brings in
## The paid step
## Economics and measurement
## Diagnosis
<the leak or leaks, with counts, and alternative explanations>
## Tests to run (owner approval needed for live changes)
| Hypothesis | Change | Metric, window, stopping rule | Owner skill |
| --- | --- | --- | --- |
## Claims and sources
| Claim or number | Source or calculation |
| --- | --- |
## Open questions
## Principle, framework, source
```

**Without evidence**, write `work/04-product/04-plg-audit-<YYYY-MM-DD>-plan.md`: the fit test answered as far as the context allows (marked `(assumption)`), the funnel events to define and export (with their definitions), the segment field to capture at signup, the cost and attribution data to pull, and how each will be read. State no rate or benchmark.

Change nothing in `context/` and nothing live. This is an audit, not a decision.

Reply, with evidence, with:
- the fit verdict and the biggest leak, with its counts and segment;
- the most important limit of the evidence;
- the first test to run and its owner skill, and a reminder that live changes need the owner's approval.

Reply, without evidence, with the plan's path and a plain list of the material to bring (a funnel export with event definitions and dates; the free and paid boundary; costs; segment at signup) and how to provide it: save the files in `inputs/` or paste them, then ask again.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The fit of a product-led model is tested before the funnel, and the model named (freemium, free trial, free tool feeding sales, or not product-led).
- [ ] Every step's count and rate comes from `funnel.py` or a shown calculation, keeps its source definition, and is split by segment; incomplete cohorts are flagged.
- [ ] First meaningful value is a user result, not signup, setup, an automatic event or a tutorial, and its evidence strength is stated.
- [ ] Who the engine brings in is compared with the ICP; a wrong-fit acquisition leak is separated from a conversion leak.
- [ ] Stated willingness to pay is not treated as a price; price and packaging go to `07-pricing`.
- [ ] Cost to serve and attribution are stated or marked unknown, and defects are separated from onboarding friction.
- [ ] Recommendations are tests with metric, window, stopping rule and owner skill; no live change is made or implied as done.
- [ ] No current platform behaviour is asserted without a first-party citation and date.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

The product is the first marketing channel: a free product grows the business only when the right people reach real value on their own, come back, and find a paid step they can buy, so audit fit, value, habit and the path to paid from evidence before adding more signups. Product-Led Growth (Wes Bush, Product-Led Growth, 2019); Hook Model (Nir Eyal, Hooked, 2014); The Complete Marketing System, section 4 Product (Servidad, 2026).
