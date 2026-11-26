# SEO: decision rules

## Intent

| Intent | The searcher wants | Usual page | Journey / awareness |
| --- | --- | --- | --- |
| Informational | To understand or fix a problem (how to, what is, template) | Guide, explainer, tool, template | See / Think; unaware to problem aware |
| Commercial | To compare options (best, vs, alternatives, for [type of business]) | Comparison, category or service page for a segment | Think; solution aware |
| Transactional | To buy or contact (pricing, near me, hire, sign up) | Service, pricing, product page | Do; product and most aware |
| Navigational | A specific brand or page | Home, login, the brand's own pages | Product aware and customers |

Read the intent from the words and from what the results already show; a "template" search wants a template, not a sales page. A page that matches the wrong intent does not rank or convert, however good it is.

## Relevance before volume

Score each search on:

1. **Buyer fit:** would the ICP type this? Evidence: their own words (Voice of customer), questions on sales calls, existing Search Console queries.
2. **Offer fit:** can the business serve the searcher? A search for a cheap generic service is a poor fit for a premium specialist.
3. **Volume:** the tool's estimate, labelled as an estimate with its source and date. Small volumes with high fit often beat large ones with none.
4. **Winnability:** what already ranks (only when observed and dated) and whether the site already has impressions for it.

## Reading Search Console

- Total by page and by query with `scripts/sum_by.py`; separate branded queries (the business's name) from non-branded.
- Impressions with few clicks at a low average position mean the page is seen but not chosen or not high enough: check intent match and title before writing new content.
- Two of the site's own pages appearing for the same query, each with a weak position, suggests cannibalisation (a pattern to confirm by intent, not proof).
- Average position is an average across searches, places and devices; it is not a rank anyone saw.
- Search Console is sampled and filtered for privacy; totals in the report can differ from the sum of rows. Say which you used.
- Striking distance (roughly positions 5 to 20) is a heuristic for where small improvements may move a page; label it as one.

## Technical checks (only what the material shows)

- **robots.txt:** which paths and user agents are disallowed, and whether any page meant to rank or convert is blocked. A disallowed page cannot be crawled, so its content cannot be read.
- **Indexing report:** indexed, crawled-not-indexed, blocked; thin tag or archive pages often sit in crawled-not-indexed.
- **Canonicals, redirects, sitemaps:** consistent and pointing at the page meant to rank.
- **Orphans:** pages with no internal links except a list page are hard to discover and carry little internal weight (structure goes to `site-architecture`).
- **Page experience:** field data over lab data; a score change is not a ranking guarantee.
- **Not checked:** say what was not in the material (crawl, logs, speed, mobile rendering) rather than assuming it is fine.

## Prioritising

Order: protect and fix what earns (technical blocks, cannibalisation, striking distance) → commercial and transactional gaps the offer serves → informational clusters that lead to a free asset or the offer → links. Each action: impact on the business outcome, confidence, effort, reversibility, and the owner skill.

## Links and authority

- Earnable: original data the business owns and may publish, free tools and templates, partner pages, podcast and interview pages, digital PR, directories that buyers actually use.
- Not allowed: buying links, link exchanges at scale, private blog networks, doorway pages, auto-generated content made to rank rather than help.
- Topical authority: group target topics into clusters per buyer problem; hand hub hierarchy, navigation and internal-link design to `11-site-architecture`.

## Causality

When traffic or rankings change, list the competing explanations (algorithm update, seasonality, competitor, technical regression, tracking change) and what would rule each out before naming a cause. A date match is a hypothesis.

## Platform claims

Search engine ranking systems, rich-result rules, Core Web Vitals thresholds, crawler names, indexing tools and Search Console features change. For each one the plan relies on, cite the engine's own current documentation `(first-party: <URL>, checked YYYY-MM-DD)` or mark *to confirm*. Do not quote a "ranking factor" from memory or from third-party studies as fact.

## Authorisation

Robots.txt, redirects, canonicals, noindex, page deletions and merges, URL changes and template changes are live changes. Each needs exact scope, expected effect, downside, stop condition, rollback, and the owner's approval; verify the live result after an approved change.
