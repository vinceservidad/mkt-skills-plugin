---
name: 17-incrementality
description: Design holdout and geo-lift tests that measure what marketing spend really adds. Use for incrementality, geo tests, holdout tests, conversion lift studies, does this channel actually work.
metadata:
  section: "17 Measurement"
  covers: "Incrementality / geo-lift"
---
# Incrementality

Incrementality asks what would have happened without the spend. A holdout or geo-lift test answers it by comparing a group or region that sees the marketing with one that doesn't. It works when the question is one decision, the groups are comparable and fixed before launch, the outcome is measured in the system of record, the test runs long enough to see an effect of the size that matters, and the read is honest about uncertainty. It fails when regions are picked after the fact, the test is stopped the day it looks good, platform conversions are the outcome, or one test is treated as a law for every season.

Save the test design as a Markdown file in `work/17-measurement/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Spend, outcome data by region or group, and the decision in `inputs/` are the evidence.
- If present, also read `context/offer.md` → Price and model; spend, sales by region and week, platform reports, tracking notes and the decision in `inputs/`; any work in `work/17-measurement/17-attribution-*.md`, `17-unit-economics-*.md` or `work/18-experimentation/`.
- **When `inputs/` contains spend and monthly store/subscriber totals or margin/retention notes** (even without a regional breakdown CSV yet), **write the complete draft test design file** to `work/17-measurement/17-incrementality-<YYYY-MM-DD>-<slug>.md` — never stop with just a reply outline. Compute unit-economics contribution margin and break-even incremental CAC from `inputs/`, size the test duration from baseline monthly volume with explicit assumptions, specify matched US regions fixed before launch (noting pre-launch baseline export needed to balance them), and write the read rule and guardrails in advance.
- **No data:** Only when `inputs/` has no spend or store/outcome figures at all, design the test in outline, list the data needed to size it (spend by channel, new customers by region and week), give no expected lift, and explicitly state **how to provide it** (drop exports in `inputs/` or paste into chat). Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/incrementality-guide.md](references/incrementality-guide.md) for holdout and geo-lift designs, choosing regions, sizing, duration, reading results and platform lift studies, and [references/measurement-trifecta-and-meridian.md](references/measurement-trifecta-and-meridian.md) when connecting incrementality tests with attribution and Bayesian Marketing Mix Modeling (such as Google Meridian calibrated with lift priors).

1. **One decision.** State the decision the test informs (double, hold or cut a channel) and the effect size that would change it, from the business's own unit economics.
2. **Design.** Choose the method: a user holdout (where the platform supports it), a geo-lift test (regions on and off), or a time-based on/off with controls. Fix the groups before launch, matched on past sales; the platform's own lift studies are facts to cite with URL and date or mark *to confirm*.
3. **Outcome.** Measure in the system of record (new customers, orders, revenue by region from the store or CRM), not platform conversions. Fix collection defects first (`17-tracking-plan`).
4. **Size and duration.** From baseline volume and variability by region, estimate whether the test can detect the effect that matters in the planned weeks, with the arithmetic or the assumptions shown; if it can't, say so and change the design.
5. **Guardrails.** Spend cap, stop rules for harm, no other big changes in test regions during the test, and a pre-written read rule.
6. **Read.** Lift = test minus control (scaled), with uncertainty; incremental CAC = test spend ÷ incremental customers. Scope the learning to the season, offer and channel tested.
7. **Approval.** The design is a draft. Changing campaign targeting or budgets for the test needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no lift, incremental CAC or results that aren't measured; no expected lift is stated as fact. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/17-measurement/17-incrementality-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Incrementality test: <channel, period>
Skill: 17-incrementality · Date: <YYYY-MM-DD> · Framework: Incrementality / geo-lift (holdout test)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; no campaign changed
## The decision and the effect that matters
## Design
## Groups or regions
| Group | Regions | Past baseline (source) | Treatment |
| --- | --- | --- | --- |
## Outcome and data
## Size and duration
## Guardrails and read rule
## How to read the result
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

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/17-measurement/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the decision, the design and regions, the outcome measure, duration, and the read rule, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] One decision and the effect size that matters are stated from the business's own economics.
- [ ] Groups are fixed before launch and matched on past data; outcomes come from the system of record.
- [ ] Duration and power are estimated with assumptions shown, or the limit is stated.
- [ ] Guardrails and the read rule are written before launch; platform facts are dated or *to confirm*.
- [ ] The learning is scoped to the conditions tested; nothing changes without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Measure what the spend adds by comparing like with like that didn't see it, decide the read before you start, use your own sales as the outcome, and keep the learning to the conditions you tested. Incrementality / geo-lift, The Complete Marketing System, section 17 Measurement (Servidad, 2026); Meta and Google lift-study documentation and open-source geo-lift methods (to be cited with dates).
