---
name: 14-lead-scoring
description: Score and qualify leads on fit and intent (BANT) and route them to sales or nurture. Use for lead scoring, MQL and SQL rules, which leads to call first, lead qualification, routing leads.
metadata:
  section: "14 Sales"
  covers: "BANT; Lead scoring"
---
# Lead scoring

Lead scoring decides which leads get a person's time first. It works when fit (is this account the ICP?) and intent (are they acting like a buyer now?) are scored separately from evidence, the weights come from which leads actually became clients, disqualifiers override points, and each band has a clear next step. It fails when points are invented, every download counts as intent, a high score can't override a misfit, or the model is never checked against outcomes. BANT is a quick qualification check, not the whole model.

Save the scoring model as a Markdown file in `work/14-sales/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: the fit criteria and the disqualifiers.
- If present, also read `context/customer.md` → Segments, Buying triggers and process; `context/offer.md` → Price and model, Urgency and scarcity (capacity); lead exports with outcomes, CRM fields, page and download data, and the current routing in `inputs/`; any work in `work/14-sales/14-discovery-spin-*.md` or `work/17-measurement/17-tracking-plan-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (closed-deal records, interviews or sales notes in `inputs/`): run `02-icp-persona` first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (ICP and personas → `02-icp-persona`), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/lead-scoring-guide.md](references/lead-scoring-guide.md) for fit and intent signals, weighting from outcomes, BANT, bands and routing.

1. **Read the leads.** Count leads, outcomes and conversion by field (source, size, role, location, pages viewed, downloads) from `inputs/` with [scripts/sum_by.py](scripts/sum_by.py) or [scripts/tally.py](scripts/tally.py). Say how many outcomes there are; with few closed leads, weights are *(assumption)* until more data arrives.
2. **Fit score.** Points from ICP traits (size band, type, location, revenue band, deciding role). Disqualifiers (from the ICP — including wanting an excluded service such as strategic CFO advice rather than bookkeeping) **must override all fit and intent points immediately** when scoring leads in `inputs/`, banding those leads as *Not a fit* (never *Sales now*).
3. **Intent score.** Points from behaviour that the data links to buying (booked a call, viewed pricing, asked about price in a DM, a referral) and less for weaker signals (a single download). Never treat every download as a buyer. **Do not use email opens as an intent signal** (even if the user asks to score opens): explain that automated email privacy features and security bots make open counts unreliable (mark vendor-specific mechanics *to confirm* rather than stating them as current fact), check whether `inputs/` even shows leads being emailed, and replace opens with real buying-intent behaviours from the data.
4. **BANT check.** Budget (fits a price band), Authority (decides or reaches who does), Need (named pain), Timing. Use it at the first conversation, recorded as heard or unknown.
5. **Bands and routing.** For each band (for example sales now, nurture, not a fit): who acts, how fast, and with what. Fit it to the time sales has.
6. **Score the current leads.** Apply the model to the leads in `inputs/` as a worked example, showing each score.
7. **Check against outcomes.** How often the model will be checked (won and lost by band), and what changes it. A model nobody checks drifts.
8. **Approval.** The model is a draft. Changing CRM fields, automations or routing needs the owner's explicit approval.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no conversion rates, weights presented as proven, leads or outcomes that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/14-sales/14-lead-scoring-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Lead scoring model: <business, date>
Skill: 14-lead-scoring · Date: <YYYY-MM-DD> · Framework: Lead scoring (fit and intent) with BANT
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; no CRM or routing changed
## What the lead data shows
## Fit score
| Trait | Points | Evidence |
| --- | --- | --- |
## Disqualifiers
## Intent score
| Signal | Points | Evidence |
| --- | --- | --- |
## BANT at first contact
## Bands and routing
## Current leads scored
| Lead | Fit | Intent | Band | Next step |
| --- | --- | --- | --- | --- |
## How the model is checked
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/14-sales/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the fit and intent rules, the disqualifiers, the bands with next steps, and the current leads scored, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Lead outcomes are counted from the data; weights with few outcomes are labelled assumptions.
- [ ] Fit and intent are scored separately; disqualifiers override points.
- [ ] Intent weights favour signals linked to buying; single downloads are weak.
- [ ] Each band has an owner, a speed and a next step that fit sales time; the current leads are scored as a worked example.
- [ ] The model has a check against outcomes; nothing changes in the CRM without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Score fit and intent separately from your own outcomes, let disqualifiers override points, and give each band a next step sales can keep. Lead scoring and BANT (IBM), The Complete Marketing System, section 14 Sales (Servidad, 2026).
