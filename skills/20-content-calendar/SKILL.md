---
name: 20-content-calendar
description: Plan a marketing content calendar, what ships when and who owns it, for seasonal campaigns. Use for content or editorial calendar, posting schedule, holiday campaigns. Not for personal events.
metadata:
  section: "20 Operations"
  covers: "Content calendar; Seasonal campaigns"
---
# Content calendar

A content calendar sets what ships when, on which channel, for which goal, and who owns it. It works when it is built backwards from the dates that matter (launches, seasonal campaigns, holidays), each item has a job tied to the journey and the plan, production lead times are included, and the volume fits the hours the team actually has. It fails when it is a grid of daily posts nobody can make, seasonal dates are remembered a week before, items have no owner or goal, or it ignores what the audience responds to.

Save the content calendar as a Markdown file in `work/20-operations/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Dates, capacity, past content results and plans in `inputs/` and context are the evidence.
- If present, also read `context/awareness.md` → Journey; `context/brand.md` → Voice; plans, dates, capacity and past content results in `inputs/`; any work in `work/20-operations/20-marketing-plan-*.md`, `work/11-distribution/11-content-strategy-*.md` or `work/20-operations/20-sops-*.md`.
- **No data:** Without dates or capacity, ask for key dates, who makes content and how many hours they have, explicitly say how to provide them (drop dates or capacity notes in `inputs/` or paste into chat), and give the calendar template only. Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/content-calendar-guide.md](references/content-calendar-guide.md) for working back from dates, lead times, seasonal campaigns, capacity and the calendar format.

1. **Dates first.** Launches, seasonal campaigns and holidays in the period from `inputs/` and the plan; date facts (holiday dates) checked.
2. **Seasonal campaigns.** For each, the goal, offer (owner's), audience and channels, built backwards with production lead times; flag any claim, pricing or urgency compliance issues in proposed campaigns for `20-compliance`.
3. **Capacity.** Hours per person per week from `inputs/`; the calendar volume fits them, with buffer.
4. **Items.** Each with date, channel, format, the journey stage or job it serves, owner, status and due date for the draft.
5. **Recurring content.** The steady items (guides, emails, posts) at a rate the team can keep.
6. **Review.** Weekly check on what shipped and what it did; content results feed the next month.
7. **Approval.** The calendar is a draft. Publishing content or committing offers needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no dates, offers, results or capacity that aren't in `context/` or `inputs/` or checked. Offers are the owner's. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/20-operations/20-content-calendar-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Content calendar: <business, period>
Skill: 20-content-calendar · Date: <YYYY-MM-DD> · Framework: Content calendar with seasonal campaigns
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing published
## Key dates and seasonal campaigns
## Capacity
## Calendar
| Date | Channel | Item | Job or journey stage | Owner | Draft due | Status |
| --- | --- | --- | --- | --- | --- | --- |
## Recurring content
## Weekly review
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/20-operations/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the key dates and campaigns, how the volume fits the team's hours, and the first items due, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Key dates and seasonal campaigns come first, with lead times worked backwards.
- [ ] Volume fits the hours in `inputs/` with buffer.
- [ ] Every item has a channel, job or journey stage, owner and draft due date.
- [ ] Offers are the owner's; nothing is published without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Work back from the dates that matter, give every item a job and an owner, and plan only what the team can actually make. Content calendar and Seasonal campaigns, The Complete Marketing System, section 20 Operations (Servidad, 2026).
