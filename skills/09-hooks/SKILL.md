---
name: 09-hooks
description: Write hooks for ads, videos and posts from the hook library, matched to awareness and customer words. Use for hooks, first lines, first three seconds. Not for page headlines (10-headlines).
metadata:
  section: "09 Creative Strategy"
  covers: "Hook"
---
# Hooks

The hook decides whether the rest of the ad or post exists: if the first line or the first three seconds don't earn attention, nothing after them is seen. A good hook speaks to one person at their awareness level, in words they would use, and makes a promise the rest of the piece can keep. A hook that lies to stop the scroll buys a view and loses the viewer.

Save the hooks as a Markdown file in `work/09-creative-strategy/` when the required inputs are present. Creating this deliverable is part of the task. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/message.md` → **Promise**, from `08-message-doc`.
- `context/customer.md` → **Voice of customer** (from `02-voc-mining`) or `context/awareness.md` → **Awareness map** (from `03-awareness-map`). At least one; read both if present.
- If present, also read `context/message.md` → Big idea, Mechanism, Enemy, Proof stack, Story and Objection map; `context/customer.md` → Pains, desires and fears, Beliefs, objections and drivers; `context/awareness.md` → Traffic temperature; `context/offer.md` for real terms; `context/brand.md` → Voice; any angle matrix in `work/09-creative-strategy/09-angle-matrix-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (reviews, interviews or tickets in `inputs/`): run the skill that fills it first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Promise → `08-message-doc`; Voice of customer → `02-voc-mining`; Awareness map → `03-awareness-map`), and ask for evidence (reviews, interviews, comments), not a description of the buyer. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If `02-voc-mining` is not loaded, stop and say: enable mkt-q1-audience.
- If `03-awareness-map` is not loaded, stop and say: enable mkt-q1-audience.

## Process

Use [references/hook-library.md](references/hook-library.md) for the hook types, the three layers of a video hook and the honesty rules, and [references/hook-execution-and-layers.md](references/hook-execution-and-layers.md) for the five hook layers, eight-step execution sequence, structural frames and native voice checks.

1. **Fix the piece and the viewer:** the format (video ad, Reel, post, YouTube intro), the channel, the traffic temperature, and the awareness level from the map. Unaware and problem-aware viewers get hooks about their world, not the product. Every hook in the file is for the level asked; none opens on the product, the box or an internal metric for a cold viewer. Ideas that only suit a warmer level go under Open questions as a one-line note, not as hooks.
2. **Pick the angle** the hook opens: from the angle matrix if one exists, otherwise from the promise, a pain, the enemy or the mechanism, with its evidence ID.
3. **Write hooks across the library:** question, bold claim, contrarian, curiosity gap, pattern interrupt, callout, number, story open. Two or three per type that fits the level; skip a type the evidence can't support (a number hook needs a real number; a bold claim needs proof).
4. **For video, write all three layers:** what is *seen* in the first frame, what is *said* in the first line, and the *on-screen text*. They carry one idea together, and the on-screen text works with the sound off.
5. **Make each hook keepable.** The body that follows must pay off the hook within the next few seconds or lines. Write the one-line payoff next to each hook. No claim, number, result or testimonial the context doesn't hold. Implied comparisons are claims too (*better than the supermarket*, *finally good coffee*): check each hook against the proof stack's unproven claims and the objection map, and drop any that implies one. Customer words go in quotation marks only when copied exactly from a source, with its ID.
6. **Check policy risks:** hooks that assert or ask about the viewer's personal attributes (health, finances, identity) can breach ad policies on some platforms. Flag them *policy check: to confirm* against the platform's current ad policy, rather than stating a rule from memory.
7. **Recommend hooks to test:** three to five that differ in hook type with the same body, so the test isolates the hook. Name the decision metric: early retention or hold rate is a diagnostic only; the deciding outcome is a business one (qualified leads, trials, orders). Hand test design to `18-creative-testing`.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers or features that aren't in `context/` or `inputs/`. No generalisations about buyers in your own lines, including in payoffs and frequency words (*most owners*, *many people*, *everyone*, *so often*, *usually*, *always*), unless a source counts them; say it about the evidence instead (*10 of 12 closed deals*) or mark it `(assumption)`. Mark inferences `(assumption)`, and list what is needed under Open questions. Never assert what a platform's algorithm rewards (for example a watch-time threshold); cite the platform's own documentation with URL and date, or leave it out. "Hook first" is a principle of the system map; any hold-rate benchmark needs a source.

## Output

Write `work/09-creative-strategy/09-hooks-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Hooks: <piece and channel>
Skill: 09-hooks · Date: <YYYY-MM-DD> · Awareness level: <level> · Framework: Hook library
Built from: <context sections used, with their status (draft or confirmed)>
Viewer: <segment · traffic temperature · awareness level> · Angle: <angle — evidence>
## Hooks
| # | Type | Seen (first frame) | Said (first line) | On-screen text | Payoff that follows | Evidence |
| --- | --- | --- | --- | --- | --- | --- |
## Hooks to test
<3–5 hooks, the shared body, the decision metric>
## Claims and sources
| Claim in a hook | Source |
| --- | --- |
## Policy checks to confirm
## Open questions
## Principle, framework, source
```

For text posts, the Seen and On-screen columns may be *n/a*.

Change nothing in `context/`. Hooks are a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a review, an interview, a VoC line), with the source named. Write your own hooks in plain text or italics, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/09-creative-strategy/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the hooks to test and why, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The awareness level and traffic temperature are stated, and every hook fits them; no hook for a cold viewer opens on the product.
- [ ] Hooks span several library types, and each cites the evidence it rests on.
- [ ] Every video hook has seen, said and on-screen layers carrying one idea.
- [ ] No hook states or implies a comparison the proof stack lists as unproven or a review contradicts.
- [ ] Every hook has a payoff the body can keep; no invented number, result, testimonial, claim or unsourced generalisation about buyers (*most owners*, *many people*).
- [ ] Personal-attribute hooks are flagged for a policy check; no platform rule or algorithm claim stated from memory as current.
- [ ] The test isolates the hook and is decided by a business outcome, not hold rate or CTR alone.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

The first line or the first three seconds decide whether the rest is seen, so open on the viewer's own world at their awareness level, and promise only what the body can keep. Hook library, The Complete Marketing System, section 9 Creative Strategy (Servidad, 2026); Hook–Story–Offer, DotCom Secrets (Russell Brunson); Tested Advertising Methods (John Caples).
