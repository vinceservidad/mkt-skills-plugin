# Sign-up flow: fields, first value and the Fogg diagnosis

The Fogg Behavior Model (B = MAP: behaviour happens when motivation, ability and a prompt are present at the same moment) is a **model** for diagnosing why people stop. It does not prove that a change will raise completions; only this flow's own data or a test can show that. Rules below are **heuristics** for what to test first.

## Boundary

- **Start:** the click on *sign up* or *start free*.
- **End:** first meaningful value, the first moment the user gets the result they came for.
- In between: account creation, verification, connection or import, first setup choices.
- After first value, habit and onboarding belong to `15-onboarding`; the paid step belongs to `13-paywalls`.

## First meaningful value

A candidate must be something the user experiences as the result (they saw next month's cash, sent the first invoice, booked the first class). Not, by default:
- account created;
- integration connected;
- a report or forecast generated automatically without the user doing or seeing anything;
- a tutorial, checklist or welcome email completed or opened.

Fix the denominator (all sign-ups, or the right segment's sign-ups) and the window (within 7 days, within the first month) before reading the rate. State the evidence strength: user feedback that names the moment, return or payment rates of users who reached it versus not, or untested.

## Fogg diagnosis by step

| Signal | Likely factor | First test |
| --- | --- | --- |
| Errors, retries, a step failing for some users | Ability (defect) | Fix it; read before and after the fix date separately |
| Many fields, unclear labels, verification delays | Ability (effort) | Remove or defer fields; clearer step |
| Drop concentrated in a segment the paid step can't serve | Motivation (wrong fit) | Qualification or source change, not a shorter form |
| Users stop and never return | Prompt | A reminder tied to the next step, sent once, with an exit |
| Users finish setup but never see value | Ability or product | Make the value visible; check the product works |

Raise ability before motivation: removing a step usually beats adding persuasion.

## Field test

| Question | If no |
| --- | --- |
| Does delivering the value need it now? | Defer it |
| Does the business use it to qualify or route the user (for example a size band that decides who is offered a call)? | Remove, unless it qualifies |
| Could it come after first value (progressive profiling)? | Ask later |
| Does anyone use it? | Remove |

When the owner wants more qualifying questions: list what each new question would decide, check whether the flow already captures it, and test it on a share of traffic with a guardrail on completions from the right segment. A question that rejects wrong-fit users can be worth its cost; say so with evidence.

## Social login, verification, connections

- Social login and magic links reduce typing; email verification can delay value. Which options a given platform or provider supports, and how, is a current platform fact: cite first-party documentation with a date, or mark *unverified*.
- A connection to another app that fails for some users is a defect. Count the failures, note any fix date, and separate cohorts before and after.

## Reading the numbers

- Read by segment and by cohort; a blended rate hides a segment that never converts.
- Exclude or flag cohorts too young to have reached a later step.
- Small counts (single digits) cannot rank one segment above another.
- Do not compare with "typical" sign-up or activation rates.
