---
name: 06-category-design
description: Name and own a new problem and category instead of competing in an old one. Use for category design, creating a category, category name, point of view on the problem.
metadata:
  section: "06 Positioning"
  covers: "Category Design"
---
# Category design

Buyers file every new thing under a category they already know, and judge it by that category's rules. If the business keeps being judged by rules it loses on (*you looked like bookkeepers*), one answer is to change the frame: name a problem buyers already feel but no category solves, name the category that solves it, and teach the market to see it that way. That is category design. It can make a business the default choice in its own space, and it is also the slowest, most expensive kind of positioning, because it creates demand instead of capturing it. So the first output of this skill is a decision, not a name: design a new category, own a subcategory, or win the existing one.

## Needs (read before writing)

- Required (drafted or confirmed, with content):
  - `context/positioning.md` → **Positioning statement**, written by `06-positioning-statement`: the current position, category frame, target customer and differentiation.
  - `context/market.md` → **Competitors and alternatives**, written by `01-competitor-profiling`: the categories buyers already use and what the alternatives claim.
- If present, also read:
  - `context/positioning.md` → Category, Differentiation, Unique mechanism, and any earlier Category design;
  - `context/market.md` → Demand (`01-demand-check`), Market sophistication, Market definition, Size;
  - `context/customer.md` → Pains desires and fears, Jobs to be done, Beliefs objections and drivers, Voice of customer, Buying triggers and process;
  - `context/offer.md` → Core offer and Urgency and scarcity (capacity);
  - `inputs/`: keyword exports, search observations, industry data, sales-call notes.
- If a required section is missing:
  - **Its upstream exists** (customer ICP and alternatives for the positioning statement; dated competitor notes for the competitor section): run `06-positioning-statement` or `01-competitor-profiling` first, then continue.
  - **It doesn't:** stop. Name each missing section with its owner (Positioning statement → `06-positioning-statement`; Competitors and alternatives → `01-competitor-profiling`), and ask for customer evidence and dated competitor observations. Never design a category from your sense of the market or from famous category stories. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If `01-competitor-profiling` is not loaded, stop and say: enable mkt-q1-audience.

## Process

Use [references/category-design.md](references/category-design.md) for the tests, the parts of a category and the traps.

1. **The frame buyers use today.** From the evidence: which category buyers put the business in, the words they use, what they compare it with, and where that frame hurts (losses or objections caused by the frame). Cite each.
2. **The evidence test.** Score the case for a new category on five conditions, each *met*, *partly* or *not met*, with evidence:
   - **A felt problem no category owns:** buyers describe a problem the existing categories don't solve (their words, lost deals to a mismatch).
   - **The current frame costs deals:** losses or objections come from being filed in the wrong category.
   - **A real difference to anchor it:** a differentiator or unique mechanism that exists today.
   - **Demand signal:** buyers search for or ask about the problem (search data, call questions), or the absence of such data is named.
   - **Capacity to educate:** time, budget and team to teach a market, and delivery capacity to serve the demand it creates. Unknown is a real answer; never assume a budget.
3. **Decide.** One of:
   - **Win the existing category** when buyers already know how to buy it and the business can win on its criteria;
   - **Own a subcategory** (*the X for Y*, or a named problem inside an existing category) when the difference is real but demand lives in the existing search terms;
   - **Design a new category** only when most conditions are met.
   State the decision as a recommendation with its reasons, what would change it, and the cost of the path not taken. If the user has already decided, record it as the owner's decision, and still state plainly the evidence for and against.
4. **Design the parts** (for a subcategory, the lighter version of each):
   - **Problem:** the named problem, in the buyer's language, with the evidence that buyers feel it.
   - **Category name:** two or three candidates in italics, descriptive enough to be understood without explanation, untested, not cleared. Compare with the terms buyers search and say.
   - **Point of view:** the old way, why it fails now (from evidence), the new way, and why this business delivers it (the differentiation and mechanism). A short draft, marked for the owner's review.
   - **Category king criteria:** what would show the business owns the category (buyers using the term, search for it, being named first), each measurable.
5. **Plan the lightning strike only as far as the evidence goes.** List the moments and assets a launch would need (POV document, sales framing, a launch moment) and who owns them (`12-launch`, `08-message-doc`, `11-pr`). Leave dates, budgets, media and partners to the owner: do not invent them.
6. **Test before committing.** A cheap test first: frame the next set of sales calls around the named problem and log reactions; check search and call language for the term over a stated period; hand search questions to `01-demand-check`. Name the result that would stop the effort.
7. **Check before saving.** Re-read the draft against the Checks and run `scripts/check_quotes.py`. Fix every failure before you save.

**Nothing the context doesn't support.** No market size, search volume, trend, budget, timeline, competitor move or case-study outcome that isn't in `context/` or `inputs/`. Famous category stories are illustrations, not evidence for this business, and are never used to promise a result. Inferences carry `(assumption)`.

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from a source, with the source named. Category names, the point of view and your summaries go in italics or plain text. Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py context/positioning.md`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches.

## Output

Write `context/positioning.md` → `## Category design`, replacing that section's body and leaving every other section (and every other file) exactly as it was:

```markdown
## Category design
Status: draft (<YYYY-MM-DD>, 06-category-design)
Written by: 06-category-design, <YYYY-MM-DD>
Frame today: <the category buyers use, their words, where it costs deals — with evidence>
| Condition | Met / partly / not met | Evidence |
| --- | --- | --- |
Decision: <win existing / own subcategory / design new category> — recommendation or owner's decision; reasons; what would change it; cost of the other path
Problem: <named problem, buyer's language, evidence>
Category name candidates: *<name>*, *<name>* — untested, not cleared; vs the terms buyers use: <…>
Point of view (draft): <old way → why it fails → new way → why us>
Ownership signals: <measurable signs of owning it>
Lightning strike: <assets and owners; dates, budget and media left to the owner>
Test first: <what, how long, stop rule; demand questions → 01-demand-check>
Evidence: <sources>
Method: Category Design, Play Bigger (Ramadan, Peterson, Lochhead, Maney); Positioning (Ries & Trout)
```

- Write only this section: no separate POV document, manifesto or launch file. Assets go to their owner skills as hand-offs.
- When the section says what the business does or doesn't offer, match `offer.md`'s wording; a link between offer items that `offer.md` doesn't state (who delivers what, what feeds what) carries `(assumption)`.
- Never set `confirmed` unless the user approves.
- If the decision changes the category frame in `## Category` or the statement, hand that to `06-positioning-statement`; do not edit those sections.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.

Reply with:
- the decision in one line and the condition it hinges on;
- the cheapest test and its stop rule;
- the next skill: `06-positioning-statement` (if the frame changes), `08-message-doc` (POV into the message), or `01-demand-check`.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The decision comes after the five-condition evidence test, and names the cost of the path not taken; a new category is never the default.
- [ ] The problem is in the buyer's language with sources; the frame today cites evidence of where it costs deals.
- [ ] Category name candidates are in italics, compared with the terms buyers actually use, and marked untested and not cleared.
- [ ] The point of view uses only differentiators and mechanisms that exist today.
- [ ] No budget, date, search volume, market size or competitor move is invented; the lightning strike leaves those to the owner.
- [ ] A cheap test with a stop rule comes before any commitment.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean. No unmarked inference.
- [ ] Only `## Category design` changed. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

If you cannot be first in an existing category, create one you can be first in, but only when buyers feel a problem no category owns and you can afford to teach the market; otherwise own a subcategory where the demand already is. Category Design, Play Bigger (Al Ramadan, Dave Peterson, Christopher Lochhead, Kevin Maney); Positioning: The Battle for Your Mind (Al Ries and Jack Trout); The Complete Marketing System, section 6 Positioning (Servidad, 2026).
