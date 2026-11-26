---
name: 09-ugc-brief
description: Brief creators for UGC such as problem-solution, testimonial, unboxing, day-in-the-life and before-after. Use for UGC briefs, creator scripts, briefing TikTok or Reels creators.
metadata:
  section: "09 Creative Strategy"
  covers: "UGC"
---
# UGC brief

UGC works because it is a real person's real experience, filmed the way people film for each other. The brief's job is to point the creator at the moments and words that matter to buyers (from voice of customer) and to the claims that are off-limits, then get out of the way. A UGC brief that scripts a testimonial for someone who hasn't used the product is a fake review, whatever it looks like.

Save the brief as a Markdown file in `work/09-creative-strategy/` when the required inputs are present and the creator terms are confirmed. Creating this deliverable is part of the task. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/message.md` → **Promise**, from `08-message-doc`.
- `context/customer.md` → **Voice of customer**, from `02-voc-mining`.
- If present, also read `context/message.md` → Proof stack, Objection map, Story; `context/awareness.md` → Awareness map, Pains desires and fears, Segments; `context/offer.md` → Core offer and any terms; `context/brand.md` → Voice and Distinctive assets; any `work/09-creative-strategy/09-angle-matrix-*.md` or `work/09-creative-strategy/09-hooks-*.md` file.
- If a required section is missing:
  - **The upstream evidence exists** (reviews, tickets or interviews in `inputs/`): run the skill that fills it first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Promise → `08-message-doc`; Voice of customer → `02-voc-mining`), and ask for evidence (reviews, interviews, tickets), not a description of the buyer. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Creator terms are the owner's commitments.** Payment or free product, usage rights (where and for how long the business may run the content, including as paid ads), exclusivity, revisions and deadlines. If the request needs these in the brief and the owner hasn't given them, stop before writing, ask for each, and write no brief on assumed terms. A brief without terms is fine when the user asks only for the creative direction; then list the terms as *to be set by the owner*.
- If `02-voc-mining` is not loaded, stop and say: enable mkt-q1-audience.

## Process

Use [references/ugc-formats.md](references/ugc-formats.md) for the formats, the brief anatomy and the disclosure and authenticity rules.

1. **Who films:** paid creators, gifted creators, influencers or real customers. Real experience is required for any testimonial, before-after or result: the creator must actually use the product for a stated period first. If they haven't, the format is a demonstration or unboxing, not a testimonial.
2. **Pick the format** per brief: problem-solution, testimonial, unboxing, day-in-the-life or before-after, matched to the awareness level and the evidence. Before-after needs a real, typical before and after; skip it if the evidence doesn't hold one.
3. **Talking points, not a script.** Give the moments that matter to buyers (from VoC themes, with IDs) and questions the creator answers in their own words. Never hand creators customer quotes to say as their own. Hooks may be suggested as options (from `work/09-creative-strategy/09-hooks-*.md` if present), clearly marked as optional.
4. **Must say and must not say.** Must: what the product is and the real terms exactly as `offer.md` states them. Must not: unproven or contradicted claims from the proof stack and objection map, results they haven't had, comparisons with named competitors, medical, financial or other regulated claims, and anything the brand voice rules out.
5. **Disclosure:** the creator discloses the paid or gifted relationship in the way the law and the platform require. State that it is required and that the exact wording and placement are *to confirm* against current law (for example the FTC's endorsement guidance in the US) and the platform's own branded-content tools and rules; don't state the current rule from memory.
6. **Shot list and delivery:** the shots needed (product in use, setting, face to camera), orientation and length *to confirm* against the platform, raw files wanted, captions. Ask for distinct takes on the hook, so the business can test hooks without reshooting.
7. **How content will be used and judged:** organic or paid, and the business outcome it is for; usage beyond what the owner set needs the creator's agreement.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features or delivery terms that aren't in `context/` or `inputs/`. No generalisations about buyers in your own lines, including in payoffs and frequency words (*most owners*, *many people*, *everyone*, *so often*, *usually*, *always*), unless a source counts them; say it about the evidence instead (*10 of 12 closed deals*) or mark it `(assumption)`. Mark inferences `(assumption)` and list what is needed under Open questions. Never write a testimonial for a creator to read. Customers' personal details stay out of the brief. When the creators are customers, the brief tells them to keep private details (revenue, payroll, their own clients' names) out unless they themselves choose to share them, and gets their consent for each use; how the videos are used is for the owner and the customer to agree.

## Output

Write `work/09-creative-strategy/09-ugc-brief-<YYYY-MM-DD>-<slug>.md`:

```markdown
# UGC brief: <product or campaign> — <format>
Skill: 09-ugc-brief · Date: <YYYY-MM-DD> · Framework: UGC and creator frameworks
Built from: <context sections used, with their status (draft or confirmed)>
Status: draft for the owner's approval
Who films: <creator type — must have used the product for <period> before filming a testimonial>
Format: <format — why, awareness level>
## What this is for
## The moments that matter (from customers)
| Moment or theme | Why buyers care (evidence ID) | Question for the creator |
| --- | --- | --- |
## Optional hooks
## Must say
## Must not say
## Disclosure
## Shot list and delivery
## Terms (set by the owner)
<payment · usage rights and duration · exclusivity · revisions · deadline — or "to be set by the owner">
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The brief is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a review, a ticket, an interview), with the source named, and only to show the creator what buyers said, never as lines to repeat. Questions, talking points and suggested hooks go in plain text or italics. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/09-creative-strategy/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the format chosen and why, and what is still missing (including terms for the owner), then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The format fits the evidence and the awareness level; testimonials and before-afters require real use for a stated period.
- [ ] Talking points come from VoC with IDs; no scripted testimonial and no customer quote handed to the creator as their own line.
- [ ] Must-not-say lists the unproven and contradicted claims from the proof stack and objection map.
- [ ] Disclosure is required, with the exact rule *to confirm* against current law and platform rules.
- [ ] Payment, usage rights, exclusivity and deadlines are the owner's; none is invented, and no line generalises about buyers (*most people*) without a source.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

UGC persuades because it is a real person's real experience, so brief the moments and limits from customer evidence and let the creator tell the truth in their own words, disclosed. UGC and creator frameworks (problem-solution, testimonial, unboxing, day-in-the-life, before-after), The Complete Marketing System, section 9 Creative Strategy (Servidad, 2026); Influence (Robert Cialdini), social proof.
