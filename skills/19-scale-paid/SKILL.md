---
name: 19-scale-paid
description: Scale paid media through gated budget steps, more creative, broader targeting and new placements. Use for scaling ads, raising ad budget, should we double spend, ads stopped scaling.
metadata:
  section: "19 Growth"
  covers: "Scaling paid media"
---
# Scaling paid media

Scaling paid media means buying more customers at a cost the business can still afford. It works only after readiness checks: the economics allow a higher marginal cost per customer, measurement reflects real customers, the constraint is acquisition rather than retention or capacity, and delivery can absorb the volume. Then spend rises in steps with a guardrail on cost per customer from the business's own data, creative volume grows with it, and each step has a stop or roll-back rule. It fails when a platform ROAS is the reason to double, the budget jumps overnight, the same tired ads carry more spend, or growth stalls because retention or fulfilment was the real limit.

Save the paid scaling plan as a Markdown file in `work/19-growth/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Spend, platform data, business outcomes, margin, retention and capacity in `inputs/` and context are the evidence.
- If present, also read `context/offer.md` → Price and model; spend, platform reports, store orders, cohorts, margin and capacity in `inputs/`; any work in `work/17-measurement/` (unit economics, attribution, incrementality), `work/18-experimentation/18-creative-testing-*.md` or `work/19-growth/19-constraint-finder-*.md`.
- **No data:** Without spend and business outcome data, list the readiness gates and ask for spend, new customers from the source of truth, margin, retention and capacity, and explicitly state **how to provide them** (save exports or notes in `inputs/`, or paste into chat); propose no budget. Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Every budget level, bid strategy and spend change is the owner's commitment; the plan proposes steps and the owner sets them.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/scale-paid-guide.md](references/scale-paid-guide.md) for readiness gates, marginal cost, budget steps, creative volume, broader targeting, new placements and stopping rules.

1. **Readiness gates.** Economics (contribution margin and payback allow the target cost per customer, from `17-unit-economics` or computed), measurement (platform counts reconciled with the source of truth; known defects named), constraint (acquisition is the limit, not retention or capacity), capacity (fulfilment and team can absorb the volume), and creative supply. Any failed gate stops the plan at that gate with the fix.
2. **Marginal, not average.** Cost per new customer from the business's own data at the current spend, and what is known about the next dollar (spend vs new customers by month, any lift test); platform ROAS is a signal only.
3. **Budget steps.** Steps the owner sets, each held long enough to read, with a guardrail cost per new customer and a roll-back rule; no single overnight jump.
4. **Creative volume.** More distinct concepts as spend rises (`18-creative-testing`), with fatigue signals (frequency, rising cost).
5. **Broader targeting and new placements.** Wider audiences or placements as tests with their own read; platform features and limits are facts to cite with URL and date or mark *to confirm*.
6. **Watch and stop.** Weekly: spend, new customers (source of truth), marginal cost, retention of new cohorts; stop, hold or roll back by the written rules.
7. **Approval.** The plan is a draft. Any budget, bid or campaign change needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no ROAS, costs, margins, budgets or platform behaviour that aren't in `context/` or `inputs/`, computed from them, or cited with a date. No universal budget-increase rule. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/19-growth/19-scale-paid-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Paid scaling plan: <business, platform, date>
Skill: 19-scale-paid · Date: <YYYY-MM-DD> · Framework: Scaling paid media (readiness gates, budget steps, creative volume)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; no budget changed
## Readiness gates
| Gate | Evidence | Pass, fail or unknown |
| --- | --- | --- |
## Marginal cost per new customer
## Budget steps (owner to set)
| Step | Spend | Hold for | Guardrail | Roll back if |
| --- | --- | --- | --- | --- |
## Creative volume
## Targeting and placements tests
## Weekly watch and stopping rules
## Platform facts
| Fact the plan relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/19-growth/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, which readiness gates pass or fail with the numbers, whether to scale now, and the first step and its stop rule, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every readiness gate is checked with evidence; a failed gate stops the plan with its fix.
- [ ] Cost per new customer comes from the source of truth; platform ROAS is not the reason to scale.
- [ ] Budget rises in owner-set steps with guardrails and roll-back rules; no overnight jump or universal rule.
- [ ] Creative volume and fatigue are planned; targeting and placement changes are tests with dated platform facts.
- [ ] Nothing changes without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Scale only when the economics, measurement, constraint and capacity say the next customer is worth buying, then raise spend in steps you can read and roll back. Scaling paid media, The Complete Marketing System, section 19 Growth (Servidad, 2026).
