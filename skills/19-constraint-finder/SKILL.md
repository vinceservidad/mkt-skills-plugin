---
name: 19-constraint-finder
description: Find the growth stage and the constraint limiting growth now, with evidence, before choosing what to fix. Use for what is holding us back, growth bottleneck, why growth stalled, what to fix first.
metadata:
  section: "19 Growth"
  covers: "Growth stages (validate → optimize); Theory of Constraints"
---
# Constraint finder

Growth is limited by whatever is scarcest right now: demand, conversion, retention, delivery capacity, cash or the team's time. Finding it stops effort going into steps that won't move the total. It works when the business is placed in its growth stage (validating, then repeating, then optimizing, then expanding), each candidate constraint is checked against numbers from the same period, and the diagnosis says plainly when two limits bind together or the evidence can't separate them. It fails when the constraint is whatever the owner already wanted to fix, a generic funnel checklist replaces the numbers, or a scaling plan is written while customers leave as fast as they arrive.

Save the constraint diagnosis as a Markdown file in `work/19-growth/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Acquisition, conversion, retention, capacity and cash figures in `inputs/` and context are the evidence.
- If present, also read `context/customer.md` → Segments; `context/offer.md` → Core offer, Price and model; funnel, cohort, spend, capacity and cash figures in `inputs/`; any work in `work/17-measurement/`, `work/15-retention/` or `work/04-product/04-pmf-check-*.md`.
- **No data:** Without figures, give the stage questions and the checks, ask for new customers, losses, conversion, capacity and cash by month, and explicitly state **how to provide them** (save exports or notes in `inputs/`, or paste them into chat); name no constraint. Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/constraint-guide.md](references/constraint-guide.md) for growth stages, the constraint checks, stock-and-flow arithmetic and co-limiting constraints.

1. **Primary business outcome and baseline.** Name it (for example active paying customers, contribution margin), its current level and trend, and the period, from `inputs/`.
2. **Growth stage.** Validate (does a defined buyer keep buying?), repeat (can we get more of them on purpose?), optimize (are the steps efficient?), expand (new segments, offers or markets). Place the business with evidence.
3. **Stock and flow.** Customers in, customers out, net change per month; the level the business would settle at if inflow and loss rates stayed the same (inflow ÷ loss rate). Compute with [scripts/sum_by.py](scripts/sum_by.py) or plain arithmetic shown.
4. **Check each candidate.** Demand (enough reachable buyers?), conversion (step rates), retention (loss rate, cohorts), delivery and capacity, cash and margin, team time, and measurement quality. For each: the number, the evidence, and whether it limits the outcome now.
5. **Theory of Constraints.** Name the constraint (or say co-limiting or unresolved, and what evidence would separate them); exploit it before adding elsewhere; say what not to work on now and why.
6. **Hand-offs.** Route the work to the owning skill (for example `15-churn-prevention`, `13-cro-audit`, `19-scale-paid`) with the number to watch.
7. **Approval.** The diagnosis is a draft. Changing budgets, offers, pages or operations needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no figures, benchmarks or causes that aren't in `context/` or `inputs/` or computed from them. Guesses are labelled. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/19-growth/19-constraint-finder-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Constraint diagnosis: <business, date>
Skill: 19-constraint-finder · Date: <YYYY-MM-DD> · Framework: Growth stages (validate → optimize); Theory of Constraints
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval
## Outcome and baseline
## Growth stage
## Stock and flow
## Candidate constraints
| Candidate | Number (source) | Limits the outcome now? | Evidence strength |
| --- | --- | --- | --- |
## The constraint (or co-limiting / unresolved)
## Not now
## Hand-offs and the number to watch
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/19-growth/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the stage, the constraint with its numbers (or why two bind together), what not to work on now, and the first hand-off, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The primary business outcome, baseline and period are named from the data.
- [ ] Stock and flow arithmetic is shown, including the level growth would settle at.
- [ ] Every candidate is checked with a number and source; measurement defects are noted.
- [ ] The constraint is named, or co-limiting or unresolved constraints are stated with what would separate them.
- [ ] Non-priorities are explicit; nothing changes without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Find what limits the outcome now with numbers from one period, fix that before feeding more into the system, and say so when two limits bind together. Growth stages (validate → optimize) and Theory of Constraints (Eliyahu Goldratt, The Goal); The Complete Marketing System, section 19 Growth (Servidad, 2026).
