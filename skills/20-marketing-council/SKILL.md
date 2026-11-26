---
name: 20-marketing-council
description: Council critique of email, page, offer, campaign, plan as customer, copywriter, lawyer. Use whenever asked to critique (even before pasted), red team, pressure test, second opinion, or say good to go.
metadata:
  section: "20 Operations"
  covers: "Marketing council (multi-perspective review)"
---
# Marketing council

A marketing council reviews a plan or asset from several expert viewpoints (customer, copy, offer, brand, compliance, data, operations) before it ships, then merges what they find into one verdict and a short fix list. It works when each viewpoint checks against the business's own context and evidence, disagreements are kept visible, and the verdict says what must change before launch versus what is optional. It fails when every viewpoint says the same polite thing, opinions replace evidence, or the review becomes a rewrite nobody asked for.

Save the council review as a Markdown file in `work/20-operations/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. The asset or plan under review, plus context, are the evidence.
- If present, also read All of `context/`; the asset, plan, data and notes in `inputs/`; any related work in `work/`.
- **No data:** Without the asset or plan, ask for it and its goal, explicitly say how to provide it (drop it in `inputs/` or paste into chat), and give only the plain list of review viewpoints (do not run checks against `context/` files or cite business, segment or offer specifics yet). Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/council-guide.md](references/council-guide.md) for the viewpoints, what each checks, merging findings and the verdict scale.

1. **Goal and audience.** What the asset or plan must achieve and for whom, from `inputs/` or context.
2. **Viewpoints.** Choose the ones that matter (customer, copy and message, offer and price, brand voice, compliance, data and measurement, operations and capacity). Each checks against context and evidence and gives findings with the evidence line. Check every promise or operational friction in the asset (such as cancellation, shipping, pricing or guarantees) against both current operations notes and the core offer or brand promises in context/offer.md and context/message.md, flagging any contradiction where current friction breaks a promise even if factually true today.
3. **Disagreements.** Where viewpoints conflict, show both and the trade-off; don't average them away.
4. **Merge.** One verdict (ship, ship with fixes, rework, stop), must-fix items before launch, optional improvements, and the owning skill for each fix. Never rubber-stamp a rushed draft: even under time pressure, give the shortest must-fix list with evidence and a fast fix for each, and leave sending to the owner.
5. **Approval.** The review is a draft. Shipping or changing the asset needs the owner's explicit approval.
6. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no facts, results, rules or customer reactions that aren't in `context/` or `inputs/`. Opinions are labelled. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/20-operations/20-marketing-council-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Council review: <asset or plan, date>
Skill: 20-marketing-council · Date: <YYYY-MM-DD> · Framework: Marketing council (multi-perspective review)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval
## Goal and audience
## Findings by viewpoint
| Viewpoint | Finding | Evidence | Severity |
| --- | --- | --- | --- |
## Disagreements
## Verdict
## Must fix before launch
## Optional
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/20-operations/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the verdict, the must-fix items with their evidence, and any disagreement worth the owner's decision, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Each viewpoint checks against context or evidence, with the evidence line.
- [ ] Disagreements are shown with the trade-off.
- [ ] The verdict separates must-fix from optional, with an owning skill per fix.
- [ ] Opinions are labelled; nothing ships without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Look at the work through the eyes of the customer, the brand, the numbers, the rules and the people who must deliver it, keep disagreements visible, and end with one clear verdict. Marketing council (multi-perspective review), The Complete Marketing System, section 20 Operations (Servidad, 2026).
