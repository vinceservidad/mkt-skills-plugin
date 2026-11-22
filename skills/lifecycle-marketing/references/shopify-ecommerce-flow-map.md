# Ecommerce lifecycle: event-to-message flow map

```yaml
artifact_type: playbook
decision: design ecommerce communication flows that respond to the actual customer state
scope: owned-channel ecommerce automation design; no sends, new connectors or inferred attachment access
owner: lifecycle-marketing
inputs: reliable events, lifecycle definitions, consent and suppression state, product cycle, platform capacity
evidence_status: inferred
confidence: not-assessed
freshness: 180-days
dependencies: owning skill rules, supplied evidence, measurement and economic definitions
authorization: draft
rollback_or_stop: stop unsupported claims or unauthorized actions; review guardrail breaches before expanding
```

## Source and evidence boundary

[Shopify: Ecommerce Email Automation Types, Examples, and Tips](https://www.shopify.com/ph/blog/ecommerce-email-automation), published 2026-09-02; reviewed 2026-09-29.

Shopify separates welcome, browse abandonment, cart/checkout abandonment, post-purchase, reengagement, win-back and loyalty communications. It distinguishes inactive subscribers from previously purchasing customers and event-triggered communication from a scheduled promotion.

This is Shopify editorial guidance, not a controlled effectiveness study. The MKT application below is an original operational adaptation using this system's existing governance. No merchant result, benchmark, universal timing rule, or performance guarantee is imported. Verify current platform features separately before implementation.

## MKT application

Use the smallest set of flows that addresses an evidenced objective. Do not deploy every flow because a catalog lists it. A view without a cart, a cart without checkout, and an incomplete checkout are different observed events; none independently proves why the person left.

For every selected flow, fill an executable specification: entry event and source, eligibility, deduplication key, wait condition, state recheck immediately before delivery, exit event, suppression and consent conditions, late/missing-event fallback, owner, and measurement window. If order or consent data are stale, do not label the recipient eligible by assumption.

Resolve collisions explicitly. A verified completed order cancels a pending abandonment message; an existing service failure or refund should route to the responsible service/retention owner rather than trigger a generic cross-sell. Coordinate multiple campaigns under the actual contact policy. Do not invent a fixed number of hours or days when the purchase/replenishment cycle is unknown.

Keep never-purchased inactive subscribers distinct from lapsed customers. `$retention-strategy` determines a win-back rationale, `$activation` defines first meaningful value, and `$copywriting` drafts the requested words. A user asking for a complete sequence should receive the coordinated flow and copy, with assumptions visible, rather than being told to start a new task for each owner.

**Deliverable:** populated flow table, collision/exit rules, copy brief or coordinated finished copy, test fixtures and success/stop conditions. Test duplicate events, late purchases, consent withdrawal and retries before approval. An attributed recovery or email open is not evidence of incremental business value.
