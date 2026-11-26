---
name: 09-angle-matrix
description: Generate ad angles across awareness level, emotional driver and format, where every cell is a test. Use for ad angles, what to test next in creative, creative ideas, guerrilla or meme-style ads.
metadata:
  section: "09 Creative Strategy"
  covers: "Angle; Angle matrix; Guerrilla marketing; Memes / culture-jacking"
---
# Angle matrix

The angle is the strategy; the ad is only its execution. One offer has many angles: the pain it ends, the desire it serves, the fear it removes, the enemy it opposes, the mechanism that makes it work, the proof that it does. An angle matrix lays the angles out against the buyer's awareness level and the format that carries them, so each cell is a distinct test, and shows which cells the evidence can support today.

Save the matrix as a Markdown file in `work/09-creative-strategy/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as brainstorming or questions. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/message.md` → **Promise**, from `08-message-doc`.
- `context/awareness.md` → **Awareness map**, from `03-awareness-map`.
- If present, also read `context/customer.md` → Voice of customer (`02-voc-mining`), Pains, desires and fears, Beliefs, objections and drivers and Segments; `context/awareness.md` → Traffic temperature; `context/message.md` → Big idea, Mechanism, Enemy, Proof stack, Objection map and Message house; `context/offer.md` → Core offer, Price and model, Guarantee; `context/brand.md` → Brand foundation and Voice; any past ad results in `inputs/`.
- Voice of customer missing? Continue, but say the angles rest on the message and awareness map only, and lower confidence.
- If a required section is missing:
  - **The upstream evidence exists** (for example interviews or reviews in `inputs/` for the awareness map): run the skill that fills it first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Promise → `08-message-doc`; Awareness map → `03-awareness-map`), and ask for evidence (interviews, reviews, sales-call notes), not a description of the buyer. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If `03-awareness-map` is not loaded, stop and say: enable mkt-q1-audience.

## Process

Use [references/drivers-and-formats.md](references/drivers-and-formats.md) for the driver definitions, format list, and the rules for guerrilla and meme angles.

1. **Fix the scope:** the offer or promise being advertised, the segment, the channels in play and their traffic temperature. One matrix per offer and segment.
2. **Rows: awareness levels** from the awareness map, with each level's share or *unknown* exactly as the map gives it. Keep levels the map marks as not worth targeting, but mark them *not now*.
3. **Columns: emotional drivers** that have evidence. For each driver, cite the evidence ID (a VoC quote, a pain, an objection, a proof item). A driver with no evidence for this buyer is left out, or listed under *untested drivers* as an `(assumption)`. Never fill a column because the framework has one.
4. **Fill the cells.** Each cell is one angle: a one-line reason to care, in italics, for that level and driver, plus the evidence it rests on and the proof it needs. A cell whose angle needs proof that does not exist (a result, a comparison, a number) is marked *gated: needs <proof>* and is not testable yet. A cell that would promise something the offer doesn't do is dropped, with the reason.
5. **Pick formats per cell** (static, carousel, short video, UGC, long-form, native post, search). The format is a hypothesis about how the angle lands on that channel, not a fact about the platform. Any claim about current platform formats, specs or what an algorithm favours must cite the platform's own documentation with the URL and date checked, or be marked *to confirm*.
6. **Choose the first tests.** Pick three to six cells: the levels the map says to win first, the strongest evidence, and angles that differ from each other in the driver, not only in wording. For each, state the hypothesis, the one variable that differs from its comparison cell, the outcome that decides it (a qualified business outcome such as booked calls, trials or orders; never clicks or CTR alone), and a stopping rule. Hand detailed test design to `18-creative-testing`.
7. **Guerrilla, memes and culture-jacking** go in only when the user asks or the brand's voice allows it. Each needs a named risk check (brand fit, legal and IP rights, sensitivity and timing). Trends are dated observations, never facts asserted from memory.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, guarantees, offers, features or delivery terms that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Claims about competitors or what *everyone in the category says* need a dated source or an `(assumption)` label. "Volume wins" and "creative is the biggest lever" are heuristics from the system map, not proof for this account; label them that way if you use them.

## Output

Write `work/09-creative-strategy/09-angle-matrix-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Angle matrix: <offer> for <segment>
Skill: 09-angle-matrix · Date: <YYYY-MM-DD> · Framework: Angle matrix (awareness × driver × format)
Built from: <context sections used, with their status (draft or confirmed)>
Scope: <offer · segment · channels · traffic temperature>
## Matrix
| Awareness level (share) | <Driver 1 (evidence)> | <Driver 2 (evidence)> | … |
| --- | --- | --- | --- |
| <level> | *<angle>* · evidence <ID> · proof <item or gated: needs …> · format <…> | … |
Untested drivers: <driver — why no evidence — what would test it>
Dropped cells: <cell — reason>
## First tests
| Cell | Hypothesis | Variable vs comparison | Decides it (outcome) | Stop rule |
| --- | --- | --- | --- | --- |
## Guerrilla and memes (only if in scope)
## Claims and sources
| Claim or angle | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The matrix is a deliverable, not a decision; the business's message and awareness map stay with their owners.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a review, an interview, a VoC line), with the source named. Write every angle, line and label you compose in italics or plain text, never in quotation marks; in table cells, paraphrase and cite the ID. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/09-creative-strategy/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the first cells to test and why, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Rows are the awareness map's levels, with shares exactly as the map gives them (or *unknown*).
- [ ] Every driver column and every cell cites evidence; drivers without evidence are listed as untested, not filled.
- [ ] Cells that need missing proof are marked *gated*; no cell promises what the offer doesn't do.
- [ ] First tests differ in one strategic variable each and are decided by a business outcome, not clicks or CTR alone, with a stop rule.
- [ ] No platform format, spec or algorithm claim is stated as current without a dated first-party source; otherwise *to confirm*.
- [ ] Guerrilla or meme angles, if any, carry a brand, rights and sensitivity check.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

The angle is the strategy and the ad is the execution: one offer has many angles, and each cell of awareness × driver × format is a separate, evidence-backed test. Angle matrix, The Complete Marketing System, section 9 Creative Strategy (Servidad, 2026); levels of awareness, Breakthrough Advertising (Eugene Schwartz); message-market-media match (Dan Kennedy).
