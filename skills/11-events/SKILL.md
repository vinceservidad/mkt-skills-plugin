---
name: 11-events
description: Use events, trade shows and speaking to meet buyers and book conversations. Use for conference booths, trade shows, speaking slots, meetups, hosting an event, whether an event is worth it.
metadata:
  section: "11 Distribution"
  covers: "Events, trade shows and speaking"
---
# Events

Events put the business in a room with buyers. They work when the room holds the ICP, the business has a reason for those buyers to talk to it (a talk, a useful session, a specific offer), conversations are booked before and during the event, and the follow-up happens within days. They fail when a booth is bought on the organiser's attendance figure, the goal is badge scans, nobody plans the follow-up, or the cost is never compared with what else the money could do. Speaking and small hosted events are often cheaper and better than a booth.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present (unless stopping under Owner commitments). Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: who must be in the room.
- If present, also read `context/customer.md` → Buying triggers and process, Voice of customer; `context/offer.md` → Core offer, Price and model, Urgency and scarcity (capacity); `context/message.md` → Big idea, Story, Proof stack; `context/brand.md` → Voice; event details, costs, attendance claims, staff time and past event results in `inputs/`; any work in `work/11-distribution/11-co-marketing-*.md` or `work/14-sales/`.
- If the required section is missing:
  - **The upstream evidence exists** (interviews, sales notes in `inputs/`): run `02-icp-persona` first, then continue.
  - **It doesn't:** stop. Name the missing section with the skill that fills it (ICP and personas → `02-icp-persona`) and ask for evidence. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Booth fees, sponsorship packages, travel, show-only offers and staff days are the owner's commitments. When evaluating event options whose costs are in `inputs/`, the plan compares options with their costs and leaves the spend decision to the owner. If the request asks to plan around an unconfirmed show-only discount, freebie or unpriced spend that `offer.md` and `inputs/` don't hold, stop, ask the owner to confirm the exact offer terms (eligibility, end date or sign-up deadline, margin impact, capacity) and spend, and write no deliverable file in `work/11-distribution/` (a stop reply still ends with the **Principle, framework, source** block).
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/events-guide.md](references/events-guide.md) for event types, the fit test, the cost per conversation, and the before, during and after plan.

1. **Outcome.** Name what the event must produce (qualified conversations, booked calls, clients) and the count that would make it worth repeating, from the business's own deal value and capacity. Badge scans and booth visits are signals.
2. **Options.** List each event or format in `inputs/` (booth, sponsorship, speaking slot, attending, a small hosted event, a co-hosted event) with dates, deadlines and costs. Never invent an event, its date or its audience.
3. **Fit test.** For each: evidence that the ICP attends (the organiser's figure labelled as their claim; ask for attendee breakdown by role, company size and location), the share likely to fit, and conflicts with capacity or blocked weeks.
4. **Cost per conversation.** Compute the full cost (fees, travel, materials, staff days) and the conversations needed to justify it with the arithmetic shown, labelled *calculated* and built on stated assumptions. Compare options on this, and against the cheapest fit option (speaking, attending, a meetup).
5. **Before.** A reason to talk (a talk, a useful resource that exists, a short diagnostic), outreach to booked meetings with attendees who fit (only through channels the organiser allows), and roles.
6. **During.** What staff do, how conversations are qualified against the ICP, how notes are captured, and what is booked on the spot.
7. **After.** Follow-up within days, by priority, with the next step; contacts collected at the event are used only as the attendee agreed.
8. **Measure.** Conversations, qualified, calls booked, clients, cost per each, with counts and dates; compare with the threshold set in step 1.
9. **Approval.** The plan is a draft. Buying a booth or ticket, applying to speak, or contacting attendees needs the owner's explicit approval.
10. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no attendance, results, offers or costs that aren't in `context/` or `inputs/`. Count from files with [scripts/tally.py](scripts/tally.py), never by eye. Mark inferences `(assumption)` and list what is needed under Open questions. No benchmark event return is evidence.

## Output

Write `work/11-distribution/11-events-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Events plan: <business, period>
Skill: 11-events · Date: <YYYY-MM-DD> · Framework: Events, trade shows and speaking (cost per qualified conversation)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing bought, applied for or sent
## Outcome and the threshold
## Options
| Event or format | Date and deadline | Cost | Buyer fit (evidence; claimed or verified) | Capacity conflict |
| --- | --- | --- | --- | --- |
## Cost per conversation
## Recommendation
## Before
## During
## After
## How we judge it
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Titles of books, essays or talks, including in the Principle, framework, source block, go in italics, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`) and fix every line it prints until it reports every quotation matches.

Reply with the file path, the recommended option and why, the cost per conversation needed for each option, the dates and deadlines, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every option is judged on evidence the ICP attends; organiser figures are labelled claims with a request for a breakdown.
- [ ] Full costs and the conversations needed to justify each option are calculated and shown, with assumptions labelled.
- [ ] Cheaper fit formats (speaking, attending, a meetup) are compared, not skipped.
- [ ] Before, during and after are planned; follow-up has a deadline; attendee data is used only as agreed.
- [ ] The event is judged on qualified conversations, calls and clients with counts, not scans.
- [ ] Deadlines and capacity are respected; nothing is bought, applied for or sent without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Go where your buyers gather, give them a reason to talk to you, book the conversations before you arrive, and follow up within days; judge every event on qualified conversations per dollar. Events, trade shows and speaking, The Complete Marketing System, section 11 Distribution (Servidad, 2026); Traction (Gabriel Weinberg and Justin Mares), offline events and speaking engagements.
