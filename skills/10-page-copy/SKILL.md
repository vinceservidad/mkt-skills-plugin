---
name: 10-page-copy
description: Write home, about, product, feature and service page copy from the offer and awareness level, using PAS, AIDA, BAB, FAB or a BrandScript. Use for website words. Not for long pages (use 10-sales-page).
metadata:
  section: "10 Copywriting"
  covers: "ACCA; AIDA; BAB (Before–After–Bridge); BrandScript (StoryBrand); FAB; Great Leads (Masterson & Forde); PAS / PASTOR; Problem–Promise–Proof–Proposal"
---
# Page copy

Words on a page exist to move one reader to the next action. Page copy is assembled from the offer, the message and the buyer's own words, not invented. It is written for the awareness level of the traffic that lands on it, and every sentence earns the next one.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Core offer**, from `07-offer-design`.
- `context/message.md` → **Promise**, from `08-message-doc`.
- `context/awareness.md` → **Awareness map**, from `03-awareness-map`.
- If present, also read `context/customer.md` → Voice of customer (`02-voc-mining`) and `context/awareness.md` → Traffic temperature; `context/message.md` → Message house, Proof stack and Objection map; `context/brand.md` → Voice (`05-brand-voice`); and any existing page copy the user supplies.
- If a required section is missing:
  - **The upstream evidence exists:** run the skill that fills it first, then continue. If that skill is not loaded, stop and say: enable mkt-q1-audience; enable mkt-q2-offer.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Core offer → `07-offer-design`; Promise → `08-message-doc`; Awareness map → `03-awareness-map`), and what the user should bring. Do not write copy on an invented offer, promise or proof. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Decide the page's one job** and its reader: which traffic arrives, at what awareness level (use Traffic temperature if present), and the one action you want.
2. **Pick the structure** that fits that level, using [references/structures.md](references/structures.md). For example: PAS or BAB for problem-aware readers, FAB or a feature page for product-aware readers, a BrandScript for a homepage, Problem–Promise–Proof–Proposal for a landing or service page, ACCA where the reader must understand before they trust.
3. **Write the sections in order:** headline and subhead (the promise at this level, as a Great Leads lead chosen by awareness level), the problem in the buyer's words, the solution or mechanism, the benefits ladder, proof, objections answered, and the call to action. Use Voice of customer phrases where they fit.
4. **Tie every claim to its source** in the claims table: proof stack, offer or inputs. A claim with no proof is cut or softened to what is provable. Never add numbers, testimonials, logos, guarantees or prices that the context doesn't hold.
   Write nothing in the copy that the context doesn't support: no illustrative guidance, no generalisations such as *many people* or *most customers*, and no delivery terms, timings or conditions beyond what `offer.md` says. If the copy needs it, put it under Open questions instead.
   Present each source as what it is: two lines from one review are one customer, never *one customer… another said…*.
5. **Edit:** cut adjectives that don't add meaning, make every line specific, and keep one call to action.
6. **Run the Anti-AI second pass** in [references/anti-ai-check.md](references/anti-ai-check.md): name the reader and cut lines that don't serve them, fix the 6 whole-piece rules (max 4 items per sentence list, one point one proof, match terms to the reader, varied paragraph shape), fix all 13 sentence issues (0 em dashes, no buzzwords, no "It's not X, it's Y", no colon reveals, no mid-sentence bold), and reread once as the reader.
7. **Check before saving.** Re-read the draft against the Checks and fix any failure.

## Output

Write `work/10-copywriting/10-page-copy-<YYYY-MM-DD>.md`. When you write more than one the same day, add `-<slug>` after the date, for example `work/10-copywriting/10-page-copy-2026-11-13-<slug>.md`:

```markdown
# Page copy: <what it is for>
Skill: 10-page-copy · Date: <YYYY-MM-DD> · Awareness level: <level> · Framework: <name>
Built from: <context sections used, with their status (draft or confirmed)>
## Copy
<the copy>
## Claims and proof
| Claim in the copy | Proof or source |
| --- | --- |
Open questions: <anything the copy needs that the context doesn't hold>
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

- [ ] The page has one job, one reader at a stated awareness level, and one call to action.
- [ ] The structure named in the header is visible in the copy.
- [ ] Every claim, number, testimonial, guarantee and price is in the claims table with a source from context or inputs. Nothing is invented.
- [ ] Buyer language from Voice of customer is used where it exists. Adjectives are replaced by specifics.
- [ ] The Anti-AI second pass in `references/anti-ai-check.md` (reader check, 6 whole-piece rules, 13 sentence fixes with 0 em dashes, and final reread) is completed.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Every sentence exists to get the next one read, and every claim needs its proof: write to one reader, in their words, at their awareness level. AIDA, PAS, BAB and FAB structures; the slippery slide, The Adweek Copywriting Handbook (Joseph Sugarman); StoryBrand BrandScript (Donald Miller); The Complete Marketing System, section 10 Copywriting (Servidad, 2026).
