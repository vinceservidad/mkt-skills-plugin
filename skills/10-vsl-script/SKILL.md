---
name: 10-vsl-script
description: Script a video sales letter or webinar with the Perfect Webinar (big domino, three secrets, stack, close). Use for VSL, webinar, masterclass or launch video. Not for pages (use 10-sales-page).
metadata:
  section: "10 Copywriting"
  covers: "Perfect Webinar; Star–Story–Solution; VSL"
---
# VSL and webinar script

A sales video or webinar changes beliefs in order: it names one big domino (the belief that, once knocked over, makes buying inevitable), then rebuilds the vehicle, internal and external beliefs with true stories and proof, then presents the offer. This skill scripts it from the story, offer and proof already decided, never from invented results.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Core offer**, from `07-offer-design`.
- `context/message.md` → **Story**, from `08-story-epiphany-bridge`.
- `context/message.md` → **Big idea**, from `08-message-doc`.
- `context/message.md` → **Proof stack**, from `08-proof-stack`.
  (Story or Big idea: at least one)
- If present, also read `context/offer.md` → Price and model, Guarantee, Bonuses, and Urgency and scarcity; `context/message.md` → Objection map and Mechanism; Beliefs, objections and drivers in `context/customer.md`.
- If a required section is missing:
  - **The upstream evidence exists:** run the skill that fills it first, then continue. If that skill is not loaded, stop and say: enable mkt-q2-offer.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Core offer → `07-offer-design`; Story → `08-story-epiphany-bridge`, or Big idea → `08-message-doc`; Proof stack → `08-proof-stack`), and what the user should bring. Do not write copy on an invented offer, promise or proof. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Name the big domino:** the one belief that, if the viewer accepts it, makes the offer the obvious next step. Take it from the big idea and the top vehicle belief.
2. **Choose the format and length:** a VSL (5–20 minutes, or Star–Story–Solution when the origin story carries the pitch) or a webinar (45–90 minutes, Perfect Webinar). See [references/perfect-webinar.md](references/perfect-webinar.md).
3. **Script it:**
   - the hook and the promise of the talk;
   - the origin story (from Story; skip it if absent, never invent one);
   - three secrets, each rebuilding one belief (vehicle, internal, external) with a true story or proof;
   - the transition;
   - the stack (offer elements from `offer.md`), the price with its anchor, and the guarantee;
   - urgency (only what's true), the close, and a Q&A or objections segment from the objection map.
4. **Mark the slides or visual cues** in brackets, and keep each script line speakable.
   Write nothing in the copy that the context doesn't support: no illustrative guidance, no generalisations such as *many people* or *most customers*, and no delivery terms, timings or conditions beyond what `offer.md` says. If the copy needs it, put it under Open questions instead.
   Present each source as what it is: two lines from one review are one customer, never *one customer… another said…*.
5. **Fill the claims table** for every result, number and testimonial.
6. **Run the Anti-AI second pass** in [references/anti-ai-check.md](references/anti-ai-check.md): name the reader, fix the 6 whole-piece rules (max 4 items per sentence list, one point one proof, varied paragraph shape, spoken lines) and all 13 sentence issues (0 em dashes, no buzzwords, no rhetorical setups or mic-drop endings, no "It's not X, it's Y"), and reread once aloud as the viewer. Keep every number, count, and qualifier strictly identical to `context/` and `inputs/` during the Anti-AI pass; never invent an extrapolated summary count (such as "none of those ten") that is not in the source.
7. **Check before saving.** Re-read the draft against the Checks and fix any failure.

## Output

Write `work/10-copywriting/10-vsl-script-<YYYY-MM-DD>.md`. When you write more than one the same day, add `-<slug>` after the date, for example `work/10-copywriting/10-vsl-script-2026-11-13-<slug>.md`:

```markdown
# Script: <what it is for>
Skill: 10-vsl-script · Date: <YYYY-MM-DD> · Awareness level: <level> · Framework: <name>
Built from: <context sections used, with their status (draft or confirmed)>
## Copy
<the copy>
## Claims and proof
| Claim in the copy | Proof or source |
| --- | --- |
Big domino: <belief>
Running time: <estimate>
## Principle, framework, source
```

Change nothing in `context/`. Copy is a deliverable, not a decision.

**Quotation marks are evidence.** In the copy, quotation marks hold only words that appear exactly in a source, such as a testimonial from the proof stack or a review in `inputs/`, with its source in the claims table. Put each quote in the mouth of the person who said it in that source: never combine words from two sources into one speaker, and never invent who said it. Do not wrap your own headlines or lines in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/10-copywriting/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the key choice made (structure, angle or level) and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] One big domino is named, and three secrets each rebuild a named belief (vehicle, internal, external).
- [ ] Stories and results come only from Story, Proof stack or inputs. No invented case studies, numbers or testimonials.
- [ ] The stack, price, guarantee and urgency match `offer.md` exactly.
- [ ] Objections from the objection map are answered before or in the close.
- [ ] The Anti-AI second pass in `references/anti-ai-check.md` (reader check, 6 whole-piece rules, 13 sentence fixes with 0 em dashes, and final reread) is completed.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] Each quote is attributed to the person and source it came from; no speaker is built from two sources.
- [ ] No file in `context/` changed.

## Principle and source

Change one big belief and the sale follows: knock over the big domino, rebuild the vehicle, internal and external beliefs with true stories, then make the offer. Perfect Webinar, Expert Secrets (Russell Brunson); video sales letter structure; The Complete Marketing System, section 10 Copywriting (Servidad, 2026).
