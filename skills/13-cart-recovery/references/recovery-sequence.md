# Recovery sequence: timing, escalation, eligibility, measurement

The cart recovery sequence (messages at about 1 hour, 24 hours and 72 hours, each with an escalating reason to return) is a **framework** from the system map. Its timings are a **heuristic** starting point, not a proven rule: test them against the store's own data. Nothing here is a benchmark for recovery rates.

## Diagnose first

| Reason buyers give | Where it is fixed |
| --- | --- |
| A cost appeared late (shipping, fees) | Checkout (`13-checkout`): show it earlier. An email cannot undo the surprise |
| Forced account, too many fields | Checkout |
| Didn't know how to cancel, skip or what happens next | Checkout terms first; the emails can explain the true terms |
| Not sure which product or option | Emails: help choosing, with real guidance |
| Doubt it is worth the price | Emails: proof from the Proof stack; risk reversal if approved |
| Just looking, interrupted | Message 1 reminder |

Exit-poll answers are stated reasons from those who answered; say how many answered of how many were asked.

## Escalation ladder

| Message | Reason to return | Content |
| --- | --- | --- |
| 1 (about 1 hour) | Help | What they left; what happens after ordering; a way to ask a question; no pressure |
| 2 (about 24 hours) | Answer the top objection | The evidenced objection, answered with real proof and true terms |
| 3 (about 72 hours) | Take the risk away | The approved guarantee, or the real cancel and skip terms; a plain last note |

The reason escalates; the discount does not. An incentive appears only if `offer.md` holds an approved one, once, last, with its cost stated.

## Eligibility and consent

- Eligible: an abandoned checkout with an email address, no purchase since, not unsubscribed, not already an active customer for this product.
- Whether a recovery message counts as marketing and needs consent depends on the market and the message: mark *to check with counsel*. Until confirmed, a safe design sends only to people who opted in, or sends a plain service-style reminder without promotional content (counsel to confirm which is allowed).
- SMS: only to people with recorded SMS consent. A phone number collected for delivery is not consent.
- Never message after a purchase, an unsubscribe or a reply asking to stop.

## Stop rules

Stop on purchase, unsubscribe or reply. Cap messages per abandoned checkout. Suppress people who abandoned and were messaged recently (state the window).

## Measurement

- **Recovery rate:** recovered eligible checkouts ÷ eligible abandoned checkouts, with the recovery window and attribution rule named.
- **Attributed is not incremental.** A tool that credits any order within N days of an open counts buyers who would have returned anyway. Only a holdout (a random share of eligible abandoners who get nothing) shows what the sequence adds: incremental orders = treated recovery rate minus holdout recovery rate, times the treated group size.
- **Guardrails:** unsubscribes, spam complaints, discount cost, refunds and cancellations after recovered orders, and for subscriptions, second-order retention of recovered buyers.
- Do not compare with "typical" recovery rates.

## Words not to use

*Your cart expires*, *items selling fast*, *last chance* — unless true. No shaming (*Did you forget about yourself?*). No fake personal notes from someone who did not write them.
