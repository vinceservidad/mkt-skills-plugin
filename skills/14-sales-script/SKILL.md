---
name: 14-sales-script
description: Write a sales call script that diagnoses, sells the outcome and closes honestly (CLOSER, Challenger). Use for sales scripts, closing calls, call structure, proposal presentation, setter-closer.
metadata:
  section: "14 Sales"
  covers: "Challenger Sale; CLOSER (Hormozi); Consultative / solution selling; Proposal and pricing presentation; Sales script; Sandler; Setter–closer model; Straight Line"
---
# Sales script

A sales call is a conversation the buyer should leave clearer, whether or not they buy. A script works when it spends most of the call on the buyer's situation, plays back the gap in their own words, presents only the part of the offer that closes that gap, handles the real objection, and asks for a decision with true terms. It fails when the seller talks first and longest, invents urgency, pushes past a no, or reads lines that ignore what the buyer just said. This skill writes the call structure, the questions and the close; deep discovery questioning belongs to `14-discovery-spin` and the objection answers to `14-objection-handling`.

Save the script as a Markdown file in `work/14-sales/` when the required inputs are present and the commercial terms are confirmed. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Core offer**, from `07-offer-design`: what is sold, and what each part solves.
- `context/customer.md` → **Beliefs, objections and drivers**, from `02-buyer-psychology`: what the buyer believes and fears when they get on the call.
- If present, also read `context/offer.md` → Price and model, Guarantee, Bonuses, Urgency and scarcity, Value ladder; `context/customer.md` → ICP and personas, Pains, desires and fears, Buying triggers and process, Voice of customer; `context/message.md` → Objection map, Proof stack, Story; call notes, lost reasons, win rates and the current process in `inputs/`; any work in `work/14-sales/14-discovery-spin-*.md` or `14-objection-handling-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (interviews, call notes or sales notes in `inputs/`): run the skill that fills the missing section (`07-offer-design` or `02-buyer-psychology`) first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Core offer → `07-offer-design`; Beliefs, objections and drivers → `02-buyer-psychology`), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Prices, discounts, deadlines, guarantees, payment terms and start dates said on the call are the owner's commitments. Use only what `offer.md` and `inputs/` hold.
  - If the request asks to include **false urgency** (for example telling buyers the price goes up when notes say it is not), **refuse the false urgency and still write the complete sales script file** to `work/14-sales/` using only true offer terms and real capacity urgency from `offer.md`.
  - Only **stop and withhold the deliverable file** (write nothing to `work/14-sales/`) when the request asks to write a **new, unconfirmed commercial concession** not in `offer.md` (such as an unapproved discount, payment plan, or call-only concession): ask the owner to confirm the exact terms and margin impact, flag any call-only deadline as pressure, and end the stop reply with the **Principle, framework, source** block.
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.
- If `02-buyer-psychology` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/sales-script-guide.md](references/sales-script-guide.md) for the call frameworks, talk-time balance, the close and what never to say.

1. **Read the current process.** From `inputs/`, record how calls run today (length, who talks when, what happens after), the win rate and lost reasons with counts from [scripts/tally.py](scripts/tally.py), and where deals are lost. Name the two or three changes that matter most, each tied to evidence.
2. **Choose the frame.** Pick the structure that fits the sale (see the guide): CLOSER (Hormozi) for a single-call close, consultative / solution selling for a considered B2B buy, Challenger for teaching a buyer a new view of their problem, Sandler for qualifying out early, Straight Line for keeping a long call on track. Name one primary frame and why.
3. **Who decides.** Ask early who else decides and how they decide. If another person signs, the script books a call with them rather than closing without them.
4. **Diagnose first.** Most of the call is the buyer talking: the situation, the cost of the problem in their words, what they tried, what a good outcome is. Use the buyer's language from Voice of customer. Hand deeper question design to `14-discovery-spin`.
5. **Play back the gap.** Summarise the gap (where they are, where they want to be, what it costs) and ask if it is right before any pitch.
6. **Present only what closes the gap.** Map each offer component to a pain the buyer named. Proof only from Proof stack or `inputs/` with permission. The proposal and pricing presentation: state the price, what is included, the guarantee as written, and the next step; no hidden terms.
7. **Objections.** For the top objections by count, a short acknowledge, ask, answer pattern; the full answers come from `14-objection-handling`. Treat *not ready* and price as questions to explore, not walls to push.
8. **The close.** A plain ask with true terms and a real next step (start date, onboarding slot from capacity). If the answer is no, agree a clear next step or close the file politely. No fake deadlines, no price rises that aren't real, no pressure after a no.
9. **Setter–closer.** If volume or roles call for it, say what a setter qualifies and hands over; otherwise state why one person running calls is right for now.
10. **Approval.** The script is a draft. Using it on calls, changing prices or terms, or adding a new role needs the owner's explicit approval.
11. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, case studies, client names, prices, guarantees, deadlines or claims that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/14-sales/14-sales-script-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Sales call script: <business, offer>
Skill: 14-sales-script · Date: <YYYY-MM-DD> · Framework: Sales script (<primary frame: CLOSER, consultative, Challenger, Sandler or Straight Line>)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; not yet used on calls
## What changes and why (evidence)
## Call structure
| Part | Minutes | Who talks most | Goal |
| --- | --- | --- | --- |
## Opening and agenda
## Who decides
## Diagnosis questions
## Playback
## Presentation and price
## Objections (short form)
## Close and next step
## After the call
## What never to say
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/14-sales/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the frame chosen and why, the biggest change to the current call, how the close works, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Changes are tied to the current process, win rate and lost reasons, counted with `tally.py`.
- [ ] The buyer talks most; diagnosis and playback come before any pitch; who decides is asked early.
- [ ] Each offer component presented maps to a pain the buyer named; proof is only what exists with permission.
- [ ] Price, guarantee and terms are stated as in `offer.md`; no false urgency, invented price rise or pressure after a no.
- [ ] Objections are explored before answered; the plan says the script is not used without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Diagnose before you prescribe: let the buyer state the gap, show only what closes it, and ask for the decision on true terms. Sales script frames from The Complete Marketing System, section 14 Sales (Servidad, 2026); CLOSER from $100M Leads and Hormozi's sales training; The Challenger Sale (Dixon and Adamson); Sandler selling (David Sandler); Way of the Wolf (Jordan Belfort) for the Straight Line.
