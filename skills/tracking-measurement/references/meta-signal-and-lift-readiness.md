# Meta signal and lift readiness: implementation evidence before interpretation

```yaml
artifact_type: playbook
decision: specify the evidence needed to trust Meta outcome signals and distinguish attribution settings from valid lift measurement
scope: Meta web/app/offline/messaging and CRM measurement handoffs; no production tagging or study launch
owner: tracking-measurement
inputs: business outcome chain, source events, dataset, permitted identifiers, values, account configuration and measurement question
evidence_status: inferred
confidence: not-assessed
freshness: live-check
dependencies: current technical requirements, event integrity, causal evidence and channel owner
authorization: draft
rollback_or_stop: stop fabricated event quality, privacy bypass, duplicate outcomes or unsupported causal claims
```

## Source basis

BUY-2026-02 pages 41-46 distinguish data sources, events, parameters and custom-conversion rules; page 24 describes standard and model-driven incremental attribution. Pages 88-96 discuss A/B, Brand Lift and Conversion Lift. ASSOC-2026-01 pages 107-108 emphasize privacy controls and hashing. PLAN-2026-02 page 83 contains differing prose/table statements about study data sources. [Source record](../../meta-ads/references/meta-2026-guides-source-notes.md).

A publicly retrieved [Blueprint CRM course overview](https://fbp.exceedlms.com/student/path/253141-conversions-api-crm-lead-quality), checked 2026-09-30, describes feeding first-party CRM outcomes back for lead quality rather than volume. Its lesson content was sign-in gated. The workflow below is an original MKT application; it is not a recovered lesson, a connected CRM or current API documentation.

## Build a source-to-business handoff

Start with a business outcome and map `real action | originating system | event/trigger | source connector | dataset | parameters/value/currency | consent basis | receipt | deduplication | reporting | reconciled business record`.

The guide's channels are useful planning categories: browser website activity, app activity, server/shared outcomes, offline activity and business messaging. Verify each actual integration rather than assume every named source is installed or eligible. A custom-conversion rule refines event classification; it does not create another real purchase or prove a more valuable customer.

Use existing [event integrity](event-integrity.md) and [Google/Meta signal validation](google-meta-signal-validation.md), not a second tagging standard. Select permitted representative events and verify semantic correctness, completeness, uniqueness, value/currency, timing, source receipt and business reconciliation. Match implementation fields and normalization rules to current official technical specifications. Do not fabricate payload names or expose personal identifiers in an audit artifact.

For leads, preserve stages such as submitted, contacted, qualified and won only when the business actually defines and records them. State who determines qualification, the delay, cohort matching, duplicate/update handling and what evidence is missing. Do not relabel every instant form as qualified or assign fictional LTV to force value bidding. Return the exact missing CRM event/data request and a bounded validation plan.

Catalog product matching and customer event matching are different. A high event-match indicator alone does not prove correct triggers, values or deduplication. **Original synthetic case:** 18 real orders each emitted through browser and server create 36 transmissions, not 36 orders. Confirm whether duplication is actually resolved downstream; two collection paths are not automatically a defect and do not prove extra sales.

Hashing and server-side transport do not remove consent, suppression, sensitive-data or contractual obligations. Neither converts a prohibited data use into an allowed one. If required privacy or data handling evidence is absent, stop that implementation path and obtain an appropriate review.

## Separate four measurement questions

| Question | Evidence needed |
|---|---|
| Was the outcome collected correctly? | Event-level QA and source-to-business reconciliation. |
| Why do reports differ? | Matched definitions, windows, timezone/currency, lag and coverage through the existing attribution-reconciliation method. |
| Which alternative performed better? | A valid comparison design; two live ads receiving unequal algorithmic delivery are not automatically an A/B test. |
| What additional outcome did ads cause? | A valid incremental design and appropriate uncertainty, not the presence of the word incremental in an attribution setting. |

The guide's model-driven incremental attribution is a documented source description of a predictive approach. It is not the same evidence as a newly run randomized holdout, and it cannot prove the counterfactual for a particular order. Preserve the returned label and method; do not rename model estimates as experimentally observed results.

Use [platform lift studies](platform-lift-studies.md) and the existing [creative learning agenda](meta-creative-learning-agenda.md) for study selection and execution requirements. Define assigned opportunity-to-see versus no-opportunity groups, not only people who actually viewed the ad. Check contamination, outcome lag, treatment changes, sample/power, guardrails and stopping rules before interpreting results.

BUY pages 90, 93 and 96 give duration, response, spend and holdout recommendations. These do not guarantee sufficient power, current account eligibility or a statistically significant result. PLAN page 83's source inconsistency remains disclosed; verify the actual study's data-source requirements before recommending configuration.

**Return:** populated source map; verified checks and missing evidence; precise implementation handoff; named measurement method and evidence level; study feasibility or bounded alternative; no unsupported winner, causal lift or live change. Reuse the existing experiment and learning templates when the task reaches those stages.
