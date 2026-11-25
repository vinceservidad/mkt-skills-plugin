# Local SEO and Google Business Profile guide

## 1. The three Local Map Pack pillars

Google evaluates local results on:
1. **Relevance:** How closely the Google Business Profile (categories, services, description) and linked landing page match the searcher's intent. Primary category is the highest-leverage relevance signal.
2. **Distance:** Physical proximity between the verified address (or service area) and the searcher's location or specified city. Cannot be faked; trying to spoof addresses risks suspension.
3. **Prominence:** Real-world authority — review count, rating, recency and velocity; local backlinks and press; consistent NAP citations; organic strength of the linked page.

## 2. Google Business Profile eligibility (verify before building)

Under Google Business Profile guidelines (verify current Help Center wording and cite date):
- **Eligible:** Businesses that make in-person contact with customers during stated hours — either at a staffed physical storefront/office with permanent signage, or as a Service-Area Business (SAB) that travels to customers (plumbers, mobile clinics, cleaners, local consultants meeting clients in person).
- **Not eligible:** Purely online-only businesses with no in-person customer contact, PO boxes, mail drops, or unstaffed virtual offices / coworking mail-only addresses.
- **Storefront vs. SAB:** Storefronts show their street address; SABs hide the street address and list realistic service areas (typically within ~2 hours' drive). Never display a home address unless customers visit there during stated hours with signage.

## 3. Google Business Profile checklist

- **Business Name:** Exact real-world brand name matching signage and legal registration. Adding city names or extra keywords violates guidelines and triggers suspension.
- **Primary Category:** Choose the single most specific category describing the core business. Add only directly accurate secondary categories (typically 1–4).
- **Website Link:** Point to the homepage (single location) or the dedicated location page (multi-location) with UTM parameters (`utm_source=google&utm_medium=organic&utm_campaign=gbp`) so Maps clicks are separated from standard organic search in GA4.
- **Services, Attributes, Hours, Photos:** Complete every relevant service item with plain descriptions, accurate hours (including holiday hours), real photos of the team/premises/work (no stock photos), and seed common buyer questions in Q&A.

## 4. Canonical NAP and core citations

Standardize one exact **Name, Address, Phone** string everywhere (same street abbreviation, suite format, local phone number):
- Priority tier 1: Google Business Profile, Apple Business Connect, Bing Places, Facebook Page, LinkedIn Company Page (if B2B).
- Priority tier 2: High-trust country/industry directories (Yelp, BBB, Yellow Pages, Yell UK, industry associations — e.g., state CPA/legal/medical boards).
- Clean up duplicates and old addresses before building new listings.

## 5. Local landing pages vs. doorway pages

- **Good local page:** Built for a real physical location or actively served metro, containing unique local proof (clients or work in that city, local team/office details, directions/parking for storefronts, local regulations or pricing nuances, genuine FAQs, click-to-call/book CTA, and `LocalBusiness` JSON-LD handed to `11-schema`).
- **Doorway page (avoid):** Mass-generating 50 pages with identical copy swapping only the city name. Risks demotion or non-indexing.

## 6. Reviews and local prominence

- Reviews drive both Map Pack prominence and click-to-call conversion.
- Never gate reviews ("only send happy customers to Google") and never pay or offer discounts in exchange for positive reviews (violates Google/FTC rules).
- Reply promptly and specifically to every review (positive and negative). Hand the ongoing review-request cadence to `16-reviews`.
