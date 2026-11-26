---
name: 10-sales-page
description: Write a long-form sales page or letter from the offer, proof and objections, with fascinations and a P.S. Use for sales page, order page or direct-response page. Not for webinars (use 10-vsl-script).
metadata:
  section: "10 Copywriting"
  covers: "Bullet-proof fascinations (Bencivenga); Direct response (discipline); Fascinations (bullets); P.S.; QUEST"
---
# Sales page

A sales page is the offer, the proof and the answers to every objection, in the order the reader needs them. Long copy outperforms short when the reader is interested and the price is high, but only if every section is earned. This skill assembles the page from the decisions already made upstream, so it never invents an offer term, a result or a testimonial.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Core offer**, from `07-offer-design`.
- `context/offer.md` → **Price and model**, from `07-pricing`.
- `context/offer.md` → **Guarantee**, from `07-guarantee-risk-reversal`.
- `context/message.md` → **Proof stack**, from `08-proof-stack`.
- `context/message.md` → **Objection map**, from `08-objection-map`.
- `context/awareness.md` → **Awareness map**, from `03-awareness-map`.
- If present, also read `context/message.md` → Story (`08-story-epiphany-bridge`), Promise, Big idea and Mechanism; `context/offer.md` → Bonuses, Urgency and scarcity, and Name and one-liner; Voice of customer.
- If a required section is missing:
  - **Price and model or Guarantee is missing:** stop and ask. These are the owner's commercial commitments; you may offer to run `07-pricing` or `07-guarantee-risk-reversal` as a proposal for approval (if they are not loaded, say: enable mkt-q2-offer), but never write the page on terms nobody approved.
  - **Another section is missing and the upstream evidence exists:** run the skill that fills it first, then continue. If that skill is not loaded, stop and say: enable mkt-q2-offer (for `07-offer-design`, `07-pricing`, `07-guarantee-risk-reversal`) or enable mkt-q1-audience (for `03-awareness-map`).
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Core offer → `07-offer-design`; Price and model → `07-pricing`; Guarantee → `07-guarantee-risk-reversal`; Proof stack → `08-proof-stack`; Objection map → `08-objection-map`; Awareness map → `03-awareness-map`), and what the user should bring. Do not write copy on an invented offer, promise or proof. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Set the reader and level:** the awareness level of the traffic, which decides how long the lead and the problem section run.
2. **Outline in direct-response order** (the direct response discipline: one measurable action, every claim backed by the offer and proof), using [references/sales-page.md](references/sales-page.md) and [references/direct-response-masters.md](references/direct-response-masters.md): headline and lead → problem in their words → story (if Story exists) → mechanism → benefits and fascination bullets → proof → the offer stack (core, bonuses) → price with the anchor → guarantee → objections and FAQ → urgency (only what's true) → close → P.S.
3. **Write each section from its source:**
   - offer terms, price, guarantee, bonuses and urgency exactly as in `offer.md`;
   - proof from the proof stack, with testimonials word for word;
   - answers from the objection map.

   Never add a number, a testimonial, a bonus value, a deadline or a scarcity claim that isn't there.
4. **Write fascinations:** bullets that tease a specific benefit. Each one must be delivered by the offer.
   Write nothing in the copy that the context doesn't support: no illustrative guidance, no generalisations such as *many people* or *most customers*, and no delivery terms, timings or conditions beyond what `offer.md` says. If the copy needs it, put it under Open questions instead.
   Present each source as what it is: two lines from one review are one customer, never *one customer… another said…*.
5. **Write the P.S.:** restate the promise, the guarantee and the call to action.
6. **Fill the claims table** for every claim in the page.
7. **Run the Anti-AI second pass** in [references/anti-ai-check.md](references/anti-ai-check.md): name the reader, fix the 6 whole-piece rules (max 4 items per sentence list, one point one proof, varied paragraph shape, say each thing once) and all 13 sentence issues (0 em dashes, no mid-sentence bold, no buzzwords, no "It's not X, it's Y", no colon reveals, no recap endings), and reread once as the reader.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

## Output

Write `work/10-copywriting/10-sales-page-<YYYY-MM-DD>.md`. When you write more than one the same day, add `-<slug>` after the date, for example `work/10-copywriting/10-sales-page-2026-11-13-<slug>.md`:

```markdown
# Sales page: <what it is for>
Skill: 10-sales-page · Date: <YYYY-MM-DD> · Awareness level: <level> · Framework: <name>
Built from: <context sections used, with their status (draft or confirmed)>
## Copy
<the copy>
## Claims and proof
| Claim in the copy | Proof or source |
| --- | --- |
Missing for a stronger page: <proof or terms the context doesn't hold>
## Principle, framework, source
```

Change nothing in `context/`. Copy is a deliverable, not a decision.

**Quotation marks are evidence.** In the copy, quotation marks hold only words that appear exactly in a source, such as a testimonial from the proof stack or a review in `inputs/`, with its source in the claims table. Do not wrap your own headlines or lines in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/10-copywriting/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the key choice made (structure, angle or level) and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The page follows direct-response order, and the lead fits the reader's awareness level.
- [ ] Price, guarantee, bonuses, urgency and offer terms match `offer.md` exactly. No invented scarcity, deadlines or bonus values.
- [ ] Every testimonial and result comes from the proof stack or inputs, word for word, and is listed in the claims table.
- [ ] The top objections from the objection map are answered on the page.
- [ ] The Anti-AI second pass in `references/anti-ai-check.md` (reader check, 6 whole-piece rules, 13 sentence fixes with 0 em dashes, and final reread) is completed.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Long copy sells when every section is earned: the offer, the proof and the answer to each objection, in the order the reader needs them, and nothing the business can't stand behind. Direct-response copywriting, Scientific Advertising (Claude Hopkins); The Boron Letters (Gary Halbert); Persuasion Equation and bullet-proof fascinations (Gary Bencivenga); Breakthrough Advertising (Eugene Schwartz); Ogilvy on Advertising (David Ogilvy); QUEST (Michel Fortin); The Ultimate Sales Letter (Dan Kennedy); The Complete Marketing System, section 10 Copywriting (Servidad, 2026).
