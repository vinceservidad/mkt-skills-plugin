# Shopify CRO Framework

## Knowledge metadata

- Primary type: framework
- Secondary type: audit checklist
- Decision: where a Shopify store's pre-conversion journey loses qualified buyers, and which hypothesis to fix or test first
- Owner: `$cro`
- Evidence status: diagnostic lens; findings require store evidence. The Shopify platform notes are officially documented as of the checked date, and the store's own plan and setup must still be confirmed from its admin (account-visible)
- Freshness: Shopify notes checked 2026-09-26; recheck the first-party page before relying on a note for a checkout recommendation

## Journey map

Traffic source → customer intent → product page → offer presentation → trust → cart → checkout (conversion boundary)

The map organizes evidence. It does not rank causes. Find the first meaningful pre-conversion leak, and fix verified defects before testing persuasion variants.

## Audit

- Value proposition and message scent from the traffic source
- Product page clarity
- Images and creative consistency
- Reviews and proof, traceable to a real source
- Price, shipping, and fee presentation: CRO judges clarity and placement of approved terms. Price level, discounts, and packaging go to `$pricing-monetization`
- Mobile experience and accessibility
- Cart and checkout friction, including technical errors
- Upsell, cross-sell, and bundle offers: CRO judges placement and friction only. The offer itself goes to `$offer-strategy`
- Repeat purchase and post-purchase retention are outside CRO scope and go to `$retention-strategy`

## Shopify-specific notes

- **Conversion-rate denominator.** The Shopify Help Center page on behavior reports defines conversion rate as the percentage of sessions that resulted in a purchase, and calculates each funnel step (cart additions, reached checkout, completed checkout) against total sessions (first-party: https://help.shopify.com/en/manual/reports-and-analytics/shopify-reports/report-types/default-reports/behaviour-reports, checked 2026-09-26). Treat it as a session-level journey diagnostic, not the primary business outcome. Reconcile orders, net revenue, and contribution with `$tracking-measurement` before judging a change.
- **Checkout surface feasibility.** The Shopify Help Center page on customizing payment methods and delivery options at checkout states that apps that customize the information, shipping, and payment pages of the checkout are available only to Shopify Plus (first-party: https://help.shopify.com/en/manual/checkout-settings/checkout-customization, checked 2026-09-26). Before proposing an intervention on those checkout pages, confirm the store's plan and current checkout setup. If the pages can't be customized, scope the hypothesis to product, cart, or pre-checkout surfaces.
- **Recent storefront changes (heuristic).** App installs or storefront code changes inside the comparison window are candidate technical-defect explanations. Verify them with error, page-speed, or before-and-after evidence before treating them as the cause.

Optimize for the primary business outcome, using customer behavior and evidence. Live store changes require explicit approval, and test validity goes through `$tracking-measurement`.
