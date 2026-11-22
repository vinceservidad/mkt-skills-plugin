# Google audience relationship and delivery readiness

```yaml
artifact_type: checklist
decision: determine whether an audience relationship and its proposed delivery use match the business question
scope: Google audience planning and review; current controls vary by campaign type and account
owner: google-ads
inputs: campaign type, business outcome, audience source, qualifying event, membership rules, consent and account-visible controls
evidence_status: inferred
confidence: not-assessed
freshness: 30-days
dependencies: source signal validation, library/contracts/PLATFORM-CURRENCY.md, authorized customer data and approved exclusions
authorization: read-only
rollback_or_stop: stop unauthorized uploads or reach changes; hold claims based on unverified membership or incremental effect
```

## Populate the audience decision

Define the actual business question: acquire a new customer, address an unresolved purchase concern, support an eligible prior customer, or observe a relationship inside existing coverage. A relationship label does not establish intent, consent, eligibility or a profitable outcome.

Record the source system, qualifying event, membership window and why it fits the purchase/use cycle, refresh cadence, expiry/re-entry behavior, matching gaps, overlap and exclusions. Include the intended next action, compatible creative and destination. A purchase exclusion may make sense for new-customer acquisition but remove relevant people from a different repeat-purchase question; do not apply it universally.

Inspect the actual campaign/ad-group use separately from audience membership. Google's [targeting and observation documentation](https://support.google.com/google-ads/answer/7365594?hl=en), checked on 2026-09-30, distinguishes reach-restricting targeting from observation within existing targeting. It also says first-party observation segments can inform Smart Bidding. Therefore observation does not mean no delivery/bidding influence. Confirm supported controls and their reach/signal meaning in the current campaign; do not apply Search/Display settings to every Google campaign type or assume an audience signal confines Performance Max delivery.

For uploaded lists, establish authorized source use and current eligibility with the measurement/data owner. A tag, match receipt or hashing does not establish complete membership or permission. For website or other engagement sources, validate the qualifying event and suppression updates rather than assuming every visitor is a ready buyer.

## Interpret evidence and return the handoff

Compare audience reporting on the same event definitions, periods and business-outcome basis. Prior-relationship users may have bought anyway; low attributed CPA or high ROAS does not establish incremental efficiency. Frequency or weak response is supporting evidence, not a universal saturation threshold. Use actual demand/capacity and measurement evidence before changing scope or allocating more spend.

Return the populated source/membership/delivery record, compatible message and destination, overlap/exclusion rationale, validation gaps and proposed bounded test or justified hold. Creative Strategy writes paid assets, Tracking Measurement validates signals and causal claims, and Optimization Scaling owns expansion of an existing system. A design is not a configured audience or a verified campaign; material uploads, exclusions, targeting and spend changes need explicit authorization.

## Source boundary

Shopify's [Google retargeting guide](https://www.shopify.com/ph/blog/google-ads-retargeting) (published 2023-03-10), fully read on 2026-09-30, suggests considering prior relationships and relevant next messages. This is an original MKT operational adaptation, not adoption of dated UI steps, fixed windows, cost benchmarks, tag replacement or guaranteed retargeting superiority. Current terminology and controls are governed by first-party documentation and actual account visibility. See the [article coverage review](shopify-google-ad-copy-source-review.md) for source limits.
