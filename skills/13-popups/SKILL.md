---
name: 13-popups
description: Design popups and slide-ins that capture without annoying. Use for popups, exit-intent, email capture modal, slide-in offers, popup timing and copy.
metadata:
  section: "13 Conversion"
  covers: "Popups / slide-ins"
---
# Popups

A popup interrupts. It earns the interruption only when it offers this visitor something they want at the moment they are ready for it, closes easily, and never comes back to nag. This skill designs each popup from a real offer in the business's ladder, with its trigger, audience, frequency and honest close, and judges it by the leads and customers it brings, not by sign-ups alone. It changes nothing live.

Save the design as a Markdown file in `work/13-conversion/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content), at least one of:
- `context/offer.md` → **Core offer**, from `07-offer-design`;
- `context/offer.md` → **Value ladder**, from `07-value-ladder`: the free and low-ticket steps a popup can carry.

A section counts only when its `Status:` line says drafted or confirmed and it has content under it. A file that exists with `Status: empty` (the installer's template) is missing. Check this first, before asking for page or other material: a missing upstream section is a stop, not a baseline.

If present, also read:
- `context/offer.md` → Price and model (`07-pricing`, for any discount stance), Bonuses, Urgency and scarcity;
- `context/awareness.md` → Traffic temperature, Awareness map, Beliefs, objections and drivers;
- current popups and their numbers (views, sign-ups, orders, downstream quality), in `inputs/` or pasted.

If both required sections are missing: stop. Name Core offer → `07-offer-design` and Value ladder → `07-value-ladder`, and say what to bring (what the business sells and what it can give away). A stop reply still ends with the **Principle, framework, source** block.
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.
- If `07-value-ladder` is not loaded, stop and say: enable mkt-q2-offer.

## Process

Use [references/popup-rules.md](references/popup-rules.md) for triggers, frequency, mobile, consent and the dark patterns to avoid.

1. **Diagnose the current popups, if any.** Rate views to sign-ups to orders with [scripts/funnel.py](scripts/funnel.py) or a shown calculation. Compare downstream quality (orders, second orders, qualified leads) of popup sign-ups with others only as an observation: people who chose an incentive are not a random group, so the gap is not proof the incentive caused it. Flag any close text that shames the visitor and any trigger that blocks content.
2. **Choose the offer for each popup** from what exists in `offer.md`: a free asset, a sample, a low-ticket first step, a consult. A proposed asset that does not exist yet is a gap, named with its owner (`12-lead-magnet` to build it). A discount appears only if `offer.md` holds one the owner has approved. If a live discount contradicts `offer.md` (for example Price and model recommends no default discount), do not redesign around it and do not remove it on your own: lay out the evidence and the options, and mark the decision *owner to decide*.
3. **Read each popup with Fogg (B = MAP)** before designing it: *motivation* (what this visitor, on these pages, already wants, from the evidence), *ability* (what the popup asks of them: fields, effort, interruption) and *prompt* (the trigger and moment). A popup fails when one is missing: an offer nobody on that page wants, a form too long for a phone, or a prompt that fires before the visitor has any reason to care. Write this read for the current popups and for every new one.
4. **Match offer to visitor:** cold readers on content pages get the free step; visitors on product or pricing pages get help with the decision or the first step; existing subscribers and customers see nothing.
5. **Design each popup:** pages it shows on and where it never shows (checkout, account pages), audience, trigger (time, scroll depth, exit intent, a click on a link), the offer, copy direction in italics, fields (email only, unless the next step needs more), the close (a plain *No thanks* or an X), frequency cap and suppression, and mobile behaviour (a small slide-in or banner rather than a full-screen cover).
6. **Consent.** Say exactly what the visitor signs up for, keep any marketing opt-in unticked, and mark consent wording *to check with counsel* for the markets served. Do not assert what the law requires.
7. **Measure what matters.** Primary: the downstream outcome the business values (first orders, second orders or qualified leads per 1,000 views), with sign-ups per view as a supporting metric. Guardrails: bounce or exit rate on the pages it shows on, unsubscribes, complaints, discount cost. Each change is a test with a holdout or a split, a window and a stopping rule; hand design of the test to `18-ab-testing`, and the follow-up emails to `12-email-sequences`.
8. **Authorization.** Every live change to the popups, their offers or any discount needs the owner's approval and a check afterwards against the baseline.
9. **Check before saving.** Re-read the draft against the Checks, run `scripts/check_quotes.py`, and fix any failure.

**Nothing the context doesn't support.** Write no discounts, free assets, deadlines, stock counts, numbers of subscribers or results that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. No fake urgency, no confirmshaming, no hidden close buttons, no pre-ticked boxes.

**Platform facts.** Do not state how a popup tool, email platform or search engine currently treats popups (for example on mobile) unless you cite its own documentation as `(first-party: <URL>, checked YYYY-MM-DD)`. Otherwise mark it *to check*.

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from a source, with the source named. Your popup headlines, buttons and close text go in italics. Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py <file>`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches.

## Output

Write `work/13-conversion/13-popups-<YYYY-MM-DD>-popups.md`:

```markdown
# Popups: <site> (<date>)
Skill: 13-popups · Framework: Fogg Behavior Model (prompt at the right moment)
Built from: <context sections and inputs used, with status and dates>
## Current popups (if any): numbers and problems
| Popup | Views | Sign-ups | Orders or leads | Rate (calculation) | Downstream quality | Problems |
| --- | --- | --- | --- | --- | --- | --- |
## Decisions for the owner
## Fogg read (motivation, ability, prompt) per popup
| Popup | Motivation (evidence) | Ability (what it asks) | Prompt (trigger and moment) | Weakest factor and the fix |
| --- | --- | --- | --- | --- |
## Popup designs
| Popup | Pages (and never on) | Audience | Trigger | Offer (exists or gap) | Copy direction | Fields | Close | Frequency and suppression | Mobile |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
## Consent
## Metrics and tests
## Claims and sources
| Claim or number | Source or calculation |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/` and nothing live.

Reply with the file path, the main design decision, any decision the owner must make (such as a live discount), and a reminder that live changes need the owner's approval.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every popup carries an offer that exists in `offer.md`, or the gap is named with its owner; no discount, freebie or deadline is invented.
- [ ] A live offer that contradicts `offer.md` is laid out as an owner decision, not silently kept or removed.
- [ ] Every current and new popup has a written Fogg read (motivation from evidence, ability, prompt) that names its weakest factor, and the design fixes that factor.
- [ ] Each popup has page scope, audience, trigger, frequency cap, suppression (customers, subscribers, checkout) and mobile behaviour.
- [ ] The close is plain, consent is unticked and marked *to check with counsel*, and no dark pattern is used.
- [ ] Current numbers are calculated with numerators and denominators, and downstream differences are observations, not proof of cause.
- [ ] Success is judged by downstream outcomes with guardrails, as tests with a window and stopping rule; no live change is made or implied as done.
- [ ] Every test is written out on its own: metric, guardrails, window and stopping rule (when to stop early or call it), none blank or deferred to another test.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

A popup is a prompt: it works only when it offers something this visitor already wants, at the moment they are able to act, and it respects them when they say no. Fogg Behavior Model (BJ Fogg, Tiny Habits, 2019); reciprocity (Cialdini, Influence); The Complete Marketing System, section 13 Conversion (Servidad, 2026).
