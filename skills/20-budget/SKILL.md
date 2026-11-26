---
name: 20-budget
description: Allocate and pace the marketing budget across proven, growing and test work, with rules for moving money. Use for marketing budget, budget split, 70/20/10, how much to spend, budget pacing.
metadata:
  section: "20 Operations"
  covers: "70/20/10 budget"
---
# Marketing budget

A marketing budget sets how much money goes where, how fast it is spent, and when it moves. It works when it starts from what the business can afford (margin and cash), splits spend between proven work, scaling work and experiments, paces it month by month against the plan, and has written rules for moving money based on cost per business outcome. It fails when the split comes from a rule of thumb with no link to the economics, spend is decided month by month by feel, experiments get nothing, or money follows platform ROAS.

Save the budget plan as a Markdown file in `work/20-operations/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Spend, revenue, margin, cash and outcome figures in `inputs/` and context are the evidence.
- If present, also read `context/offer.md` → Price and model; spend, revenue, margin, cash and outcome figures in `inputs/`; any work in `work/17-measurement/17-unit-economics-*.md`, `work/19-growth/` or `work/20-operations/20-marketing-plan-*.md`.
- **No data:** Without spend, margin or cash figures, give the allocation method, ask for those figures, and explicitly say how to provide them (drop exports or notes in `inputs/` or paste into chat); propose no amounts. Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** The total budget and every allocation are the owner's; the plan proposes and the owner sets them.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/budget-guide.md](references/budget-guide.md) for affordability, the 70/20/10 split as a heuristic, brand and activation, pacing and reallocation rules.

1. **Affordability.** What the business can spend from contribution margin, payback and cash (from `17-unit-economics` or computed from `inputs/`), shown with arithmetic; the total is the owner's.
2. **Current spend.** By line and month from `inputs/`, with cost per new customer from the source of truth; compute with [scripts/sum_by.py](scripts/sum_by.py).
3. **70/20/10 budget.** A heuristic, not a rule: most to proven work, some to scaling what is promising, a little to experiments; the actual split follows the evidence and the plan's priorities, with the reason for each line. Brand versus activation is discussed as a published heuristic, labelled, not applied blindly.
4. **Pacing.** Month by month, including seasonal dates and freelancer and tool costs.
5. **Reallocation rules.** Written in advance: when a line hits or misses its guardrail cost per business outcome, what moves where; scaling goes through `19-scale-paid` gates.
6. **Approval.** The budget is a draft. Committing or moving money needs the owner's explicit approval.
7. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no budgets, margins, costs or benchmarks that aren't in `context/` or `inputs/`, computed from them, or set by the owner. Heuristics are labelled as heuristics. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/20-operations/20-budget-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Marketing budget: <business, period>
Skill: 20-budget · Date: <YYYY-MM-DD> · Framework: 70/20/10 budget (heuristic) with affordability and reallocation rules
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; no money committed
## Affordability
## Current spend and cost per new customer
## Allocation
| Line | Proven, scaling or experiment | Monthly amount (owner to set) | Reason | Guardrail |
| --- | --- | --- | --- | --- |
## Pacing by month
## Reallocation rules
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/20-operations/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, what the business can afford with the arithmetic, the proposed split and why, and the rules for moving money, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Affordability is computed from margin, payback or cash, or the gap is named.
- [ ] Current spend and cost per new customer come from the source of truth, not platform ROAS.
- [ ] 70/20/10 and brand-versus-activation are labelled heuristics; each line has a reason tied to evidence or the plan.
- [ ] Pacing covers every month, tools and freelancers; reallocation rules are written in advance.
- [ ] Amounts are the owner's; nothing is committed without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Spend what the economics can afford, put most of it where evidence is strongest, keep a small share for learning, and write the rules for moving money before you need them. 70/20/10 budget (a heuristic); The Complete Marketing System, section 20 Operations (Servidad, 2026); The Long and the Short of It (Les Binet and Peter Field) for brand and activation.
