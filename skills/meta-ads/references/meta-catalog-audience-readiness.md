# Meta catalog and audience readiness

```yaml
artifact_type: checklist
decision: establish whether catalog products and audience inputs support the intended campaign without losing required constraints
scope: Meta catalog/audience planning and QA; no catalog edits, audience uploads or campaign changes
owner: meta-ads
inputs: catalog and event evidence, product truth, market and fulfillment constraints, audience source and current account controls
evidence_status: inferred
confidence: not-assessed
freshness: live-check
dependencies: product owner, tracking-measurement, current eligibility and authorized access
authorization: draft
rollback_or_stop: stop mismatched products, assumed audience restrictions or unapproved coverage expansion
```

## Source basis

BUY-2026-02 pages 44-53 distinguish event parameters, catalog item data and product sets; recommend accurate product information and describe catalog match rate. Pages 55-70 distinguish audience sources, estimates, controls/suggestions and responses to overlap. [Source provenance and edition limits](meta-2026-guides-source-notes.md).

This operational checklist is an original MKT extension of the existing [prospecting](prospecting.md) and [retargeting](retargeting.md) references. Do not interpret source recommendations as verified current defaults.

## Product-to-event-to-destination checks

Record the actual artifact/version and what was inspected. A screenshot of the catalog overview is not an inspection of every item or event.

| Check | Required evidence and disposition |
|---|---|
| Product truth | Reconcile item/variant identity, price, currency, availability, image and destination with the business's source of truth for the intended market. Flag stale or contradictory records. |
| Feed responsibility | Identify each data source, its owner and update process. Avoid two writers unintentionally overwriting the same item. Do not assume that a connected Shopify app means a successful current sync. |
| Product sets | Express the commercial inclusion/exclusion rule, test its actual membership, and preserve market, stock, offer and fulfillment restrictions. Use sets rather than unnecessary catalog duplication when the business context permits. |
| Event matching | Trace a representative permitted event's product identifiers to the intended catalog item/variant. Distinguish product-ID matching from matching a customer identity. Use `$tracking-measurement` for event integrity and deduplication. |
| Delivery readiness | Record current item issues, permissions, catalog/ad-account association, destination eligibility and what remains unverified. A healthy feed does not prove an ad is eligible or live. |

The source recommends broad product sets, at least 20 products in one context and a catalog match rate above 75%. Those figures are edition recommendations, not a reason to invent products, include an unfulfillable item or assert every event is correct. Keep the denominator and period of a supplied match rate visible. Product match rate, event match quality, event receipt and valid purchase measurement are different checks.

**Original synthetic example:** a GBP-only campaign can deliver only three verified in-stock UK variants. A larger global set contains items unavailable in that market. Keep the verified eligible set while checking current campaign requirements; do not expand it simply to meet a study-guide count. If a Purchase payload names a parent ID while the catalog expects variant IDs, record the observed mismatch and ask the technical owner to verify the integration's intended mapping before changing production.

## Audience constraints ledger

For every input, record `business reason | source/window | proposed audience | hard requirement or suggestion | actual control/level | account evidence | exception`.

The guide's distinction is important: controls restrict delivery, while suggestions guide it and may allow expansion. A custom audience used as a suggestion does not by itself establish a retargeting-only campaign. Verify the actual account options and exclusions. Do not describe source-audience membership, a model suggestion or a lookalike percentage as proof of who received an ad.

Use authorized and current source lists. Check whether they represent frequent/high-value customers, all contacts, or an outdated mix, and whether consent/use restrictions permit the proposed use. Do not expose list members or upload customer information in a method response. Source counts and similarity percentages are not evidence of audience quality.

Separate potential audience size, estimated daily reach/results and actual delivered reach. Do not sum daily reach to obtain unique campaign reach. For overlap, compare definitions, outcome quality, delivery and reasons for separate budgets. Overlap alone neither proves auction self-competition nor requires consolidation. Preserve meaningful language, eligibility, offer and cost-control distinctions.

**Return:** item/set QA findings; event-mapping dependencies; audience ledger; keep/fix/test decisions with evidence; retained exclusions; current-platform checks; implementation owner and exact status. Any expansion of an existing system's eligible products, audiences or coverage goes through `$optimization-scaling` before execution.
