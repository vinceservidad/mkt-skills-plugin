---
name: 08-objection-map
description: Pair every reason not to buy with the belief to shift, the answer and the proof. Use for FAQ, objection answers in marketing, doubts. Not for live calls (use 14-objection-handling).
metadata:
  section: "08 Message"
  covers: "Objection map"
---
# Objection map

Every unanswered objection is a sale that waits or walks. The objection map pairs each evidenced reason not to buy with the belief that has to shift, the answer that shifts it, and the proof that makes the answer believable. Pages, emails, scripts and FAQs answer objections from this map, instead of improvising.

## Needs (read before writing)

- `context/customer.md` → **Beliefs, objections and drivers**, from `02-buyer-psychology`. It must be present (drafted or confirmed, with content).
- If present, also read:
  - `context/message.md` → Proof stack (`08-proof-stack`), Promise and Message house;
  - `context/offer.md`: Guarantee, Bonuses, and Price and model;
  - Voice of customer, for the buyers' exact words.
- If Beliefs, objections and drivers is missing:
  - **Raw evidence supplied** (call notes, lost-deal reasons, reviews): run `02-buyer-psychology` first, then continue. If it is not loaded, stop and say: enable mkt-q1-audience.
  - **Nothing supplied:** stop. Name every missing section with the skill that fills it (Beliefs, objections and drivers → `02-buyer-psychology`; Research log → `02-customer-research`; Voice of customer → `02-voc-mining`; Proof stack → `08-proof-stack`), and ask for lost-deal reasons, call notes or critical reviews. Never list "common objections" from imagination. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Take the objections from the beliefs section,** in rank order, with their evidence and type.
2. **For each objection, write:**
   - **The belief to shift:** what the buyer must come to believe instead.
   - **The answer:** the reframe, explanation or offer element that shifts it. Use the offer's real terms: the guarantee, bonuses or packaging.
     Build it only from what `offer.md` and the evidence state. Never describe how the service works, who approves, sees or does what, or any step, role or process that no source states. If the answer needs such a fact, write a direction naming the missing fact and put the gap in Proof, or route it to the offer owner (`07-offer-design`). Do not add glosses to evidence either.
   - **The proof:** an item from the proof stack, or a named gap ("collect: …"). See [references/answer-patterns.md](references/answer-patterns.md).
   - **Where it is answered:** the awareness level or stage, and the place (offer page, call script, FAQ, onboarding email).
3. **Send real problems elsewhere.** Some objections reveal a problem with the offer or product, not the message: wrong segment, missing capability, an operations failure. Mark these for `07-offer-design`, `04-pmf-check` or the ICP disqualifiers. Don't paper over them with copy.
4. **Write the answers as directions, not finished copy.** Proposed lines go in italics, not quotation marks.
5. **Check before saving.** Re-read the draft against the Checks and fix any failure.

## Output

Write `context/message.md` → `## Objection map`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Objection map
Status: draft (<YYYY-MM-DD>, 08-objection-map)
Written by: 08-objection-map, <YYYY-MM-DD>
| Objection (evidence, count) | Belief to shift | Answer | Proof (or gap) | Where answered |
| --- | --- | --- | --- | --- |
Not a message problem: <objection → fix in 07-offer-design / 04-pmf-check / ICP>
Evidence: <sources>
Method: Objection map; belief mapping (Brunson)
```

Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/message.md` does not exist, first copy [assets/message.md](assets/message.md) to `context/message.md`, then write this section.

Reply with:
- the top objection and its answer;
- what is not a message problem;
- the next skill: `08-story-epiphany-bridge`, or `10-sales-page`.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

**Quotation marks are evidence.** Put words in quotation marks only when they appear exactly in a source (a review, an interview, the story material), with its ID. Everything you write yourself (a promise, a belief to shift, an answer, a softened claim, a line of copy, a story line) goes in italics: *like this*. Before saving, find every quotation mark in your draft and check the words against the source.
Then run [scripts/check_quotes.py](scripts/check_quotes.py) on the file you wrote (`python3 <this skill's folder>/scripts/check_quotes.py context/message.md`). For every line it prints, copy the exact words from the source or drop the quotation marks and use italics, then run it again until it reports every quotation matches.

## Checks

- [ ] Every objection comes from the evidence with its count. None is a generic "common objection".
- [ ] Every objection has a belief to shift, an answer, proof (or a named gap) and a place where it is answered.
- [ ] Answers use only real offer terms and real proof. No invented guarantees, results or testimonials.
- [ ] Every process, access, approval or role fact in an Answer cell traces to `offer.md` or a source; otherwise it is a named gap or routed out.
- [ ] Objections that reveal offer, product or fit problems are routed out, not answered with copy.
- [ ] Quotation marks hold only buyers' exact words. Proposed lines are in italics.
- [ ] Only `## Objection map` changed. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

Every reason not to buy needs an answer and the proof behind it, placed where the buyer meets the doubt, and objections that reveal a real flaw get fixed in the offer, not hidden by copy. Belief mapping, Expert Secrets (Russell Brunson); reason to believe (Hopkins); The Complete Marketing System, section 8 Message (Servidad, 2026).
