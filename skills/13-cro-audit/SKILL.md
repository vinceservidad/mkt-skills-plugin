---
name: 13-cro-audit
description: Audit a page for clarity, friction, anxiety and proof using analytics, heatmaps and session recordings. Use for CRO audit, why a page doesn't convert, page review, conversion rate optimization.
metadata:
  section: "13 Conversion"
  covers: "Behavioral nudges; Chatbots / conversational marketing; Conversion rate optimization (CRO); Five-second test; Fogg Behavior Model; Heatmaps / session recordings; Heuristic evaluation (Nielsen); LIFT model; Live chat; MECLABS sequence; Personalization; User testing"
---
# CRO audit

Conversion rate optimisation turns the visitors a page already gets into leads and buyers. An audit says, from evidence, where and why a page loses the right visitors, separates what is broken or untrue from what is a persuasion hypothesis, and ranks the fixes as tests with an owner. It writes no new copy and changes nothing live: clarity beats cleverness, friction comes out before persuasion goes in, and big changes (offer, headline, layout) are tested before small ones (button colours).

Save the audit as a Markdown file in `work/13-conversion/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content), at least one of:
- `context/offer.md` → **Core offer**, from `07-offer-design`: what the page should be selling.
- `context/message.md` → **Promise**, from `08-message-doc`: what the page should be saying.

A section counts only when its `Status:` line says drafted or confirmed and it has content under it. A file that exists with `Status: empty` (the installer's template) is missing. Check this first, before asking for page or other material: a missing upstream section is a stop, not a baseline.

If present, also read:
- `context/awareness.md` → Awareness map (`03-awareness-map`), Traffic temperature, Beliefs, objections and drivers;
- `context/message.md` → Proof stack and Objection map; `context/offer.md` → Price and model, Guarantee, Urgency and scarcity.

The page material, in `inputs/`, elsewhere in the project, or pasted by the user:
- the page itself (copy, screenshots, or a URL you can actually read, with the date read), including its form or checkout entry;
- analytics with definitions and dates (sessions, clicks, form views, submits, orders), ideally by device and source;
- anything else observed: polls, recordings or heatmaps, user tests, support or sales questions, past test results.

If something is missing:
- **Core offer and Promise both missing:** stop. Name both sections with their skills (Core offer → `07-offer-design`; Promise → `08-message-doc`) and say what to bring: the offer and the page. A stop reply still ends with the **Principle, framework, source** block.
- **The page itself is missing:** ask for its copy or screenshots, or a URL to read; audit nothing from imagination.
- **No analytics:** audit the page against context, mark every finding as a heuristic read, and list the numbers to pull. Never state a "typical" conversion rate or benchmark from memory.
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.
- If `08-message-doc` is not loaded, stop and say: enable mkt-q3-message.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/lift-audit.md](references/lift-audit.md) for the LIFT questions, the five-second test, the defect-versus-hypothesis rule and the ranking.

1. **Fix the scope.** One page, its one conversion goal (a booked call, a sign-up, a purchase), the traffic sources and their temperature, and where the conversion boundary is (form submit, order paid). Name the business outcome behind the goal (qualified calls, paid orders), not clicks.
2. **Read the numbers.** Sum and rate every step with [scripts/funnel.py](scripts/funnel.py) (`python3 <this skill's folder>/scripts/funnel.py <export.csv> <column> ...`), never by eye, overall and by device and source. Keep each step's source definition, period and denominator. Flag counts too small to read (single digits) and say how the page's numbers relate to downstream records (a form submit may already be counted under another lead source).
3. **Run the five-second test on the page as written.** From the words above the fold only: what is it, who is it for, what do I do next? Quote the page's own words. This is a heuristic read by you, not a user test, unless a real test was supplied.
4. **Walk the LIFT factors.** For each: value proposition (does the page say the Core offer and Promise?), relevance (does it match the sources and their awareness?), clarity, anxiety (which evidenced objections and fears are unanswered at the point of decision; which claims are unsupported), distraction (competing links, navigation, extra fields), urgency (only what offer.md says is true). For each finding record: location, what the page says (quoted), the evidence, the factor, who it affects, the suspected mechanism, and confidence.
5. **Separate defects from hypotheses.** A defect is something broken, false or contradicting context: a service the offer doesn't include, an unsupported claim, a promise of a slower or different next step than the business delivers, a field nobody uses. Defects are fixed first, with the owner's approval. Everything else is a hypothesis to test, not a diagnosed cause.
6. **Rank.** Order fixes by evidence strength, how many of the right visitors the step touches, and effort. Bigger levers first (offer, headline, form, layout), small cosmetic changes last. Keep necessary qualification, legal, pricing and expectation-setting information even if removing it would raise raw conversion.
7. **Hand off, don't rewrite.** For each fix name the owner skill: copy → `10-page-copy` with a brief of the problem the rewrite must solve; trust elements → `13-trust-signals`; pricing display → `13-pricing-page`; checkout → `13-checkout`; sign-up flows → `13-signup`; traffic quality → `11-channel-selection`; the test design → `18-ab-testing`. Every row of Ranked tests fills all four parts, each written out for that test: a metric, a guardrail, a window, and a stopping rule (when to stop early or call it: for example the guardrail falls below its baseline, or the window ends without a readable difference). "Same as above" or a blank part fails the check.
8. **Authorization.** This is an audit. Say that every live change needs the owner's approval and a check afterwards against the baseline.
9. **Check before saving.** Re-read the draft against the Checks, run `scripts/check_quotes.py`, and fix any failure.

**Labels.** Every number is copied from a named export or note (with its date), *calculated* (show numerator and denominator), or marked `(assumption)`. Every motive or behaviour you attribute to visitors is evidence-backed or marked `(assumption)`. No unmarked inference.

**Platform facts.** Do not state how an analytics tool, page builder, search engine or ad platform currently works unless you cite its own documentation as `(first-party: <URL>, checked YYYY-MM-DD)`. Otherwise describe only what the material shows and mark anything else *unverified*.

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from the page or a source, with the source named. Your own suggested directions go in italics. Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py <file>`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches.

## Output

Write `work/13-conversion/13-cro-audit-<YYYY-MM-DD>-<page-slug>.md`:

```markdown
# CRO audit: <page> (<date>)
Skill: 13-cro-audit · Framework: LIFT model (WiderFunnel); five-second test
Built from: <page material, exports and context sections used, with dates and status>
Scope: <page> · Goal: <one conversion> · Business outcome: <…> · Sources: <…>
## The numbers
| Step | Count | Rate (calculation) | By device / source | Reading |
| --- | --- | --- | --- | --- |
## Five-second test
## Findings by LIFT factor
| # | Location | What the page says | Evidence | Factor | Who it affects | Suspected mechanism | Confidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
## Defects to fix first (owner approval)
## Ranked tests
| Rank | Hypothesis | Change | Metric, guardrail, window, stopping rule | Owner skill |
| --- | --- | --- | --- | --- |
## Hand-offs
## Claims and sources
| Claim or number | Source or calculation |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/` and nothing live. This is an audit, not a decision.

Reply with the file path, the biggest leak with its numbers, the first fix or test and its owner skill, the most important limit of the evidence, and a reminder that live changes need the owner's approval.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] One page, one conversion goal and the business outcome behind it are named.
- [ ] Every count and rate comes from `funnel.py` or a shown calculation, keeps its definition and period, is split by device or source where the data allows, and small counts are flagged. No benchmark is stated.
- [ ] The five-second test and every LIFT factor are applied to the page's actual words, and each finding names its evidence and confidence.
- [ ] Defects (broken, false, contradicting context) are separated from hypotheses, and no hypothesis is stated as a proven cause.
- [ ] Fixes are ranked, bigger levers first, and each has an owner skill. Every ranked test row states its own metric, guardrail, window and stopping rule; none is blank or deferred to another row. Necessary qualification and expectation-setting information is kept.
- [ ] No new copy is written as final; rewrites go to `10-page-copy` with a brief. No live change is made or implied as done.
- [ ] No current platform behaviour is asserted without a first-party citation and date.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Clarity beats cleverness, and friction comes out before persuasion goes in: find where the page loses the right visitors from evidence, fix what is broken or untrue first, and test the biggest levers before the small ones. LIFT model (Chris Goward, WiderFunnel, You Should Test That!, 2013); five-second test; Don't Make Me Think (Steve Krug); The Complete Marketing System, section 13 Conversion (Servidad, 2026).
