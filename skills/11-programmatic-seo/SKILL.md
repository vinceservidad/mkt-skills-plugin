---
name: 11-programmatic-seo
description: Plan or vet templated pages at scale from a data set without thin or doorway content. Use for programmatic SEO, auto-generated pages, city or integration pages, catalog templates.
metadata:
  section: "11 Distribution"
  covers: "Programmatic SEO"
---
# Programmatic SEO

Programmatic SEO builds many pages from one template and a data set. It works when every page answers a distinct search with something real the business holds (inventory, data, documented experience), so each page is the best answer for its own query. It fails, and can harm the whole site, when the pages differ only by a swapped word: city pages for a service that is the same everywhere, or filler text spun to make empty rows look full. The data decides how many pages deserve to exist, not the spreadsheet's length.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: whose searches the pages serve.
- If present, also read `context/awareness.md` → Journey, Voice of customer, Segments; `context/offer.md` → Core offer, Value ladder; `context/positioning.md` → Target customer; the proposed data set, keyword or Search Console data, page inventory and any notes on what the business holds per row in `inputs/`; any work in `work/11-distribution/11-seo-*.md` or `work/11-distribution/11-site-architecture-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (for example interview notes in `inputs/` but no ICP): run the skill that fills it first, then continue.
  - **It doesn't:** stop. Name the missing section with the skill that fills it (ICP and personas → `02-icp-persona`), and ask for evidence about the buyer, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- No data set is not a stop: say what data each page would need, and plan nothing at scale until it exists.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.

## Process

Use [references/pseo-guide.md](references/pseo-guide.md) for the value test, the quality gates and the platform-claims rule.

1. **The outcome and the pattern.** Name the business outcome the pages should produce and the search pattern (head term plus modifier, such as *bookkeeping for* + *agency type*). Show the evidence that people search the pattern (keyword export, Search Console queries), with tool volumes labelled estimates. No evidence for a modifier is a finding, not a gap to fill with guesses.
2. **Audit the data, row by row.** For each proposed page type, list the fields each row has and which are unique, true and useful to the searcher (not just the modifier name). Count rows that pass and fail with [scripts/tally.py](scripts/tally.py) or a line-by-line table, never by eye. Rows without enough real data are excluded, not padded.
3. **The value test.** For each page type, answer: does the page answer a distinct intent, with something the business genuinely has, that a searcher could not get from one general page? A location or type page where the service, price and content are identical everywhere is a doorway page: reject it and say what single page serves that intent instead.
4. **The template.** For the page types that pass: the sections, which data field fills each, what must be unique per page, the title and H1 pattern, the call to action (only offers that exist), the hub page and internal links (with `11-site-architecture`), canonicals, and the structured data if any (with `11-schema`). AI-written or spun text never stands in for missing data.
5. **Quality gates.** Before any page is indexable: minimum real fields per page, a duplication check across pages, a human review sample, an owner who checks facts, and a rule for rows whose data changes (sold out, discontinued, out of date): keep with status, redirect to the nearest equivalent, or noindex, as a proposal.
6. **Pilot, then decide.** Publish a small batch (the rows with the strongest data and search evidence), measured on indexing, impressions for the target queries and the business outcome over a stated window. Keep, change and stop rules are written in advance; label the batch size and window as heuristics. Expanding beyond the pilot is a new decision with its own evidence.
7. **Platform facts.** Search engines' spam policies (doorway pages, scaled or auto-generated content), indexing behaviour and quality guidance change: cite the engine's own current documentation with URL and date, or mark *to confirm*. Never state one from memory as current.
8. **Approval.** Publishing, deleting, redirecting or noindexing pages is a live change: scope, expected effect, risk, rollback, and the owner's approval before anything is built or published. Nothing is published by this plan.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features, benchmarks, platform capabilities or delivery terms that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Describe each source only as it reads. Third-party benchmarks (traffic per page, indexing rates) are not evidence about this site; leave them out. Competitor claims need a dated source or an `(assumption)` label.

## Output

Write `work/11-distribution/11-programmatic-seo-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Programmatic SEO plan: <site, page types>
Skill: 11-programmatic-seo · Date: <YYYY-MM-DD> · Framework: Programmatic SEO (data set → template → quality gates → pilot)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing built or published
## Outcome and search pattern
| Page type | Pattern | Search evidence (source, estimate) |
| --- | --- | --- |
## Data audit
| Page type | Rows | Rows with enough real data | Unique fields per page | Excluded rows and why |
| --- | --- | --- | --- | --- |
## Value test: build, merge or reject
| Page type | Distinct intent? | Real data the business holds | Decision | Instead (for rejected types) |
| --- | --- | --- | --- | --- |
## Template
## Quality gates
## Pilot and stop rules
## Not now
## Platform facts
| Fact the plan relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/` and publish nothing. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a data file, a page, a note), with the source named. Write your own titles, patterns and template text in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, which page types to build, merge or reject and why, the pilot, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every page type has search evidence (labelled estimates) or is marked as unevidenced; no volumes are invented.
- [ ] The data audit counts rows that pass and fail with `tally.py` or a line-by-line table; rows without real data are excluded, not padded with generated text.
- [ ] Page types that differ only by a swapped word (doorway pages) are rejected, with the single page that serves the intent instead.
- [ ] The template names the unique data per page, the hub and internal links, and only offers that exist.
- [ ] Quality gates, a pilot batch with keep, change and stop rules, and a rule for changing or sold-out rows are set before any page is indexable.
- [ ] Every search-engine policy fact is cited with a dated official URL or marked *to confirm*; nothing is published without the owner's approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Build a page for every row that answers a distinct search with real data you hold, and no page for rows that only swap a word: the data decides how many pages deserve to exist. Programmatic SEO (data set, template, quality gates, pilot), The Complete Marketing System, section 11 Distribution (Servidad, 2026); Google Search Central spam policies on doorway pages and scaled content (verify current wording).
