---
name: 13-paywalls
description: Design paywalls, feature gates and in-app nudges to upgrade or book a sales call. Use for paywall design, upgrade screens, free-to-paid prompts, trial-end screens.
metadata:
  section: "13 Conversion"
  covers: "Paywalls / upgrade prompts"
---
# Paywalls

A paywall or upgrade prompt asks a user to pay, or to take the paid step, at a moment inside the product. It works when it appears right after the user has felt the value, speaks to users who can buy, states the plan, price and terms exactly as the business set them, and lets the user say no without penalty. This skill designs the moments, the audience and the message. It never sets the price, the plan boundaries or the trial length, which belong to `07-pricing`, and it changes nothing live.

Save the design as a Markdown file in `work/13-conversion/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Price and model**, from `07-pricing`: what the paid step is and what it costs.

A section counts only when its `Status:` line says drafted or confirmed and it has content under it. A file that exists with `Status: empty` (the installer's template) is missing. Check this first, before asking for page or other material: a missing upstream section is a stop, not a baseline.

If present, also read:
- `context/offer.md` → Core offer, Value ladder, Guarantee;
- `context/customer.md` → Jobs to be done, Segments, ICP and personas;
- product evidence, in `inputs/` or pasted: a usage or funnel export with event definitions and dates, what is free and what is paid today, feedback, and any `work/04-product/04-plg-audit-*.md` file.

If something is missing:
- **Price and model missing:** stop. Name Price and model → `07-pricing` and say what to bring (what the paid step is and its price). A stop reply still ends with the **Principle, framework, source** block.
- **The paid step this paywall needs is not in Price and model** (for example a paid plan of the app that the owner has not decided): stop and ask the owner for the plan, price and trial or renewal terms, or offer to run `07-pricing`. Do not design a paywall around a price a user said they would pay, or one you choose.
- If `07-pricing` is not loaded, stop and say: enable mkt-q2-offer.

## Process

Use [references/upgrade-moments.md](references/upgrade-moments.md) for paywall types, value moments, targeting and the honesty rules.

1. **Name the paid step exactly** as `offer.md` states it: plan or service, price, billing, trial or renewal terms, guarantee if approved. If the paid step is a call or a service rather than a plan, the prompt asks for that step.
2. **Find the value moments** from evidence: the events or feedback that show a user getting the result they came for (not sign-up, a connection or an automatic event). Sum and rate events with [scripts/funnel.py](scripts/funnel.py) (`python3 <this skill's folder>/scripts/funnel.py <export.csv> <segment column>`), never by eye. The prompt appears there, not on the first screen.
3. **Choose the type** from the evidence: a soft prompt (dismissable, at a value moment), a feature gate, a usage limit, or a time limit (trial end). Where the type changes what is free, the boundary is a pricing decision: propose it, with evidence, for `07-pricing` and the owner.
4. **Choose who sees it.** Show the paid step to the segments that get value and can buy it. For users the paid step does not fit, say what honest alternative exists in `offer.md` (or that none does), and never push them with pressure.
5. **Read each prompt with Fogg (B = MAP):** *motivation* (the value this user has just seen, from evidence), *ability* (what taking the paid step asks: price, a call, setup) and *prompt* (the trigger and moment). Name the weakest factor for each prompt and design to fix it; a prompt at a moment with no visible value is a motivation failure, however good the copy.
   Then **write the prompt at wireframe level:** trigger, placement, what the user has already got (from their own data where possible), what the paid step adds, the price and terms exactly as set, one primary action, a plain dismiss, and how often it can reappear. Copy directions in italics; final copy goes to `10-page-copy`.
6. **Keep it honest.** No hidden or pre-selected renewals, no countdown that isn't real, no shaming dismiss text, no blocking data the user already put in, and cancelling as easy as upgrading. A guarantee appears only in the owner-approved wording.
7. **Measure.** Primary: the paid step taken by the right segment within a fixed window after the prompt (upgrades, booked calls, then paid clients). Guardrails: refunds, cancellations, support tickets, retention of free users, wrong-fit calls. Each change is a test with a window and a stopping rule; hand the design to `18-ab-testing`. Read attribution: a call booked from the product may already be counted under another lead source.
8. **Authorization.** Every live change to the product, its prompts, the free boundary or any price needs the owner's approval and a check afterwards against the baseline.
9. **Check before saving.** Re-read the draft against the Checks, run `scripts/check_quotes.py`, and fix any failure.

**Nothing the context doesn't support.** Write no plans, prices, trial lengths, discounts, features or guarantee terms that aren't in `context/` or `inputs/`. A price a user says they would pay is stated preference for `07-pricing`, not a price. Mark inferences `(assumption)` and list what is needed under Open questions.

**Platform facts.** Do not state how an app store, payment provider or subscription tool currently handles trials, renewals or in-app purchases unless you cite its own documentation as `(first-party: <URL>, checked YYYY-MM-DD)`. Otherwise mark it *to verify*.

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from a source, with the source ID. Your prompt headlines and buttons go in italics. Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py <file>`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches.

## Output

Write `work/13-conversion/13-paywalls-<YYYY-MM-DD>-<product>.md`:

```markdown
# Paywall and upgrade prompts: <product> (<date>)
Skill: 13-paywalls · Framework: Fogg Behavior Model (prompt at the value moment); honest anchoring
Built from: <context sections and inputs used, with status and dates>
Paid step: <exactly as offer.md states it, with its status>
## Value moments (evidence)
| Moment | Event (source definition) | Count | Rate (calculation) | By segment | Why it is value |
| --- | --- | --- | --- | --- | --- |
## Who sees it, and who doesn't
## Fogg read (motivation, ability, prompt) per prompt
| Prompt | Motivation (value just seen, evidence) | Ability (what the paid step asks) | Prompt (trigger and moment) | Weakest factor and the fix |
| --- | --- | --- | --- | --- |
## Prompt designs
| Prompt | Trigger and placement | Audience | Message direction | Price and terms shown | Primary action | Dismiss and frequency |
| --- | --- | --- | --- | --- | --- | --- |
## Free boundary (proposal for 07-pricing, if any)
## Honesty rules applied
## Metrics and tests (owner approval needed for live changes)
## Claims and sources
| Claim or number | Source or calculation |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/` and nothing live.

Reply with the file path, the main value moment and who sees the prompt, anything the owner must decide (plan, price, free boundary), and a reminder that live changes need the owner's approval.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every prompt has a written Fogg read (motivation from evidence, ability, prompt) naming its weakest factor, and the design addresses it.
- [ ] The paid step, price and terms are copied exactly from `offer.md`; none is invented, and a price a user said they'd pay is not used as a price.
- [ ] Each prompt fires at an evidenced value moment, not on sign-up, a connection or an automatic event, with counts from `funnel.py` or a shown calculation.
- [ ] The audience is the segments that get value and can buy; others get an honest alternative or nothing, never pressure.
- [ ] No hidden renewal, fake timer, shaming dismiss or blocked data; cancelling is as easy as upgrading.
- [ ] Changes to the free boundary are proposals for `07-pricing` and the owner; tests have metric, guardrails, window and stopping rule; no live change is made or implied as done.
- [ ] Every test is written out on its own: metric, guardrails, window and stopping rule (when to stop early or call it), none blank or deferred to another test.
- [ ] No current platform behaviour is asserted without a first-party citation and date.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Ask for the upgrade right after the user has felt the value, show it to people who can buy it, state the real price and terms, and let them say no: an honest prompt at the value moment beats pressure at the door. Fogg Behavior Model (BJ Fogg, Tiny Habits, 2019); anchoring (Kahneman, Thinking, Fast and Slow); Product-Led Growth (Wes Bush, 2019); The Complete Marketing System, section 13 Conversion (Servidad, 2026).
