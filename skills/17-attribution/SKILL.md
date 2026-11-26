---
name: 17-attribution
description: Choose and caveat a marketing attribution view (last click, MMM, store vs ad-platform totals). Use for attribution, ROAS disagreements, summing Meta/Google purchases, MMM. Not for team credit.
metadata:
  section: "17 Measurement"
  covers: "Attribution; Marketing Mix Modeling"
---
# Attribution

Attribution splits credit for sales across the channels that touched the buyer. Every model is a view, not the truth: last click under-credits channels that start demand, platform reports over-credit themselves, and self-reported surveys miss what people forget. Attribution works when the business compares several views against the system of record, picks one primary view for decisions with its caveats, and tests the big questions with incrementality. It fails when one platform's ROAS is taken as fact, credit adds up to more sales than exist, or a model is chosen because a tool defaults to it. Marketing Mix Modeling needs enough history and spend variation to be useful.

Save the attribution read as a Markdown file in `work/17-measurement/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Platform reports, the system of record, UTMs and survey answers in `inputs/` are the evidence.
- If present, also read `context/offer.md` → Price and model; `context/awareness.md` → Journey; spend and platform reports, store or CRM orders by source, survey answers and tracking notes in `inputs/`; any work in `work/17-measurement/17-tracking-plan-*.md` or `17-incrementality-*.md`.
- **No data:** Without channel and sales data, explain the attribution views available and their biases, ask for spend, platform-reported conversions, source-system orders by UTM/source and survey answers for the same period, and explicitly state **how to provide them** (save exports in `inputs/` or paste into chat). **Do NOT recommend a specific starting attribution model** before data arrives. Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/attribution-guide.md](references/attribution-guide.md) for attribution views, their biases, reconciliation, MMM requirements and decision rules.

1. **Check collection first.** If the tracking plan or reconciliation shows a defect (platform conversions above total orders), say so and read attribution only after correcting or excluding it.
2. **Lay out the views.** For each channel and the same period: spend, platform-reported conversions and revenue, source-system orders by UTM (last click), and self-reported source, computed with [scripts/sum_by.py](scripts/sum_by.py). Show the total each view claims against total orders.
3. **Explain the gaps.** Windows and view-through, cross-device, untagged links (direct and none), and self-report bias. Label each explanation observed or inferred.
4. **Choose the decision view.** A primary view for routine decisions (often source-system last click plus survey) with its known bias stated, and a rule for when to use a test instead.
5. **Marketing Mix Modeling.** Say whether MMM fits: statistical MMM requires many weekly periods across channels with real spend variation and few confounders. Judge directly against the data in `inputs/` (e.g. one quarter / 3 monthly points is far too short and thin to separate channels reliably, marked *(assumption)* unless citing a verified official doc with URL and access date). Never cite a bare tool guide or print unverified numeric year thresholds as fact. If it doesn't fit, say what history and variation would make it possible.
6. **What to test.** The decisions that need incrementality (`17-incrementality`), such as doubling a channel or cutting one with no last-click sales.
7. **Approval.** The read is a draft. Budget or bid changes based on it need the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no conversions, revenue, ROAS or shares that aren't computed from `inputs/`; no channel is called incremental without a test. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/17-measurement/17-attribution-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Attribution read: <business, period>
Skill: 17-attribution · Date: <YYYY-MM-DD> · Framework: Attribution (multiple views reconciled to the system of record); Marketing Mix Modeling fit
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's review; no budget changed
## Collection check
## Views by channel
| Channel | Spend | Platform conversions | Store last click | Self-reported | Label |
| --- | --- | --- | --- | --- | --- |
## Why the views differ
## Decision view and its bias
## Marketing Mix Modeling: fit or not
## What needs a test
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/17-measurement/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the views side by side, why they differ, the decision view, and which questions need a test, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Collection defects are flagged before attribution is read.
- [ ] Every view is computed for the same period and compared with total orders; no view's credit is taken as truth.
- [ ] Gaps are explained and labelled observed or inferred.
- [ ] A decision view is chosen with its bias stated; MMM fit is judged on data length and variation.
- [ ] Big budget questions are routed to incrementality; nothing changes without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Every attribution model is a view with a bias: fix collection first, compare views against the orders you actually have, decide with a stated view, and test the big bets. Attribution and Marketing Mix Modeling, The Complete Marketing System, section 17 Measurement (Servidad, 2026).
