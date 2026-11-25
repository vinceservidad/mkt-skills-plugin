# Popup rules: triggers, frequency, mobile, consent, what not to do

The Fogg Behavior Model says a prompt works only when motivation and ability are already present. A popup is a prompt. The rules here are **heuristics** for designing one; they are not proof that a popup will add customers. Only the site's own numbers, read downstream and ideally against a holdout, can show that.

## Offer by visitor

| Visitor | Page | Offer that fits |
| --- | --- | --- |
| Cold, reading content | Blog, guides | The free step in the value ladder (a checklist, template, guide), if it exists |
| Considering | Product, pricing | Help to decide: a sample, a first step, answers to the top objection, a consult |
| Leaving with something in the cart | Cart | Usually nothing; the recovery email (`13-cart-recovery`) handles it |
| Existing subscriber or customer | Any | No popup |

If the right offer does not exist yet, the popup waits or uses the nearest real one, and the gap goes to `12-lead-magnet` or `07-value-ladder`.

## Discounts

A discount popup trains visitors to wait for a code and can bring buyers who leave once the price returns. Use one only if `offer.md` holds an approved incentive. If a live discount popup contradicts `offer.md`, present the evidence and options (keep, remove, replace with the free step, test against a holdout) and leave the decision to the owner. Downstream comparisons between code users and others are observational: code users chose the code.

## Triggers

| Trigger | Use when |
| --- | --- |
| Click (the visitor asks for it) | Always the least intrusive; links in content |
| Scroll depth | The visitor has read enough to know the content is useful |
| Time on page | Only long enough to have read something; never on landing |
| Exit intent | Desktop only in practice; one last relevant offer |

Never fire on arrival before any content is visible. Never on checkout or account pages.

## Frequency and suppression

- Once per visitor per period (state the period), and never again after a sign-up or a close for that period.
- Suppress for subscribers, customers and anyone who arrived from an email.
- One popup per page view at most.

## Mobile

Prefer a small slide-in or a bottom banner that leaves the content readable. A full-screen cover on phones blocks the page. How search engines treat intrusive interstitials is a current platform fact: cite the search engine's own documentation with a date, or mark it *to check*.

## Consent

- Say what the visitor gets and what they will receive by email.
- Marketing opt-in boxes are unticked.
- Consent wording and record-keeping differ by market: mark *to check with counsel*.

## Dark patterns to avoid

Confirmshaming close text (*No thanks, I like paying full price*), hidden or tiny close buttons, fake countdowns, invented stock or demand, pre-ticked boxes, popups that reappear on every page, and "spin to win" games with invented odds.

## Metrics

- Supporting: sign-ups per view.
- Primary: the downstream outcome per 1,000 views (first orders, second orders, qualified leads), so a popup that adds sign-ups but no customers is visible.
- Guardrails: exit or bounce rate on the pages it shows on, unsubscribes and complaints from popup sign-ups, discount cost.
- A holdout (a share of visitors who never see it) is the cleanest read of what the popup adds.
