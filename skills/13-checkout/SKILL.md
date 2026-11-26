---
name: 13-checkout
description: Optimize checkout fields, guest checkout, payments and order bumps. Use for checkout drop-off, checkout UX, payment step. Not for shipping prices (07-pricing) or recovery emails (13-cart-recovery).
metadata:
  section: "13 Conversion"
  covers: "Checkout optimization"
---
# Checkout

The checkout is where a decided buyer either pays or leaves. Most losses here are friction and surprise, not lack of desire: a forced account, fields nobody uses, a shipping cost that appears at the last step, terms the buyer can't find, a payment method they don't have. This skill maps the checkout step by step from evidence, cuts what doesn't need to be there, shows what the buyer needs to know before paying, and ranks the changes as tests. It changes nothing live.

Save the plan as a Markdown file in `work/13-conversion/` when the checkout material is present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Nothing upstream is required. If present, read:
- `context/offer.md` → Price and model (`07-pricing`): prices, shipping, renewal terms; Guarantee (`07-guarantee-risk-reversal`); Core offer (what exists and what is only proposed); Value ladder;
- `context/customer.md` → Beliefs, objections and drivers (`02-buyer-psychology`);
- `context/message.md` → Objection map.

The checkout material, in `inputs/`, elsewhere in the project, or pasted by the user. Any of these counts:
- a walk-through of the checkout as it is (steps, every field and whether it is required, payment methods, when shipping, tax and fees appear, what terms are shown), with the date it was checked and the devices;
- a step-by-step export (cart, checkout started, each step, orders) with definitions and dates, ideally by device and new or returning;
- exit polls, support tickets, recordings, past test results.

If there is no checkout material, do not audit an imagined checkout. Write the plan described under Output and ask for the material. Never state a "typical" abandonment rate or benchmark from memory.

## Process

Use [references/checkout-friction.md](references/checkout-friction.md) for the field test, the surprise list and the payment and account rules.

1. **Map the checkout as it is,** step by step, from the walk-through: every field, whether it is required, who uses it and for what. Copy the step definitions from the export.
2. **Read the numbers.** Sum and rate every step with [scripts/funnel.py](scripts/funnel.py) (`python3 <this skill's folder>/scripts/funnel.py <export.csv> <column> ...`), never by eye, overall and by device and visitor type. Name the step that loses the most buyers, for whom, with counts. Count poll answers with [scripts/tally.py](scripts/tally.py) or copy the source's own counts, and treat them as stated reasons from the people who answered, not measured causes.
3. **Test every field.** Keep it only if fulfilment, payment, the law or a named downstream decision needs it now. Otherwise make it optional, move it after purchase, or remove it. Where you are not sure whether a field is legally or operationally needed (a phone number for the carrier, a tax field), mark it *to check with <who>*; do not assert the law.
4. **Remove surprises.** The full price, including shipping, tax and fees, is visible before the checkout starts. For a subscription, the renewal, how to skip, pause and cancel, and any guarantee are stated next to the pay button, using only terms that exist today. Proposed terms (a one-step cancel, an automatic refund, a guarantee the owner has not approved) are held and listed under Open questions, never shown as live.
5. **Account.** Prefer guest checkout, or an account created after payment from the confirmation, when the product allows it. For a subscription the buyer needs a way to manage it; say how that would work and mark the store's capability *unverified* until checked.
6. **Payment options.** List what is live. Recommend adding a method only from evidence (polls, tickets, the device mix), and never state which wallets or providers a platform supports, or whether they work with subscriptions, unless you cite the platform's own documentation as `(first-party: <URL>, checked YYYY-MM-DD)`. Otherwise mark it *to verify in the platform's documentation*.
7. **Progress and mobile.** A visible progress indicator, the right keyboard for each field, autofill, and error messages next to the field. These are usability heuristics, labelled as such, not proven lifts.
8. **Order bump.** Note only whether a bump belongs in this checkout and where; its design, offer and price go to `12-upsell-path`, using real offers only. Never pre-checked.
9. **Rank the changes as tests.** Defects and surprises first (a cost shown late, an unused required field), then friction, then additions. Each test gets a metric (orders per checkout started, by device), guardrails (refunds, cancellations before the second order, support tickets, order value), a window and a stopping rule. Hand test design to `18-ab-testing`, page copy to `10-page-copy`, and recovery messages to `13-cart-recovery`.
10. **Authorization.** Every live change to the checkout, prices, payment methods or terms needs the owner's approval and a check afterwards against the baseline.
11. **Check before saving.** Re-read the draft against the Checks, run `scripts/check_quotes.py`, and fix any failure.

**Nothing the context doesn't support.** Write no prices, fees, terms, guarantees, offers, payment methods or delivery promises that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. No dark patterns: no pre-checked boxes, hidden renewals, fake timers, or confirmshaming.

**Labels.** Every number is copied from a named export or note (with its date), *calculated* (show numerator and denominator), or marked `(assumption)`.

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from a source, with the source ID. Your proposed field labels and microcopy go in italics. Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py <file>`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches.

## Output

**With checkout material**, write `work/13-conversion/13-checkout-<YYYY-MM-DD>-checkout.md`:

```markdown
# Checkout plan: <store or offer> (<date>)
Skill: 13-checkout · Framework: Checkout optimization; Fogg Behavior Model (ability before motivation)
Built from: <walk-through, exports, polls and context sections used, with dates and status>
## The checkout today, step by step
## Where buyers leave
| Step | Count | Rate (calculation) | By device / visitor | Reading |
| --- | --- | --- | --- | --- |
## Field by field
| Step | Field | Required now? | Who uses it, for what | Keep / optional / after purchase / remove / to check |
| --- | --- | --- | --- | --- |
## Surprises to remove (price, fees, terms)
## Account and payment
## Progress and mobile
## Ranked tests (owner approval needed for live changes)
| Rank | Change | Why (evidence) | Metric, guardrails, window, stopping rule | Owner |
| --- | --- | --- | --- | --- |
## Claims and sources
| Claim or number | Source or calculation |
| --- | --- |
## Open questions
## Principle, framework, source
```

**Without checkout material**, write `work/13-conversion/13-checkout-<YYYY-MM-DD>-plan.md`: the walk-through to record (each step, every field and whether it is required, payment methods, when each cost appears, which terms are shown), the step events to export with definitions, the device and visitor splits, an exit poll to run, and how each will be read. State no rate or benchmark.

Change nothing in `context/` and nothing live.

Reply, with material, with the file path, the step that loses the most buyers (with counts), the first change to test and why, and a reminder that live changes need the owner's approval. Reply, without material, with the plan's path and a plain list of what to bring and how (save it in `inputs/` or paste it, then ask again).

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every step's count and rate comes from `funnel.py` or a shown calculation, keeps its definition and period, and is split by device or visitor type where the data allows. No benchmark is stated.
- [ ] Every field has a reason to stay, or is made optional, moved after purchase, removed, or marked *to check* with a named person; no law is asserted.
- [ ] The full price and the subscription or renewal terms are shown before payment, using only terms that exist; proposed terms and unapproved guarantees are held.
- [ ] No platform or payment-provider capability is asserted without a first-party citation and date.
- [ ] Order bumps are handed to `12-upsell-path`; nothing is pre-checked and no dark pattern is proposed.
- [ ] Changes are ranked as tests with metric, guardrails, window, stopping rule and owner; no live change is made or implied as done.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

A buyer at checkout has already decided; every extra field, forced account, late cost or hidden term is a reason to stop, so raise ability before adding persuasion, and test each change against orders, not clicks. Checkout optimization; Fogg Behavior Model (BJ Fogg, Tiny Habits, 2019); Don't Make Me Think (Steve Krug); The Complete Marketing System, section 13 Conversion (Servidad, 2026).
