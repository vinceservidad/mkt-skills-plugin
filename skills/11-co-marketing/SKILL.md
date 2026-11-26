---
name: 11-co-marketing
description: Borrow audiences through partnerships, the Dream 100 and newsletter sponsorships. Use for co-marketing, joint webinars, list swaps, partner promotions, sponsoring a newsletter, Dream 100 list.
metadata:
  section: "11 Distribution"
  covers: "Co-marketing / partnerships; Dream 100; Newsletter sponsorships"
---
# Co-marketing

Co-marketing borrows an audience another business, community or newsletter already built. It works when that audience is the buyer, each side brings something real, the people on both lists keep control of their data, and the result is counted in leads or customers. It fails when the partner's audience is taken on trust, a list swap hands over contacts who never agreed, a sponsorship is bought on a subscriber count alone, or the deal has no owner and no end date. Paid-per-sale partners are `11-affiliate-jv`; individual creators are `11-influencer`.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present (unless stopping under Owner commitments). Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: whose audience counts and who is disqualified.
- If present, also read `context/customer.md` → Segments, Buying triggers and process, Voice of customer; `context/offer.md` → Core offer, Price and model, Value ladder, Urgency and scarcity (capacity); `context/message.md` → Big idea, Promise, Proof stack, Story; partner offers, media kits, rate cards, list and consent notes in `inputs/`; any work in `work/11-distribution/11-channel-selection-*.md`, `11-affiliate-jv-*.md`, `11-influencer-*.md` or `work/12-funnel/12-webinar-challenge-*.md`.
- If the required section is missing:
  - **The upstream evidence exists** (interviews, sales notes or reviews in `inputs/`): run `02-icp-persona` first, then continue.
  - **It doesn't:** stop. Name the missing section with the skill that fills it (ICP and personas → `02-icp-persona`) and ask for evidence. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Sponsorship fees, partner offers or discounts, event dates and anything given to a partner are the owner's commitments. If the request asks to book or build a promotion around an unpriced commitment or an offer or discount that `offer.md` and `inputs/` don't hold (such as a multi-issue package with no price or a free-month offer), stop, ask the owner to confirm the exact terms, and write no deliverable file in `work/11-distribution/` (a stop reply still ends with the **Principle, framework, source** block). When evaluating priced options from `inputs/` on existing offers, leave the spend decision to the owner as *owner to set*.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/co-marketing-guide.md](references/co-marketing-guide.md) for partner types, the fit test, deal formats, data rules and sponsorship checks.

1. **Outcome.** Name the outcome (qualified leads, booked calls, customers) and how each partnership is judged, with counts, recorded by a unique link, a registration source or the CRM source field.
2. **Dream 100.** List the places the ICP already gathers (newsletters, podcasts, communities, complementary businesses, events), each with the evidence that buyers follow it. Use only places named in `inputs/` or by buyers; describe people by role; never look up or add real names or contacts.
3. **Fit test per partner.** Audience fit to the ICP and its disqualifiers, with the source; the partner's own audience figure labelled as their claim; overlap and conflict (a competitor, a disqualified segment); what each side gains.
4. **Format per partner.** Joint webinar or content, co-hosted event, newsletter mention or sponsorship, bundle, integration listing, guest content. Pick the smallest format that tests fit; a partner-hosted local event where the partner covers venue cost is a low-cost test with attendance marked unknown until registrations (qualify fit and cap against capacity rather than inventing attendance).
5. **Data rules.** Never swap or share contact lists unless every contact agreed to that sharing. In a joint promotion each side promotes to its own list, and registrants choose what they share with whom on the sign-up form. Privacy rules are facts to verify (see the guide) or mark *to confirm*.
6. **Sponsorships.** Judge a paid slot on audience fit, then cost per qualified reader: ask for platform figures (opens, clicks, audience by role and country), label the media kit as the seller's claim, and buy one issue as a test before a package. The price and the decision are the owner's.
7. **Terms.** Who does what by when, the offer used (from `offer.md`), approvals, branding, data handling, how results are shared, and the end date.
8. **Capacity.** Fit the plan to what the business can deliver (onboarding slots, the founder's hours) and to how many partnerships it can run well at once.
9. **Approval.** The plan is a draft. Contacting partners, agreeing deals, paying for sponsorships or sharing any data needs the owner's explicit approval.
10. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no audience sizes, results, offers, partner commitments or quotes that aren't in `context/` or `inputs/`. Count from files with [scripts/tally.py](scripts/tally.py), never by eye. Mark inferences `(assumption)` and list what is needed under Open questions. No benchmark sponsorship rate is evidence.

## Output

Write `work/11-distribution/11-co-marketing-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Co-marketing plan: <business, period>
Skill: 11-co-marketing · Date: <YYYY-MM-DD> · Framework: Co-marketing / partnerships, Dream 100, newsletter sponsorships
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nobody contacted, nothing paid or shared
## Outcome and how each partnership is judged
## Dream 100
| Place | Type | Buyer fit (evidence) | Their figures (claimed / verified) | Decision |
| --- | --- | --- | --- | --- |
## Partnerships
| Partner | Format | What we give | What we get | Data handling | Test and end date |
| --- | --- | --- | --- | --- | --- |
## Sponsorships
## Terms to settle
## Capacity
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

Reply with the file path, the partners chosen and declined with the reason, the first test, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every partner and place is judged on buyer fit with evidence; partner figures are labelled claims.
- [ ] No contact list is swapped or shared without each contact's agreement; joint promotions use each side's own list.
- [ ] Sponsorships are judged on fit and platform figures, tested with one slot, and the cost is the owner's decision.
- [ ] Each deal has a format, terms, an end date and a way to count leads or customers.
- [ ] The plan fits capacity and says nobody is contacted, paid or shared without approval.
- [ ] Privacy and platform facts are dated or *to confirm*.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Borrow audiences that are already your buyers, give each partner something real, keep every person's data where they put it, and count the customers each partnership brings. Co-marketing / partnerships, Dream 100 and Newsletter sponsorships, The Complete Marketing System, section 11 Distribution (Servidad, 2026); Dream 100 from Traffic Secrets (Russell Brunson).
