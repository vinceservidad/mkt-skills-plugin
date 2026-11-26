# Programmatic SEO: decision rules

## The value test

A page type deserves to exist at scale only if all four hold:

1. **Distinct intent:** searchers using this modifier want something different from searchers using another (a video production company's books differ from a PR agency's; a bookkeeper's service in Denver does not differ from Austin's if it is fully remote).
2. **Real data:** the business holds facts per row that answer that intent: inventory, specifications, documented processes, its own records, first-hand experience. The modifier's name, population or a generic paragraph is not data.
3. **Evidence of search:** keyword or Search Console data shows the pattern is searched, or the plan says it is unevidenced and tests it small.
4. **Can be kept true:** someone owns updating the data (stock, prices, availability).

Fail on 1 or 2 → doorway or thin pages. Reject and point the intent at one strong page instead (a single service page, a hub, a guide).

## Common page types

| Type | Builds well when | Usually fails when |
| --- | --- | --- |
| Location | The business has a physical presence, local staff, local inventory, local rules or prices | Service is identical everywhere and remote |
| Type or segment ("X for Y") | The offer, process or data genuinely differ by segment | Only the segment name changes |
| Product or item | Each item has its own attributes, availability and use | Items are near-duplicates or mostly unavailable |
| Integration, template, tool | Each has real functionality or content | Placeholder pages for things that do not exist |
| Comparison | Facts about each alternative are dated and sourced | Claims about competitors are unsourced (see 06-competitor-pages) |

## Data audit

- One row per proposed page. Columns: the fields that would fill the template, and for each whether it is present, unique to that row and useful.
- Set a minimum (for example: at least N real, row-specific fields, and the core answer to the intent) and label it a heuristic.
- Count passing rows with `scripts/tally.py` on the data file or a line-by-line table.
- Rows with empty or one-word fields are excluded or held until the data exists.

## Template

- Sections mapped to fields; the unique, useful content near the top.
- Title and H1 pattern from the search pattern, in the buyer's words.
- Call to action: only offers in `offer.md` or on the site.
- Hub page linking to every page in the set, and pages linking to their nearest neighbours where a reader would go next.
- Canonical to itself unless a page is a variant; structured data only where it matches visible content.
- No AI-written or spun paragraphs to make thin rows look full; generated text may draft only from real row data and must pass human review.

## Quality gates (before indexing)

1. Every page passes the data minimum.
2. Duplication check: no two pages substantially the same; pick one and merge.
3. Human review of a sample (and every page in the pilot), with an owner checking facts.
4. Lifecycle rule for rows whose data changes: keep the page with the true status (sold out, seasonal, returns in month X), redirect to the nearest equivalent, or noindex, chosen per type and approved by the owner.

## Pilot

- Start with the rows that have the strongest data and search evidence.
- Measure over a stated window: indexing status, impressions and clicks for the target queries, and the business outcome (calls, orders, subscribers) from analytics.
- Keep, change and stop rules written in advance. Label batch size and window heuristics.
- A pilot that indexes but brings no qualified outcome is a stop or change signal, not a reason to publish more pages.

## Platform claims

Search engines publish spam policies (for example on doorway pages and on content produced at scale mainly to rank) and quality guidance that change. Cite the engine's own current page with URL and date, or mark *to confirm*. Do not quote policy wording from memory.

## Authorisation

Publishing a page set, mass redirects, deletions and noindex rules are live changes: scope, expected effect, risk, rollback, owner's approval, and a check of the live result.
