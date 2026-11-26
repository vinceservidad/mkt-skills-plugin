---
name: 16-referral-program
description: Design a referral program with the reward, timing, ask and tracking that turn happy customers into new ones. Use for referral programs, refer-a-friend, word of mouth, referral rewards.
metadata:
  section: "16 Referral and Community"
  covers: "Referral program; Word of mouth"
---
# Referral program

Word of mouth already happens; a referral program makes it easier and more frequent. It works when the ask comes at a moment the customer has just felt the value, the referrer has something easy to send, the reward suits the relationship (and is affordable from margin), referred buyers are qualified the same way as any lead, and referrals are tracked well enough to thank people and count results. It fails when the reward is copied from an app, cash is offered where it would embarrass the referrer, the program is announced once and forgotten, or referred customers who don't fit are rewarded anyway. Paid partners are `11-affiliate-jv`.

Save the referral program design as a Markdown file in `work/16-referral-community/` when the required inputs are present (unless withholding under Owner commitments). Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Core offer**, from `07-offer-design`: what referred customers buy.
- If present, also read `context/customer.md` → Buying triggers and process, ICP and personas, Voice of customer; `context/offer.md` → Price and model, Bonuses (a referral kit), Urgency and scarcity (capacity); `context/message.md` → Proof stack; referral counts and sources, close rates, margin, tenure and client comments in `inputs/`; any work in `work/11-distribution/11-affiliate-jv-*.md` or `work/15-retention/15-nps-feedback-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (sales notes or interviews in `inputs/`): run `07-offer-design` first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Core offer → `07-offer-design`), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Referral rewards (cash, credits, free months, gifts), rewards for the referred friend and any terms are the owner's commitments.
  - When the request asks to build a referral program around an unconfirmed concession to the referred customer not in `offer.md` (e.g., first two months free), **stop and withhold all deliverable files** (write nothing to `work/16-referral-community/`): compute the **gross margin cost explicitly** as `free period × monthly price × gross margin %` (for example, `2 months × $1,450 × 60% = $1,740` in foregone gross margin) plus any service delivery impact, keep capacity in view, ask the owner to confirm the exact terms, and end the stop reply with **Principle, framework, source**.
  - When the request asks to design the overall referral program from `inputs/` (even if the user proposes a candidate referrer reward such as cash), **write the complete referral program file** (`work/16-referral-community/16-referral-program-<YYYY-MM-DD>-<slug>.md`): keep every referrer source count explicit (do not collapse distinct partner/referrer sources into subtotals), cost the proposed reward plus alternatives (none/thank-you, fee credit, gift, donation) as a % of first-year gross margin, label founder margin/tenure figures as owner estimates, note referrer comfort/feedback, leave reward selection as *owner to set*, and mark unverified legal/professions rules *to confirm*.
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/referral-guide.md](references/referral-guide.md) for when to ask, reward types and their cost, the kit, qualification, tracking and legal checks.

1. **Read word of mouth today.** Count referred leads, clients and close rates by referrer type from `inputs/` with [scripts/tally.py](scripts/tally.py), compared with other sources. Note when referrals happen (after which moment) and how they are recorded.
2. **The moment to ask.** Tie the ask to the moment of felt value the evidence shows (a good review, a result, a milestone), not a random email blast.
3. **Reward options and cost.** From margin, price and tenure, compute what a qualified referred customer is worth and what each reward option costs, with the arithmetic shown and labelled. Options include none (a thank-you), a fee credit, a gift, a donation, a two-sided reward and cash. Weigh what the evidence says referrers would feel comfortable with; the owner sets the reward.
4. **The kit.** What the referrer sends: a short description in plain words, the real offer, proof that exists, a link or an intro template. Built from context, not invented claims.
5. **Qualification and capacity.** Referred leads go through the same fit check as any lead; rewards pay only for referred customers who fit and sign (and stay past any stated period). Cap volume to capacity.
6. **Tracking and thanks.** A referral link or code, or a required CRM field; thank every referrer whether or not the lead closes; report referrals, qualified, clients and reward cost.
7. **Legal and platform checks.** Referral rewards can need disclosure and some professions restrict paying for referrals; verify for the country and trade or mark *to confirm*.
8. **Approval.** The design is a draft. Launching the program, promising rewards or contacting clients needs the owner's explicit approval.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no referral counts, rewards, results, quotes or client details that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/16-referral-community/16-referral-program-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Referral program: <business, date>
Skill: 16-referral-program · Date: <YYYY-MM-DD> · Framework: Referral program (word of mouth made easier)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing launched or promised
## Word of mouth today
| Referrer type | Leads | Clients | Close rate | How recorded |
| --- | --- | --- | --- | --- |
## When to ask
## Reward options
| Option | Cost per referred client | Share of first-year margin | Fit with referrers (evidence) |
| --- | --- | --- | --- |
## Referral kit
## Qualification and capacity
## Tracking and thanks
## Legal checks
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/16-referral-community/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, what word of mouth already brings, when to ask, the reward options with cost, and the kit, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Referral results are counted against other sources, with how they are recorded.
- [ ] The ask is tied to an evidenced moment of value.
- [ ] Every reward option is costed from the business's own margin and tenure; referrer comfort is weighed; the owner sets the reward.
- [ ] Referred leads are qualified like any lead; rewards pay only for fitting customers; volume fits capacity.
- [ ] Tracking and thanks are planned; legal checks are dated or *to confirm*; nothing launches without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Ask when customers have just felt the value, give them something easy to send, reward in a way that suits the relationship and the margin, and thank everyone who refers. Referral program and Word of mouth, The Complete Marketing System, section 16 Referral and Community (Servidad, 2026); The Referral Engine (John Jantsch).
