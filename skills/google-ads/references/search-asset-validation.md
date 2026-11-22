# Search asset validation and insertion

```yaml
artifact_type: checklist
decision: check whether drafted Search assets can be used accurately in the proposed configuration
scope: responsive Search assets, keyword insertion and ad-to-destination fit; paid wording remains with creative-strategy
owner: google-ads
inputs: drafted assets, eligible keywords, offer terms, locale, final URLs, required text, account-visible settings
evidence_status: officially-documented
confidence: not-assessed
freshness: 30-days
dependencies: library/contracts/PLATFORM-CURRENCY.md, current Google documentation, actual account availability, supplied evidence
authorization: read-only
rollback_or_stop: stop unsupported claims or incompatible combinations; require authorization for material account edits
```

## First-party verification: 2026-09-30

Google's [responsive Search ad documentation](https://support.google.com/google-ads/answer/7684791?hl=en) documents assets that can appear in different orders and combinations, optional text omission, previews that do not show every combination, and flexible uses of assets. It documents 3–15 headline inputs and 2–4 description inputs, limits of 30 characters per headline, 90 per description and 15 per path, with double-width language characters counted differently. These are documented input constraints, not instructions to fill every slot or expected performance improvements.

Mandatory-text and pinning guidance must be read together with actual serving behavior. Google documents designated positions for required text, while other parts of the same help article describe omission/shortening in some formats. Prefer claims that remain accurate independently; verify the intended pinning/format in the current account instead of asserting that every draft preview guarantees every live rendering.

Google's [keyword insertion explanation](https://support.google.com/google-ads/answer/2454041?hl=en) says the eligible ad-group keyword is inserted, which may differ from the person's search term. Its [setup and troubleshooting guide](https://support.google.com/google-ads/answer/6371157?hl=en) covers default text, capitalization, length, grammar and policy restrictions. Treat insertion as a conditional configuration choice, not a default relevance technique.

No account was inspected for this verification. Recheck these high-change claims when current behavior affects the decision; check availability before recommending a live control. Vendor averages and Ad Strength recommendations are not promises of client results.

## Validate a proposed asset set

- **Scope:** identify the actual ad group, locale, keywords/query evidence, destination and requested copy job. Keep brand, category, competitor and product intent distinguishable where they need different truthful promises.
- **Input fit:** validate required input counts and character accounting against current rules. Preserve terms and meaning while shortening. Do not remove a material qualifier to get a green length check.
- **Combination fit:** inspect independently truthful assets, product/offer consistency, pronoun dependence, missing qualifications, contradiction, truncation and omission. Record mandatory language, approved positions and account checks still needed.
- **Automation fit:** distinguish the supplied assets from text customization, URL expansion and other generated/borrowed assets. Inspect their controls and destinations where relevant; do not claim all serving text was reviewed from one preview.
- **Insertion fit:** enumerate each eligible keyword and fallback; inspect grammar, supported availability/affiliation, claim scope, length and policy constraints. Do not assume that safe fallback text protects unsafe inserted alternatives.
- **Destination fit:** follow the actual final URL, product/variant, geography and approved offer. Confirm that the page supports the ad's promise and next action. Route rewriting to Copywriting and page diagnosis to CRO.
- **Outcome fit:** define the conversion action, goal inclusion, action-optimization status, value basis and business outcome separately. Ad Strength, Quality Score, CTR and public asset frequency do not establish commercial success.

Return a usable draft/validation handoff with exact supported assets, incompatibilities, required revisions and unresolved checks. A proposal is not an authorized account edit. When an edit is authorized, preserve downloaded/draft, validated, posted and verified live states rather than treating a successful local Editor check as publication.

## Source boundary

The [Shopify article coverage review](shopify-google-ad-copy-source-review.md) records editorial examples and dated tutorial issues. Those sources inform questions to investigate; the first-party pages above govern current mechanics. Draft finished assets with [Search ad drafting](../../creative-strategy/references/search-ad-drafting.md), preserving Creative Strategy's ownership.
