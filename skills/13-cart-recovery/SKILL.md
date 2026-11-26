---
name: 13-cart-recovery
description: Write the cart and checkout recovery sequence with an escalating reason to return. Use for abandoned cart emails or SMS, checkout recovery. Not for fixing the checkout (13-checkout).
metadata:
  section: "13 Conversion"
  covers: "Cart abandonment recovery"
---
# Cart recovery

Someone who left a cart or checkout was close to buying. A recovery sequence brings them back by solving the reason they left: a question, a doubt, a surprise cost, or simply being interrupted. It escalates the reason to return (help, then the answer to the top objection with proof, then the risk taken away), not the discount. It messages only people who may be messaged, stops the moment they buy, and is judged by the orders it adds, not the orders it touches. It changes nothing live.

Save the sequence as a Markdown file in `work/13-conversion/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **Beliefs, objections and drivers**, from `02-buyer-psychology`: why buyers hesitate.

A section counts only when its `Status:` line says drafted or confirmed and it has content under it. A file that exists with `Status: empty` (the installer's template) is missing. Check this first, before asking for page or other material: a missing upstream section is a stop, not a baseline.

If present, also read:
- `context/offer.md` → **Guarantee**, from `07-guarantee-risk-reversal`; Price and model (any incentive stance), Core offer (what exists and what is proposed), Bonuses;
- `context/message.md` → Objection map, Proof stack; `context/brand.md` → Voice;
- evidence of why people leave and how the current recovery performs (exit polls, tickets, the current messages, sent and recovered counts, consent records), in `inputs/` or pasted.

If Beliefs, objections and drivers is missing: stop. Name the section and `02-buyer-psychology`, and say what to bring (reviews, tickets, exit-poll answers or sales notes that show why people hesitate). A stop reply still ends with the **Principle, framework, source** block.

Price, discounts and guarantees are the owner's commitments. A discount or guarantee appears in a message only if `offer.md` holds it with the owner's approval; never generate one.
- If `02-buyer-psychology` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/recovery-sequence.md](references/recovery-sequence.md) for timing, the escalation ladder, eligibility and the measurement rules.

1. **Diagnose before writing.** Why do people leave? Use exit polls (count with [scripts/tally.py](scripts/tally.py) or the source's own counts, and say how many answered of how many asked), tickets and Beliefs, objections and drivers. A reason caused by the checkout (a cost shown late, a forced account) is fixed in the checkout first: hand it to `13-checkout` and say the emails cannot fix it.
2. **Read the current recovery, if any.** Rate sent, opened or clicked, and attributed orders with [scripts/funnel.py](scripts/funnel.py) or a shown calculation, and name the attribution rule. Attributed orders are not incremental orders: some would have come back anyway. Without a holdout, the true lift is unknown; say so.
3. **Eligibility and consent.** Who may receive each message: an abandoned checkout with an email, minus anyone who bought, unsubscribed or is already a subscriber. Whether a recovery email needs marketing consent where the buyers live is a legal question: mark it *to check with counsel*, and design so it works for both answers (for example, send only to people who opted in until counsel confirms). SMS goes only to people with recorded SMS consent; a phone number collected for shipping is not consent.
4. **Write the sequence: one reason per message, escalating.**
   - **About 1 hour:** a reminder and help. What they left, what happens after ordering, a way to ask a question.
   - **About 24 hours:** the top evidenced objection answered with real proof and true terms.
   - **About 72 hours:** the risk taken away (the approved guarantee, or the real cancel and skip terms), and a plain last note.
   The timings are the framework's starting point, a heuristic to test, not a proven rule. Each message: subject, preview, body, one call to action back to the cart, sender. Copy in the brand voice.
5. **Incentives.** No discount by default. If `offer.md` holds an approved incentive, use it once, last, and say what it costs. If a live discount contradicts `offer.md`, lay out the options for the owner rather than keeping or dropping it yourself.
6. **Stop rules.** Stop immediately on purchase, unsubscribe or reply; no more than the planned messages per abandoned checkout; suppress repeat abandoners within a stated window.
7. **Measure.** Primary: incremental orders (or revenue and margin) per abandoned checkout, against a holdout that receives nothing. Report attributed recoveries as a secondary number with their rule. Guardrails: unsubscribes, spam complaints, discount cost, cancellations or refunds after recovered orders. Hand test design to `18-ab-testing`; platform setup is the owner's job.
8. **Authorization.** Switching the sequence on, changing who receives it, or offering any incentive needs the owner's approval, and counsel where consent is unclear.
9. **Check before saving.** Re-read the draft against the Checks, run `scripts/check_quotes.py`, and fix any failure.

**Nothing the context doesn't support.** Write no discounts, deadlines (*your cart expires*), stock levels, terms, guarantees, results or customer numbers that aren't in `context/` or `inputs/`. Proposed offer elements (a one-step cancel not yet built, an automatic refund rule) are not promised. Mark inferences `(assumption)` and list what is needed under Open questions.

**Platform facts.** Do not state how an email or SMS tool, store platform or mailbox provider currently works (triggers, attribution windows, sender requirements) unless you cite its own documentation as `(first-party: <URL>, checked YYYY-MM-DD)`. Otherwise mark it *to verify*.

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from a source, with the source and date (a review used in a message must be verbatim and permitted). Your subject lines and email copy go in italics or plain text, never in quotation marks. Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py <file>`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches.

## Output

Write `work/13-conversion/13-cart-recovery-<YYYY-MM-DD>-cart-recovery.md`:

```markdown
# Cart recovery sequence: <store or offer> (<date>)
Skill: 13-cart-recovery · Framework: Cart recovery sequence (1 hour, 24 hours, 72 hours, escalating reason to return)
Built from: <context sections and inputs used, with status and dates>
## Why buyers leave (evidence)
## The current recovery (if any): numbers and problems
## Fix in the checkout first (hand to 13-checkout)
## Who receives it, and consent
## The sequence
| # | Timing | Channel | Reason to return | Objection and proof (source) | Stop rules |
| --- | --- | --- | --- | --- | --- |
### Message 1
Subject: … · Preview: … · Body: … · Call to action: …
### Message 2
### Message 3
## Incentives (owner decision)
## Measurement
## Claims and sources
| Claim or number | Source or calculation |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/` and nothing live.

Reply with the file path, the reason each message escalates, anything the owner or counsel must decide (consent, incentives), and how to read whether it works.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Why buyers leave is diagnosed from evidence first, and checkout-caused reasons are handed to `13-checkout`.
- [ ] Each message carries one escalating reason to return drawn from an evidenced objection, with real proof and true terms; no discount by default and no invented deadline or guarantee.
- [ ] Eligibility, suppression and stop rules are stated; consent questions are marked *to check with counsel*, and SMS goes only to people with SMS consent.
- [ ] Attributed recoveries are kept apart from incremental orders, and a holdout is proposed when none exists.
- [ ] A live discount that contradicts `offer.md` is laid out as an owner decision; switching the sequence on needs the owner's approval.
- [ ] No current platform behaviour is asserted without a first-party citation and date.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Bring back the buyer who almost bought by solving the reason they left, escalating help and reassurance rather than discounts, messaging only those who may be messaged, and counting only the orders the sequence truly adds. Cart recovery sequence; Fogg Behavior Model (BJ Fogg, Tiny Habits, 2019); The Complete Marketing System, section 13 Conversion (Servidad, 2026).
