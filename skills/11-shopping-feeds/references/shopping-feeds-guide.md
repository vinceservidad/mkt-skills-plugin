# Shopping and product feeds guide

## 1. Feed-first principle

Google Shopping and Performance Max Shopping placements do not take keyword lists. Query matching is driven primarily by:
1. `title` (strongest signal; first 70 characters show in most Shopping cards)
2. `product_type` and `google_product_category`
3. `description`, `brand`, `gtin` / `mpn`, `color`, `size`, `material`, `pattern`, `age_group`, `gender`
4. Landing page structured data (`Product` JSON-LD price and availability parity with feed)

Fix feed quality and Merchant Center hygiene before adjusting bids or restructuring campaigns.

## 2. Primary feed vs. supplemental feed

- **Primary feed** (Shopify / WooCommerce / Content API): owns live truth — `id`, `price`, `availability`, `link`, `image_link`, `brand`, `gtin`. Never break ID stability (`id` changes wipe SKU-level bidding history).
- **Supplemental feed** (Google Sheet or TSV/XML keyed on `id`): safe layer for marketing optimization without altering customer-facing storefront titles or CMS fields:
  - Enriched `title` overrides (buyer-intent attributes added cleanly)
  - `custom_label_0` through `custom_label_4` (margin tier, performance bucket, seasonality, price band, stock priority)
  - `excluded_destination` (pull out low-margin, sold-out, subscription-only or ineligible SKUs cleanly)
  - `google_product_category` and `product_type` normalization

## 3. Title formulas by vertical

Order attributes left-to-right by how buyers actually search (and keep the core product noun + defining modifier inside the first 70 characters):
- **Food / Consumables / Coffee:** `[Brand] [Product Name] [Roast / Variant] [Origin / Flavor] [Form / Grind] [Size / Weight]`
- **Apparel:** `[Brand] [Gender] [Product Type] [Key Feature / Material] [Color] [Size]`
- **Home / Furniture / Hardware:** `[Brand] [Product Type] [Style / Material] [Dimensions] [Color]`
- **Electronics / Parts:** `[Brand] [Product Type] [Model / MPN] [Key Spec] [Compatibility]`
- **Avoid:** promotional text in titles (`Free Shipping`, `20% Off` — policy violation), ALL CAPS, internal SKU codes nobody searches.

## 4. Custom labels and SKU segmentation

Use `custom_label_0..4` so campaigns stay clean and measurable:
- **Performance buckets (when export data exists):** Heroes (high volume + profitable ROAS), Sidekicks (profitable, moderate volume), Villains (high spend, unprofitable), Zombies (zero/near-zero impressions — isolate in a catch-all or low-bid campaign so heroes do not starve them).
- **Margin tiers:** Separate high-margin SKUs from thin-margin accessories so one blended ROAS target does not overbid low-margin items and underbid high-margin ones.
- **Seasonality / availability:** Isolate seasonal or limited-harvest SKUs so they can be paused cleanly when stock drops without disrupting evergreen learning.

## 5. Standard Shopping vs. Performance Max (PMax)

- **Standard Shopping:** Best when you need explicit search-term visibility, negative keywords, brand/non-brand query sculpting (priority tiers), or are starting on a small budget with few conversions.
- **Feed-only PMax:** Good middle ground for e-commerce catalogs with steady conversion volume when you want Shopping + dynamic remarketing without unverified video/display waste.
- **Full-asset PMax:** Only after clean conversion tracking, verified margin guardrails, brand exclusions, and tested creative assets (`09-ad-creative`).
- Always exclude brand terms (via negatives in Standard Shopping or brand exclusions in PMax — verify exact current controls in official docs) before judging non-brand acquisition ROAS.

## 6. Merchant Center disapproval & hygiene checklist

Check before spending:
1. **Price and availability mismatch:** Feed `price` and `availability` must match visible landing page AND `Product` schema (watch currency/region mismatches and dynamic discounts).
2. **Shipping and returns parity:** Merchant Center shipping rates, transit times and return policy must match checkout and the public return policy page.
3. **Identifiers:** Real manufacturer `gtin` when one exists; for custom/private-label/house-roasted goods with no GTIN, set `identifier_exists=false` (verify current Merchant Center Next specification).
4. **Images:** Clean product image, no watermarks, no promo overlays, HTTPS reachable.
5. **Policy triggers:** Subscription-only products have specific Google Shopping subscription rules (must check official Merchant Center subscription/installment policy before listing).
6. **Country / currency separation:** Each target country requires localized currency, language, shipping and tax settings (never mix UK GBP and US USD into one unsegmented feed).

## 7. Fixing Serving Limitations, Image Guidelines & Peak/Holiday Readiness

Distilled from official `@GoogleAds` Merchant Center tutorials (*Fix Serving Limitations*, *Image Guidelines*, *Product Data Holiday Ready*). Verify exact current Merchant Center Next policy rules (URL and date) or mark *to confirm*.

### Serving limitations & policy triage
1. **Separate account-level vs. item-level issues:** Fix account-level misrepresentation, website-not-reachable ("Destination not working"), missing business/contact details, or checkout shipping/returns mismatches FIRST — they suppress the entire catalog.
2. **Item-level serving limits:** Audit missing `gtin`/`brand`, inaccurate availability/price (enable automatic item updates carefully or fix feed sync latency), restricted category claims, and landing page mobile crawl errors.
3. **Request review only after root-cause verification:** Re-submitting before the live storefront, schema and feed match risks longer review cooldowns.

### Product image compliance & CTR rules
- Use high-resolution, uncluttered images showing the exact sold variant (right color/pack size) on a clean neutral or contextual background.
- **Zero promotional overlays, watermarks, borders, badges or placeholder graphics** on `image_link` (instant disapproval trigger).
- Supply `additional_image_link` angles (lifestyle, scale, detail) and keep variants mapped to variant-specific URLs/images so buyers see the exact SKU they clicked.

### Peak & holiday readiness checklist (prep 2–4 weeks ahead)
- **Inventory & availability sync:** Tighten feed fetch frequency so fast-selling hero SKUs never advertise out-of-stock during peak traffic.
- **Promotions & `sale_price`:** Submit Merchant Center promotions and `sale_price_effective_date` early to allow approval review lead time; verify checkout displays the identical discounted price and shipping cutoff dates.
- **Hero SKU protection:** Tag peak/giftable hero SKUs via `custom_label` so holiday budgets concentrate on proven in-stock winners rather than thin-margin or slow-moving SKUs.

## 8. Platform facts rule

Google Merchant Center Next rules, attribute limits, subscription eligibility, image resolution minimums, supplemental feed setup steps and PMax brand-exclusion controls change. Verify against current official Google Merchant Center Help docs (cite URL + date) or mark *to confirm*.
