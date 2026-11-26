---
name: 19-growth-model
description: Build a growth model and forecast from real funnel rates, with scenarios and the levers that move it. Use for growth forecasts, growth models, is our target realistic, what it takes to hit a goal.
metadata:
  section: "19 Growth"
  covers: "Abraham's three ways to grow; Growth model / forecast"
---
# Growth model

A growth model links the inputs the business controls (traffic, conversion, price, retention, referrals) to the outcome it wants, so a target can be checked and the biggest lever found. It works when every input comes from observed data for a stated period, assumptions are labelled and varied in scenarios, losses are modelled as well as gains, and the forecast shows what would have to be true to hit a goal. It fails when a target is divided back into made-up rates, retention is left out, one optimistic line is presented as a plan, or the model is more precise than the data under it.

Save the growth model as a Markdown file in `work/19-growth/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Volumes, rates, price and retention figures in `inputs/` and context are the evidence.
- If present, also read `context/offer.md` → Price and model; funnel, spend, cohort, cancellation and capacity figures in `inputs/`; any work in `work/17-measurement/17-unit-economics-*.md` or `work/19-growth/19-constraint-finder-*.md`.
- **No data:** Without figures, give the model structure and ask for monthly new customers, conversion by step, price, and losses or cohort retention, and explicitly state **how to provide them** (save exports or notes in `inputs/`, or paste into chat); forecast nothing. Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/growth-model-guide.md](references/growth-model-guide.md) for model structure, the three ways to grow, scenarios, sensitivity and the settling level.

1. **Structure.** Outcome (for example active subscriptions, revenue, contribution margin) = starting level + new − lost per period; new = traffic × conversion by step; revenue = customers × frequency × price. Draw it as a short chain.
2. **Inputs from data.** Each input with its value, period and source; derived rates shown with their arithmetic; measurement defects noted. Unknowns are labelled assumptions.
3. **Abraham's three ways to grow.** Show the effect of more customers, higher value per purchase and more purchases per customer (or longer retention) on the outcome.
4. **Forecast and scenarios.** Base (current rates), low and high, month by month for the horizon asked; include the settling level (new ÷ loss rate) and capacity limits. Use [scripts/sum_by.py](scripts/sum_by.py) or arithmetic shown.
5. **Goal check.** If a target is given, show what would have to be true to reach it (for example new per month at the current loss rate, or the loss rate at the current inflow) and whether evidence supports that.
6. **Sensitivity.** Which input moves the outcome most per realistic change; hand the lever to the owning skill.
7. **Approval.** The model is a draft. Using it to set budgets, targets or hires needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no rates, volumes, prices or benchmarks that aren't in `context/` or `inputs/` or computed from them. Scenario changes are labelled assumptions. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/19-growth/19-growth-model-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Growth model: <business, horizon>
Skill: 19-growth-model · Date: <YYYY-MM-DD> · Framework: Growth model / forecast; Abraham's three ways to grow
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; projections, not results
## Structure
## Inputs
| Input | Value | Period | Source or assumption |
| --- | --- | --- | --- |
## Three ways to grow
## Forecast and scenarios (projected)
## Goal check
## Sensitivity and the lever
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/19-growth/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the base forecast and settling level, whether the goal is reachable and what would have to be true, and the biggest lever, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every input has a value, period and source, or is labelled an assumption.
- [ ] Losses are modelled; the settling level and capacity limits are shown.
- [ ] Scenarios vary labelled assumptions; forecasts are labelled projected.
- [ ] The goal check shows what would have to be true and whether evidence supports it.
- [ ] The biggest lever is named and handed to its owner; nothing is set without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Model growth from observed rates, include what you lose as well as what you gain, show what must be true to hit a goal, and let the biggest lever choose the work. Abraham's three ways to grow (Jay Abraham, Getting Everything You Can Out of All You've Got); Growth model / forecast, The Complete Marketing System, section 19 Growth (Servidad, 2026).
