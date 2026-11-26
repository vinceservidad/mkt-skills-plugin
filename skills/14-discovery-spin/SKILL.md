---
name: 14-discovery-spin
description: Run discovery that makes the prospect state the gap and qualify the deal (SPIN, Gap Selling, MEDDIC). Use for discovery calls, qualifying questions, what to ask prospects, deal qualification.
metadata:
  section: "14 Sales"
  covers: "Gap Selling; MEDDIC / MEDDPICC; SPIN Selling"
---
# Discovery (SPIN, Gap, MEDDIC)

Discovery is where the buyer, not the seller, states the problem, what it costs and what good looks like. Good discovery makes the gap obvious to the buyer and tells the seller whether the deal is real: who decides, how, by when, and against what. It fails when questions are a checklist read in order, the seller answers their own questions, the cost of the problem is never put into the buyer's numbers, or the person who signs is never found. This skill writes the questions and the qualification record; the full call and the close belong to `14-sales-script`.

Save the discovery guide as a Markdown file in `work/14-sales/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **Pains, desires and fears**, from `02-customer-research`: the problems the questions should surface, in the buyer's words.
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: who is worth qualifying in and who is disqualified.
- If present, also read `context/customer.md` → Jobs to be done, Buying triggers and process, Beliefs, objections and drivers, Voice of customer; `context/offer.md` → Core offer, Price and model; `context/message.md` → Objection map; call notes, lost reasons, deal records and the current process in `inputs/`; any work in `work/14-sales/14-sales-script-*.md` or `14-lead-scoring-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (interviews, call notes or reviews in `inputs/`): run `02-customer-research` or `02-icp-persona` first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Pains, desires and fears → `02-customer-research`; ICP and personas → `02-icp-persona`), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If `02-customer-research` is not loaded, stop and say: enable mkt-q1-audience.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/discovery-guide.md](references/discovery-guide.md) for SPIN question types, the gap, MEDDIC and MEDDPICC fields and when to use each.

1. **Read what loses deals.** From `inputs/`, count lost reasons and deal outcomes with [scripts/tally.py](scripts/tally.py). Name which ones discovery could have caught (a hidden decider, a poor fit, an unstated alternative) and say how.
2. **Pick the depth.** SPIN Selling (Rackham) for most considered sales; Gap Selling (Keenan) when the buyer must see the distance between current and future state; MEDDIC or MEDDPICC for larger, multi-person enterprise B2B deals. Name the choice and why. Fit qualification depth to deal size and complexity: for a small founder-led sale (e.g., 10–40 person companies with 1–2 deciders), **push back and do NOT force all eight MEDDPICC fields as mandatory on every call — even if the user explicitly asks to require all eight**; keep only the lightweight fields that fit the sale (such as fit/disqualifiers, economic buyer/co-founder, pain/metrics, timing) and explicitly drop or defer heavy enterprise fields (Paper process, Champion, formal Decision Process bureaucracy).
3. **Situation and early gatekeepers (few, early).** Only what the seller can't find out before the call; ask fewer as the CRM and research fill them. Put two checks **early in the call** (before deep pitching): (a) who else decides (partner, co-founder, economic buyer) when lost-deal notes show partner vetoes, and (b) whether the buyer wants a service outside the ICP disqualifiers (e.g., strategic/CFO advice vs. bookkeeping).
4. **Problem and implication.** Questions that let the buyer describe the problem and then its cost: money, time, risk, a decision they couldn't make. Use the pains and triggers in context, in the buyer's words. Explicitly link *not ready* or timing losses to **implication questions about the cost of waiting**, and show that link in the lost-reasons table.
5. **Need-payoff and future state.** Questions that let the buyer say what good looks like and what it is worth to them. The gap is current state minus future state, in their numbers.
6. **Qualification.** Record the fields that decide whether to continue: fit to the ICP and disqualifiers, the economic buyer and other deciders, decision criteria and process, timing, the alternative they would choose (including doing nothing), and the pain's size. Each field is *heard on the call* or *unknown*, never guessed.
7. **Disqualify cleanly.** Write the exit for a prospect who fails a disqualifier: say so plainly and, if useful, point them elsewhere.
8. **Record.** A one-page call record so the next step and the proposal use the buyer's words.
9. **Approval.** The guide is a draft. Using it on calls or changing CRM fields needs the owner's explicit approval.
10. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no pains, results, deal facts or buyer quotes that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/14-sales/14-discovery-spin-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Discovery guide: <business, offer>
Skill: 14-discovery-spin · Date: <YYYY-MM-DD> · Framework: SPIN Selling / Gap Selling / MEDDIC (<chosen>)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; not yet used on calls
## What discovery must catch (evidence)
## Situation questions
## Problem and implication questions
## Need-payoff and future state
## The gap, in the buyer's numbers
## Qualification record
| Field | Question that gets it | Heard / unknown |
| --- | --- | --- |
## Disqualify and exit
## Call record template
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/14-sales/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the method chosen and why, the questions that catch the top lost reasons, the qualification fields, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Lost reasons are counted and linked to the questions that would catch them.
- [ ] Questions move from situation to problem, implication and payoff; the buyer states the cost and the future state.
- [ ] Qualification covers fit, deciders, criteria, process, timing and the alternative; each field is heard or unknown.
- [ ] Disqualifiers from the ICP have a clean exit; the plan says it is not used without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Let the buyer state the problem, its cost and what good looks like, and find every person who decides before you propose. SPIN Selling (Neil Rackham), Gap Selling (Keenan), MEDDIC / MEDDPICC (Dick Dunkel and Jack Napoli, PTC); The Complete Marketing System, section 14 Sales (Servidad, 2026).
