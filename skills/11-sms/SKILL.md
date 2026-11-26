---
name: 11-sms
description: Plan SMS as an owned channel with consent, cadence and message types. Use for SMS marketing, text message campaigns, shipping texts, collecting phone opt-ins, how often to text customers.
metadata:
  section: "11 Distribution"
  covers: "SMS marketing"
---
# SMS

A text lands on the phone in someone's pocket, so it is the most personal channel a business has and the easiest to abuse. SMS works when people have agreed to texts in writing, each message is something they want now (a shipping heads-up, a reply to their question, an offer they asked for), and texts are few. It fails when a phone number given for delivery is treated as permission, promotions go out on a schedule nobody asked for, or the opt-out is missing. The legal exposure is higher than email in many countries. This skill plans who can be texted, what, when, and how consent is collected.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present and the request does not depend on unconfirmed commercial terms (see Owner commitments). Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/awareness.md` → **Journey** (from `03-journey-map`) or **Awareness map** (from `03-awareness-map`): the moments where a text helps.
- If present, also read `context/offer.md` → Core offer, Price and model, Bonuses, Urgency and scarcity; `context/customer.md` → ICP and personas, Voice of customer; `context/brand.md` → Voice; phone-number, consent, ticket and tool notes in `inputs/`; any work in `work/11-distribution/11-email-channel-*.md` or `work/15-retention/15-lifecycle-*.md`.
- If the required section is missing:
  - **The upstream evidence exists** (tickets, reviews or interviews in `inputs/`): run `03-journey-map` first, then continue.
  - **It doesn't:** stop. Name the missing section with the skill that fills it (Journey → `03-journey-map`; Awareness map → `03-awareness-map`) and ask for evidence. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Any offer, price, discount or deadline in a text is the owner's commitment. If the request asks to write or send a promotional blast or campaign built around an unconfirmed offer, discount or deadline that `offer.md` and `inputs/` don't hold (such as a flash sale), stop, ask the owner to confirm the exact terms, and write no deliverable file in `work/11-distribution/` (a stop reply still ends with the **Principle, framework, source** block). If the request asks for a full SMS channel plan that also mentions an unconfirmed offer idea alongside confirmed channel needs (such as service texts and opt-in design), write the plan without writing that proposed offer as a live text, mark it *owner to set*, and ask for confirmation.
- If `03-journey-map` and `03-awareness-map` are both not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/sms-guide.md](references/sms-guide.md) for consent, message types, cadence and the legal and carrier facts to verify.

1. **Outcome.** Name what SMS is for (fewer missed deliveries and "where is my box" tickets, repeat orders, replies) and how it is judged, with counts. Click rate alone is not the outcome.
2. **Who can be texted, and for what.** Count phone numbers by how they were collected with [scripts/tally.py](scripts/tally.py) or the notes. A number given at checkout for delivery is not consent to marketing texts. Separate transactional or service messages (shipment notices, order updates the customer opted into) from marketing messages (offers, promotions). Marketing texts need prior express written consent where the law requires it (for example the US TCPA) and a clear opt-in; verify the rules for each country and mark *to confirm*.
3. **Collect consent.** Design the opt-in: where it appears (checkout, account, app), the exact disclosure the owner must approve (what messages, roughly how often, that rates may apply, how to stop), a confirmation text, and keyword opt-out (STOP) honored at once. The final wording goes to legal review.
4. **Message types by journey moment.** Map each text to a moment in Journey with its evidence (a ticket group, a review). Service texts that answer a real problem come first. Each message type gets its trigger, content, and whether it is service or marketing.
5. **Cadence and quiet hours.** Few marketing texts, sent at reasonable local hours, never more often than the disclosure says. Service texts follow the event. State the caps.
6. **The texts.** Short, from the brand by name, one action, the opt-out on the first message and as required after. Only offers in `offer.md`; a proposed offer is marked *owner to set*.
7. **Tool and cost.** SMS tools charge per message and carriers require registration for business texting in some countries (for example US 10DLC). Costs and registration are platform facts: cite with URL and date or mark *to confirm*. Buying a tool needs the owner's approval.
8. **Tracking.** Per message type: sent, delivered, opt-outs, clicks, orders or tickets avoided, with counts. Watch opt-out rate per send.
9. **Approval.** The plan is a draft. Sending any text, adding an opt-in to checkout or buying a tool needs the owner's explicit approval.
10. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, rates, offers, prices or consent records that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. No benchmark click or opt-out rate is evidence.

## Output

Write `work/11-distribution/11-sms-<YYYY-MM-DD>-<slug>.md`:

```markdown
# SMS plan: <business, period>
Skill: 11-sms · Date: <YYYY-MM-DD> · Framework: SMS marketing (consent first, service before promotion)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing sent, no opt-in changed, no tool bought
## Outcome
## Who can be texted
| Group | Count | How the number was collected | Service texts? | Marketing texts? |
| --- | --- | --- | --- | --- |
## Consent and opt-in
## Message types
| Journey moment (evidence) | Trigger | Type (service / marketing) | Text | Cap |
| --- | --- | --- | --- | --- |
## Cadence and quiet hours
## Tool, registration and cost
## Tracking
## Platform and legal facts
| Fact the plan relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Titles of books, essays or talks, including in the Principle, framework, source block, go in italics, never in quotation marks. Write draft texts in italics or a plain block. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`) and fix every line it prints until it reports every quotation matches.

Reply with the file path, who can be texted now and for what, the first message types, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Phone numbers are grouped by how they were collected; a delivery number is never treated as marketing consent.
- [ ] Service and marketing texts are separated; marketing texts wait for documented opt-in; legal rules are dated or *to confirm* and legal review is flagged.
- [ ] Every message type maps to a journey moment with evidence; service texts that fix a real problem come first.
- [ ] Cadence, caps and quiet hours are stated; every marketing text has the opt-out.
- [ ] Only offers in `offer.md`; proposed offers are marked *owner to set*.
- [ ] Tool cost and carrier registration are dated or *to confirm*; the plan says nothing is sent or bought without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Text only people who asked for texts, send what helps them at that moment before anything that sells, and keep it rare. SMS marketing, The Complete Marketing System, section 11 Distribution (Servidad, 2026); permission marketing (Seth Godin).
