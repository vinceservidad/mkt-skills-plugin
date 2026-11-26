---
name: 17-dashboard
description: Design a dashboard around the north star and its input metrics, with sources, owners and decisions. Use for marketing dashboards, KPI tree, north star metric, weekly metrics, what to track.
metadata:
  section: "17 Measurement"
  covers: "Dashboards; KPI tree / driver tree; North Star Metric"
---
# Dashboard

A dashboard is for decisions, not decoration. It works when it starts from one north star metric tied to customer value and revenue, breaks it into the few input metrics the team can move (a KPI or driver tree), names the source, definition, owner and review rhythm for each, and shows the trend against a target. It fails when it lists every number the tools offer, mixes vanity metrics with outcomes, uses platform numbers as truth, or nobody knows what decision a chart serves. A rendered dashboard is not proof the data is right.

Save the dashboard design as a Markdown file in `work/17-measurement/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. The data sources and definitions in `inputs/` and the business's outcomes in context are the evidence.
- If present, also read `context/offer.md` → Price and model, Value ladder; `context/customer.md` → Segments; data sources, definitions, current reports and meeting rhythms in `inputs/`; any work in `work/17-measurement/` (tracking plan, unit economics, attribution).
- **No data:** Without any data sources, propose the north star and driver tree from context, list the sources and fields needed for each metric (marking all values *unknown*), and **explicitly tell the user how to provide them** (drop exports or notes in `inputs/`, or paste them into chat). Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/dashboard-guide.md](references/dashboard-guide.md) for choosing a north star, building the driver tree, metric definitions, layout and review rhythm.

1. **North Star Metric.** One metric that reflects value delivered to customers and leads to revenue (for example active subscribers), with its definition and why. If asked to make a single channel's platform metric or ROAS (such as Meta ROAS) the north star, **decline that request**: explain that it measures one platform's view of one channel (and is unreliable when tracking defects exist), not customer value delivered; choose a customer-value north star instead and demote channel ROAS to a secondary channel signal.
2. **KPI tree / driver tree.** Break it into input metrics the team can move (acquisition, activation, retention including **both voluntary cancellations and involuntary churn / failed payments** whenever billing/payment issues appear in `inputs/`, and **revenue or contribution per subscriber**), each with the formula linking it upward.
3. **Definitions and sources.** For each metric: definition, grain, source of truth, refresh, owner and known data issues (from `17-tracking-plan`).
4. **Cut the rest.** Vanity metrics (likes, followers, impressions) and duplicate views go off the main view or to a channel appendix, with the reason.
5. **Layout.** North star and trend at the top, drivers below, each with target, current value and change; a short notes area for data issues. Fewer than a dozen numbers on the main view.
6. **Rhythm and decisions.** Who reviews it when, and the decision each metric informs; a metric no decision uses is removed.
7. **Current values.** Where data exists, compute current values with [scripts/sum_by.py](scripts/sum_by.py) and label them; otherwise *unknown*.
8. **Approval.** The design is a draft. Building dashboards in tools or sharing data needs the owner's explicit approval.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no values, targets or definitions that aren't in `context/` or `inputs/` or computed from them. Targets are the owner's. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/17-measurement/17-dashboard-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Dashboard design: <business, date>
Skill: 17-dashboard · Date: <YYYY-MM-DD> · Framework: North Star Metric and KPI tree / driver tree dashboard
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing built
## North star
## Driver tree
## Metric definitions
| Metric | Definition | Source of truth | Refresh | Owner | Current (label) |
| --- | --- | --- | --- | --- | --- |
## What is left off and why
## Layout
## Review rhythm and decisions
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/17-measurement/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the north star, the driver tree, the metrics kept and cut, and the review rhythm, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] One north star tied to customer value and revenue, defined.
- [ ] The driver tree links each input metric upward with a formula.
- [ ] Each metric has a definition, source of truth, refresh, owner and known issues.
- [ ] Vanity metrics are cut from the main view with the reason; the main view stays under a dozen numbers.
- [ ] Each metric serves a named decision; targets are the owner's; nothing is built without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Put one north star that reflects customer value at the top, show only the inputs the team can move, define every number and its source, and cut what no decision uses. North Star Metric, KPI tree / driver tree and Dashboards, The Complete Marketing System, section 17 Measurement (Servidad, 2026); Sean Ellis and Amplitude's North Star framework.
