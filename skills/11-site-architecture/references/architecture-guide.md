# Site architecture: decision rules

## Hubs and clusters

- One hub per buyer problem or job (from the Journey, the offer's problems, or the questions pages already answer). The hub introduces the problem, summarises each cluster page and links to all of them.
- Cluster pages each answer one question or intent and link back to the hub and to the next page a reader would want.
- Money pages (service, pricing, product, the core offer, contact) stay one click from the home page and are linked from every relevant hub.
- Free assets (templates, checklists, tools) sit inside the hub of the problem they solve and are linked from the informational pages that lead to them.

## Depth and discovery

- Important pages should be reachable in a few clicks from the home page; label any specific click-depth target a heuristic.
- A page linked only from a paginated blog list or tag page is effectively an orphan: hard for readers to find and given little internal weight.
- Tag and archive pages with no content of their own rarely serve a search intent; propose noindex, consolidation or removal only with evidence (for example the indexing report listing them as crawled but not indexed).

## Internal links

- Link where a reader would naturally go next; avoid site-wide link blocks that link everything to everything.
- Anchor text describes the destination in the buyer's words; avoid "click here".
- Every informational page ends with a next step that exists (a free asset, a hub, the offer).
- Fix links pointing at redirected or deleted URLs.

## Cannibalisation

Two pages for the same intent split signals and confuse readers. Pick the page to keep (the one with better evidence: clicks, links, fit with intent), then merge the other's useful content into it, re-target the other to a distinct intent, or redirect it. A shared query in Search Console is a clue, not proof; check intent.

## Merges, removals and redirects

- Removing or moving a page: 301 redirect to the closest equivalent (not the home page by default), update internal links and the sitemap, and keep a list of old → new URLs as the rollback.
- Sold-out or discontinued items: keep the page with the true status, redirect to the nearest equivalent, or retire it; never leave deleted URLs returning errors without a decision.
- Off-topic pages with no evidence of value: propose removal or noindex, with the evidence.
- Protect any page that earns clicks, impressions or external links.

## Navigation

- Few top-level items, each a real destination named in the buyer's words.
- The footer carries utility links and can carry hub links; it is not a dumping ground.
- Breadcrumbs reflect the hierarchy (structured data for them goes to `schema`).

## URLs

- Keep working URLs. Change one only when the benefit is clear, with a redirect.
- New pages: short, readable, lowercase words under their hub path.

## Platform claims

How search engines follow links, treat redirects, canonicals, noindex and sitemaps, and how a CMS or website builder handles redirects and URL rules, are platform facts. Cite the engine's or vendor's own current documentation with URL and date, or mark *to confirm*.

## Authorisation

Navigation changes, URL changes, redirects, removals, noindex and template changes are live. Each needs exact scope, expected effect, downside, rollback and the owner's approval; verify the live result after an approved change.
