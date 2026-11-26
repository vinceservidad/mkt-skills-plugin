---
name: 15-onboarding
description: Onboard customers to first value and adjust first-box or week-one steps without cutting essentials. Use for onboarding, activation, aha moment, first-week setup, trimming onboarding steps.
metadata:
  section: "15 Retention"
  covers: "Activation / aha moment; Activation path-to-value audit; Onboarding"
---
# Onboarding

Onboarding is the path from paying to the first result the customer bought. It works when activation is defined as that first meaningful value (not a click the tool can track), the steps to reach it are as few as the result allows, each common question is answered before it is asked, and the plan is judged on how many customers reach the first result and stay. It fails when activation is an email open or a tutorial completed, onboarding tours features, necessary setup is cut to look faster, or the real cause of early loss (fit, the product, delivery) is blamed on onboarding.

Save the onboarding plan as a Markdown file in `work/15-retention/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Dream outcome**, from `07-offer-design`: the result the customer bought.
- `context/customer.md` → **Jobs to be done**, from `02-jobs-to-be-done`: the job and the first moment it is done.
- If present, also read `context/offer.md` → Core offer, Guarantee; `context/customer.md` → Pains, desires and fears, Voice of customer, ICP and personas; `context/awareness.md` → Journey; cohort data, tickets, first-order timelines and current onboarding steps in `inputs/`; any work in `work/04-product/` or `work/15-retention/15-churn-prevention-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (tickets, reviews or interviews in `inputs/`): run the skill that fills the missing section (`07-offer-design` or `02-jobs-to-be-done`) first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Dream outcome → `07-offer-design`; Jobs to be done → `02-jobs-to-be-done`), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.
- If `02-jobs-to-be-done` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/onboarding-guide.md](references/onboarding-guide.md) for defining activation, the path to first value, the first-week plan and what to measure, and [references/activation-path-and-friction.md](references/activation-path-and-friction.md) for cohort retention validation of activation events, classifying essential setup vs. unnecessary friction, and equal-window activation experiments.

1. **Define activation.** The first meaningful value in the customer's terms (from Dream outcome and Jobs), with a time window and a denominator (new customers in the period). Reject tracking-convenience definitions such as an email open, a login or a tutorial completed, and say why. If the value can't be observed directly, name the closest true proxy and label it.
2. **Map the path.** Every step from payment to activation, with time and who acts; mark necessary steps (qualification, safety, setup the result depends on) as kept, and remove or merge the rest.
3. **Find where people stall.** From cohorts and tickets in `inputs/`, compute early retention and count first-period questions with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py). Separate causes: fit (wrong customers sold), product or service failure, operations (late delivery), measurement, and onboarding friction. Only the last is fixed here; hand the rest to their owners (`04-product`, `07-offer-design`, operations).
4. **Design the first week.** For each stall the evidence supports: the message, setting or step that answers it before it is asked (a sign-up question, a welcome message, a guide), when it happens and on which channel. Each item names the ticket group or cohort drop it targets.
5. **Measure.** Activation rate and time to first value by cohort, early retention, and the ticket groups targeted, with counts and dates. Compare cohorts before and after on equal windows.
6. **Approval.** The plan is a draft. Changing sign-up flows, emails, product settings or what ships needs the owner's explicit approval.
7. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no activation rates, retention, results, features or customer quotes that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/15-retention/15-onboarding-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Onboarding plan: <business, offer>
Skill: 15-onboarding · Date: <YYYY-MM-DD> · Framework: Onboarding to first value (activation / aha moment)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing changed
## Activation: definition, window, denominator
## Path to first value
| Step | Time | Who acts | Keep / change / remove |
| --- | --- | --- | --- |
## Where people stall (evidence)
## Causes that are not onboarding
## First-week plan
| When | Channel | What it does | Targets (evidence) |
| --- | --- | --- | --- |
## How we measure it
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/15-retention/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the activation definition and why, the biggest stall with its cause, and the first-week changes, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Activation is first meaningful value with a window and denominator; tracking-convenience definitions are rejected.
- [ ] Necessary steps are kept; only friction is removed.
- [ ] Stalls are counted from cohorts and tickets; fit, product, operations and measurement causes are separated and handed off.
- [ ] Each first-week item targets an evidenced stall.
- [ ] Measurement compares cohorts on equal windows; nothing changes without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Onboard to the first result the customer paid for: define activation as real value, keep the steps that result needs, answer the questions before they are asked, and check fit, product and delivery before blaming onboarding. Onboarding and Activation / aha moment, The Complete Marketing System, section 15 Retention (Servidad, 2026); Lincoln Murphy's desired outcome framing for customer success.
