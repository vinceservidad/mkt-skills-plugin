# Schema: decision rules

## Choosing types (schema.org vocabulary)

| Page | Usual type(s) | Notes |
| --- | --- | --- |
| Home / about | `Organization` (or a `LocalBusiness` subtype such as `ProfessionalService`, `AccountingService`, `CafeOrCoffeeShop`, `Store` when the page shows a public address customers can use) plus `WebSite` | `name`, `url`, `logo`, `sameAs` (profiles shown or linked on the site), `address` only if shown |
| Service page | `Service` with `provider` pointing to the organisation `@id` | `serviceType`, `areaServed` only if stated; an `Offer` only with a visible price |
| Product page | `Product` with `offers` (`Offer`; for subscriptions, the price as shown and any unit, such as per bag) | `name`, `image`, `description`, `brand`, `sku` if shown; `availability` only if the page states it |
| Pricing page | `Offer` or `Service` with offers | Prices exactly as displayed, with currency |
| FAQ section | `FAQPage` with `Question` / `acceptedAnswer` | Only questions and answers written by the site and visible; not user forums |
| Article / blog post | `Article` or `BlogPosting` | `headline`, `datePublished`, `author` (organisation or a named author only if shown) |
| Breadcrumb trail | `BreadcrumbList` | Only if a breadcrumb is visible |
| Reviews shown on the page | `Review` / `AggregateRating` nested in the item reviewed | Only if visible; see the review rules |
| Events | `Event` | Date, place or online, offers as shown |

Use one `@graph` per page with stable `@id` values (for example `https://site/#organization`) so the organisation, website and page connect.

## Visible facts without a dedicated property

- Attributes with no specific schema.org property (origin, process, roast, material notes, service bands) go in `additionalProperty` (`PropertyValue` with `name` and `value` as the page words them) or in `description`. Dropping a visible fact is a loss, not caution.
- When a property needs sub-values the page does not state (a shipping rate with no destination, a price valid-until date), keep the visible text in `description` or offer text and list the missing values as open questions. Do not fill them with assumptions.

## Do not mark up

- Ratings or reviews that are not visible on the page.
- Review stars for the business's own organisation or local business, based on reviews it collected or embeds about itself: search engines have restricted these ("self-serving reviews"); confirm the current rule in the engine's documentation before marking up, and never promise stars.
- Reviews copied from another platform where the page only shows a widget whose content the site does not host, unless the guidelines allow it (to confirm).
- Prices, currencies, availability or offers that differ from the page, or that the page does not show.
- FAQs that are not on the page, or that are marketing claims dressed as questions.
- Addresses, phone numbers, opening hours, founders or awards the page does not show.
- Hidden text added only for markup.

## Aggregates

- Count the reviews shown on the page and average their ratings line by line; state the computation.
- If the page's widget shows a rounded figure (for example 4.3 from values averaging 4.25), the markup value must not contradict what visitors see; note the rounding and choose a value consistent with the display.
- `reviewCount` or `ratingCount` must equal the reviews the rating is based on.

## Existing markup

Themes and plugins often output partial markup (a `Product` with name and price only, a generic `WebSite`). Read the page source in the material. Extend it, replace it, or turn it off; never ship two blocks describing the same entity with different values.

## Validation and verification

1. Validate syntax and vocabulary with a schema.org validator.
2. Test eligibility with the search engine's rich-result testing tool (eligibility is its decision).
3. After an approved deployment, inspect the live URL and watch the structured-data reports for errors over the following weeks.
4. Record the state: drafted, approved, deployed, validated, verified live.

## Platform claims

Which types earn rich results, the required and recommended properties, restrictions by site type (for example on FAQ results) and review policies change. Cite the search engine's own current documentation `(first-party: <URL>, checked YYYY-MM-DD)` or mark *to confirm*. The schema.org vocabulary itself is stable reference; it does not establish eligibility.

## Authorisation

Editing theme templates, plugins or page code to add, replace or remove markup is a live change: scope, rollback and the owner's approval, then verification on the live page.
