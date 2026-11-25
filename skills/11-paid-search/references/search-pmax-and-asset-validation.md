# Paid Search Alignment, Performance Max, AI Max and Asset Validation

Use when designing or auditing Search, Performance Max, AI Max, or responsive Search assets. Treat all platform defaults, eligibility limits, and UI names as high-change platform facts to verify against official docs or the live account (*to confirm*).

## 1. Search outcome alignment chain

Verify every link in order before altering bids or keywords:

`business outcome -> qualified conversion action -> Primary/Secondary goal status -> value basis -> bid strategy -> eligible keywords & negatives -> search terms -> ad promise -> landing page`

- Quality Score, Ad Strength, CTR, and raw form-fill conversions are diagnostics, never commercial outcomes.
- Keep brand, category, competitor, and product-specific intent in separate intent themes when they require distinct promises or landing pages.

## 2. Current Google Ads layers (*to confirm* in docs and account)

| Concept | Google documented label | Audit check |
| --- | --- | --- |
| Search automation layer | AI Max for Search campaigns | Optimization layer on Search (not a separate campaign type) combining search term matching and asset optimization |
| Automated ad text | Text customization | Google's label replacing automatically created assets inside AI Max |
| Landing page matching | Final URL expansion | Check URL inclusions and URL exclusions plus destination parity before enabling |
| AI Max controls | Locations of interest, brand settings, URL controls | Verify account defaults and traffic leakage |
| Cross-inventory automated campaign | Performance Max | Automated inventory toward configured conversion goals |
| PMax channel breakdown | Channel performance report | Verify date-range availability and channel mix in account |
| PMax query control | Performance Max campaign and account negatives | Google documents Search/Shopping inventory negatives separately from brand exclusions |

## 3. Performance Max inspect checklist

Before recommending PMax restructuring:
1. Audit conversion-goal and value integrity first (exclude low-intent micro-goals from Primary bidding).
2. Check Shopping-only (feed-only) vs asset-supported scope, listing groups, asset groups, search themes, audience signals, Final URL expansion, text customization, and brand exclusions.
3. Inspect overlap with Standard Search or Standard Shopping and verify product GTIN/brand/MPN and Merchant Center health (`>= 500 x 500` px minimum image check and feed accuracy *to confirm*).
4. Never infer hidden channel splits or query coverage not shown in reporting, and never split asset groups without a distinct product, message, destination, market, or margin hypothesis.

## 4. Responsive Search ads and Dynamic Keyword Insertion (*to confirm*)

- **Documented input limits:** 3–15 headlines (30 chars max each), 2–4 descriptions (90 chars max each), 15 chars per display path (*to confirm* against current Google RSA docs; fill quality assets rather than padding weak variations).
- **Combination integrity:** Google warns assets can reorder or omit optional lines in previews and live formats. Write lines that stay accurate independently without relying on another headline to add a material qualifier, price condition, or eligibility rule. Verify pinning only where mandatory legal or commercial disclaimers require fixed placement.
- **Keyword Insertion (`{KeyWord:...}`):** Inserts eligible ad-group keywords (not raw user search terms). Check every single eligible keyword and fallback against grammar, length limits, brand/competitor trademark policy, and offer truthfulness before proposing insertion.
- Route finished ad copy rewriting to `10-ad-copy` and landing page changes to `12-landing-page` or `13-*`.
