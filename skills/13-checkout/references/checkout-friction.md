# Checkout friction: fields, surprises, accounts and payment

Checkout optimisation is a **tactic** set inside a conversion strategy. The rules below are **heuristics** from usability practice (Krug; the Fogg Behavior Model's point that ability is easier to raise than motivation). They tell you what to test first. They are not proof that a change will lift orders for this store; only its own test or before-and-after data with a stated window can show that.

## The field test

For every field, answer four questions:

| Question | If no |
| --- | --- |
| Does fulfilment, payment or the law need it now? | Not required at checkout |
| Does a named person use it for a named decision? | Remove, or make optional |
| Is it needed before payment, or could it come after (on the confirmation page or in the first email)? | Move after purchase |
| Are we sure? | Mark *to check with <shipping team / payment provider / counsel>* |

Common fields that fail the test: confirm-password, company name, phone with no stated use, "how did you hear about us" as a required field, birthdays, a second address line shown as required. Keep a field the business genuinely relies on; say what it costs.

## Surprises that stop buyers

| Surprise | What to show, and where |
| --- | --- |
| Shipping, tax or fees appear only at the payment step | The full price on the product page and the cart, before checkout starts |
| A free-shipping claim that applies to only some orders | The exact condition next to the claim |
| Subscription renewal not stated | Price, frequency and renewal next to the pay button |
| Skip, pause, cancel unclear | How to do each, in the words of what exists today, next to the pay button |
| A guarantee mentioned but undefined | The approved terms, or nothing. A guarantee the owner has not approved is not shown |
| What happens after paying | When it ships or starts, and what the buyer receives |

Never show a proposed term (one-step cancel not yet built, automatic refunds not yet live) as if it were live.

## Accounts

- Forced account creation before payment is a common reason buyers give for leaving. Options to test: guest checkout; account created from the confirmation (set a password later); sign-in by email link. Which of these the store supports is a platform question: mark *unverified* until checked in the platform's own documentation.
- A subscription needs a way for the buyer to manage it (skip, pause, cancel). Whatever replaces the forced account must keep that, or the cancellation promise breaks.

## Payment methods

- List what is live today.
- Add a method only from evidence: buyers asking for it (polls, tickets), the device mix (more mobile buyers), the market.
- Whether a wallet or provider is available on a platform, in a country, or for subscriptions is a current platform fact. Cite the platform's or provider's own documentation as `(first-party: <URL>, checked YYYY-MM-DD)` or mark it *to verify*.

## Progress and mobile

- A progress indicator that names the steps.
- Numeric keyboards for numbers, autofill for addresses, errors shown next to the field, a single column on phones.
- Read the device split: if phones lose far more buyers at one step, test that step on phones first.

## Reading the numbers

- Rate each step from the previous step and from checkout started, with numerators and denominators.
- Compare devices and new versus returning visitors; returning visitors may already have accounts, which hides an account-step problem in the blended rate.
- Exit-poll answers are stated reasons from those who answered (say how many answered of how many shown). They point to tests; they are not measured shares of all abandoners.

## Guardrails for every checkout test

Orders per checkout started (primary), by device; refunds; cancellations before the second order for subscriptions; support tickets about charges or terms; average order value; any fraud or failed-payment change.

## Owners

| Work | Owner |
| --- | --- |
| Order bumps, upsells | `12-upsell-path` |
| Recovery emails and SMS | `13-cart-recovery` |
| Page copy and microcopy | `10-page-copy` |
| Prices, shipping charges as a pricing decision | `07-pricing` |
| Guarantee terms | `07-guarantee-risk-reversal` |
| Test design | `18-ab-testing` |
