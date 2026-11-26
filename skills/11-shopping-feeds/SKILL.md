---
name: 11-shopping-feeds
description: Plan and audit Google Shopping, Merchant Center and product feeds. Use for Google Shopping ads, Merchant Center disapprovals, supplemental feeds, product titles, GTINs, or PMax listing groups.
metadata:
  section: "11 Distribution"
  covers: "Shopping & product feeds"
---
# Shopping and product feeds

Shopping ads do not run on keywords you type into an ad group; the product feed is the keyword list, the ad creative and the price tag at once. Google Merchant Center matches buyer queries to your titles, attributes, identifiers and landing pages, then auctions impressions by margin-aware bidding. Shopping works when the feed is clean (no disapprovals or price mismatches), titles lead with how buyers search, supplemental feeds enrich attributes without breaking the store catalog, and campaigns segment SKUs by stock status, margin and performance. It fails when out-of-stock or low-margin SKUs eat the budget, titles use internal jargon instead of buyer attributes, or Merchant Center errors silently drop top sellers.

Save the plan or audit as a Markdown file in `work/11-distribution/` when the required inputs are present and the request does not depend on unconfirmed commercial terms (see Owner commitments). Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Core offer**, from `07-offer-design`.
- `context/awareness.md` → **Awareness map**, from `03-awareness-map`.
- If present, also read `context/offer.md` → Price and model; `context/customer.md` → ICP and personas, Voice of customer; product catalogs, Merchant Center exports, Shopping/PMax SKU reports or margin sheets in `inputs/`; any work in `work/11-distribution/11-paid-search-*.md` or `work/17-measurement/17-unit-economics-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (interviews, reviews or product notes in `inputs/`): run the skill that fills it first (`07-offer-design` or `03-awareness-map`), then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Core offer → `07-offer-design`; Awareness map → `03-awareness-map`) and ask for evidence. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Prices, sale prices, shipping rates, return policies, promo badges, target ROAS and budgets are the owner's commitments. Never invent a price, discount, free-shipping threshold or margin figure that `offer.md` and `inputs/` do not hold. If a campaign plan depends on an unconfirmed sale price or promotion, stop, ask the owner for exact terms, and write no plan on assumed terms. Unknown margins or budgets are not a stop for a feed audit: label them *owner to set* and separate feed hygiene from bidding targets.
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.
- If `03-awareness-map` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/shopping-feeds-guide.md](references/shopping-feeds-guide.md) for feed architecture, title formulas by vertical, supplemental feed rules, Merchant Center disapproval triage, custom labels and Standard Shopping vs. Performance Max SKU segmentation.

1. **Outcome that decides.** Name the business outcome (profitable SKU orders, first-order contribution margin or paying subscribers acquired through Shopping) and the SKU-level guardrail. Raw clicks or ROAS without margin or stock status are never enough.
2. **Audit the catalog and feed.** Count products by availability/status (active, seasonal, past/sold-out) and missing attributes with [scripts/tally.py](scripts/tally.py) and [scripts/sum_by.py](scripts/sum_by.py) (`python3 <this skill's folder>/scripts/sum_by.py <file> <col>`), never by eye. Flag every SKU that should be excluded from paid Shopping (sold-out/past SKUs, missing images or landing pages, non-compliant items) and every Merchant Center risk (price/availability mismatch, missing GTIN/MPN, policy or shipping/return settings).
3. **Title and attribute rules (primary + supplemental feed).** Build a title template ordered by buyer search intent (brand + product type + key attributes buyers search for from `inputs/` or VoC, never internal SKU codes) and keep critical words in the first 70 characters. Specify what stays in the primary store feed vs. what belongs in a **supplemental feed** (title overrides, `custom_label_0`..`4` for margin tier, hero/villain status, seasonality or price band, and missing `product_type` / `google_product_category`). Never overwrite clean storefront titles when a supplemental feed can override the Shopping title safely.
4. **SKU segmentation and campaign structure.** Group active SKUs using custom labels (hero sellers, seasonal/launch SKUs, low-volume "zombies", margin tiers) and exclude sold-out or past products. Choose Standard Shopping vs. Performance Max (feed-only or full asset) based on catalog size, conversion volume and control needs; hand pure text-search keyword campaigns to `11-paid-search` and budget increases to `19-scale-paid`.
5. **Bidding, margin guardrails and negative hygiene.** Tie target ROAS or max CPC to contribution margin when known, otherwise give the formula and mark *owner to set*. State search-term review cadence and brand vs. non-brand query controls.
6. **Tracking and Merchant Center prerequisites.** Check purchase conversion tracking, cart-data reporting (optional), auto-tagging, Merchant Center shipping/returns parity with checkout, and hand tagging gaps to `17-tracking-plan`.
7. **Platform facts.** Merchant Center Next requirements, GTIN exemptions, supplemental feed limits, PMax listing-group rules and free-listing eligibility change. Cite verified official Google documentation (URL and date) or mark *to confirm*.
8. **Approval.** The audit and feed plan are a draft. Editing live feeds, attaching supplemental feeds, changing Merchant Center settings or launching Shopping/PMax campaigns requires the owner's explicit approval.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no prices, margins, GTINs, stock counts, ROAS targets or performance numbers that are not in `context/` or `inputs/`. Mark inferences `(assumption)` and list missing facts under Open questions. No third-party benchmark ROAS or CPC is evidence.

## Output

Write `work/11-distribution/11-shopping-feeds-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Shopping and feed plan: <business, period>
Skill: 11-shopping-feeds · Date: <YYYY-MM-DD> · Framework: Shopping & product feeds (feed-as-targeting, supplemental enrichment, margin-tier SKU segmentation)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; no feed, Merchant Center setting or campaign changed
## Outcome that decides
## Catalog and feed audit
| Group / SKU status | Count | Units / sales (if present) | Paid Shopping action | Evidence / reason |
| --- | --- | --- | --- | --- |
## Title and attribute rules (primary vs. supplemental feed)
| Field | Primary feed | Supplemental feed rule | Example (from actual catalog) |
| --- | --- | --- | --- |
## Custom labels and campaign segmentation
| Segment (`custom_label`) | Included SKUs | Excluded SKUs | Campaign type & bidding rule |
| --- | --- | --- | --- |
## Merchant Center hygiene and disapproval checklist
## Tracking and negative-query hygiene
## Platform facts
| Fact the plan relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write proposed Shopping titles and rules in italics, code spans or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`) and fix every line it prints until it reports every quotation matches.

Reply with the file path, the catalog audit summary (active vs. excluded SKUs), the supplemental feed title/label design, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Catalog counts and any sales totals are calculated with `tally.py` / `sum_by.py`, never by eye, and sold-out or ineligible SKUs are explicitly excluded from paid Shopping.
- [ ] Shopping title rules place buyer search attributes first, keep storefront copy clean via a supplemental feed, and use real catalog items without inventing prices, GTINs or attributes.
- [ ] Custom labels and campaign segmentation separate hero/active SKUs from seasonal, low-volume or excluded SKUs; pure text-search goes to `11-paid-search` and scaling to `19-scale-paid`.
- [ ] Merchant Center parity checks (price, availability, shipping, returns, GTIN/identifier hygiene) are listed and unconfirmed margins/budgets are marked *owner to set*.
- [ ] Every platform fact is cited with a dated official URL or marked *to confirm*, and the plan states nothing changes without the owner's approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

On Shopping, the product feed is the targeting, the ad and the eligibility gate, so clean catalog hygiene, search-ordered supplemental titles and margin-aware SKU segmentation beat blind bidding every time. Shopping & product feeds, The Complete Marketing System, section 11 Distribution (Servidad, 2026); Google Merchant Center product data specification.
