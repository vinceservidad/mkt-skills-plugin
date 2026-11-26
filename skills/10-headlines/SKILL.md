---
name: 10-headlines
description: Write headlines, subheads and leads by awareness level, using Bly's types, Great Leads, the 4Us and open loops. Use for headline options, hooks for a page top, taglines to test or a weak headline.
metadata:
  section: "10 Copywriting"
  covers: "4Us (Masterson); Bly's headline types; Headline formulas; Open loops / curiosity gap"
---
# Headlines and leads

The headline does most of the work: it decides whether anything else is read. A headline is chosen for the reader's awareness level. Most-aware readers get the product and the deal, unaware readers get a story or an identity hook. Every headline carries the promise in a form the offer can keep.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/message.md` → **Promise**, from `08-message-doc`.
- `context/awareness.md` → **Awareness map**, from `03-awareness-map`.
- If present, also read `context/customer.md` → Voice of customer (`02-voc-mining`) for the buyer's phrases; `context/message.md` → Big idea, Mechanism and Proof stack; `context/offer.md` for real terms.
- If a required section is missing:
  - **The upstream evidence exists:** run the skill that fills it first, then continue. If that skill is not loaded, stop and say: enable mkt-q1-audience.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Promise → `08-message-doc`; Awareness map → `03-awareness-map`), and what the user should bring. Do not write copy on an invented offer, promise or proof. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Fix the target:** the asset (page, email, ad), the traffic, and its awareness level from the map.
2. **Choose the lead type for that level,** using [references/headline-types.md](references/headline-types.md): offer or promise for most and product aware, problem–solution or big secret for solution and problem aware, story or proclamation for unaware.
3. **Write 15–25 headlines across Bly's headline types:** direct, indirect, news, how-to, question, command, reason-why, testimonial (Caples' tested types are among them). Kennedy's headline formulas are a source of shapes ([references/headline-types.md](references/headline-types.md)). Build them from the promise, the mechanism and Voice of customer phrases. A testimonial headline must quote a real testimonial word for word.
4. **Score each on the 4Us (Masterson)** (useful, urgent, unique, ultra-specific, 1–4 each). Check that the offer can keep every specific in it. Cut any that promise more than the context supports.
   Write nothing in the copy that the context doesn't support: no illustrative guidance, no generalisations such as *many people* or *most customers*, and no delivery terms, timings or conditions beyond what `offer.md` says. If the copy needs it, put it under Open questions instead.
5. **Write two or three leads,** the opening paragraph after the headline, for the top headlines.
6. **Recommend three to test,** each with the reason and what the test would learn.
7. **Run the Anti-AI second pass** in [references/anti-ai-check.md](references/anti-ai-check.md): name the reader, fix the 6 whole-piece rules and all 13 sentence issues (0 em dashes, no buzzwords, no "It's not X, it's Y", no colon reveals, no negative listing), and reread once as the reader.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

## Output

Write `work/10-copywriting/10-headlines-<YYYY-MM-DD>.md`. When you write more than one the same day, add `-<slug>` after the date, for example `work/10-copywriting/10-headlines-2026-11-13-<slug>.md`:

```markdown
# Headlines: <what it is for>
Skill: 10-headlines · Date: <YYYY-MM-DD> · Awareness level: <level> · Framework: <name>
Built from: <context sections used, with their status (draft or confirmed)>
## Copy
<the copy>
## Claims and proof
| Claim in the copy | Proof or source |
| --- | --- |
Scores: <headline — U1 U2 U3 U4 — total>
To test: <three headlines, and what each test would learn>
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

- [ ] The awareness level and lead type are stated, and the headlines fit that level.
- [ ] At least 15 headlines across several Caples types (within Bly's headline types), each scored on the 4Us.
- [ ] Every specific (a number, a time frame, a result) is kept by the offer or proved in context, and listed in the claims table.
- [ ] Testimonial headlines quote real testimonials word for word. Headlines are not wrapped in quotation marks, and `check_quotes.py` reports clean.
- [ ] Three are recommended to test, with the reason for each.
- [ ] The Anti-AI second pass in `references/anti-ai-check.md` (reader check, 6 whole-piece rules, 13 sentence fixes with 0 em dashes, and final reread) is completed.
- [ ] No file in `context/` changed.

## Principle and source

The headline decides whether anything else is read, so choose it by the reader's awareness level and make it specific enough to believe. Tested Advertising Methods (John Caples); Great Leads (Michael Masterson & John Forde); 4Us (Michael Masterson); Bly's headline types (Bob Bly, The Copywriter's Handbook); headlines by awareness, Breakthrough Advertising (Eugene Schwartz); The Complete Marketing System, section 10 Copywriting (Servidad, 2026).
