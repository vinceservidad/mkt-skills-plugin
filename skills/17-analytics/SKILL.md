---
name: 17-analytics
description: Answer a business question from funnel and cohort data with the right denominator, window and caveats. Use for funnel analysis, cohort retention, conversion drop-off, why sales fell.
metadata:
  section: "17 Measurement"
  covers: "Cohort analysis; Funnel analytics"
---
# Analytics

Analysis answers one business question with data, and says how sure the answer is. It works when the question is stated first, the source and its limits are named, every rate has its denominator and window, segments are compared on equal terms, and the answer separates what the data shows from what it suggests. It fails when the analysis is a tour of every chart, rates are compared across different windows, small samples are treated as patterns, or correlation is reported as cause. Building warehouses and pipelines belongs to analytics engineering, not this skill.

Save the analysis as a Markdown file in `work/17-measurement/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. The data in `inputs/` is the evidence; context says which segments and outcomes matter.
- If present, also read `context/customer.md` → Segments, ICP and personas; `context/offer.md` → Price and model; `context/awareness.md` → Journey; exports (funnels, cohorts, orders, sessions, surveys) and how they were pulled in `inputs/`; any work in `work/17-measurement/17-tracking-plan-*.md`.
- **No data:** Without data, restate the question, list the exact exports needed (fields, period, grain), and say what each would show. Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/analytics-guide.md](references/analytics-guide.md) for funnel and cohort methods, denominators and windows, segment comparisons, sample-size caution and causal language.

1. **The question.** State the business question and the decision it feeds in one or two sentences.
2. **The data.** Name each source, its grain, period, and known limits (sampling, tracking defects, self-report). If sources disagree, say which is the system of record.
3. **Funnel analytics.** Compute step-to-step conversion with counts and denominators, by segment (device, source, new or returning) with [scripts/sum_by.py](scripts/sum_by.py). Name the largest drop in absolute and relative terms.
4. **Cohort analysis.** Retention by start cohort on the same window (box, week or month since start), with counts; compare only cohorts with the same exposure time.
5. **Answer.** What the data shows (observed), what it suggests (inference, labelled), and what it can't show. Small counts are flagged; no causal claim without a test.
6. **Next step.** The decision it supports, and the test or data that would make it surer (`18-ab-testing`, `17-incrementality`, `17-tracking-plan`).
7. **Approval.** The analysis is a draft. Acting on it in live accounts or pages needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no figures that aren't computed from `inputs/`, and no causes stated as facts without a test. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/17-measurement/17-analytics-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Analysis: <question>
Skill: 17-analytics · Date: <YYYY-MM-DD> · Framework: Funnel analytics and cohort analysis
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's review; nothing changed in any account
## The question and the decision
## Data and limits
## Funnel
| Step | Segment | Count | Conversion from previous | Label |
| --- | --- | --- | --- | --- |
## Cohorts
| Cohort | Started | Retained at step | Rate | Exposure |
| --- | --- | --- | --- | --- |
## Answer: observed, inferred, unknown
## Next step
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/17-measurement/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the answer to the question in one or two sentences, the key numbers with denominators, and how sure it is, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The question and decision are stated first.
- [ ] Sources, grain, period and limits are named; disagreements between sources are explained.
- [ ] Every rate has a count, denominator and window, computed with `sum_by.py`; segments are compared on equal terms.
- [ ] Cohorts are compared only at equal exposure.
- [ ] Observed, inferred and unknown are separated; no causal claim without a test.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Answer one question, show every rate with its denominator and window, compare like with like, and keep what the data shows apart from what you think it means. Funnel analytics and Cohort analysis, The Complete Marketing System, section 17 Measurement (Servidad, 2026); Lean Analytics (Alistair Croll and Benjamin Yoskovitz).
