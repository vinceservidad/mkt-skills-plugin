# Google lead capture to offline outcome validation

```yaml
artifact_type: checklist
decision: establish which offline business outcomes can be matched, reported and used by a Google campaign
scope: lead or offline outcome measurement design and reconciliation; no uploads or account changes
owner: tracking-measurement
inputs: acquisition identifiers, CRM/POS stages, outcome records, consent state, timestamps, values, currencies and selected import method
evidence_status: inferred
confidence: not-assessed
freshness: 30-days
dependencies: current Google method documentation, authorized data sources, campaign goal/action definitions
authorization: read-only
rollback_or_stop: hold unverified or duplicate outcomes; stop unauthorized data transmission and escalate source mismatches
```

## Validate the whole chain

Specify each stage separately: ad interaction, authorized identifier collection, form/lead record, qualification, realized sale or other agreed outcome, import receipt, matching/attribution, campaign goal use and business-source reconciliation. A tag firing or a captured email completes only part of this chain. Do not label every lead a qualified lead, assign a purchase value to checkout activity or claim revenue because an upload returned success.

For a bounded sample, record the business record key, source system, stage definition, permitted identifiers, consent, outcome timestamp/timezone, value basis and currency, conversion action, deduplication/adjustment key, receipt/error state and reconciliation result. Distinguish event time, upload time and attribution reporting time. Account for conversion lag and late/refunded/reversed outcomes without silently double-counting stages or subtracting costs twice.

Separate losses by layer: uncaptured identifiers, ineligible/unconsented data, invalid fields, missing outcomes, rejected imports, unmatched records, reporting lag and attribution differences. A difference is not automatically a broken tag or a causal effect. Report observed sample counts and unknowns instead of inventing a matching percentage.

Google Ads owns conversion-action configuration, goal inclusion and how the campaign uses those goals. Tracking supplies the validated event/value contract. Lead value needs the client's actual qualification, close and realized-value basis with the economics owner; it is not a benchmark CPL or a form-completion count.

## Current method verification

Read on 2026-09-30: Google's [enhanced conversions for leads overview](https://support.google.com/google-ads/answer/15713840?hl=en), [settings updates](https://support.google.com/google-ads/answer/16884284?hl=en) and [implementation checklist](https://support.google.com/google-ads/answer/16782203?hl=en). The overview/settings notice describes a 2026 move toward Data Manager API uploads and changes to enhanced-conversion settings, while some tutorial bodies retain legacy API or setup paths. Treat this as a migration/access check for the actual implementation, not permission to use a dated upload recipe.

Confirm the supported current method, identifier requirements, customer-data terms, consent and diagnostic surfaces before planning an integration. Hashing supports matching; it does not remove authorization, minimization or consent obligations. Never include real identifiers in a public report or source-review artifact. No MKT upload adapter, customer connection or live eligibility is established by this reference.

## Source boundary and deliverable

Shopify's [offline conversion tracking](https://www.shopify.com/ph/blog/offline-conversion-tracking) (published 2025-05-20) and [Google conversion tracking](https://www.shopify.com/ph/blog/google-ads-conversion-tracking) (published 2025-08-26) were fully read on 2026-09-30. They are editorial setup guidance; automatic capture, anonymous-data assurances and receipt-as-performance conclusions are excluded. This validation matrix is an original MKT adaptation using the existing measurement contract.

Return the populated stage map, sample reconciliation, rejected/unknown records, source defects, exact measurement status and required repair or verification handoff. For broader collection or causal questions use [Google/Meta signal validation](google-meta-signal-validation.md). Consult the [article source review](../../google-ads/references/shopify-google-ad-copy-source-review.md) only when provenance or a source conflict matters.
