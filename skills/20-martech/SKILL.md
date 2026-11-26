---
name: 20-martech
description: Map marketing tools, costs, owners and fix broken data flows. Use for martech stack, tool audit, tool consolidation, which app to keep, duplicate apps, broken data flows, do we need a CRM, RevOps.
metadata:
  section: "20 Operations"
  covers: "CRM; Marketing automation; Martech stack; RevOps"
---
# Martech stack

A martech map shows every marketing tool, the job it does, the data it sends and receives, who owns it and what it costs, so overlaps, gaps and broken hand-offs become visible. It works when it is built from what is actually installed and paid for, data flows are traced end to end (for example a cancellation reaching the email tool), each tool has one owner, and changes are justified by a job the business needs. It fails when tools are bought for features nobody uses, two tools do one job, nobody owns the connections, or a new CRM is chosen before the process it should support is clear.

Save the stack map as a Markdown file in `work/20-operations/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Tool lists, costs, owners and integration notes in `inputs/` are the evidence.
- If present, also read Tool lists, costs, statements, integration and data-flow notes in `inputs/`; any work in `work/17-measurement/17-tracking-plan-*.md` or `work/15-retention/`.
- **No data:** Without a tool list in `inputs/`, ask for every tool with its cost, owner and what it connects to, explicitly say how to provide it (drop tool lists, statements or integration notes in `inputs/` or paste into chat), and **give only the blank stack-map template** (do not analyze unrelated tickets or speculate about tool gaps yet). Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/martech-guide.md](references/martech-guide.md) for the stack map, data-flow tracing, CRM and marketing automation choices, RevOps and consolidation.

1. **Inventory.** Every tool from `inputs/` with its job, monthly cost, owner and status (used, unused); sum cost with [scripts/sum_by.py](scripts/sum_by.py).
2. **Data flows.** Trace the flows that matter (sign-up, purchase, cancellation, consent, attribution) across tools; mark breaks.
3. **Overlaps and gaps.** Tools doing the same job; jobs no tool does; owners missing.
4. **CRM and marketing automation.** Whether the business needs a CRM or more automation, from the process it must support; a choice of vendor waits until requirements are clear. Vendor features and prices are facts to cite with URL and date or mark *to confirm*.
5. **RevOps.** Who owns the data and connections across marketing, sales and support; one owner per flow.
6. **Changes.** Remove, fix, add, each with the job, cost, risk (data loss, consent) and owner; reversible steps first.
7. **Approval.** The map is a draft. Cancelling, buying or reconfiguring tools needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no tools, costs, features or data flows that aren't in `inputs/` or cited with a date. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/20-operations/20-martech-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Martech stack map: <business, date>
Skill: 20-martech · Date: <YYYY-MM-DD> · Framework: Martech stack map; CRM and Marketing automation needs; RevOps ownership
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; no tool changed
## Inventory
| Tool | Job | Cost a month | Owner | Status |
| --- | --- | --- | --- | --- |
## Data flows and breaks
## Overlaps and gaps
## CRM and automation needs
## Ownership (RevOps)
## Changes
## Facts to confirm
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/20-operations/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, total cost, overlaps and unused tools, the broken data flows that matter, and the first changes, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every tool has its job, cost, owner and status from `inputs/`; total cost is computed.
- [ ] Key data flows are traced and breaks named.
- [ ] Overlaps, gaps and missing owners are listed.
- [ ] CRM or automation needs come from the process; vendor facts are dated or *to confirm*.
- [ ] Changes name job, cost, risk and owner; nothing changes without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Map what you actually have, trace the data that matters end to end, give every tool and connection an owner, and buy only for a job you can name. Martech stack, CRM, Marketing automation and RevOps, The Complete Marketing System, section 20 Operations (Servidad, 2026).
