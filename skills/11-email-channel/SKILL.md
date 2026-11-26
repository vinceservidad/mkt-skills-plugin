---
name: 11-email-channel
description: Run email as a channel with list growth, consent, deliverability and a broadcast calendar. Use for email marketing, newsletter plan, growing the list, inbox placement, how often to email.
metadata:
  section: "11 Distribution"
  covers: "Email marketing; Permission Marketing (Godin)"
---
# Email channel

Email is the channel a business owns, so its value is the list's trust. It works when every contact agreed to hear from the business, the sending domain is healthy, each email is worth opening, and the plan is judged on orders or qualified replies. It fails when old or borrowed contacts are mailed, frequency jumps overnight, opens are taken as results, or growth is bought with an offer the owner never approved. This skill plans the channel: who is on the list and why, how it grows, how mail lands, and what goes out when. Writing one email belongs to `10-email-copy`; automated sequences belong to `12-email-sequences` and `15-lifecycle`.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present and the commercial terms are confirmed. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: who the list is for.
- If present, also read `context/offer.md` → Core offer, Price and model, Bonuses, Urgency and scarcity, Value ladder; `context/brand.md` → Voice; `context/awareness.md` → Journey; `context/message.md` → Promise, Proof stack; list exports, sign-up wording, sending reports and setup notes in `inputs/`; any work in `work/12-funnel/12-lead-magnet-*.md`, `work/12-funnel/12-email-sequences-*.md` or `work/15-retention/15-lifecycle-*.md`.
- If the required section is missing:
  - **The upstream evidence exists** (reviews, tickets or interviews in `inputs/` but no ICP): run `02-icp-persona` first, then continue.
  - **It doesn't:** stop. Name the missing section with the skill that fills it (ICP and personas → `02-icp-persona`) and ask for evidence, not a description of the buyer. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Discounts, sign-up incentives, deadlines and new products in emails are the owner's commitments. If the plan needs one that `offer.md` and `inputs/` don't hold, ask for the exact terms and plan the calendar without it.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/email-channel-guide.md](references/email-channel-guide.md) for consent, list hygiene, deliverability, cadence and measurement, and [references/godin-permission.md](references/godin-permission.md) for Seth Godin's Permission Marketing ladder and three-part email test.

1. **Outcome.** Name what the channel is judged on (orders, repeat orders, qualified replies) and the measure the plan reports (orders or revenue per email delivered, with the attribution rule the tool uses). Opens are a weak signal; privacy features inflate them.
2. **The list by source and consent.** Count contacts by source with [scripts/tally.py](scripts/tally.py) or the export, never by eye. For each source, record what the person agreed to (the exact sign-up wording if supplied). Contacts with no record of consent to marketing email are held out of broadcasts until the owner gets consent or confirms a lawful basis; never mail them to "warm up" or to see what happens. Consent and legal rules are facts to verify (see the guide) or mark *to confirm*.
3. **Read the reports.** Compute click rate, unsubscribe rate and orders per 1,000 delivered from the reports with [scripts/sum_by.py](scripts/sum_by.py), with each figure labelled *observed* (tool) or *calculated*. Note trends (rising unsubscribes, falling clicks) and the limit of the tool's attribution window. No industry benchmark is evidence.
4. **Deliverability.** Check authentication (SPF, DKIM, DMARC), the sending domain, list hygiene (bounces, long-inactive contacts), complaint handling and one-click unsubscribe. If DMARC is unknown, say so and put it first. Raise frequency gradually from what the list is used to; a list mailed every two months is not ready for weekly email overnight. Mailbox-provider rules are platform facts: cite the current page with URL and date, or mark *to confirm*.
5. **Growth.** Plan how the list grows from sources that fit the ICP and collect clear consent: the sign-up points that exist, a lead magnet (`12-lead-magnet`), checkout opt-in. An incentive is an owner commitment. Never suggest buying, renting or scraping lists.
6. **Broadcast calendar.** Cadence the owner can sustain (their stated time), content types that serve the ICP and the journey, and the share that sells versus helps. Each slot names its purpose and the offer it may use, only from `offer.md`.
7. **Segments and suppression.** Simple segments the data supports (customers vs non-customers, by source, by recent engagement); who is suppressed (no consent, unsubscribed, bounced, long-inactive) and when inactive contacts get a re-permission email.
8. **Approval.** The plan is a draft. Sending any email, importing contacts or changing sign-up forms needs the owner's explicit approval.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, subscriber counts, rates, offers or testimonials that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions.

## Output

Write `work/11-distribution/11-email-channel-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Email channel plan: <business, period>
Skill: 11-email-channel · Date: <YYYY-MM-DD> · Framework: Email marketing (consent, deliverability, cadence)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing sent or imported
## Outcome and how it is measured
## The list
| Source | Contacts | What they agreed to (wording) | Mail now? |
| --- | --- | --- | --- |
## What the reports say
| Send | Delivered | Click rate | Unsubscribe rate | Orders per 1,000 | Label |
| --- | --- | --- | --- | --- | --- |
## Deliverability fixes
## List growth
## Broadcast calendar
## Segments and suppression
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

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Titles of books, essays or talks, including in the Principle, framework, source block, go in italics, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`) and fix every line it prints until it reports every quotation matches.

Reply with the file path, which contacts can be mailed now and which are held with the reason, the cadence and why, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Contacts are counted by source with what each agreed to; contacts with no consent record are held out of broadcasts.
- [ ] Rates come from the reports via `sum_by.py`, labelled; opens are not treated as a result; no benchmark is used.
- [ ] Authentication, hygiene and unsubscribe are checked; unknowns come first; frequency rises gradually from the current rhythm.
- [ ] List growth uses consented sources that fit the ICP; no bought or scraped lists; incentives are owner commitments.
- [ ] The calendar fits the owner's stated time and uses only offers in `offer.md`.
- [ ] Platform and legal facts are dated or *to confirm*; the plan says nothing is sent or imported without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Mail only people who asked to hear from you, often enough to stay useful and never faster than the domain can carry, and judge email on the orders it brings. Email marketing, The Complete Marketing System, section 11 Distribution (Servidad, 2026); Permission Marketing (Seth Godin).
