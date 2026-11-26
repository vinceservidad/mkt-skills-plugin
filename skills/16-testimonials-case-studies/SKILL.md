---
name: 16-testimonials-case-studies
description: Collect testimonials and case studies with before, after, specific result and the objection beaten, with permission. Use for testimonials, case studies, customer stories, social proof.
metadata:
  section: "16 Referral and Community"
  covers: "Case studies; Testimonials"
---
# Testimonials and case studies

A testimonial or case study is a customer's own account of the change: where they were, what they doubted, what happened, and the specific result. It persuades when it is true, specific, in the customer's words, aimed at the objection buyers have, and published with permission. It fails when the business writes it for the customer, results are rounded up or uncheckable, the customer is named without consent, or the story answers a doubt nobody has. Proof in copy is chosen in `08-proof-stack`; this skill collects it.

Save the proof plan as a Markdown file in `work/16-referral-community/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Dream outcome**, from `07-offer-design`: the result the proof must show.
- `context/customer.md` → **Beliefs, objections and drivers**, from `02-buyer-psychology`: the doubts each story must beat.
- If present, also read `context/message.md` → Proof stack, Objection map; `context/customer.md` → Voice of customer, Segments; client records, results, review text, call notes and permission status in `inputs/`; any work in `work/08-message/08-proof-stack-*.md` or `work/16-referral-community/16-reviews-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (interviews, call notes or reviews in `inputs/`): run the skill that fills the missing section (`07-offer-design` or `02-buyer-psychology`) first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Dream outcome → `07-offer-design`; Beliefs, objections and drivers → `02-buyer-psychology`), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.
- If `02-buyer-psychology` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/proof-collection-guide.md](references/proof-collection-guide.md) for choosing candidates, the interview, the story structure, verifying results and permissions.

1. **Which doubts need proof.** From Beliefs, objections and the Objection map, list the top doubts with counts and which kind of customer story beats each.
2. **Candidates.** From `inputs/`, list customers whose results answer those doubts, with the evidence available (records, what they said) and the permission status (none, verbal, written).
3. **The interview.** Questions that draw out before, the doubt they had, why they chose, what happened, the specific result with a number they can stand behind, and what they'd tell a peer. Record their exact words.
4. **Verify results.** Each number is checked against records and signed off by the customer; vague or unverifiable results are written as the customer's words, not as data.
5. **Permission.** Written consent for name, company, photo, numbers and where it will appear; options for anonymity. Until then, the story is *blocked until permission*. Never write a testimonial the customer didn't say.
6. **Formats.** A short testimonial (quote, name or role, result), a case study (before, doubt, choice, after, result, quote), and where each appears (sales page, enablement, proposals).
7. **Rules.** Testimonials must reflect typical results or say they don't; endorsement rules are legal facts to verify or mark *to confirm*.
8. **Approval.** The plan is a draft. Contacting customers, publishing any story or using any name needs the owner's explicit approval.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no testimonials, quotes, results, names or company details that aren't in `context/` or `inputs/`. Never invent or paraphrase a testimonial as if the customer said it. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/16-referral-community/16-testimonials-case-studies-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Proof plan: <business, date>
Skill: 16-testimonials-case-studies · Date: <YYYY-MM-DD> · Framework: Testimonials and case studies (before, after, result, objection beaten)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nobody contacted, nothing published
## Doubts that need proof
| Doubt | Count (source) | Story that beats it |
| --- | --- | --- |
## Candidates
| Customer | Result (evidence) | Doubt it beats | Permission | Status |
| --- | --- | --- | --- | --- |
## Interview guide
## Verification
## Permission request
## Formats and placement
## Rules
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/16-referral-community/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the doubts that need proof, the candidates with permission status, and the interview to run first, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Each story is aimed at a counted doubt.
- [ ] Candidates list evidence and permission status; stories without written permission are blocked.
- [ ] Results are verified against records and signed off; unverifiable claims stay in the customer's words.
- [ ] No testimonial is written for a customer; quotes are exact.
- [ ] Endorsement rules are dated or *to confirm*; nothing is published without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Let customers tell the change in their own words, aimed at the doubt buyers have, with numbers they stand behind and their written permission. Testimonials and Case studies, The Complete Marketing System, section 16 Referral and Community (Servidad, 2026); FTC Guides Concerning the Use of Endorsements and Testimonials (verify current version).
