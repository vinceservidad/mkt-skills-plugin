---
name: 11-marketplace-retail-media
description: Plan and audit marketplace and retail media channels. Use for Amazon Ads, TikTok Shop, Etsy or Walmart listings, Buy Box readiness, marketplace SEO, ACoS vs TACoS, or creator shop commissions.
metadata:
  section: "11 Distribution"
  covers: "Marketplace & retail media"
---
# Marketplace and retail media

Marketplaces (Amazon, TikTok Shop, Walmart, Etsy) are closed commerce ecosystems where buyers already have a card on file, and paid ads directly feed organic ranking velocity — or drain margin if the listing is not retail-ready. Marketplace and retail media works when you verify unit economics after referral, fulfillment and ad fees first, fix retail readiness (Buy Box ownership, main image CTR, title/bullets/backend search terms, stock depth and review floor) before turning on spend, and judge campaigns on **TACoS** (Total Advertising Cost of Sale) and contribution margin rather than isolated ad-platform ACoS. It fails when brands send paid traffic to a listing without the Buy Box or stock, ignore marketplace referral/FBA/fulfillment fees, bid on brand terms while calling it new growth, or cannibalize DTC subscriptions without checking margin and customer ownership.

Save the plan or audit as a Markdown file in `work/11-distribution/` when the required inputs are present and the request does not depend on unconfirmed commercial terms (see Owner commitments). Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Core offer**, from `07-offer-design`.
- `context/awareness.md` → **Awareness map**, from `03-awareness-map`.
- If present, also read `context/offer.md` → Price and model, Value ladder; `context/customer.md` → ICP and personas, Voice of customer; product catalogs, marketplace exports, fee sheets, COGS/margin notes or review exports in `inputs/`; any work in `work/11-distribution/11-channel-selection-*.md` or `work/17-measurement/17-unit-economics-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (interviews, reviews or product notes in `inputs/`): run the skill that fills it first (`07-offer-design` or `03-awareness-map`), then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Core offer → `07-offer-design`; Awareness map → `03-awareness-map`) and ask for evidence. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Marketplace pricing (and DTC price parity), commission rates for TikTok Shop creators, promotional coupons, FBA/fulfillment choices, inventory commitments and ad budgets are the owner's commitments. Never invent COGS, marketplace fee percentages, prices, creator commission rates or sales figures that `offer.md` and `inputs/` do not hold. If the request asks to launch a marketplace discount, coupon or creator commission rate not confirmed in `offer.md` or `inputs/`, stop, ask the owner to confirm the exact terms, and write no launch plan on assumed terms. Unknown COGS or referral fees are not a stop for an entry or catalog readiness audit: give the contribution-margin formula, mark missing economics *owner to supply*, and hold ad-spend targets until confirmed.
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.
- If `03-awareness-map` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/marketplace-retail-media-guide.md](references/marketplace-retail-media-guide.md) for retail readiness gates, SKU selection, Amazon Sponsored Ads structure, TikTok Shop + creator affiliate setup, ACoS vs. TACoS unit economics and DTC cannibalization checks.

1. **Outcome and channel role.** Name what the marketplace is for (incremental new-to-brand discovery, sampling entry SKUs that feed DTC repeat/subscription, or capturing existing category demand) and check the strategic trade-off: marketplaces own the buyer relationship and charge referral + fulfillment fees.
2. **Unit economics and break-even ACoS first.** Compute break-even ACoS only from confirmed numbers (`(Price - COGS - Referral Fee - Fulfillment/Shipping Fee) / Price`). When COGS or marketplace fees are missing from `inputs/`, show the exact formula, mark each input *owner to supply / to confirm*, and never invent a fee rate or target ACoS.
3. **SKU selection and catalog readiness.** Count catalog SKUs by status and demand with [scripts/tally.py](scripts/tally.py) and [scripts/sum_by.py](scripts/sum_by.py), never by eye. Start with 2 to 5 high-velocity, evergreen, in-stock hero SKUs — exclude sold-out, past, fragile/short-shelf-life or thin-margin SKUs that cannot survive marketplace fees and fulfillment SLAs.
4. **Retail readiness gate (before spending $1 on ads).** Require all six gates before turning on retail media: Buy Box / Featured Offer ownership, conversion-ready main image and gallery, search-indexed listing title/bullets/backend terms (using buyer language from `inputs/` or VoC), A+ / enhanced content, inventory buffer (never run ads into a stockout, which destroys organic rank), and a baseline review plan (e.g., official platform review programs like Amazon Vine — verify current eligibility/fees).
5. **Retail media structure (platform-matched).**
   - **Amazon Ads:** Separate Sponsored Products into exact/discovery (Auto + Broad/Phrase harvesting into Exact winners), isolate branded vs. non-branded queries so brand defense never hides weak non-brand efficiency, add negative keywords on wasted search terms, and layer Sponsored Brands / Sponsored Display only after Sponsored Products converts cleanly.
   - **TikTok Shop:** Pair shop listing readiness with Open vs. Target creator affiliate collaborations (`11-influencer` handles creator sourcing/briefs; this skill owns shop offer structure, sample/commission economics and Shop Ads / GMV Max guardrails).
   - **Walmart / Etsy / others:** Apply the same retail-readiness-first and margin-gated bidding structure; cite current ad formats from official docs or mark *to confirm*.
6. **Measurement (ACoS, TACoS and incrementality).** Track **ACoS** (ad spend / ad-attributed sales) alongside **TACoS** (ad spend / total marketplace sales, including organic lift), new-to-brand percentage (where available) and true post-fee contribution profit. Hand multi-channel incrementality and DTC cannibalization testing to `17-incrementality` and budget scaling to `19-scale-paid`.
7. **Platform facts.** Referral fees, FBA/fulfillment fees, Vine enrollment fees, TikTok Shop commission/shipping SLAs, Brand Registry rules and ad formats change often. Cite verified official documentation (URL and date) or mark *to confirm*.
8. **Approval.** The plan is a draft. Opening seller accounts, listing SKUs, setting creator commission rates, shipping FBA inventory or launching retail media campaigns requires the owner's explicit approval.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no COGS, referral fees, fulfillment fees, conversion rates, review counts or ACoS/TACoS targets that are not in `context/` or `inputs/`. Mark inferences `(assumption)` and list missing facts under Open questions. No third-party benchmark ACoS is evidence.

## Output

Write `work/11-distribution/11-marketplace-retail-media-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Marketplace and retail media plan: <business, marketplace(s), period>
Skill: 11-marketplace-retail-media · Date: <YYYY-MM-DD> · Framework: Marketplace & retail media (unit-economics gate, retail readiness before spend, ACoS vs. TACoS)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; no listings, commissions or ad campaigns launched
## Outcome, marketplace role and DTC trade-off
## Unit economics and break-even ACoS
| Line item | Value | Status / source |
| --- | --- | --- |
## SKU selection (from catalog)
| SKU / group | Status & volume (if present) | Marketplace fit | Reason |
| --- | --- | --- | --- |
## Retail readiness checklist (gate before ad spend)
## Campaign and affiliate structure
| Campaign / program | Goal | Targeting / creator tier | Brand vs. non-brand rule | Guardrail metric |
| --- | --- | --- | --- | --- |
## Measurement (ACoS, TACoS and cannibalization)
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

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write proposed listing titles, bullets and campaign names in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`) and fix every line it prints until it reports every quotation matches.

Reply with the file path, the unit-economics gate, which SKUs fit (and which stay out), and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Break-even ACoS and post-fee contribution margin are addressed first; missing COGS and marketplace fees are marked *owner to supply / to confirm* and never guessed.
- [ ] Catalog SKU counts and sales totals are calculated with `tally.py` / `sum_by.py`; sold-out, past or unfit SKUs are excluded.
- [ ] Retail readiness gates (Buy Box, listing SEO, images, inventory buffer, baseline reviews) are required before turning on paid retail media.
- [ ] Branded and non-branded queries are separated; ACoS is evaluated alongside TACoS and net contribution margin, with scaling handed to `19-scale-paid`.
- [ ] DTC cannibalization and customer-ownership trade-offs are explicit; platform fees and rules are cited with a dated official URL or marked *to confirm*.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

On marketplaces, ads amplify a retail-ready listing and punish a broken or thin-margin one, so prove post-fee unit economics and pass retail readiness before spending, isolate brand from non-brand, and manage to TACoS and net profit rather than raw ACoS. Marketplace & retail media, The Complete Marketing System, section 11 Distribution (Servidad, 2026); Amazon Ads retail readiness and TACoS methodology.
