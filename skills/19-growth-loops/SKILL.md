---
name: 19-growth-loops
description: Design growth loops where each cycle's output feeds the next (referral, content, paid, sales). Use for growth loops, flywheel, compounding growth, self-sustaining growth, loops vs funnels.
metadata:
  section: "19 Growth"
  covers: "Flywheel; Growth loops"
---
# Growth loops

A growth loop is a cycle where new customers or their output bring the next ones: customers refer friends, content brings searchers who create more content, revenue funds ads that bring revenue. It works when the loop is drawn step by step with real rates, the cycle time and the multiplier per cycle are measured or labelled assumptions, the weakest step is fixed first, and the loop is checked to be closing (each cycle brings back at least part of what went in). It fails when a funnel is renamed a flywheel, a loop is claimed with no measured return, incentives buy low-value customers, or the loop's maths is assumed rather than counted.

Save the loop design as a Markdown file in `work/19-growth/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Referral, content, spend and revenue figures in `inputs/` and context are the evidence.
- If present, also read `context/offer.md` → Core offer, Price and model; `context/customer.md` → Segments; referral, survey, content, spend and revenue figures in `inputs/`; any work in `work/16-referral/`, `work/11-distribution/` or `work/19-growth/`.
- **No data:** Without figures, draw candidate loops with each step's metric, ask for the rates, and explicitly state **how to provide them** (save exports or notes in `inputs/`, or paste into chat); claim no loop as working. Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/growth-loops-guide.md](references/growth-loops-guide.md) for loop types, step metrics, cycle time, the multiplier per cycle, the flywheel and incentive risks.

1. **Candidate loops.** From the business: referral or word of mouth, content or SEO, paid (revenue funds acquisition), sales, or user-generated content. Draw each as steps that return to the start.
2. **Step rates.** Each step's rate from `inputs/` with its source, or *unknown*; compute with [scripts/sum_by.py](scripts/sum_by.py).
3. **Loop maths.** Multiplier per cycle (new customers from one cohort's output), cycle time, and whether the loop closes (paid loop: contribution margin per customer within payback funds the next customer; referral loop: referred customers per customer). Below 1 it adds to growth but doesn't sustain itself; say so.
4. **Weakest step.** The step whose improvement lifts the multiplier most; hand it to the owning skill (for example `16-referral-program`, `11-seo`, `19-scale-paid`).
5. **Flywheel.** How the loops feed each other and what slows them (friction such as late deliveries), so friction is removed before force is added.
6. **Measure.** The loop's metrics on a dashboard (`17-dashboard`) and the first test.
7. **Approval.** The design is a draft. Launching incentives, programs or spend needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no rates, multipliers, cycle times or benchmarks that aren't in `context/` or `inputs/` or computed from them. Unknown rates stay *unknown*. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/19-growth/19-growth-loops-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Growth loops: <business, date>
Skill: 19-growth-loops · Date: <YYYY-MM-DD> · Framework: Growth loops; Flywheel
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval
## Candidate loops
## Step rates
| Loop | Step | Rate | Source or unknown |
| --- | --- | --- | --- |
## Loop maths
## Weakest step and hand-off
## Flywheel and friction
## Measure and first test
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/19-growth/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, which loops exist with their measured rates, which closes, the weakest step, and the first test, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Each loop is drawn as steps that return to the start, not a funnel renamed.
- [ ] Each step has a rate with a source or *unknown*; loop maths (multiplier, cycle time, closing) is shown.
- [ ] The weakest step is named and handed to its owner; incentive risks are named.
- [ ] Friction in the flywheel is addressed before adding force.
- [ ] Nothing launches without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Draw the loop with real rates, find the step that limits the return, remove friction before adding force, and never call a funnel a loop until you have counted what comes back. Growth loops (Reforge), Flywheel (Jim Collins, Good to Great; Amazon); The Complete Marketing System, section 19 Growth (Servidad, 2026).
