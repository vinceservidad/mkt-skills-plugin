---
name: 20-campaign-review
description: Run a blameless post-mortem on a campaign and the weekly growth meeting. Use for post-mortem, campaign review, what went wrong, lessons learned, weekly marketing meeting.
metadata:
  section: "20 Operations"
  covers: "Post-mortem / campaign review; Weekly growth meeting"
---
# Campaign review

A campaign review compares what was planned with what happened, finds why, and decides what to keep, change or stop, so the next campaign is better. It works when the goal and result are stated with numbers from the source of truth, the timeline shows where things slipped, causes are separated from guesses, it is blameless (process, not people), and each lesson becomes an owned action or a change to an SOP. A weekly growth meeting keeps this rhythm going. It fails when it lists feelings, blames people, judges on platform metrics alone, or produces lessons nobody acts on.

Save the campaign review as a Markdown file in `work/20-operations/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Plans, results, timelines and notes in `inputs/` are the evidence.
- If present, also read Campaign plans, results, timelines, spend and notes in `inputs/`; any work in `work/18-experimentation/18-experiment-log-*.md`, `work/20-operations/20-sops-*.md` or `work/20-operations/20-marketing-plan-*.md`.
- **No data:** Without the plan or results, ask for the goal, dates, what was done and the results from the source of truth, explicitly say how to provide them (drop plans or result exports in `inputs/` or paste into chat), and give only the blank review template (do not analyze unrelated inputs or speculate about leads/causes before campaign data arrives). Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/campaign-review-guide.md](references/campaign-review-guide.md) for the post-mortem structure, timeline, cause analysis, blameless language and the weekly growth meeting agenda.

1. **Goal versus result.** The goal as set, the result from the source of truth, the gap; computed with [scripts/sum_by.py](scripts/sum_by.py) where needed.
2. **Timeline.** Planned versus actual dates for each step; where it slipped.
3. **What happened and why.** Observed facts first, then only causal links explicitly stated in `inputs/` (e.g. page live before stock causing refunds, or unready photos causing email delay) — never label inferred process gaps (such as no checklist or no gating) as proven unless `inputs/` explicitly states them — then every inferred gap or unproven explanation (such as missing checks, promo volume, paid spend, season or product mix) as a labelled guess `(assumption)`; process, not people.
4. **Keep, change, stop.** Each with the evidence and an owner.
5. **Actions.** Each lesson becomes an action with owner and date, an SOP change (`20-sops`) or a test (`18-hypothesis`); learning goes to `18-experiment-log` where it was a test.
6. **Weekly growth meeting.** A short agenda: numbers against plan, last week's actions, what shipped and what it did, blockers, next week's priorities.
7. **Approval.** The review is a draft. Changing processes, budgets or plans needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, dates, causes or numbers that aren't in `inputs/` or computed from them. Guesses are labelled. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/20-operations/20-campaign-review-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Campaign review: <campaign, dates>
Skill: 20-campaign-review · Date: <YYYY-MM-DD> · Framework: Post-mortem / campaign review (blameless); Weekly growth meeting
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval
## Goal versus result
## Timeline
| Step | Planned | Actual | Slip |
| --- | --- | --- | --- |
## What happened and why
## Keep, change, stop
## Actions
| Action | Owner | Due | Type (action, SOP change, test) |
| --- | --- | --- | --- |
## Weekly growth meeting agenda
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/20-operations/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the gap between goal and result, the main causes with evidence, and the actions with owners, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Goal and result are stated with numbers from the source of truth.
- [ ] The timeline shows planned versus actual; slips are located.
- [ ] Causes are separated from labelled guesses; language is blameless.
- [ ] Every lesson becomes an owned action, SOP change or test.
- [ ] A weekly growth meeting agenda is included; nothing changes without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Compare plan with result in numbers, find where and why it slipped without blaming people, and turn every lesson into an owned action. Post-mortem / campaign review (blameless) and the Weekly growth meeting, The Complete Marketing System, section 20 Operations (Servidad, 2026); Hacking Growth (Sean Ellis and Morgan Brown).
