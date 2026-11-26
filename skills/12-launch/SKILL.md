---
name: 12-launch
description: Plan a launch, product launches included, with the Product Launch Formula, from pre-launch to close and review. Use for course or beta launches. Not for one live event (use 12-webinar-challenge).
metadata:
  section: "12 Funnel"
  covers: "Keynote launch playbook (Jobs); Launch playbook; Product Launch Formula"
---
# Launch

This is the launch playbook for any offer, product launches included (a new product, course, cohort, beta or relaunch), built on the Product Launch Formula. A launch concentrates attention and decision into a short window. It builds anticipation with useful pre-launch content, opens the cart, and closes it on a real date or limit. The urgency is the engine, so it must be true: a fake close date that reopens tomorrow trains buyers to wait and breaks trust.

Save the requested plan or asset as a Markdown file in `work/12-funnel/` (file name under Output) when the required inputs are present. Creating this deliverable is part of the task, including requests worded as planning or design. Complete the file and its checks before replying with its path. This save instruction does not apply when context has no true urgency for this launch, or no terms for the specific offer being launched (for example a gift or other variant): then Process step 1's stop applies, and you write no file. A section with draft status counts as present: when it states a real capacity, date or limit and the launched offer's terms, write the plan and list what the owner should confirm under Open questions.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Core offer**, from `07-offer-design` (plugin mkt-q2-offer).
- `context/offer.md` → **Urgency and scarcity**, from `07-bonuses-urgency` (plugin mkt-q2-offer).
- `context/message.md` → **Big idea**, from `08-message-doc` (plugin mkt-q3-message).
- If present, also read `context/message.md` → Story, Proof stack and Objection map; `context/offer.md` → Price and model, Guarantee and Bonuses; `context/awareness.md` → Awareness map and Traffic temperature; list size or past launch data in `inputs/`.
- If a required section is missing:
  - **The upstream evidence exists:** run the skill that fills it first, then continue. If that skill is not loaded, stop and say: enable mkt-q2-offer (Core offer, Urgency and scarcity) or mkt-q3-message (Big idea). Price and guarantee are the owner's commitments: never generate them yourself; stop and ask, or offer the owning skill's proposal for approval.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Core offer → `07-offer-design`, Urgency and scarcity → `07-bonuses-urgency`, both in mkt-q2-offer; Big idea → `08-message-doc`, in mkt-q3-message), the plugin to enable if that skill is not loaded,, and what the user should bring. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Confirm the true urgency** from `offer.md` → Urgency and scarcity: a real close date, cohort start, capacity or price change. If none is true, stop and ask the owner to decide one they will honour; never invent it.
   At that stop, also ask for the missing commercial terms of the specific offer being launched. For a gift or other variant, do not inherit the regular product's price, duration, renewal, start-date or delivery terms. Bundle the unresolved terms with the date/time, timezone and delivery-region questions, and ask for the owner's confirmed terms or the relevant fulfilment schedule before dating the plan. Ask about bonuses only when one is actually proposed; a bonus is not required.
   Draft status alone is not a reason to stop: urgency and terms written in context, drafted or confirmed, are enough to build the plan. At this stop, write no file in `work/12-funnel/`, not even a draft in relative days (O, K, Day 1) or with undated placeholders. Reply only with the questions and the closing block.
2. **Lay out the phases,** using [references/plf.md](references/plf.md) alongside Steve Jobs's keynote launch narrative and live-proof discipline in [references/jobs-keynote-launch.md](references/jobs-keynote-launch.md):
   - **Pre-pre-launch:** seed interest and listen.
   - **Pre-launch:** three pieces of useful content, opportunity → transformation → ownership.
   - **Open cart:** the offer, proof, FAQ, and objection emails.
   - **Close:** reminders and the real deadline.
   - **Post-launch:** onboarding, and a review.
3. **Build the calendar:** day by day, which asset (content, email, live session, ad) and its job. Name assets to be built by their skills: `12-email-sequences`, `10-sales-page`, `10-vsl-script`.
   Every asset to create needs an exact skill name, including internal assets: for example `20-marketing-plan` for the brief and `20-campaign-review` for the review memo. A human team such as Marketing or Operations may review or execute the work, but is not a substitute for the asset's skill hand-off. Owner confirmations remain human decisions.
4. **Set the targets and metrics:** registrations, open-cart conversion, sales, refunds, each with a baseline from past launches or "unknown".
   Keep observed totals in their original period and population. Show the formula for calculated rates or averages and label them as calculations. A quarterly total does not establish monthly results, a campaign-window forecast, or which wins met an unrecorded condition.
5. **Plan the review:** what will be measured, and what changes next time.
6. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features, platform capabilities or delivery terms that aren't in `context/` or `inputs/`. Mark inferences `(assumption)`, and list what is needed under Open questions. Describe each source only as it reads: no outcome, motive or behaviour the source doesn't state. In the founder's or brand's voice, add no habits, promises or operational details (who reads replies, what a call covers) that context doesn't contain.

## Output

Write `work/12-funnel/12-launch-<YYYY-MM-DD>.md`, adding `-<slug>` after the date when more than one is written the same day:

```markdown
# Launch plan: <what it is for>
Skill: 12-launch · Date: <YYYY-MM-DD> · Framework: <name>
Built from: <context sections used, with their status>
Urgency (true, from offer.md): <…>
## Phases and calendar
| Day | Phase | Asset | Job | Owner skill |
| --- | --- | --- | --- | --- |
## Metrics and targets
## Post-launch review plan
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. This is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a review, an interview, a testimonial in the proof stack), with the source named. Write your own lines, proposals and copy in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py <file>`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the key decision, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The urgency is true and comes from `offer.md` or an owner decision. No invented deadlines, scarcity or reopen tricks.
- [ ] If context had no true urgency or no terms for the specific offer, no file was written in `work/12-funnel/` (not even a relative-day draft); the reply asks only the questions.
- [ ] Missing terms for the specific launch offer are explicitly requested with the urgency confirmation; regular-product terms are not transferred to an unconfirmed variant.
- [ ] Every phase and asset has a job and a date. Every asset to build names its exact skill, with human reviewers or approval owners separate.
- [ ] Targets use real baselines or say unknown. No invented benchmarks.
- [ ] A post-launch review is planned.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.
- [ ] The reply, including a stop reply, ends with all three lines: **Principle**, **Framework** and **Source**.

## Principle and source

Concentrate attention and decision into a window with useful pre-launch content and true urgency: a real close date or limit is the engine, and a fake one destroys the next launch. Product Launch Formula (Jeff Walker, Launch); Apple keynote launch narrative and demo-first proof (Steve Jobs); The Complete Marketing System, section 12 Funnel (Servidad, 2026).
