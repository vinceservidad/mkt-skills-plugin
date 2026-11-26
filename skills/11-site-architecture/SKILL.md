---
name: 11-site-architecture
description: Design site structure, navigation and internal linking so pages are found and rank. Use for site architecture, sitemap, URL structure, internal links, menu and hub pages.
metadata:
  section: "11 Distribution"
  covers: "Site architecture / internal linking"
---
# Site architecture

A site's structure decides which pages buyers can reach in a few clicks and which pages search engines treat as important. Good architecture groups pages by the problems buyers bring, puts a hub over each group, links pages the way a reader would move between them, and keeps every page that matters within easy reach. Bad architecture hides the best content behind a blog list, lets two pages fight for the same search, and changes URLs without redirects. Structure is designed from the pages that actually exist and the evidence of what buyers look for, never from a generic template.

Save the plan as a Markdown file in `work/11-distribution/` when the material is present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

- **The material:** the site's page inventory, from `inputs/` or the user: URLs, titles or headings, what each page is for, and how pages are linked now (menu, footer, body links). Search Console, analytics or crawl exports help when present.
- **No material?** Check for a page inventory, sitemap, crawl or page list before reading or summarising other files. If none is present, stop and write nothing to `work/`: ask only for the inventory, how to get it (the CMS page list, the sitemap, a crawl, plus current menu/footer links) and how to provide it (drop the export in `inputs/` or paste it into chat). Do not preview tentative hubs, quote or summarise ticket/review findings, or reference test/fixture headers; invent no pages, links, traffic or findings. End with the **Principle, framework, source** block.
- Optional context, read if present: `context/awareness.md` → Journey (from `03-journey-map`: what each stage asks), Awareness map, ICP and personas, Voice of customer; `context/offer.md` → Core offer, Value ladder (the pages that sell and the free assets); `context/positioning.md` → Category; any work in `work/11-distribution/11-seo-*.md`, `work/11-distribution/11-content-strategy-*.md` or `work/11-distribution/11-programmatic-seo-*.md`. If Journey is missing, say so and group by the problems the pages already address, marked `(assumption)`; recommend `03-journey-map` to sharpen it.

## Process

Use [references/architecture-guide.md](references/architecture-guide.md) for hub design, link rules and the redirect rules.

1. **Inventory.** List every page from the material with its purpose, its journey stage or intent, what links to it now and its evidence of value (clicks, impressions, links, conversions, where supplied). Count pages and inbound links with [scripts/tally.py](scripts/tally.py) or a line-by-line table, never by eye. Say what the material does not show (no crawl, no backlinks, no analytics).
2. **Problems found.** From the inventory: orphans (no internal links except a list or tag page), pages buried deep, money pages missing for an evident intent, two pages for one intent (possible cannibalisation), thin or off-topic pages, tag or archive pages with no content of their own, blocked or deleted pages without redirects. Cite the evidence for each.
3. **The target structure.** Build a dedicated hub for every distinct evidenced buyer problem or job (from the Journey, tickets/keywords and the offer — e.g. learning/choosing, account/subscription help, gifting — never collapsing a distinct buyer job into *Shop* or *Blog* or skipping a hub just because only one page exists today), marking missing hubs or supporting pages *proposed* (inventing no unconfirmed offers or features). Each hub has one page that introduces it and links to the cluster. Keep money pages (service, pricing, product, offer) close to the home page. Keep the hierarchy shallow enough that every important page is a few clicks from the home page (label any click-depth target a heuristic).
4. **Navigation and footer.** Propose the menu and footer from the hubs and money pages, in the buyer's words; few top-level items, each a real destination.
5. **Internal links.** For each cluster: links from the hub to every page, from each page back to its hub, between pages where a reader would go next, and from informational pages to the next step (a free asset or offer that exists). Descriptive anchor text in the buyer's language. List the specific links to add for the priority pages.
6. **Merge, keep, remove.** For each problem page: keep and improve, merge into another (which one and why), re-target, noindex, or remove, as a proposal. Any URL change or removal needs a 301 redirect to the closest equivalent, an updated sitemap and internal links, and a rollback. Protect pages that earn clicks or links.
7. **URLs.** Keep existing URLs that work; change a URL only when the benefit is clear, with a redirect. New pages follow a short, readable pattern under their hub.
8. **Hand-offs.** Keyword priorities and on-page work → `11-seo`; structured data such as breadcrumbs → `11-schema`; templated page sets → `11-programmatic-seo`; the editorial calendar → `11-content-strategy`; page copy → `10-page-copy`.
9. **Platform facts and approval.** How search engines treat redirects, canonicals, noindex, sitemaps and crawl depth is engine documentation: cite it with URL and date, or mark *to confirm*. Website-builder or CMS capabilities (redirect managers, URL rules) are *to confirm* unless the material shows them. Every structural change is a live change: exact scope, expected effect, risk, rollback and the owner's approval before anything is changed.
10. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features, benchmarks, platform capabilities or delivery terms that aren't in `context/` or `inputs/`. Compute every count, total, share or rank (such as "top" or "2nd highest") across all rows with Python or a complete sorted table, never by eye. Mark inferences `(assumption)` and list what is needed under Open questions. Describe each source only as it reads. Third-party benchmarks are not evidence about this site; leave them out.

## Output

Write `work/11-distribution/11-site-architecture-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Site architecture: <site>
Skill: 11-site-architecture · Date: <YYYY-MM-DD> · Framework: Hub-and-spoke site architecture and internal linking
Built from: <inputs and context sections used, with their status>
Status: draft for the owner's approval; nothing on the site changed
## Inventory
| URL | Purpose / intent | Journey stage | Linked from now | Evidence of value | Not known |
| --- | --- | --- | --- | --- | --- |
## Problems found
| Problem | Pages | Evidence |
| --- | --- | --- |
## Target structure
<hubs, their pages, and money pages, as a tree>
## Navigation and footer
## Internal links to add
| From | To | Anchor (buyer's words) | Why |
| --- | --- | --- | --- |
## Merge, keep, remove (proposals)
| Page | Proposal | Redirect to | Rollback | Needs approval |
| --- | --- | --- | --- | --- |
## URL rules
## Hand-offs
## Platform facts
| Fact the plan relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/` and nothing on the site. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a page title, a heading, a query), with the source named. Write your own labels, anchors and menu names in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the target structure in a few lines, the top fixes, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every page in the material is in the inventory with how it is linked now; counts come from `tally.py` or a line-by-line table; what the material does not show is stated.
- [ ] Problems (orphans, cannibalisation, missing money pages, thin or tag pages, blocked or deleted pages) cite their evidence.
- [ ] Hubs follow every evidenced buyer problem or job in the Journey, tickets or offer (with missing hubs or pages marked *proposed*, not omitted); money pages sit close to the home page.
- [ ] Specific internal links are listed with descriptive anchors and a next step that exists.
- [ ] Every merge, removal or URL change has a redirect target, a rollback and needs the owner's approval; pages that earn clicks or links are protected.
- [ ] Search-engine and CMS facts are cited with a dated official URL or marked *to confirm*.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Group pages by the problems buyers bring, put a hub over each group, link pages the way a reader moves between them, keep money pages close to home, and never move a page without a redirect. Hub-and-spoke site architecture and internal linking (topic clusters), The Complete Marketing System, section 11 Distribution (Servidad, 2026); Information Architecture for the Web and Beyond (Rosenfeld, Morville and Arango); Google Search Central documentation on links and site structure (verify current).
