---
name: 06-competitor-pages
description: Write comparison and alternative pages that hold the position honestly. Use for X vs Y pages, alternatives to competitor pages, comparison tables. Not for competitor research (01-*).
metadata:
  section: "06 Positioning"
  covers: "Comparison / alternative pages; Competitive posture playbook (Kotler)"
---
# Competitor pages

A buyer who searches *X vs Y* or *alternatives to X* is close to a decision and suspicious of every vendor's page. The page that wins their trust is the one that is fair: it says who each option is best for, including when the competitor is the better fit, states only facts it can show with a date, and makes the business's position obvious to the buyer it is actually for. A page that sneers, guesses at a rival's prices or overclaims is a liability as well as a weak page.

Save the page as a Markdown file in `work/06-positioning/` when the required context is present. Writing this deliverable is the task, even when the request is worded as a question.

## Needs (read before writing)

- Required (drafted or confirmed, with content):
  - `context/positioning.md` → **Positioning statement**, written by `06-positioning-statement`: the position the page must hold, and who the business is for and not for.
  - `context/market.md` → **Competitors and alternatives**, written by `01-competitor-profiling`: dated facts about each alternative, and where each wins and loses.
- If present, also read:
  - `context/positioning.md` → Target customer, Competitive alternatives, Differentiation, Unique mechanism;
  - `context/offer.md` → Core offer, Price and model, Guarantee: the business's own terms, quoted as they are;
  - `context/message.md` → Proof stack and Objection map; `context/customer.md` → Voice of customer, Current alternatives; `context/brand.md` → Voice;
  - `inputs/`: newer competitor observations, with dates.
- If a required section is missing:
  - **Its upstream exists** (customer ICP and alternatives for the positioning statement; competitor notes in `inputs/` for the competitor section): run `06-positioning-statement` or `01-competitor-profiling` first, then continue.
  - **It doesn't:** stop. Name each missing section with its owner (Positioning statement → `06-positioning-statement`; Competitors and alternatives → `01-competitor-profiling`), and ask for dated competitor observations and customer evidence. Never write a comparison from memory of what a competitor offers. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- The business's price, guarantee and terms are the owner's commitments: use them only as `offer.md` states them. If the page needs a term that isn't there, ask; never generate it.
- If `01-competitor-profiling` is not loaded, stop and say: enable mkt-q1-audience.

## Process

Use [references/comparison-pages.md](references/comparison-pages.md) for page types, structure and the rules on competitor facts, and [references/kotler-competitive-posture.md](references/kotler-competitive-posture.md) for Kotler's competitive posture framing.

1. **Pick the page type and the reader.** *Us vs X*, *alternatives to X*, *us vs DIY, a hire or doing nothing*, or *best options for <buyer>*. Name the buyer from Target customer, and what they are trying to decide.
2. **Gather the facts, with dates.** For every alternative on the page, take only facts in `market.md` or dated `inputs/`: its stated promise, its price as observed (or *not shown*), its claims labelled as its claims, where it wins and loses from buyer evidence. Keep two kinds of gap apart: *not shown* means the observation looked and the item was absent (a price not on the pricing page); *not checked* means nobody looked (a guarantee, a service channel, reviews the scan didn't cover). Never write *none*, *no* or *not seen on the pages we checked* for something the recorded observation didn't look for. An absence that is only inferred from a partial scan (an upstream note such as *not listed on the pages seen*) is still *not checked* on the page: write *not checked, ask them* in the table and body, and put the inferred note on the *Verify before publishing* list. A public page about a named company never implies it lacks something no one explicitly looked for. That includes sentences that bundle the competitor into a gap, such as *neither of us offers X*, *unlike X, we…* or *only we…*: write them only when the observation records X's side; otherwise speak for the business alone (*we don't offer X*). Facts older than the newest observation, or seen on a single day, go into the *Verify before publishing* list.
3. **Decide the fair verdict.** From the positioning and the buyer evidence: who the business is the better choice for, who the competitor is the better choice for, and what is unknown. Every comparison row must be one the business can stand behind; if an option wins on a criterion (a lower price, a feature), say so.
4. **Write the page**:
   - a headline and intro in the buyer's language that name the decision, not an attack;
   - a short answer up front: who should choose which;
   - a comparison table on the criteria the target customer uses (from Differentiation and the buyer's questions), with *not shown* or *unknown* where evidence is missing, never a guessed tick or cross;
   - the business's case, from the positioning, mechanism and proof stack;
   - when the alternative is the better fit, said plainly;
   - switching or next step, using only real offers and terms;
   - an FAQ only from questions buyers actually asked, answered from the context.
5. **Claims and sources.** Add a table that traces every claim about either party to its source and date (including who-it's-for lines such as a size threshold, citing the context section that sets it), and a *Verify before publishing* list: each competitor fact to re-check on their current page, and the date it was last seen.
6. **Publishing is the owner's call.** The page is a draft. Comparative claims about named companies need the owner's review, and legal review where the business normally gets it, before publishing. Use a competitor's name only to identify it: no logos, no implied affiliation, no claims about its customers' experience except from cited reviews.
7. **Check before saving.** Re-read the draft against the Checks and run `scripts/check_quotes.py`. Fix every failure before you save.

**Nothing the context doesn't support.** No competitor price, feature, customer count, review score, weakness or lost-deal story that the context doesn't record with a source and date, and none of the business's own results, prices, guarantees or terms beyond `context/`. A competitor's claim (*150+ agencies*, *4.6 out of 5*) is written as their claim. Opinions about a competitor are not facts. Don't claim how search engines rank or treat comparison pages; that is a current platform fact you have not verified. Inferences carry `(assumption)` and go to Open questions, not onto the page.

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from a source (a competitor's page as recorded, a review, an interview), with the source named. Page copy you write goes in plain text or italics, never in quotation marks. Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py <file>`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches.

## Output

Write `work/06-positioning/06-competitor-pages-<YYYY-MM-DD>-<slug>.md`:

```markdown
# <Page title>
Skill: 06-competitor-pages · Date: <YYYY-MM-DD> · Framework: Honest comparison (They Ask, You Answer; Obviously Awesome)
Page type: <vs / alternatives / vs DIY / best for> · Reader: <target customer and the decision>
Built from: <context sections used, with their status>
Status: draft — not for publishing until the owner (and legal, where used) reviews the comparative claims
## Page copy
<headline, intro, short answer, comparison table, our case, when the other option fits better, switching / next step, FAQ>
## Claims and sources
| Claim (about us or them) | Source | Date seen |
| --- | --- | --- |
## Verify before publishing
| Competitor fact | Where to re-check | Last seen |
| --- | --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. This is a deliverable, not a decision.

Reply with the file path, the page's one-line verdict (who should choose which), the facts that must be re-verified before publishing, and what is still missing. Next skill: `10-copy-editing` for a final pass, or `11-seo` for search intent and placement.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every fact about a competitor traces to a dated source in the context or inputs; gaps say *not shown* (looked, absent) or *not checked* (never looked), never a guess and never an absence the observation didn't test. Absences inferred from a partial scan appear on the page as *not checked* and only on the verify list as a note.
- [ ] Competitor claims (counts, ratings, speeds) are attributed to the competitor, and no opinion about a competitor is stated as fact.
- [ ] The page says plainly who the competitor is the better fit for, and concedes any criterion it wins (for example price).
- [ ] The business's own claims, prices, guarantees and terms match `context/` exactly; nothing is generated.
- [ ] The page holds the positioning statement: same target customer, same primary difference.
- [ ] A claims-and-sources table and a *Verify before publishing* list are included, and the page is marked draft pending the owner's review of comparative claims.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean. No unmarked inference.
- [ ] No file in `context/` changed.

## Principle and source

Buyers comparing options trust the page that tells them honestly who each option is for, so a comparison page wins by holding the position with dated facts and conceding where the alternative fits better. They Ask, You Answer (Marcus Sheridan); Obviously Awesome (April Dunford); Competitive posture playbook, Marketing Management (Philip Kotler); The Complete Marketing System, section 6 Positioning (Servidad, 2026).
