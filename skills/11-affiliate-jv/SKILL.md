---
name: 11-affiliate-jv
description: Design affiliate and joint-venture programs that pay on performance. Use for affiliate programs, commission structure, JV partners, partner launches, referral partners.
metadata:
  section: "11 Distribution"
  covers: "Affiliate marketing; JV launches"
---
# Affiliate and JV

Affiliate and JV programs pay partners only when they bring a sale. That makes them look free, and it is why they go wrong: a commission set from what partners ask for rather than from margin, a payable sale defined as any sign-up rather than a qualified customer who stays, coupon and cashback sites credited for buyers who were already buying, and partners bidding on the brand. The plan's job is to recruit partners whose audiences are the buyer, pay a share the economics can carry on the outcome the business is actually paid for, and track it well enough to know who brought whom.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present (unless stopping under Owner commitments). Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Core offer**, from `07-offer-design`: what partners promote.
- `context/offer.md` → **Price and model**, from `07-pricing`: what a sale is worth, the base of every commission.
- If present, also read `context/offer.md` → Guarantee (refund exposure), Urgency and scarcity (capacity), Value ladder, Bonuses; `context/customer.md` → ICP and personas (whose audience counts), Segments, Buying triggers and process (how referrals close); `context/awareness.md` → Traffic temperature; `context/message.md` → Promise, Proof stack; margin, retention, partner, referral-source and capacity notes in `inputs/`; any work in `work/11-distribution/11-influencer-*.md`, `work/11-distribution/11-channel-selection-*.md` or `work/12-funnel/12-launch-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (a price list or pricing notes in `inputs/` but no Price and model): run the skill that fills it first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Core offer → `07-offer-design`; Price and model → `07-pricing`), and ask for the evidence (price list, margin, retention), not a guess. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** The commission rate or JV split, payout timing, bonuses for partners, discounts or codes for partners' audiences, launch dates and capacity are the owner's commitments. When evaluating whether to start a program from `inputs/` on existing offers, the plan proposes a range from the economics and leaves the rate to the owner. If the request asks to launch or plan around a partner discount, code, commission commitment or launch date that `offer.md` and `inputs/` don't hold, stop, show how any asked rate compares with margin (or ask if margin is unaudited/unknown), ask the owner to confirm each exact term — discount buyer eligibility (which buyers or audiences qualify, e.g. new clients only, referred listeners only, or all buyers), which plans or fee bands are covered, end date, who bears the cost; start date; and monthly capacity — before planning, invent no clawback, cap or other terms, and write no deliverable file in `work/11-distribution/` (a stop reply still ends with the **Principle, framework, source** block).
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.
- If `07-pricing` is not loaded, stop and say: enable mkt-q2-offer.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/affiliate-jv-guide.md](references/affiliate-jv-guide.md) for the economics, partner types, tracking, fraud screens and terms.

1. **The payable outcome.** Define the sale that earns a commission: the business outcome (a client who signs, a subscriber past the refund window or the second box), the qualification rule (the ICP, not disqualified segments), and the clawback (refunds, cancellations within a stated period). Clicks, leads and sign-ups are never payable on their own unless the owner chooses to.
2. **Economics.** From price, gross margin and retention in context or `inputs/`, compute the value of one payable sale (first-year revenue, gross margin, payback) and the commission range it can carry, with the arithmetic shown and each figure labelled *observed*, *owner's estimate* or *calculated*. Evaluate any partner's ask against it (what share of first-year margin it is). Unknown margin means the commission is *to set by the owner*: write the formula, not a number. Never use a "typical" commission rate as evidence.
3. **Read what referral data exists.** Count referred leads and clients by source from `inputs/` with [scripts/sum_by.py](scripts/sum_by.py) or by exact count, never by eye. Note how sources are recorded today (a CRM field, no links) and what that can't show.
4. **Partners.** List candidates by type (customers, complementary service providers, communities and coaches, content creators, newsletters, coupon or cashback sites, networks) and judge each on audience fit to the ICP and its disqualifiers, with the evidence and its source. A partner's own audience figure is their claim. Partners whose audience is mostly a disqualified segment get qualification rules or a no. Customer referral (existing clients sending friends) is `16-referral-program`; individual creators' deals are `11-influencer`.
5. **Structure.** Affiliate (ongoing, per sale) or JV (a partner promotes a launch or offer to their list for a split). Per partner type: commission or split, the payable event, cookie or attribution window, payout timing, caps tied to capacity, and whether different partner types earn different rates (content and introductions vs coupon interception).
6. **Tracking and policy.** Unique links or codes per partner, how a referral is recorded in the CRM, last-click limits, brand-bidding policy (partners do not bid on the brand unless the owner allows it), coupon-site rules, fraud screens (self-referrals, sudden spikes, cookie stuffing). Tracking gaps go to `17-tracking-plan`; whether the program adds sales the business wouldn't have had goes to `17-incrementality`.
7. **Partner kit and terms.** What partners get (approved description, the real offer, proof that exists, disclosure wording) and the terms to settle in writing: payable event, rate, window, clawback, payment timing, brand and claims rules, disclosure, termination. Regulated partners (accountants, lawyers, financial advisers, health professionals) may be restricted in taking referral fees, and disclosure rules for affiliate links vary by jurisdiction: verify in current official guidance or with qualified advice, or mark *to confirm*. Flag the agreement for legal review.
8. **Capacity and launch.** Cap partner volume to what the business can deliver (onboarding slots, stock). For a JV launch, the dates and offer come from `12-launch` and the owner.
9. **Platform facts.** Affiliate-network features, fees and tracking methods change; cite current official documentation with URL and date, or mark *to confirm*.
10. **Approval.** The plan is a draft. Agreeing a rate with any partner, paying anyone, creating codes or links, or announcing a program needs the owner's explicit approval.
11. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, discounts, partner audiences, offers or features that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Describe each source only as it reads. Competitor or industry commission claims need a dated source or are left out.

## Output

Write `work/11-distribution/11-affiliate-jv-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Partner program: <business, period>
Skill: 11-affiliate-jv · Date: <YYYY-MM-DD> · Framework: Affiliate and JV (pay on performance)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; no rate agreed, nothing paid or announced
## The payable outcome
## Economics
| Figure | Value | Label (observed / owner's estimate / calculated) | Source |
| --- | --- | --- | --- |
## Referral sources today
## Partners
| Partner | Type | Audience fit (evidence) | Their ask | Decision and conditions |
| --- | --- | --- | --- | --- |
## Structure
| Partner type | Commission or split (owner to set) | Payable event | Window | Clawback | Cap |
| --- | --- | --- | --- | --- | --- |
## Tracking, attribution and policy
## Partner kit
## Terms to settle and legal checks
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (an email, the owner's notes, a review), with the source named. Write your own terms, kit lines and proposals in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the payable outcome, the commission range and how it was derived, the partner decisions, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The payable outcome is a qualified business outcome with a clawback, not a click, lead or sign-up by default.
- [ ] The commission range comes from the business's own price, margin and retention with the arithmetic shown and labelled; any partner's ask is judged against it; no benchmark rate; the final rate is left to the owner.
- [ ] Partners are judged on audience fit to the ICP; a partner's audience figure is labelled their claim; disqualified-segment audiences get conditions or a no.
- [ ] Tracking, brand-bidding, coupon and fraud rules are set; last-click credit is not called incrementality.
- [ ] Regulated-partner fees, disclosure and the agreement are flagged to verify or for legal review; capacity caps partner volume.
- [ ] The plan says no rate is agreed and nothing paid, created or announced without the owner's approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Pay partners for the outcome the business is paid for, at a share its margin can carry, and only for buyers who fit: borrow audiences that are already your customers, and track well enough to know who brought whom. Affiliate and JV launches (pay on performance), The Complete Marketing System, section 11 Distribution (Servidad, 2026); Dream 100 from Traffic Secrets (Russell Brunson); Launch (Jeff Walker) for JV launches.
