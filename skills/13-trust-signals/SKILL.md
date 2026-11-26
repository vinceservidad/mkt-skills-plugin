---
name: 13-trust-signals
description: Place the trust stack of reviews, logos, guarantees, real people and specific numbers on a page. Use for trust signals, social proof placement, credibility on a landing or checkout page.
metadata:
  section: "13 Conversion"
  covers: "Trust signals"
---
# Trust signals

Trust on a page is built by proof, consistency and design quality, not by claims of trustworthiness. A trust signal earns its place only if it is true, specific, permitted, and placed next to the doubt it answers. One unsupported badge or invented testimonial can cost more trust than ten real reviews earn. This skill audits the trust elements a page has, takes down what is unsupported, and places real proof at the decision points. It changes nothing live.

Save the plan as a Markdown file in `work/13-conversion/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content), at least one of:
- `context/message.md` → **Proof stack**, from `08-proof-stack`: the real proof, its strength and whether permission is needed;
- `context/customer.md` → **Beliefs, objections and drivers**, from `02-buyer-psychology`: the fears the signals must answer.

A section counts only when its `Status:` line says drafted or confirmed and it has content under it. A file that exists with `Status: empty` (the installer's template) is missing. Check this first, before asking for page or other material: a missing upstream section is a stop, not a baseline.

If present, also read:
- `context/message.md` → Objection map; `context/offer.md` → Guarantee (`07-guarantee-risk-reversal`) and Core offer (what exists and what is proposed); `context/brand.md` → Reputation;
- the page or site as it is (copy, screenshots), and any review exports, in `inputs/` or pasted.

If both required sections are missing: stop. Name Proof stack → `08-proof-stack` and Beliefs, objections and drivers → `02-buyer-psychology`, and say what to bring (reviews, testimonials, the fears buyers raise). A stop reply still ends with the **Principle, framework, source** block.
- If `08-proof-stack` is not loaded, stop and say: enable mkt-q3-message.
- If `02-buyer-psychology` is not loaded, stop and say: enable mkt-q1-audience.

## Process

Use [references/trust-stack.md](references/trust-stack.md) for the signal types, the take-down rules and placement.

1. **Audit what is on the page now** (if supplied). Classify every trust element: *supported* (traceable to the Proof stack or inputs, with permission status), *unsupported* (a number, badge or claim with no source), *unapproved commitment* (a guarantee or policy the owner has not approved), or *untraceable testimonial* (a quote not found in any review export or permitted source). Unsupported, unapproved and untraceable elements are taken down or replaced, with the owner's approval; never keep them because they look good.
2. **List the fears at each decision point:** above the fold, near the price, at the call to action or form, in checkout. Use Beliefs, objections and drivers and the Objection map, with their evidence.
3. **Pick one signal per fear** from the Proof stack: reviews and testimonials (verbatim, with source and date, and permission status), real people (names or roles only with consent), specific numbers (from a named source, with period and whether self-reported), client logos (only clients who have agreed), guarantees (only owner-approved wording), security and payment cues (only what is true). Weak or contradicted proof is not used where it would mislead; say why.
4. **Place each signal** next to the claim or doubt it answers, not in a wall of badges. Keep the page consistent: a claim made in one place must not be contradicted elsewhere (a free-shipping badge that applies only to some orders, a "cancel anytime" line with no way to cancel).
5. **Name the gaps:** each fear with no real proof yet, what to collect (with the owner, `08-proof-stack` or `16-testimonials-case-studies`), and what to say meanwhile (nothing, or a softened true statement).
6. **Permission.** Mark every quote, name, photo and logo that needs permission before publishing. Remove names and details that identify a private person unless they consented.
7. **Measure.** Each placement is a test with a primary outcome (orders or qualified leads from the page), guardrails (refunds, complaints, support questions about the claim), a window and a stopping rule; hand test design to `18-ab-testing` and copy to `10-page-copy`.
8. **Authorization.** Every live change (adding, removing or rewording a trust element) needs the owner's approval and a check afterwards.
9. **Check before saving.** Re-read the draft against the Checks, run `scripts/check_quotes.py`, and fix any failure.

**Nothing the context doesn't support.** Write no customer counts, ratings, review totals, awards, press mentions, certifications, client names, logos, years in business or guarantee terms that aren't in `context/` or `inputs/`. A quote that appears in a page draft but in no review export is not proof just because it is in the file. Do not state that a payment or security provider's badge may be shown, or what a certification requires, unless you cite its own documentation as `(first-party: <URL>, checked YYYY-MM-DD)`; otherwise mark it *to check*.

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from a source, with the source and date. Your proposed lines go in italics. Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py <file>`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches. Count reviews with [scripts/tally.py](scripts/tally.py), never by eye.

## Output

Write `work/13-conversion/13-trust-signals-<YYYY-MM-DD>-<page-slug>.md`:

```markdown
# Trust signals: <page or site> (<date>)
Skill: 13-trust-signals · Framework: Trust stack; social proof and authority (Cialdini)
Built from: <context sections and inputs used, with status>
## What the page has now
| Element | Classification | Evidence or problem | Action (keep / replace / take down) |
| --- | --- | --- | --- |
## Fears at each decision point
## The trust stack, placed
| Decision point | Fear (evidence) | Signal | Source and date | Strength | Permission |
| --- | --- | --- | --- | --- | --- |
## Consistency fixes
## Gaps: proof to collect
| Fear | What to collect | Owner | Say meanwhile |
| --- | --- | --- | --- |
## Metrics and tests (owner approval needed for live changes)
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/` and nothing live.

Reply with the file path, what to take down first, the strongest real signal and where it goes, the biggest proof gap, and a reminder that live changes and quoting need approval and permission.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every existing trust element is classified, and unsupported numbers, unapproved guarantees and untraceable testimonials are marked for take-down or replacement.
- [ ] Every signal placed comes from the Proof stack or inputs, with source, date, strength and permission status; nothing is invented.
- [ ] Each signal answers a named fear with evidence and sits at the decision point where that fear arises.
- [ ] Guarantees appear only in owner-approved wording; proposed offer elements are not shown as live; claims are consistent across the page.
- [ ] Gaps name what to collect and the owner, and what to say meanwhile.
- [ ] No provider badge rule or certification is asserted without a first-party citation and date.
- [ ] Placements are tests with metric, guardrails, window and stopping rule; no live change is made or implied as done.
- [ ] Every test is written out on its own: metric, guardrails, window and stopping rule (when to stop early or call it), none blank or deferred to another test.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Trust is built by proof, consistency and design quality, not by claims of trustworthiness: put one true, specific, permitted signal next to each real fear, and take down anything you cannot back. Trust stack; social proof and authority (Robert Cialdini, Influence); Don't Make Me Think (Steve Krug); The Complete Marketing System, section 13 Conversion (Servidad, 2026).
