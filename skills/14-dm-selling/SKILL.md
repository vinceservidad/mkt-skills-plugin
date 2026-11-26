---
name: 14-dm-selling
description: Sell in DMs and chat by opening, qualifying, inviting and closing without spam. Use for DM selling, LinkedIn messages, Instagram DMs, chat sales, replying to people who message after a post.
metadata:
  section: "14 Sales"
  covers: "DM / chat selling"
---
# DM selling

A direct message is a conversation, not a broadcast. DM selling works when the seller answers the person's actual question fast, asks one or two questions to see if they fit, invites the ones who do to the next step (a call, a resource, a checkout), and lets the rest go kindly. It fails when people get a pitch the moment they reply, the price is hidden behind a call when they asked for it, replies take days, or cold messages are sprayed at people who never engaged. Platform rules on automated and bulk messages are strict.

Save the DM playbook as a Markdown file in `work/14-sales/` when the required inputs are present and the commercial terms are confirmed. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Core offer**, from `07-offer-design`: what the conversation leads to.
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: who to invite forward and who to let go.
- If present, also read `context/offer.md` → Price and model, Value ladder, Guarantee; `context/customer.md` → Voice of customer, Beliefs, objections and drivers; `context/brand.md` → Voice; DM counts, common messages, reply times and outcomes in `inputs/`; any work in `work/11-distribution/11-social-*.md` or `work/14-sales/14-lead-scoring-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (sales notes, DM logs or interviews in `inputs/`): run the skill that fills the missing section (`07-offer-design` or `02-icp-persona`) first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Core offer → `07-offer-design`; ICP and personas → `02-icp-persona`), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Prices quoted, DM-only offers and discounts are the owner's commitments. Quote only what `offer.md` holds; if a reply needs a new offer, ask for the exact terms first.
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/dm-guide.md](references/dm-guide.md) for the open, qualify, invite, close flow, reply times, price questions and platform rules.

1. **Read the DM funnel.** Count messages, replies, calls booked and clients from `inputs/` with [scripts/tally.py](scripts/tally.py), with each step's rate *calculated*. Name where people drop (no reply, slow reply, no next step).
2. **Common openings.** Group what people write first (a price question, a resource request, a comment on a post) and write a reply for each that answers the question first.
3. **Qualify lightly.** One or two questions that test the ICP (size, role, the problem) in plain words, never an interrogation.
4. **Invite.** For fits: the next step that matches their stage (a resource that exists, a short call, the offer). For non-fits: a kind reply and a pointer elsewhere.
5. **Price questions.** If the price model is public in `offer.md`, give the range and what decides it, then ask a question; don't hide it behind a call.
6. **Speed and routine.** A reply-time target the owner can keep and a daily slot for DMs; saved replies adapted to each person, never sent blind.
7. **Outbound DMs.** Only to people who engaged (commented, followed, asked) with a reason tied to that, at low volume; decline automated mass DM blasts to unengaged people. Explain the platform rules on automation/bulk messaging (cited with URL and date or marked *to confirm*), account-restriction and reputation risk, **and** compare any requested blast volume against the business's real onboarding/delivery capacity from `offer.md` / `inputs/` (e.g., if capacity is only a few new clients a month, sending hundreds of DMs a day far exceeds capacity).
8. **Track.** Conversations, qualified, invited, booked, clients, with counts and reply times.
9. **Approval.** The playbook is a draft. Sending messages, using automation tools or quoting new offers needs the owner's explicit approval.
10. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no prices, offers, results, client names or quotes that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/14-sales/14-dm-selling-<YYYY-MM-DD>-<slug>.md`:

```markdown
# DM playbook: <business, platform>
Skill: 14-dm-selling · Date: <YYYY-MM-DD> · Framework: DM / chat selling (open, qualify, invite, close)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing sent
## The DM funnel today
| Step | Count | Rate (calculated) |
| --- | --- | --- |
## Replies by opening
## Qualifying questions
## Invite and close
## Price questions
## Reply time and routine
## Outbound DMs
## Platform facts
| Fact the plan relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## Tracking
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/14-sales/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the funnel with its drop-off, the reply for each common opening, the reply-time target, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The DM funnel is counted and the biggest drop named.
- [ ] Each reply answers the person's question first; qualification is one or two plain questions.
- [ ] Price questions get the range from `offer.md`; no new offer without the owner's terms.
- [ ] Outbound DMs go only to people who engaged, at low volume, without mass automation; platform rules are dated or *to confirm*.
- [ ] Tracking counts calls and clients; nothing is sent without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Answer the question they asked, fast; qualify lightly; invite only those who fit; let the rest go kindly. DM / chat selling, The Complete Marketing System, section 14 Sales (Servidad, 2026); conversational selling principles from consultative selling.
