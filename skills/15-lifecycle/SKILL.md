---
name: 15-lifecycle
description: Plan lifecycle email, SMS and push by customer stage with welcome, post-purchase, replenishment and win-back. Use for lifecycle marketing, retention flows, RFM segments, customer marketing.
metadata:
  section: "15 Retention"
  covers: "Customer marketing; Lifecycle marketing; Push notifications; RFM; Win-back"
---
# Lifecycle marketing

Lifecycle marketing sends the right message at each stage of a customer's life: welcome, first use, repeat, at risk, lapsed, won back. It works when each flow is triggered by a real event or stage, answers what the customer needs then, sells only what the customer is ready for, respects consent per channel, and is judged on retention and revenue per customer against a holdout or baseline. It fails when every customer gets the same broadcast, flows are built because the tool has templates, win-backs lead with discounts by default, or opens are the result. This skill maps the flows; writing each message goes to `10-email-copy`, and acquisition sequences to `12-email-sequences`.

Save the lifecycle plan as a Markdown file in `work/15-retention/` when the required inputs are present and the commercial terms are confirmed. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/awareness.md` → **Journey** (from `03-journey-map`) or `context/customer.md` → **Segments**, from `02-segmentation`: the stages and the customers in them.
- If present, also read `context/offer.md` → Value ladder, Core offer, Price and model, Guarantee; `context/customer.md` → Jobs to be done, Voice of customer; `context/brand.md` → Voice; order and cohort data, current flows, consent by channel and cancellation data in `inputs/`; any work in `work/11-distribution/11-email-channel-*.md`, `11-sms-*.md` or `work/15-retention/`.
- If a required section is missing:
  - **The upstream evidence exists** (tickets, reviews, orders or interviews in `inputs/`): run `03-journey-map` or `02-segmentation` first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Journey → `03-journey-map`; Segments → `02-segmentation`), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Discounts, free gifts, win-back offers and loyalty rewards are the owner's commitments. Use only offers in `offer.md`; if the request asks to build a win-back or lifecycle flow around an unconfirmed discount or reward not in `offer.md` (for example a 40% win-back discount), **stop and withhold the deliverable file** (write nothing to `work/15-retention/`): compute the margin impact from `inputs/` / `offer.md` (e.g. whether the discount turns an order negative-margin), ask the owner to confirm the exact terms before writing the flow, and end the stop reply with the **Principle, framework, source** block.
- If `03-journey-map` is not loaded, stop and say: enable mkt-q1-audience.
- If `02-segmentation` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/lifecycle-guide.md](references/lifecycle-guide.md) for stages and flows, RFM, channel choice, win-back and how to measure with a holdout.

1. **Stages from evidence.** Define the stages (new, active, repeat, at risk, lapsed, won back) with rules the data can apply, and count customers in each from `inputs/` with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py). Include pause, skip, failed-payment, complaint/low-NPS, and product-buildup (too-much-product) signals inside the **at risk** rule with their counts rather than bundling them into healthy active. Where order data allows, segment by RFM (recency, frequency, monetary) and say what each segment needs.
2. **What exists.** List the current flows and messages; note gaps against the stages.
3. **Flows.** For each stage that the evidence says matters: trigger, timing, channel, message purpose, the offer it may use (from the Value ladder and `offer.md`), and the stop rule. Welcome and post-purchase answer the questions customers ask then; replenishment matches real usage; at-risk and win-back address the reason customers left, not a default discount.
4. **Consent per channel.** Email, SMS and push each need the consent the law and the customer gave; transactional messages stay transactional. Push notifications need the app permission and an opt-out. Rules are facts to verify or mark *to confirm*.
5. **Customer marketing.** Where the business has more to offer (the next step on the Value ladder), say who is ready and what signal shows it; expansion programs for B2B accounts go to `15-expansion`.
6. **Measure.** Per flow: retention, repeat orders or revenue per customer compared with a holdout group or the prior period, plus unsubscribes. Opens are not a result.
7. **Approval.** The plan is a draft. Turning on flows, sending messages or creating offers needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no segment sizes, rates, offers, results or quotes that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/15-retention/15-lifecycle-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Lifecycle plan: <business, period>
Skill: 15-lifecycle · Date: <YYYY-MM-DD> · Framework: Lifecycle marketing (stages, RFM, flows, win-back)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; no flow turned on, nothing sent
## Stages and counts
| Stage | Rule | Customers | What they need |
| --- | --- | --- | --- |
## What exists today
## Flows
| Flow | Trigger | Timing | Channel | Purpose | Offer (from offer.md) | Stop rule |
| --- | --- | --- | --- | --- | --- | --- |
## Consent by channel
## Win-back
## How we measure it
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/15-retention/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the stages with counts, the first three flows to build and why, and the win-back approach, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Stages have data rules and counts; RFM is used only where order data allows.
- [ ] Each flow has a trigger, timing, channel, purpose, offer from `offer.md` and stop rule.
- [ ] Win-back addresses why customers left; no default discount; offers not in `offer.md` are *owner to set*.
- [ ] Consent is respected per channel; push needs app permission; rules are dated or *to confirm*.
- [ ] Flows are judged on retention or revenue per customer against a holdout or baseline, not opens; nothing is turned on without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Send each customer what they need at the stage they are in, through a channel they agreed to, and judge every flow against customers who didn't get it. Lifecycle marketing, RFM and win-back, The Complete Marketing System, section 15 Retention (Servidad, 2026); RFM segmentation (direct marketing practice, Hughes).
