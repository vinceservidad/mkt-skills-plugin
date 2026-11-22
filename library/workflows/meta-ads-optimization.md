# Meta Ads Optimization Workflow

## Knowledge metadata

- Primary type: process
- Secondary type: diagnostic workflow / checklist
- Decision: which diagnosed Meta Ads constraint, if any, justifies a proposed change or test
- Owner: `$meta-ads`
- Evidence status: account and business source-of-truth evidence required; platform-reported results stay provisional until reconciled
- Freshness: live-check for current Meta controls through `library/contracts/PLATFORM-CURRENCY.md` and the `$meta-ads` platform registry
- Authorization: read-only; publishing, budget, bid, audience, and status changes require explicit approval

## Objective

Improve the primary business outcome (named profit level, realized revenue, or qualified pipeline) that Meta Ads contributes to. CPM, CTR, CPC, conversion rate, CPA, and platform ROAS are diagnostics, not the objective.

## Cadence

Run a cycle when a decision needs it and the data can support it: a proposed change, a matured decision window or conversion-lag period, a material metric change, or a measurement change. Habit is not a reason to run it, and it sets no fixed frequency. A scheduled recurring loop belongs to `$marketing-operations` and stays `designed` until its runtime is verified.

## Workflow

1. **Frame the decision.** Name the primary business outcome, source of truth, profit level or lead stage, date range and comparison, and the decision this cycle must support.
2. **Verify measurement.** Confirm objective, conversion location, performance goal, dataset or Meta Pixel, selected optimization event, Conversions API and deduplication, and attribution setting. When integrity is unknown, label platform results provisional and route defects to `$tracking-measurement`.
3. **Decompose.** Delivery (CPM, reach, frequency) → response (outbound CTR or the relevant attention signal) → visit quality → conversion rate → value or lead quality → profit at the profit level named in step 1. Use breakdowns only where the sample supports them.
4. **Diagnose the binding constraint first.** Test competing explanations across measurement, auction and delivery, objective and event, audience, creative, destination, offer, and operational capacity. No layer has a fixed priority: the evidence decides which one binds, and several may co-limit or remain unresolved. Record the disconfirming evidence.
5. **Route what Meta does not own.** Angle or concept → `$creative-strategy`; offer → `$offer-strategy`; landing page or checkout → `$cro`; event or attribution defect → `$tracking-measurement`; unexplained or cross-channel change → `$performance-diagnostics`.
6. **Form one hypothesis.** State the constraint, the proposed change, the expected mechanism, the primary metric tied to the business outcome, guardrails, the decision window including conversion lag, and the stop rule.
7. **Approval gate.** Present the exact entity, current and proposed state, expected effect, downside, and rollback condition. Nothing goes live without explicit approval.
8. **Measure.** After the window matures, have `$tracking-measurement` check validity before anyone reads direction, then evaluate against the business source of truth.
9. **Record a scoped learning.** Keep the result bound to its audience, placement, creative, offer, period, and spend range. Preserve nulls and contradictions.
10. **Scaling is a separate decision.** A favorable test is not scaling authorization. Any budget or exposure increase goes through the `$optimization-scaling` readiness, economics, constraint, marginal-evidence, capacity, guardrail, and authorization gates.

## Cycle record

Label every entry `observed`, `calculated`, `inferred`, `assumed`, or `unknown`.

- Primary business outcome and source of truth:
- Measurement status:
- Binding constraint or co-limiting set, with evidence:
- Competing explanations rejected, and why:
- Proposed change or test, and its owner:
- Approval status and scope:
- Exact status: draft | approved | saved | published | live | processing | verified (use only the states that apply; `processing` means live while results or conversion lag have not matured; never infer a later state from an earlier one)
