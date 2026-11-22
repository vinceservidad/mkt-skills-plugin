# Meta creative learning agenda: question, test, result and next brief

```yaml
artifact_type: playbook
decision: select valid creative measurement and turn the result into a scoped next action
scope: Meta creative learning before, during and after campaigns; not automatic spend or tracking changes
owner: tracking-measurement
inputs: decision at stake, hypothesis, available measurement, outcome definitions, valid comparison and constraints
evidence_status: inferred
confidence: not-assessed
freshness: live-check
dependencies: event integrity, existing causal/experiment contracts, creative and channel owners
authorization: draft
rollback_or_stop: stop invalid causal claims, premature winners or unauthorized implementation
```

## Source basis and ambiguity

Pages 60-62 of the July 2026 guide introduce a learning agenda and distinguish social metrics, brand outcomes and business outcomes. Pages 63-66 cover pre-campaign testing and mid-campaign reporting; pages 67-71 cover lift, creative-question alignment and subsequent learning. [Source record](../../creative-strategy/references/meta-july-2026-source-notes.md).

The rendered page 60 table has mismatched descriptions for Action plan and Marketing mix modeling. Page 67's exposed-control label conflicts with the unexposed-control and exposed-test definitions on pages 92 and 99. Do not silently repair those statements when summarizing the source. The MKT application below instead uses the existing [experiment learning system](experiment-learning-system.md) and explicit exposure roles. It is an original operational adaptation, not a verbatim source definition.

## MKT application

Write a decision-changing learning question, not a list of metrics. Populate:

`decision | question | hypothesis | evidence gap | method | assigned arms/exposure | primary metric/source | guardrails | sample/lag/window | stopping rule | owner | next decision`

Do not invent the required duration, minimum detectable effect or target lift. Estimate them with the existing measurement methods when inputs support it; otherwise identify the blocking input. A declared learning agenda is a plan, not a running experiment or scheduled monitor.

| Campaign phase | Work to complete |
|---|---|
| Pre-campaign | Confirm objective/event integrity, create materially interpretable alternatives, set the comparison and decision rule, and preflight that the creative can communicate the construct being measured. |
| Mid-campaign | Check implementation, data quality, exposure balance and guardrails. Keep routine observational reporting distinct from experiment inference; avoid treatment changes or opportunistic stopping that invalidate the planned comparison. |
| Post-campaign | Allow relevant outcome lag, assess validity and uncertainty, report the observed result separately from a mechanism story, then update the next brief and scoped learning record. |

## Match the method to the question

- **A/B Testing:** compare specified alternatives under a valid randomized design. Two ad-exposed variants may estimate their relative difference; they do not establish incremental advertising impact versus no ads. When a whole concept changes several components, interpret a bundle contrast rather than claim the hook alone caused the difference.
- **Brand Lift:** evaluate the named survey construct. Map ad recall to recognizable brand cues, awareness to a clear introduction, favorability to supported brand meaning, and purchase intent to a concrete reason to consider buying. Purchase intent remains a survey outcome, not an observed order.
- **Conversion Lift:** requires a valid exposure/holdout comparison and suitable business-event measurement. State the population, assignment, denominator, conversion definition, uncertainty and study scope. Current study availability, budget and implementation requirements must be verified; the PDF does not grant eligibility.
- **Ads Reporting and creative breakdowns:** describe delivered activity and attributed results, affected by allocation and audience mix. Use them to form hypotheses and check operations; do not turn the best-performing observed cell into a causal winner.
- **Viewability/third-party evidence:** useful for delivery and opportunity-to-see checks within the partner's measured coverage. Under MKT governance, viewability alone does not prove attention, comprehension, sales or causation. Partner reports and customer data require actual permitted access.

Keep the source's social/brand/business distinction while preserving the actual data basis. Likes and views do not establish sales; ROAS does not establish contribution profit; attribution and incrementality are not interchangeable.

**Synthetic calculation, not a study result:** two equally sized randomized populations of 10,000 eligible people have 240 purchases in an ad-eligible arm and 200 in a no-ad holdout. Their observed rates are 2.4% and 2.0%, a 0.4 percentage-point difference, corresponding to 40 additional purchases on a treated-sized basis and 20% relative lift. Those arithmetic differences alone do not establish statistical certainty, valid randomization or profit. Do not count all 240 as caused by ads. Unequal group sizes require rate-based normalization rather than raw count subtraction.

## Turn learning into work

Return the revised creative hypothesis and a specific handoff: what to retain, what to change, the evidence that could overturn the decision, and the next comparison. Retain null, inconclusive and guardrail-harming results. Do not treat the guide's favorable-result expansion examples as unconditional permission to scale; `$optimization-scaling` owns that decision with economics, maturity, capacity and explicit authorization.

**Deliverable:** populated agenda or experiment brief, validity/uncertainty assessment, result calculation with defined denominators, creative-to-study alignment, scoped learning and the next production/channel decision. Reuse the existing [experiment-learning template](../../../library/templates/experiment-learning.md). No experiment, tracking change, live campaign or background monitoring has been executed merely by returning this plan.
