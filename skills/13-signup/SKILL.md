---
name: 13-signup
description: Optimize signup and registration flows for completion and activation. Use for signup drop-off, registration form, account creation flow. Not for campaign opt-in pages (12-landing-page).
metadata:
  section: "13 Conversion"
  covers: "Signup flow"
---
# Sign-up

A sign-up flow has two jobs: let the right people in with as little effort as possible, and get them to the first moment of real value. Every field and step costs completions, but some are the qualification or setup the value depends on. This skill maps the flow from evidence, separates broken steps from friction and wrong-fit sign-ups, and ranks the changes as tests. It never shortens necessary qualification, safety or setup just to raise a rate, and it changes nothing live.

Save the plan as a Markdown file in `work/13-conversion/` when the flow material is present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Nothing upstream is required. If present, read:
- `context/customer.md` → Jobs to be done (`02-jobs-to-be-done`): what value means to the user; ICP and personas and Segments: who the flow should let in;
- `context/offer.md` → Core offer, Price and model and Value ladder: what the free or trial step leads to.

The flow material, in `inputs/`, elsewhere in the project, or pasted by the user. Any of these counts:
- the flow as it is: each screen, every field and whether it is required, verification, connection or setup steps, what the user sees after;
- a funnel export (sign-up started, completed, each setup step, first value, return) with event definitions and export date, ideally by segment and cohort;
- feedback, support tickets, error logs, recordings, the owner's goal for who should sign up.

If there is no flow material, do not design an imagined flow. Write the plan described under Output and ask for the material. Never state a "typical" sign-up or activation rate or benchmark from memory.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/signup-flow.md](references/signup-flow.md) for the field test, first meaningful value and the Fogg diagnosis.

1. **Fix the boundary and the goal.** Where the flow starts (the sign-up click), where it ends (first meaningful value), and who it should bring in, from the ICP and the owner's stated goal.
2. **Map the flow as it is,** screen by screen and field by field. Copy event definitions from the source.
3. **Read the numbers.** Sum and rate every step with [scripts/funnel.py](scripts/funnel.py) (`python3 <this skill's folder>/scripts/funnel.py <export.csv> <segment column> [--exclude <value>]`), never by eye, overall, by segment and by cohort. Exclude or flag cohorts too young for a later step. Name the step that loses the most of the *right* users.
4. **Define first meaningful value.** The first moment the user gets the result they came for. Not account creation, not a connection, not an event the system fires on its own, not a tutorial. State the candidate, why, and how strong the evidence is.
5. **Diagnose each drop with Fogg** (behaviour happens when motivation, ability and a prompt meet):
   - **ability:** effort, errors, unclear steps, a failing connection. A defect is fixed before anything else, and read by date if it was fixed part-way through the period;
   - **motivation:** the wrong users signing up, or value not yet visible;
   - **prompt:** no reminder or next step when the user stops.
   Raise ability before motivation.
6. **Test every field and step.** Keep it if the value or the qualification needs it now. Move it after first value (progressive profiling) if it is only useful later. Remove it if nobody uses it. When the owner wants more qualification, weigh what each new question costs in completions against what it decides, and prefer data the flow already has.
7. **Who gets in.** If most sign-ups come from people the paid step can't serve, that is an acquisition or qualification issue: hand sources to `11-channel-selection`, and name the qualification the flow already does.
8. **Rank the changes as tests.** Each gets a metric (the share of the right segment reaching first value within a fixed window), guardrails (wrong-fit sign-ups, support load, downstream calls or paid conversions), a window and a stopping rule. Hand onboarding after first value to `15-onboarding`, the upgrade step to `13-paywalls`, copy to `10-page-copy`, test design to `18-ab-testing`.
9. **Authorization.** Every live change to the flow, its questions or its verification needs the owner's approval and a check afterwards against the baseline.
10. **Check before saving.** Re-read the draft against the Checks, run `scripts/check_quotes.py`, and fix any failure.

**Nothing the context doesn't support.** Write no features, integrations, prices, offers or platform capabilities that aren't in `context/` or `inputs/`. Do not state how a login provider, verification service or integrated app currently works unless you cite its own documentation as `(first-party: <URL>, checked YYYY-MM-DD)`; otherwise mark it *unverified*.

**Labels.** Every number is copied from a named export or note (with its date), *calculated* (show numerator and denominator), or marked `(assumption)`. No unmarked inference about why users drop.

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from a source, with the source ID. Your proposed questions and microcopy go in italics. Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py <file>`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches.

## Output

**With flow material**, write `work/13-conversion/13-signup-<YYYY-MM-DD>-signup.md`:

```markdown
# Sign-up plan: <product> (<date>)
Skill: 13-signup · Framework: Fogg Behavior Model (B = MAP)
Built from: <flow notes, exports and context sections used, with dates and status>
Boundary: <first click> → <first meaningful value> · Who it should bring in: <…>
## The flow today
## Where users drop
| Step | Event (source definition) | Count | Rate (calculation) | By segment / cohort | Reading |
| --- | --- | --- | --- | --- | --- |
## First meaningful value
## Diagnosis (ability, motivation, prompt)
## Field by field and step by step
| Step | Field or step | Needed now? | Keep / after value / remove | Why |
| --- | --- | --- | --- | --- |
## Ranked tests (owner approval needed for live changes)
| Rank | Change | Why (evidence) | Metric, guardrails, window, stopping rule | Owner |
| --- | --- | --- | --- | --- |
## Claims and sources
| Claim or number | Source or calculation |
| --- | --- |
## Open questions
## Principle, framework, source
```

**Without flow material**, write `work/13-conversion/13-signup-<YYYY-MM-DD>-plan.md`: the flow to record (screens, fields, required or not, setup steps), the events to export with definitions, the segment to capture, the first-value candidate to test, and how each will be read. State no rate or benchmark.

Change nothing in `context/` and nothing live.

Reply, with material, with the file path, the biggest drop (with counts and segment) and its diagnosis, the first change to test and its owner, and a reminder that live changes need the owner's approval. Reply, without material, with the plan's path and a plain list of what to bring and how (save it in `inputs/` or paste it, then ask again).

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The flow's start, its end at first meaningful value, and who it should bring in are named.
- [ ] Every count and rate comes from `funnel.py` or a shown calculation, keeps its source definition, is split by segment, and incomplete cohorts are flagged. No benchmark is stated.
- [ ] First meaningful value is a user result, not sign-up, a connection, an automatic event or a tutorial, and its evidence strength is stated.
- [ ] Each drop is diagnosed as ability, motivation or prompt, defects are separated from friction, and wrong-fit sign-ups are separated from flow problems.
- [ ] No necessary qualification, safety or setup step is cut just to raise a rate; added questions are weighed against what they decide.
- [ ] Changes are tests with metric, guardrails, window, stopping rule and owner; no live change is made or implied as done.
- [ ] Every test is written out on its own: metric, guardrails, window and stopping rule (when to stop early or call it), none blank or deferred to another test.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Let the right people in with the least effort and get them to real value fast: raise ability before motivation, fix broken steps before persuading, and never trade away the qualification or setup the value depends on. Fogg Behavior Model (BJ Fogg, Tiny Habits, 2019); Product-Led Growth (Wes Bush, 2019); The Complete Marketing System, section 13 Conversion (Servidad, 2026).
