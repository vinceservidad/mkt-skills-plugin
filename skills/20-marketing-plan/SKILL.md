---
name: 20-marketing-plan
description: Write the one-page marketing plan with goals, priorities, owners, budget, KPIs and a calendar. Use for marketing plan, annual plan, quarterly plan, OKRs, who owns what, marketing roadmap.
metadata:
  section: "20 Operations"
  covers: "EOS / Scaling Up; Marketing plan; OKRs; RACI; T-shaped marketer / pod structure"
---
# Marketing plan

A marketing plan says what marketing will achieve, the few priorities that get there, who owns each, what it costs, how progress is measured and when things happen. It works when it starts from a primary business outcome with a baseline, picks priorities from the diagnosed constraint rather than a channel checklist, gives each priority one owner and a measure, fits the team's real hours and budget, and lists what is deliberately not being done. It fails when it is a list of every tactic, targets are invented, nobody owns anything, or the plan needs three times the hours the team has.

Save the one-page marketing plan as a Markdown file in `work/20-operations/` when the required inputs are present and the commercial terms are confirmed. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: who the plan is for.
- `context/offer.md` → **Core offer**, from `07-offer-design`: what the plan sells.
- If present, also read `context/message.md` → Promise; `context/customer.md` → Segments; budget, team, capacity, growth and measurement figures in `inputs/`; any work in `work/19-growth/`, `work/17-measurement/` or `work/20-operations/`.
- If a required section is missing:
  - **The upstream evidence exists** (reviews, tickets, sales or customer notes in `inputs/`): run `02-icp-persona` or `07-offer-design` first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (ICP and personas → `02-icp-persona`; Core offer → `07-offer-design`), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Targets, budgets and hires are the owner's commitments; the plan proposes and the owner sets them.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/marketing-plan-guide.md](references/marketing-plan-guide.md) for the one-page layout, OKRs, RACI, EOS and Scaling Up rhythms, and team shapes.

1. **Outcome and baseline.** The primary business outcome, its current level and period from `inputs/`, and the horizon. Targets are the owner's; if none is set, show what current rates project (`19-growth-model`) and ask.
2. **Priorities from the constraint.** Three or fewer, each tied to the diagnosed constraint (`19-constraint-finder`) or labelled as an assumption if no diagnosis exists. List explicit non-priorities.
3. **OKRs.** For each priority, an objective and two or three key results with baseline and a measure from the source of truth.
4. **Owners: RACI.** One accountable owner per priority; who does, who is consulted, who is informed.
5. **Capacity and budget.** Hours and money each priority needs against what the team has (from `inputs/`); cut or phase priorities that don't fit. Budget detail goes to `20-budget`.
6. **Rhythm.** EOS / Scaling Up style: a weekly meeting (`20-campaign-review`), monthly numbers, quarterly reset. Team shape: who covers what, T-shaped marketer or pod structure if the team grows.
7. **Calendar.** Major dates and launches by month (`20-content-calendar` for detail).
8. **Approval.** The plan is a draft. Targets, budgets, hires and launches need the owner's explicit approval.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no targets, budgets, rates or benchmarks that aren't in `context/` or `inputs/` or set by the owner. Projections are labelled. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/20-operations/20-marketing-plan-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Marketing plan: <business, period>
Skill: 20-marketing-plan · Date: <YYYY-MM-DD> · Framework: Marketing plan with OKRs and RACI; EOS / Scaling Up rhythm
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval
## Outcome and baseline
## Priorities and not now
## OKRs
| Objective | Key result | Baseline (source) | Target (owner) |
| --- | --- | --- | --- |
## Owners (RACI)
## Capacity and budget
## Rhythm and team
## Calendar
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/20-operations/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the outcome and baseline, the priorities and what is not being done, owners, and whether it fits the team's hours and budget, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The plan starts from a primary business outcome with a baseline and period; targets are the owner's.
- [ ] Priorities come from the diagnosed constraint (or are labelled assumptions); non-priorities are explicit.
- [ ] Each priority has OKRs with baselines and one accountable owner.
- [ ] Hours and budget fit the team; priorities that don't fit are cut or phased.
- [ ] Nothing is set without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Start from the outcome and the constraint, choose a few priorities that fit the team's real hours, give each an owner and a measure, and say what you will not do. Marketing plan with OKRs (Andy Grove, John Doerr), RACI, EOS / Scaling Up (Gino Wickman, Verne Harnish) and the T-shaped marketer / pod structure; The Complete Marketing System, section 20 Operations (Servidad, 2026).
