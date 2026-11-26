---
name: 11-seo
description: Plan SEO with keyword research, on-page, technical health and links. Use for SEO strategy, ranking on Google, organic traffic, keyword plans, SEO audits, or pushing blog posts to page one.
metadata:
  section: "11 Distribution"
  covers: "Guest posting / link building; SEO"
---
# SEO

Organic search pays back slowly and compounds: a page that matches what a buyer is searching for keeps bringing them for years. The job is to find the searches the business's real buyer makes, sorted by what the searcher wants (intent), to fix what stops existing pages being found, and to build topical authority around the problems the offer solves. Rankings and traffic are signals; the outcome is qualified customers. A plan that chases the biggest keyword the buyer never searches, or more pages than the team can write, is not a plan.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: whose searches matter.
- If present, also read `context/awareness.md` → Journey (what each stage asks), Awareness map, Voice of customer (buyer language), Pains, desires and fears; `context/offer.md` → Core offer, Value ladder (free assets to point searchers to); `context/positioning.md` → Category, Positioning statement; `context/market.md` → Demand, Competitors and alternatives; any Search Console, analytics, keyword-tool, crawl, page-inventory or robots.txt material in `inputs/`; any work in `work/11-distribution/11-content-strategy-*.md`, `work/11-distribution/11-site-architecture-*.md` or `work/11-distribution/11-channel-selection-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (for example interview notes in `inputs/` but no ICP): run the skill that fills it first, then continue.
  - **It doesn't:** stop. Name the missing section with the skill that fills it (ICP and personas → `02-icp-persona`, which needs `02-customer-research` evidence), and ask for evidence about the buyer (interviews, sales notes, reviews), not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- No Search Console or keyword data is not a stop: plan from the ICP and journey, mark every volume and ranking *unknown*, and make getting the data the first step.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/seo-guide.md](references/seo-guide.md) for intent, prioritisation, technical checks and the platform-claims rule.

1. **The outcome.** Name the business outcome organic search must produce (qualified calls, subscribers, template downloads that lead to calls) and how it will be measured (analytics landing page to conversion, CRM source). Rankings, impressions and clicks are signals, never the outcome.
2. **Current visibility.** From Search Console or analytics in `inputs/`, total clicks and impressions by page and by query with [scripts/sum_by.py](scripts/sum_by.py) (`python3 <this skill's folder>/scripts/sum_by.py <file> page`), never by eye. Separate branded from non-branded searches. Label each figure *observed*, *calculated* or *inferred*. A third-party tool's volume or rank estimate is an estimate; say so.
3. **Keyword research by intent.** Sort the searches (from the data, the keyword tool, and the buyer's own words in Voice of customer) into informational, commercial, transactional and navigational intent, and map each to the journey stage and awareness level it serves. Score relevance to the ICP and the offer before volume: a large generic term the ICP does not use, or whose searchers the offer cannot serve, is a non-priority, whatever its volume.
4. **Priorities.** Rank actions by expected business impact, confidence, effort and reversibility:
   - **Fix and protect** what already earns clicks and links; never delete or redirect a ranking page without evidence and approval.
   - **Striking distance:** queries already earning impressions where a page sits just off the top results; improve that page's match to intent before writing new ones (the position band is a heuristic).
   - **Cannibalisation:** two pages competing for one intent; choose the one to keep and say what happens to the other (merge, re-target, redirect), as a proposal.
   - **Gaps:** intents the buyer has, with no page that matches; commercial and transactional gaps before informational ones unless the evidence says otherwise.
5. **On-page.** For each priority page: the intent it serves, the title and H1 direction, the questions it must answer (from VoC and the journey), and the next step it offers (only offers that exist in `offer.md` or on the site).
6. **Technical health.** From the material: indexing status, robots.txt rules, canonicals, sitemaps, redirects, orphan pages, duplicate or thin pages, page experience (field data over lab data where both exist). Say what was not checked. Distinguish a crawl problem (pages not fetched) from an indexing problem (fetched, not indexed). Hand off — do not plan or design here — site structure, hub-and-spoke page hierarchy, menu/navigation and internal linking to `11-site-architecture`; structured data to `11-schema`; templated pages at scale to `11-programmatic-seo`; AI answers and AI crawlers to `11-ai-seo-geo`; the editorial calendar to `11-content-strategy`.
7. **Topical authority and links.** Group target topics into clusters around the problems the offer solves (name each cluster's core topic and supporting topics, and hand structural hub hierarchy, navigation/menu and internal-link mapping to `11-site-architecture`). Plan external links the business can earn (original data, tools, partner and podcast pages it already appears on, digital PR via `11-pr`). No paid links, link schemes or doorway pages.
8. **Capacity.** Fit the plan to the stated writing and engineering capacity; if unknown, ask, and give the order of work so the first items stand alone. Give a review rhythm, not a promise of rankings.
9. **Causality and platform facts.** A ranking or traffic change that coincides with a change is a hypothesis until algorithm updates, seasonality, competitors, technical regressions and measurement changes are ruled out. Search engine behaviour (ranking systems, rich-result eligibility, Core Web Vitals thresholds, indexing rules, tool features) changes: cite the engine's own current documentation with URL and access date only if actually opened and verified; otherwise mark *to confirm* with no unverified URL. Never state one from memory as current.
10. **Approval.** Changes to robots.txt, redirects, canonicals, noindex, deleting or merging pages, and site-wide templates are live changes: exact scope, expected effect, risk, rollback, and the owner's approval before anything is changed.
11. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features, benchmarks, platform capabilities or delivery terms that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Describe each source only as it reads. Third-party benchmarks (a "typical" click-through rate by position, traffic you will get) are not evidence about this site; leave them out. Competitor claims need a dated source or an `(assumption)` label.

## Output

Write `work/11-distribution/11-seo-<YYYY-MM-DD>-<slug>.md`:

```markdown
# SEO plan: <site, period>
Skill: 11-seo · Date: <YYYY-MM-DD> · Framework: SEO (keyword research by intent, on-page, technical, links, topical authority)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing on the site changed
## Outcome and measurement
## Current visibility
| Page or query group | Clicks | Impressions | Avg position | Label |
| --- | --- | --- | --- | --- |
## Keywords by intent
| Search (or group) | Intent | Journey stage / awareness | Relevance to ICP and offer | Volume (source, estimate) | Page that serves it | Action |
| --- | --- | --- | --- | --- | --- | --- |
## Priorities
| # | Action | Why (evidence) | Impact / confidence / effort | Reversible? | Owner skill |
| --- | --- | --- | --- | --- | --- |
## On-page briefs
## Technical health
| Check | Finding (evidence) | Proposed fix | Needs approval |
| --- | --- | --- | --- |
## Topical clusters and links
## Not now
## Capacity and review rhythm
## Platform facts
| Fact the plan relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`, and change nothing on the site. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a page, a review, an interview, a search query in an export), with the source named. Write your own titles, headings and proposals in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the top three actions, what is not a priority and why, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The plan names a business outcome; rankings, impressions and traffic are treated as signals, not the outcome.
- [ ] Visibility figures are totalled with `sum_by.py` from the supplied data and labelled; tool estimates are called estimates; missing data is marked unknown, not filled in.
- [ ] Every priority keyword has an intent, a journey stage, and relevance to the ICP and offer; high-volume generic terms the buyer does not use are non-priorities.
- [ ] Existing ranking pages are protected; merges, redirects, robots, canonical and noindex changes are proposals needing the owner's approval.
- [ ] Technical findings cite the material and say what was not checked; structure, schema, programmatic pages and AI answers are handed to their skills.
- [ ] No ranking change is attributed to a cause without ruling out alternatives; every search-engine fact is cited with a dated official URL or marked *to confirm*; no benchmark is used.
- [ ] Links are earnable; no paid links, schemes or doorway pages; the plan fits stated capacity or asks for it.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Win the searches your real buyer makes, matched to what they want at that moment, fix what stops good pages being found, and build authority around the problems your offer solves; judge it on customers, not rankings. SEO (keyword research by intent, on-page, technical health, links, topical authority), The Complete Marketing System, section 11 Distribution (Servidad, 2026); Google Search Central documentation (verify current guidance); They Ask, You Answer (Marcus Sheridan).
