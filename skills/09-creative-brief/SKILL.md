---
name: 09-creative-brief
description: Write a creative brief with audience, awareness, insight, single message, proof, format and CTA. Use for a creative brief, briefing a designer, editor or agency on an ad or asset.
metadata:
  section: "09 Creative Strategy"
  covers: "Creative brief; Honest admission and visual-verbal tension (Bernbach); Message–market–media match (Kennedy)"
---
# Creative brief

A creative brief is the contract between strategy and the people who make the work. It gives them one audience, one insight, one message and the proof behind it, so they can be creative about the execution instead of guessing at the strategy. A brief that lists five messages gets five half-ads; a brief with an invented offer gets ads the business can't honour.

Save the brief as a Markdown file in `work/09-creative-strategy/` when the required inputs are present and the commercial terms are confirmed. Creating this deliverable is part of the task. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/message.md` → **Message house**, or at least **Promise**, from `08-message-doc`.
- `context/awareness.md` → **Awareness map**, from `03-awareness-map`.
- `context/offer.md` → **Core offer**, from `07-offer-design`.
- If present, also read `context/message.md` → Big idea, Proof stack, Objection map, Enemy and Story; `context/customer.md` → Voice of customer, ICP and personas; `context/awareness.md` → Traffic temperature; `context/offer.md` → Price and model, Guarantee, Bonuses, Urgency and scarcity, Value ladder; `context/brand.md` → Brand foundation, Distinctive assets and Voice; any angle matrix in `work/09-creative-strategy/09-angle-matrix-*.md`.
- If a required section is missing:
  - **The upstream evidence exists:** run the skill that fills it first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Message house or Promise → `08-message-doc`; Awareness map → `03-awareness-map`; Core offer → `07-offer-design`), and ask for evidence, not a description of the buyer. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Price, discounts, promo codes, guarantees, deadlines, free trials and capacity are the owner's commitments. If the brief must carry one that `offer.md` doesn't hold (for example a sale, a launch date or a new bonus), stop before writing, ask the owner for the exact terms, and write no brief on assumed terms.
- If `03-awareness-map` is not loaded, stop and say: enable mkt-q1-audience.
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/brief-fields.md](references/brief-fields.md) for what each field must contain and the common failures, [references/research-to-brief-and-review.md](references/research-to-brief-and-review.md) for the evidence-to-choice ledger, reference reverse-engineering, endorsement rights ledger and production preflight, and [references/creative-classics.md](references/creative-classics.md) for Bernbach's honest admission and visual-verbal tension, Ogilvy's brief focus, and Burnett's Inherent Drama check.

1. **Objective and the job of the work:** what the creative must cause (a booked call, a trial, a download), on which channel, for which traffic temperature. One objective.
2. **Audience and awareness level:** one segment from the ICP, and one level from the awareness map, with its share as the map gives it. If the campaign spans levels, write one brief per level.
3. **The insight:** the one truth about this buyer the work turns on, from Voice of customer, a pain or a belief, with its evidence ID. Not a product feature.
4. **The single message:** one sentence, from the promise or one pillar of the message house. Name the pillar. Everything else in the brief supports it.
5. **Reason to believe:** two or three proof items from the proof stack, with strength and permission status. Name the gaps; never fill them.
6. **Tone and brand:** from `brand.md` → Voice and Distinctive assets if present; otherwise say *no brand voice on file* and give only what the evidence supports (for example words customers distrust).
7. **Format and deliverables:** formats, sizes, lengths and number of variants. Platform specs come from the platform's current documentation (URL and date checked) or the ad account; otherwise *to confirm*. Ask for distinct concepts, not cosmetic variants.
8. **Call to action and destination:** one CTA, matched to the awareness level and to an offer that exists in `offer.md`.
9. **Mandatories and do-nots:** real terms that must appear (exactly as `offer.md` states them), claims that are off-limits and why, permissions still needed, legal or platform policy checks *to confirm*.
10. **How it will be judged:** the business outcome that decides, and that the brief's own work is draft until approved.
11. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features or delivery terms that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Competitor claims need a dated source or an `(assumption)` label.

## Output

Write `work/09-creative-strategy/09-creative-brief-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Creative brief: <campaign or asset>
Skill: 09-creative-brief · Date: <YYYY-MM-DD> · Framework: Creative brief
Built from: <context sections used, with their status (draft or confirmed)>
Status: draft for the owner's approval
| Field | Brief |
| --- | --- |
| Objective | |
| Audience | |
| Awareness level | |
| Insight (evidence) | |
| Single message | |
| Reason to believe | |
| Tone and brand | |
| Format and deliverables | |
| Call to action and destination | |
| Mandatories | |
| Do not | |
| How it will be judged | |
## Proof and permissions
| Proof item | Strength | Permission |
| --- | --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The brief is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a review, an interview, a testimonial in the proof stack), with the source named. The single message, tone notes and example lines you write go in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/09-creative-strategy/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the single message and insight chosen, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] One objective, one segment, one awareness level and one single message (named pillar or promise).
- [ ] The insight is a buyer truth with an evidence ID, not a feature.
- [ ] Reason to believe uses only proof in the proof stack or inputs, with strength and permission; gaps are named.
- [ ] CTA and every term in mandatories exist in `offer.md` exactly; no assumed price, discount, deadline, guarantee or bonus.
- [ ] Platform specs are cited with a dated first-party source or marked *to confirm*.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Give the makers one audience, one insight and one message with its proof, and let them be creative about the execution, not the strategy. Creative brief, The Complete Marketing System, section 9 Creative Strategy (Servidad, 2026); Bill Bernbach (Doyle Dane Bernbach); Leo Burnett; Ogilvy on Advertising (David Ogilvy); Rule of One, Great Leads (Masterson & Forde).
