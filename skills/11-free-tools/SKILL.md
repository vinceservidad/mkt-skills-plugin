---
name: 11-free-tools
description: Build free tools that attract buyers and lead to the core offer (engineering as marketing). Use for free calculators, templates, generators, graders, interactive tools, side projects as marketing.
metadata:
  section: "11 Distribution"
  covers: "Free tools (engineering as marketing)"
---
# Free tools

A free tool does a small piece of the buyer's job for free: a calculator, a template, a grader, a generator. Engineering as marketing works when the tool answers a question the buyer already asks, its result points naturally to the paid offer, people can find it (search, partners, sales), and it is judged on qualified leads and clients. It fails when it is built because it is fun, the result has no next step, it collects sensitive data without care, or the build cost is never weighed against what the existing free resources already show.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **Jobs to be done**, from `02-jobs-to-be-done`: the job the tool does a piece of.
- If present, also read `context/customer.md` → ICP and personas, Pains, desires and fears, Voice of customer; `context/offer.md` → Core offer, Price and model, Urgency and scarcity (capacity), Value ladder; `context/message.md` → Mechanism, Promise; existing lead magnets, download counts, lead sources, build quotes and data notes in `inputs/`; any work in `work/12-funnel/12-lead-magnet-*.md`, `work/11-distribution/11-seo-*.md` or `11-programmatic-seo-*.md`.
- If the required section is missing:
  - **The upstream evidence exists** (interviews, tickets, reviews in `inputs/`): run `02-jobs-to-be-done` first, then continue.
  - **It doesn't:** stop. Name the missing section with the skill that fills it (Jobs to be done → `02-jobs-to-be-done`) and ask for evidence. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Build spend, a developer, hosting and anything the tool promises are the owner's commitments. The plan gives options with costs; the owner decides.
- If `02-jobs-to-be-done` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/free-tools-guide.md](references/free-tools-guide.md) for tool types, the fit test, data handling, the build decision and measurement.

1. **Outcome.** Name what the tool must produce (qualified leads, booked calls, clients) and the count that would justify the build.
2. **What exists already.** Count downloads, leads and clients from existing free resources with [scripts/tally.py](scripts/tally.py) or the notes. If people download a resource but are never followed up, fixing that follow-up may beat building something new; say so.
3. **Job fit.** Pick the piece of a job the buyer already asks about (in their words from Voice of customer and Jobs), that has a clear answer the tool can give, and that leads to the offer. Ideas that don't touch the core job are dropped with the reason.
4. **The tool.** Inputs, the output the user sees, and the call to action on the result screen framed around what the paid offer does beyond the tool's snapshot (never a generic call push or an inflated/scary score to frighten buyers into booking, which misleads buyers, damages trust and may break consumer-protection rules — refuse any request to rig the result).
5. **Data.** Ask only for what the result needs. Financial, health or personal figures are sensitive: decide whether anything is stored, where, for how long and who sees it; say it plainly next to the form; prefer calculating in the browser without storing. Privacy rules are facts to verify or mark *to confirm*. Email capture is optional and its consent wording is the owner's.
6. **Build decision.** Compare the cheapest test (a spreadsheet or a no-code version of the tool) with the full build (a quote, hosting, upkeep), with costs and the leads or clients needed to justify each from price, margin and tenure, shown as arithmetic and labelled, and check against capacity. Recommend testing demand before paying for the full build.
7. **Distribution.** How people will find it: search terms it answers (`11-seo`), partners and communities (`11-co-marketing`), sales follow-up, the newsletter. A tool nobody can find does nothing.
8. **Measure.** Uses, completions, leads, qualified leads and clients from the tool, with counts and dates, recorded by a source field or unique link.
9. **Approval.** The plan is a draft. Hiring a developer, publishing the tool or collecting any data needs the owner's explicit approval.
10. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no usage, results, features or costs that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. No benchmark conversion rate is evidence.

## Output

Write `work/11-distribution/11-free-tools-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Free tool plan: <business, date>
Skill: 11-free-tools · Date: <YYYY-MM-DD> · Framework: Free tools (engineering as marketing)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing built, published or collected
## Outcome and the threshold
## What exists already
| Resource | Downloads or uses | Leads | Clients | Followed up? |
| --- | --- | --- | --- | --- |
## Job fit
## The tool
## Data handling
## Build decision
| Option | Cost | Time | What it proves | Needed to justify (calculated) |
| --- | --- | --- | --- | --- |
## Distribution
## How we judge it
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Titles of books, essays or talks, including in the Principle, framework, source block, go in italics, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`) and fix every line it prints until it reports every quotation matches.

Reply with the file path, the recommended tool and why, the build decision with its cost, the data rule, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Existing free resources are counted, and unfollowed-up downloads are flagged before any new build.
- [ ] The tool does a piece of a job the buyer asks about; the result is honest (never rigged or scary) and its result-screen CTA states what the paid offer does beyond the tool.
- [ ] Data asked is the minimum; sensitive data storage is decided and stated; privacy facts are dated or *to confirm*.
- [ ] A cheap demand test is compared with the full build, with costs and thresholds calculated.
- [ ] Distribution is planned; success is leads and clients with counts.
- [ ] The plan says nothing is built, published or collected without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Give away a small, honest piece of the buyer's job that leads to the offer, test demand before paying for the build, ask for as little data as the answer needs, and judge the tool on clients. Free tools (engineering as marketing), The Complete Marketing System, section 11 Distribution (Servidad, 2026); Traction (Gabriel Weinberg and Justin Mares), engineering as marketing.
