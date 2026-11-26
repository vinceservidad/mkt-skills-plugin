---
name: 10-copy-editing
description: Edit existing marketing copy (sales emails, pages, ads) for clarity, proof and flow. Use whenever asked to edit, tighten, proofread or improve copy, even before pasted. Not for new copy.
metadata:
  section: "10 Copywriting"
  covers: "4Cs; Bucket brigade; Copy editing; Damaging admission; Future pacing; Slippery slide (Sugarman)"
---
# Copy editing

Write first, edit ruthlessly: cut every word that doesn't earn its place, and replace adjectives with specifics. Editing improves how the copy says something. It doesn't change what the business offers, and it never makes a claim stronger than the proof allows.

## Needs (read before writing)

- Nothing upstream is required. Read the copy to edit, from the user's message or a file; `context/message.md` → Promise and Proof stack (`08-proof-stack`) to check claims; `context/offer.md` for real terms; `context/brand.md` → Voice (`05-brand-voice`).
- If the material this skill works on is missing, stop and ask for it; never invent it. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Read the copy for its job:** who it's for, what action it wants, and the awareness level. If the copy is missing, the material is missing: stop and ask for it. Never write a "sample" to edit.
2. **Run the 4Cs and Anti-AI second pass,** using [references/editing.md](references/editing.md):
   - Clear: one idea per sentence; plain words.
   - Concise: cut filler, hedges and repetition.
   - Compelling: benefits and outcomes before features; you-focused; active voice.
   - Credible: specifics, and proof under claims.
   - Anti-AI second pass: name the reader and cut lines that don't serve them, fix the 6 whole-piece rules (max 4 items per sentence list, one point one proof, match terms to the reader, no table-row strings, varied paragraph shape, say each thing once), fix the 13 sentence issues (including 0 em dashes, no buzzwords, no "It's not X, it's Y", no mid-sentence bold), and reread once as the reader, rewriting weak spec-sheet paragraphs from scratch.
3. **Check every claim against the context.** If a claim isn't supported by the proof stack, offer or inputs, flag it: *needs proof*. Suggest a softer, provable version. Never strengthen a claim or add numbers, testimonials or guarantees that aren't in the context.
4. **Keep the offer's terms and the writer's voice.** Don't change prices, guarantees or promises; flag anything that contradicts `offer.md`. When editing the user's own draft, keep their voice (their hedges, bluntness, asides and long spoken sentences) and make the smallest edit that fixes the problem.
5. **Return two versions:** a marked-up version and a clean version (plus a short "What changed" list when editing the user's own draft). In the marked-up version, tag each change's one-line reason with the C or Anti-AI rule it serves, such as *[Concise] cut "really": filler*, *[Anti-AI #1] cut "It's not X, it's Y"*, or *[Credible] needs proof: no source for "thousands"*, so the edit shows its reasoning, not only its name.
6. **Check before saving.** Re-read the draft against the Checks and fix any failure.

## Output

Write `work/10-copywriting/10-copy-editing-<YYYY-MM-DD>.md`. When you write more than one the same day, add `-<slug>` after the date, for example `work/10-copywriting/10-copy-editing-2026-11-13-<slug>.md`:

```markdown
# Copy edit: <what it is for>
Skill: 10-copy-editing · Date: <YYYY-MM-DD> · Awareness level: <level> · Framework: <name>
Built from: <context sections used, with their status (draft or confirmed)>
## Copy
<the copy>
## Claims and proof
| Claim in the copy | Proof or source |
| --- | --- |
Flags: <claims that need proof; contradictions with offer.md>
## Principle, framework, source
```

Change nothing in `context/`. Copy is a deliverable, not a decision.

**Quotation marks are evidence.** In the copy, quotation marks hold only words that appear exactly in a source, such as a testimonial from the proof stack or a review in `inputs/`, with its source in the claims table. Do not wrap your own headlines or lines in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/10-copywriting/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the key choice made (structure, angle or level) and what is still missing. Your final reply message must end with the **Principle, framework, source** block, after the still-missing list, on a build and on a stop; nothing comes after it. Writing the block in the file does not replace it in the reply:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The edit keeps the offer's terms, the promise and the brand or writer's voice (smallest edit needed on a user's own draft). Contradictions with `offer.md` are flagged, not silently changed.
- [ ] The Anti-AI second pass in `references/editing.md` (reader check, 6 whole-piece rules, 13 sentence fixes with 0 em dashes, and final reread) is completed.
- [ ] No claim is made stronger than its proof, and no new numbers, testimonials or guarantees are added. Unsupported claims are flagged *needs proof*.
- [ ] Both a marked-up version (with reasons) and a clean version are delivered.
- [ ] Without the copy to edit, nothing was written except a request for it.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.
- [ ] The reply (not just the file) ends with the **Principle / Framework / Source** block, after the still-missing list.

## Principle and source

Edit for the reader: cut every word that doesn't earn its place, replace adjectives with specifics, and never let an edit promise more than the proof allows. 4Cs (Bob Bly, The Copywriter's Handbook); the slippery slide (Joseph Sugarman); The Complete Marketing System, section 10 Copywriting (Servidad, 2026).
