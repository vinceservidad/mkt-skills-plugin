---
name: 18-experiment-log
description: Keep a searchable experiment log of wins, losses and nulls and run the weekly growth meeting process. Use for logging tests, recording results, what we learned from past tests, test repository.
metadata:
  section: "18 Experimentation"
  covers: "Growth process (Hacking Growth); Learning log / experiment repository"
---
# Experiment log

A learning log turns single tests into knowledge the team keeps. It works when every test is recorded with its hypothesis, design, dates, sample, result with uncertainty, validity notes, the insight, and the next step, including nulls and failures; when entries are searchable by page, audience and theme; and when it feeds the weekly growth process. It fails when only winners are written down, results are stored without the conditions they held under, a stopped-early test is recorded as a win, or one result becomes a rule for everything.

Save the learning log as a Markdown file in `work/18-experimentation/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Past and current test records in `inputs/` are the evidence.
- If present, also read `context/customer.md` → Segments; past test notes, tool exports, dashboards and meeting notes in `inputs/`; any work in `work/18-experimentation/`.
- **No data:** Without any test records in `inputs/`, you may save the empty log template and weekly growth process in `work/18-experimentation/18-experiment-log-<YYYY-MM-DD>-<slug>.md` (or provide them in the reply) with no invented entries, ask for any past tests the team remembers (labelled by how well they are documented) and how to provide them (drop test notes or exports in `inputs/` or paste into chat). End with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/experiment-log-guide.md](references/experiment-log-guide.md) for the entry template, validity checks, insight writing, tagging and the growth meeting rhythm.

1. **Gather what exists.** List every past test from `inputs/` with what is documented; mark missing fields *unknown*.
2. **Validity first.** For each: was the sample planned, did it run to its end, were there other changes, is the metric the system of record? Rate validity (valid, weak, invalid) before recording direction.
3. **Entry.** Hypothesis, change, audience, dates, sample per arm, metric, result with interval or counts, validity, insight (what we learned about customers, separate from the mechanism we guess), and next step. Nulls and losses are recorded the same way.
4. **Scope.** Each insight states the conditions it held under (season, traffic source, offer); no universal rules from one test.
5. **Tags and search.** Page, audience, theme (for example trust, price, delivery), so future ideas check the log first.
6. **Growth process.** A weekly rhythm (Hacking Growth): review results, update the log, pick the next tests from the backlog (`18-hypothesis`), and assign owners.
7. **Approval.** The log is a draft. Changing shared documents or team processes needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, samples, dates or insights that aren't in `inputs/`. Unknown fields stay *unknown*. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/18-experimentation/18-experiment-log-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Experiment log: <business>
Skill: 18-experiment-log · Date: <YYYY-MM-DD> · Framework: Learning log / experiment repository; Growth process (Hacking Growth)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval
## Entries
| ID | Hypothesis | Change | Dates | Sample per arm | Result | Validity | Insight | Next step | Tags |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
## Validity notes
## What we have learned (scoped)
## Weekly growth process
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/18-experimentation/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the entries recorded with their validity, what is actually learned, and the weekly rhythm, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every past test is recorded with documented fields and *unknown* for the rest.
- [ ] Validity is rated before direction; early-stopped or underpowered tests are not recorded as wins.
- [ ] Nulls and losses are recorded; insights are separated from guessed mechanisms and scoped to conditions.
- [ ] Entries are tagged for search; a weekly growth process feeds the backlog.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Record every test, judge its validity before its direction, keep losses and nulls, scope each insight to the conditions it held under, and check the log before the next idea. Learning log / experiment repository and the Growth process from Hacking Growth (Sean Ellis and Morgan Brown); The Complete Marketing System, section 18 Experimentation (Servidad, 2026).
