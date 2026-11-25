# Upgrade moments: types, value, targeting, honesty

The Fogg Behavior Model says a prompt works when motivation and ability are both present. Motivation to pay is highest right after the user has felt the value. That is a **model** for where to put a prompt, not proof it will convert; the product's own data and tests decide.

## Paywall types

| Type | What is limited | Fits when | Watch |
| --- | --- | --- | --- |
| Soft prompt | Nothing; a dismissable ask | Value is clear and the paid step is a call or service | Frequency; nagging |
| Feature gate | A feature is paid | The paid feature serves the segment that can pay | Gating the feature that creates the habit |
| Usage limit | Volume (projects, seats, exports) | Usage grows with the value the user gets | A limit hit before any value |
| Time limit | Trial end | Value is reached inside the trial | Renewal terms must be stated before the trial starts |

Which features or limits are free is a **pricing** decision (`07-pricing`). The paywall skill proposes it with evidence; the owner decides.

## Value moments

A value moment is the user getting the result they came for: they saw next month's cash, sent the first invoice, finished the first project. Not by default: account created, integration connected, an output generated automatically without the user seeing it, a tutorial completed. Use events that the user causes or sees, and read them by segment.

## Targeting

- Show the paid step to segments that get value and can buy it.
- For a segment that cannot buy, say what honest alternative `offer.md` has (a lighter plan, a free resource, nothing). A user saying what they would pay is stated preference: hand it to `07-pricing`.
- Never re-prompt the same user every session; set a frequency and a stop after a dismiss.

## The prompt

1. What you already have (from their own data where possible).
2. What the paid step adds, in one line.
3. Price and terms exactly as `offer.md` states them (billing, renewal, trial end, cancel).
4. One primary action.
5. A plain dismiss (*Not now*).

## Honesty rules

- Renewal and billing stated before the user commits; no pre-selected annual plan the user did not choose clearly.
- No countdowns, "offer ends" or scarcity that aren't true.
- No shaming dismiss text.
- Never hold the user's own data hostage to force an upgrade.
- Cancel as easily as upgrade. Save offers on cancellation must match a diagnosed reason and never obstruct the cancel.
- A guarantee only in owner-approved wording.

## Metrics

- Primary: the paid step taken by the right segment within a fixed window after the prompt; then paid outcome (upgrade kept, client signed).
- Guardrails: refunds, cancellations, support tickets, free-user retention, wrong-fit calls.
- Attribution: a call or upgrade from inside the product may be recorded under another source in the CRM; do not count it twice or not at all.

## Owners

| Work | Owner |
| --- | --- |
| Price, plans, trial length, free boundary | `07-pricing` |
| The whole free-to-paid engine | `04-plg-audit` |
| Onboarding to first value | `15-onboarding` |
| Final copy | `10-page-copy` |
| Test design | `18-ab-testing` |
