# International and multi-region expansion playbook

Entering a new country is not flipping a "worldwide shipping" toggle or running machine translation. Every target country has its own landed economics, payment habits, search vocabulary, legal compliance and ad auction dynamics. Apply this playbook whenever an expansion option crosses country or currency borders.

## 1. Country selection gate (before spending)

Validate four gates before choosing a target country (start with **one** adjacent beachhead country, never five at once):
1. **Core stability first:** Never launch internationally to escape churn, fulfillment delays or weak margins in the home market.
2. **Real demand evidence:** Existing organic traffic, inbound inquiries, waitlist sign-ups or customer referrals from that country (`inputs/`), or verified search/category demand (`01-demand-check`).
3. **Landed unit economics:** Model true contribution margin **per country** before pricing:
   - `Local Selling Price (tax-inclusive where required, e.g., UK/EU VAT) - VAT/GST remitted - COGS - Cross-Border Shipping / 3PL Pick-Pack - Import Duties / Brokerage (DDP vs. DDU) - FX & Local Payment Fees - Expected Returns Cost`.
   - **Never surprise buyers with unpaid customs bills at the door (DDU):** Delivered Duty Paid (DDP) or local 3PL fulfillment protects conversion and prevents refund spikes.
4. **Regulatory & fulfillment readiness:** Check country-specific labeling, food/cosmetic/health compliance, privacy consent (GDPR, UK PECR, CASL), VAT registration thresholds and realistic delivery transit times. Mark unverified legal/tax rules *to confirm with local counsel/accountant*.

## 2. Localization vs. literal translation

- **Currency & tax display:** Show local currency and local tax convention (VAT-inclusive in UK/EU/AU; tax-at-checkout in US/CA). Clean psychological price points beat ugly FX decimals (e.g., £19 rather than £17.43 — owner confirms exact prices).
- **Vocabulary, units & spelling:** Localize regional terms, sizing/weights (g/ml/cm vs. oz/in), date formats, spelling (`colour`/`favour` UK vs. US) and local proof/reviews.
- **Local payment methods:** Cards alone lose checkout conversion in many regions (for example iDEAL in the Netherlands, Klarna/SEPA in DACH/Nordics, Apple Pay/PayPal in UK, local wallets in SEA/LATAM — verify current market share and store processor support).

## 3. Marketing, feeds and SEO separation

- **Separate ad campaigns / accounts by country:** Never mix UK, US and EU inside one blended campaign or one blended ROAS target — CPMs, AOVs, VAT treatment and shipping costs differ sharply. Separate country budgets so high-CPM markets do not starve smaller ones.
- **Country-specific Shopping feeds (`11-shopping-feeds`):** Each country needs its own localized feed matching the local landing page currency, language, shipping rates and return policy in Merchant Center; price/currency mismatch triggers immediate disapprovals.
- **SEO & URL architecture (`11-site-architecture`):** Choose ccTLDs (`example.co.uk`), subfolders (`example.com/en-gb/`) or subdomains cleanly, and implement reciprocal `hreflang` tags (plus `x-default`) so Google serves the right regional storefront instead of cannibalizing pages.

## 4. Minimum viable international test

Before signing a 3PL lease or building full regional infrastructure:
- Pick **1 country** with the smallest operational distance (same language, clear shipping/duties path, existing demand signal).
- Run a **capped test** on hero SKUs only with confirmed DDP pricing, clear delivery-time expectations, localized checkout currency and a pre-agreed stop rule on landed contribution margin and delivery/ticket rate.
- Require owner approval on exact local prices, shipping/duty terms, VAT registration and test budget before launching.
