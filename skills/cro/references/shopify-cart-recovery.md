# Cart recovery: diagnose the leak before buying the recovery

```yaml
artifact_type: playbook
decision: choose a cart or checkout intervention and interpret recovery without overstating business value
scope: pre-conversion ecommerce cart and checkout; lifecycle owns messaging and tracking owns causal validity
owner: cro
inputs: cart/checkout definitions, dated funnel data, actual fee and payment experience, costs and permissions
evidence_status: inferred
confidence: not-assessed
freshness: 180-days
dependencies: owning skill rules, supplied evidence, measurement and economic definitions
authorization: draft
rollback_or_stop: stop unsupported claims or unauthorized actions; review guardrail breaches before expanding
```

## Source and evidence boundary

[Shopify: How To Improve Your Abandoned Cart Recovery Rate](https://www.shopify.com/ca/blog/abandoned-cart-recovery-rate), published 2026-09-02; reviewed 2026-09-29.

Shopify discusses recovery measurement, follow-up messages, checkout friction and clear charges. Its recovery-rate definition relates recovered abandoned carts to the abandoned-cart population. The Canadian article was retrieved because the linked Philippine variant was unavailable; this is not a region-specific operating rule.

This is Shopify editorial guidance, not a controlled effectiveness study. The MKT application below is an original operational adaptation using this system's existing governance. No merchant result, benchmark, universal timing rule, or performance guarantee is imported. Verify current platform features separately before implementation.

## MKT application

Locate the problem in the supplied journey before selecting an incentive. Confirm technical completion and actual displayed price, shipping, fees, delivery promises and payment behavior. Route a broader unexplained performance change to `$performance-diagnostics`; do not invent a checkout defect from a high abandonment rate alone.

Define the event, unique cart/customer basis, eligible population and recovery window. Distinguish cart abandonment from checkout abandonment and platform-attributed recovery from all returning purchasers. Explain exclusions and incomplete data rather than reporting a deceptively precise rate.

**Calculation:** recovered eligible carts / eligible abandoned carts x 100. A synthetic 100 recoveries among 1,000 abandoned carts is 10%. In equal randomized groups, 100/1,000 treated versus 80/1,000 control is an observed 2 percentage-point difference, or 20 additional recoveries in the treated-sized group. It is not evidence that all 100 were caused by the intervention, nor a significance claim; assess uncertainty and validity with `$tracking-measurement`.

Prioritize verified failures before persuasion tests. For a discount, compare contribution after the incentive, fulfillment, fees, refunds and implementation costs using the business's definitions; do not double-count discounts already in net revenue. A higher recovery count may buy revenue that would otherwise have returned without an incentive.

**Deliverable:** located evidence, ranked repair/test, control and variant, reconciled recovery calculation, economic guardrails and decision rule. Route message triggers to `$lifecycle-marketing` and copy to `$copywriting`; complete their supporting work within the user's task. No automatic campaign, checkout or price change is authorized.
