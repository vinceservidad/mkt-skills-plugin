---
name: 14-prospecting
description: Build prospect lists, target account volume and an outbound cadence for the ICP. Use for prospecting, list building, how many accounts to prospect, finding leads, outbound cadence, pipeline building.
metadata:
  section: "14 Sales"
  covers: "Prospecting / list building"
---
# Prospecting

Prospecting fills the pipeline with accounts that fit before they raise their hand. It works when the list is built from the ICP's observable traits, each account has a reason to reach out now, the cadence mixes a few channels over a few weeks, and the effort is sized to what sales can actually take on. It fails when lists are bought or scraped by title, every account gets the same touch, volume outruns capacity, or meetings are counted instead of qualified pipeline. Cold email copy and deliverability belong to `11-cold-email`; scoring inbound leads belongs to `14-lead-scoring`.

Save the prospecting plan as a Markdown file in `work/14-sales/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: the traits that define a good account and the disqualifiers.
- If present, also read `context/customer.md` → Segments, Buying triggers and process, Pains, desires and fears; `context/offer.md` → Core offer, Urgency and scarcity (capacity); `context/message.md` → Promise, Proof stack; account lists, CRM exports, lead sources and win rates, capacity notes in `inputs/`; any work in `work/11-distribution/11-cold-email-*.md` or `work/14-sales/14-lead-scoring-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (interviews, sales notes or closed-deal records in `inputs/`): run `02-icp-persona` first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (ICP and personas → `02-icp-persona`), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/prospecting-guide.md](references/prospecting-guide.md) for list sources, account signals, the cadence, capacity sizing and what to measure.

1. **Where wins come from.** Count leads, wins and win rates by source from `inputs/` with [scripts/tally.py](scripts/tally.py). Prospecting adds to the sources that work; it does not replace a source that closes at a higher rate.
2. **Size from capacity.** Work backwards from what the business can take on (new clients a month) and its own win rates to the conversations and accounts needed, with the arithmetic shown and labelled *calculated*. No volume target from outside.
3. **List criteria.** Turn the ICP into observable filters (size, type, location, revenue band, role that decides) and disqualifiers. Name lawful, ethical sources (company sites, public directories, the owner's network, referrals, event lists used as agreed). Never suggest buying or scraping personal data, and never add real people's names or emails.
4. **Signals.** Dated public reasons to reach out (a hire, a move, a public question about the problem), recorded with source and date. No signal means no invented one.
5. **Cadence.** A few touches over a few weeks across channels the buyer uses (warm intro, email, LinkedIn, phone where appropriate), each adding something; stop at reply, no or opt-out. Copy and sending rules go to `11-cold-email`.
6. **Warm first.** Referrals and introductions before cold contact where the evidence shows they close better; ask existing clients and partners for introductions (`16-referral-program` owns the program).
7. **Track.** Accounts contacted, replies, meetings, qualified, proposals, clients, by source and tier, with counts.
8. **Approval.** The plan is a draft. Contacting anyone, buying data or tools, or importing contacts needs the owner's explicit approval.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no accounts, signals, contacts, win rates or results that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/14-sales/14-prospecting-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Prospecting plan: <business, period>
Skill: 14-prospecting · Date: <YYYY-MM-DD> · Framework: Prospecting / list building (ICP filters, signals, cadence sized to capacity)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nobody contacted, nothing bought or imported
## Where wins come from
| Source | Leads | Won | Win rate | Label |
| --- | --- | --- | --- | --- |
## How many accounts we need (calculated)
## List criteria and sources
## Signals
## Cadence
| Touch | Day | Channel | What is new |
| --- | --- | --- | --- |
## Warm introductions
## Tracking
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/14-sales/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the win rates by source, how many accounts the plan needs and why, the list criteria and the cadence, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Win rates by source are counted; prospecting adds to what closes rather than replacing it.
- [ ] Volume is calculated backwards from capacity and the business's own win rates.
- [ ] List criteria come from the ICP with disqualifiers; sources are lawful; no bought or scraped personal data or invented contacts.
- [ ] Signals are dated and sourced; the cadence adds something each touch and stops at reply or no.
- [ ] Tracking counts qualified pipeline and clients by source; nothing is contacted or bought without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Prospect only accounts that fit, for a true reason, at the volume your capacity and win rate call for, and count qualified pipeline, not meetings. Prospecting / list building, The Complete Marketing System, section 14 Sales (Servidad, 2026); Fanatical Prospecting (Jeb Blount); Predictable Revenue (Aaron Ross and Marylou Tyler).
