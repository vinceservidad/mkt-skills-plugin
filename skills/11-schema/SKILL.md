---
name: 11-schema
description: Add structured data that matches visible content and can earn rich results. Use for schema markup, JSON-LD, structured data, rich results, FAQ or product schema.
metadata:
  section: "11 Distribution"
  covers: "Schema / structured data"
---
# Schema and structured data

Structured data tells search engines, in a fixed vocabulary, what a page already says: this is a product at this price, this is the business and where it is, these are the questions on this page. It can make a page eligible for a rich result; it never guarantees one, and it does not by itself raise rankings. Markup that claims what the page does not show (a rating nobody can see, a price that differs, reviews the business wrote about itself) breaks search engines' guidelines and can cost the site its rich results. Every property comes from the visible page.

Save the markup and its notes as a Markdown file in `work/11-distribution/` when the material is present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

- **The material:** what each page to be marked up visibly shows, from `inputs/` or the user: the page text (headings, prices, FAQs, reviews shown, business details), the URL, and any structured data already on the page or added by the theme or a plugin.
- **No material?** If no page content or URLs were supplied, write nothing to `work/` beyond, at most, a short list of what to collect. Ask for the pages (URL plus the visible text, or the page source) and any existing markup, say how to provide them (drop files in `inputs/` or paste them into chat), and invent no prices, ratings, addresses or FAQs. End with the **Principle, framework, source** block.
- Optional context, read if present: `context/offer.md` → Core offer, Price and model (to check the page matches the offer, not to fill the markup); `context/brand.md` → Naming; `context/positioning.md` → Positioning statement; any work in `work/11-distribution/11-seo-*.md` or `work/11-distribution/11-site-architecture-*.md`. Context is never a source for a markup value the page does not show.

## Process

Use [references/schema-guide.md](references/schema-guide.md) for the type choices, the do-not-mark-up list and the validation steps.

1. **The goal per page.** Name what the markup is for on each page: describing the business entity, product details in results, breadcrumbs, a specific rich-result type. Say plainly that eligibility is decided by the search engine and that markup does not raise rankings.
2. **What the page shows.** For each page, list the visible facts that could become properties, quoted exactly from the material, and the existing markup (theme or plugin) that would duplicate or conflict.
3. **Choose types.** Pick the most specific schema.org type that fits what the page is (for example `ProfessionalService` or `LocalBusiness` subtype for a service business with a public address, `Organization` otherwise; `Product` with `Offer` for a product page; `FAQPage` only for questions and answers written by the site and visible on the page; `BreadcrumbList` for a visible breadcrumb trail). One coherent graph per page, using `@id` to connect the organisation, website and page.
4. **Do not mark up.** Reject or flag, with the reason: ratings or reviews not visible on the page; reviews the business collected about itself presented to earn review stars where the search engine's guidelines do not allow it (eligibility *to confirm* in current documentation); prices, availability or offers that differ from the page; FAQs that are not on the page; addresses or opening hours not shown; anything from context that the page does not state.
5. **Write the JSON-LD.** For each page, a complete `<script type="application/ld+json">` block with only properties whose values appear on the page (or in the page's own existing markup, when verified). Compute any aggregate (rating value, review count) from the visible reviews line by line, never by eye, and match what the page displays. Leave out a property rather than guess it; list it under Open questions. Keep every visible fact that describes the item: a fact with no dedicated property (a coffee's origin, process or roast, a plan's revenue band) goes in `additionalProperty` as a `PropertyValue` with the page's exact wording, or in `description`, never dropped as *not a property*. A visible fact whose structured form needs values the page doesn't give (free shipping with no stated destination) stays in the `description` or offer text as shown, and the missing values go under Open questions; never invent them to complete the block. Each page template is marked up from its own visible fields, so a template whose layout is supplied ("the other pages follow the same layout") is marked up from those fields, not reported as missing.
6. **Conflicts with existing markup.** Say what the theme or plugin already outputs, whether to extend, replace or remove it, and that two conflicting blocks for the same entity should not both ship.
7. **Validate and verify.** Name the steps before and after shipping: a schema validator, the search engine's rich-result test, the page's URL inspection after deployment, and the structured-data reports over the following weeks. Nothing is claimed as valid or eligible until those tests are run.
8. **Platform facts.** Which types earn rich results, for which sites, with which required properties, and how self-serving reviews or FAQ results are treated, change: cite the search engine's own current documentation with URL and date, or mark *to confirm*. Never state one from memory as current. schema.org vocabulary (types and properties) is stable reference and may be named; it says nothing about eligibility.
9. **Approval.** Adding, replacing or removing markup in a theme, template or plugin is a live change: exact scope, rollback, and the owner's approval before anything is changed.
10. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the page doesn't show.** Write no ratings, review counts, prices, addresses, phone numbers, hours, FAQs, offers or claims that aren't visible on the page in `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Never promise a rich result, stars or a ranking change.

## Output

Write `work/11-distribution/11-schema-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Structured data: <site, pages>
Skill: 11-schema · Date: <YYYY-MM-DD> · Framework: schema.org structured data (JSON-LD) matched to visible content
Built from: <inputs and context sections used>
Status: draft for the owner's approval; not deployed or validated
## Goal per page and what markup can and cannot do
## What each page shows
| Page | Visible fact | Exact text (source) | Property |
| --- | --- | --- | --- |
## Types chosen
| Page | Type(s) | Why | Existing markup and what to do with it |
| --- | --- | --- | --- |
## Not marked up, and why
| Item | Reason |
| --- | --- |
## JSON-LD
<one fenced json block per page>
## Validation and verification steps
## Platform facts
| Fact the markup relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## Claims and sources
| Claim or value | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/` and nothing on the site. The markup is a draft deliverable, not a deployment.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (the page text), with the source named. Inside the JSON-LD, every string value of four or more words (a description, an FAQ question or answer, a headline) counts as a quotation too: copy it word for word from the page, or leave the property out. Write your own explanations in plain text or italics. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`). For every line it prints, copy the page's exact words or remove the quotation marks or the property, and run it again until it reports every quotation matches.

Reply with the file path, the types per page, what was deliberately not marked up and why, and the validation steps still to run, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every property value appears on the visible page in the material; nothing comes from context alone, and missing values are left out and listed as questions.
- [ ] Every visible descriptive fact is kept, in a dedicated property, `additionalProperty` or `description`; none is dropped for lacking a property or invented to complete one.
- [ ] Ratings and review counts are marked up only if visible on the page, computed from the visible reviews and matching the page's display; self-serving review eligibility is cited or marked *to confirm*.
- [ ] FAQ markup covers only questions and answers visible on the page, and its rich-result eligibility is cited or marked *to confirm*.
- [ ] Existing theme or plugin markup is accounted for, with no conflicting duplicates shipped.
- [ ] No rich result, stars or ranking change is promised; validation and post-deployment checks are listed as still to run.
- [ ] Every search-engine fact is cited with a dated official URL or marked *to confirm*; nothing ships without the owner's approval.
- [ ] Quotation marks, including JSON string values of four or more words, hold only exact page words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Structured data describes what a page already shows, in a vocabulary machines read; mark up only what visitors can see, and let the search engine decide whether it earns a rich result. schema.org vocabulary (JSON-LD), The Complete Marketing System, section 11 Distribution (Servidad, 2026); Google Search Central structured data guidelines (verify current).
