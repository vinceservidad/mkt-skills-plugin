---
name: 11-cold-email
description: Plan cold outreach and account-based plays with a list, first line, value, soft ask and follow-up. Use for cold email, outbound, ABM, target accounts, prospecting emails.
metadata:
  section: "11 Distribution"
  covers: "Account-Based Marketing (ABM); Cold outreach"
---
# Cold email

Cold outreach works when a short list of accounts that fit is written to one at a time, with a reason to write today, one useful point and a small ask. It fails when the list is bought or scraped by title, the first line is fake personalization, the sender's main domain blasts hundreds a day, the proof is borrowed, or success is counted in opens. The plan's job is to pick the accounts that fit, earn each reply, protect the domain, stay inside the law, and judge the work on qualified conversations the business can take on.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present (unless stopping under Owner commitments). Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: which accounts fit, who decides, and who is disqualified.
- `context/offer.md` → **Core offer**, from `07-offer-design`: what the email offers and what a reply leads to.
- If present, also read `context/customer.md` → Segments, Pains, desires and fears, Buying triggers and process, Beliefs, objections and drivers, Voice of customer; `context/awareness.md` → Awareness map and Traffic temperature (cold traffic is usually problem-aware at best); `context/offer.md` → Price and model, Guarantee, Urgency and scarcity (capacity); `context/message.md` → Promise, Proof stack, Objection map; `context/brand.md` → Voice; account lists, sending setup, capacity and permission notes in `inputs/`; any work in `work/14-sales/14-prospecting-*.md` or `work/11-distribution/11-channel-selection-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (interviews, reviews or sales notes in `inputs/` but no ICP): run `02-icp-persona` first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (ICP and personas → `02-icp-persona`; Core offer → `07-offer-design`), and ask for evidence (interviews, closed-deal notes), not a description of the buyer. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Offers made in the email (a free audit, a trial, a discount, a deadline), the sending domain and mailbox, the daily volume, the sender's name and the footer address are the owner's commitments. If the request proposes an offer, discount or deadline that `offer.md` and `inputs/` don't hold, stop before writing, ask for the exact terms, and write no deliverable file in `work/11-distribution/` on assumed terms (a stop reply still ends with the **Principle, framework, source** block). Leave missing operational details (such as a sender name or exact street address) as placeholders for the owner to supply in the plan, and reshape an unsafe daily volume rather than stopping.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/cold-email-guide.md](references/cold-email-guide.md) for account tiers, the four-part email, deliverability, the law and platform facts.

1. **Outcome and capacity.** Name the business outcome that judges the outreach (qualified calls, then clients who sign) and the most the business can take on (onboarding slots, calendar hours). Opens and sends are not the outcome. Size the whole plan from capacity, not from a sending target.
2. **The list.** Score every account against the ICP and its disqualifiers with the evidence from `inputs/` (size, type, location, segment). Disqualified accounts are removed with the reason, never written to "just in case". Count accounts kept and removed with [scripts/tally.py](scripts/tally.py), never by eye. Only lawfully sourced business contacts in roles that decide; never look up, guess or add real people's names or emails, and never suggest buying or scraping a list.
3. **Account-based tiers.** Tier the kept accounts by fit and by a dated public signal (a hire, a move, a public question about the problem). Tier 1 gets a one-to-one email built on its own signal; lower tiers share a written angle. An account with no signal gets no invented one: say there is none and use the segment's pain instead.
4. **The email.** Four parts, short, plain text, from a real person: a first line that is true and specific to the account (its signal, or the segment's situation), the value (one problem the buyer has, in the buyer's words from Voice of customer, and what changes), proof only from Proof stack or `inputs/` that the owner may use in outreach, and a soft ask (an interest question, not a demand for a 30-minute call). No fake reply chains, no false urgency, no claim the context doesn't hold.
5. **Follow-up.** A short sequence of follow-ups that each add something new (another angle, a resource that exists, a plain close-the-loop note), spaced over days, stopping at the first reply, opt-out or bounce. State the number of touches and the gaps; no invented open-rate trigger.
6. **Deliverability.** Protect the main domain. If the domain has never sent cold email, say so and plan a slow start: authentication (SPF, DKIM, DMARC), a separate sending domain or mailbox only if the owner chooses one, a low daily volume that rises only while bounces and complaints stay low, list verification, no tracking pixels or link shorteners by default. A request to send hundreds a day from a cold domain is refused with the reason and a safer volume plan; mailbox-provider thresholds are platform facts to cite or mark *to confirm*.
7. **The law.** Each email needs an honest subject and sender, the business's physical address and a working opt-out that is honored. Where the account is outside the owner's country, or the jurisdiction needs consent for business email, flag it. Legal rules are facts to verify in current official guidance with URL and date, or mark *to confirm*; flag for qualified legal review. This plan is not legal advice.
8. **Tracking and the read.** Record each account's status (sent, replied, positive, meeting, qualified, client) and judge on positive replies, qualified meetings and clients per accounts contacted, with counts. Opens are unreliable and are not a result. Sales follow-up goes to `14-prospecting` and `14-discovery-spin`; lead routing goes to `14-lead-scoring`.
9. **Approval.** The plan is a draft. Sending any email, buying a domain or tool, or importing contacts needs the owner's explicit approval.
10. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, client names, prices, offers, features, signals or contact details that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Describe each source only as it reads: a public review is not permission to quote it in outreach, and a client story is usable only with the client's permission. No third-party benchmark (a "typical" reply rate) is evidence about this business.

## Output

Write `work/11-distribution/11-cold-email-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Cold outreach plan: <business, period>
Skill: 11-cold-email · Date: <YYYY-MM-DD> · Framework: Cold outreach and Account-Based Marketing (list, first line, value, soft ask, follow-up)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing sent, bought or imported
## Outcome and capacity
## The list
| Account | Fit to the ICP (evidence) | Signal (date) | Tier or removed (reason) |
| --- | --- | --- | --- |
## Emails
### Tier 1 (one per account)
### Tier 2 angle
## Follow-up sequence
| Touch | Day | What is new | Stop rule |
| --- | --- | --- | --- |
## Deliverability and volume
## Law and footer
## Tracking and how we judge it
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

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (an interview, a review, the owner's notes), with the source named. Titles of books, essays or talks, including in the Principle, framework, source block, go in italics, never in quotation marks. Write email drafts in italics or a plain block, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the accounts kept and removed with the reason, the daily volume and why, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every account is scored on ICP fit and disqualifiers before it is written to; removed accounts carry the reason; counts come from `tally.py`.
- [ ] Every first line is true and specific; accounts with no signal get no invented one; no real person's name or email is added.
- [ ] Each email has the four parts, one soft ask, proof the owner may use in outreach, and no offer, deadline or claim outside context.
- [ ] Volume is sized from capacity and domain health; a cold main domain is protected with a slow start; mailbox-provider and legal facts are dated or *to confirm*.
- [ ] Each email carries an honest sender and subject, the physical address and an honored opt-out; out-of-country accounts and legal review are flagged.
- [ ] Outreach is judged on positive replies, qualified meetings and clients with counts, not opens.
- [ ] The plan says nothing is sent, bought or imported without the owner's approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Write to fewer accounts that fit, one at a time, with a true reason to write today and a small ask, and protect the domain and the law as carefully as the message. Cold outreach and Account-Based Marketing (ABM), The Complete Marketing System, section 11 Distribution (Servidad, 2026); Predictable Revenue (Aaron Ross and Marylou Tyler) for outbound built on a narrow list and soft asks.
