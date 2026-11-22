# Google Ads Optimization Workflow

## Knowledge metadata

- Primary type: process
- Secondary type: diagnostic workflow / change-control checklist
- Decision: which diagnosed Google Ads constraint, if any, justifies a proposed change or test
- Owner: `$google-ads`
- Evidence status: account, query or item, and business source-of-truth evidence required; ROAS and CPA conclusions stay provisional without economics at a named profit level (for example contribution profit after media) or qualified-lead economics
- Freshness: live-check for current Google Ads controls through `library/contracts/PLATFORM-CURRENCY.md` and the `$google-ads` platform registry
- Authorization: read-only; every live change requires explicit approval

## Objective

Improve the primary business outcome (named profit level, realized revenue, or qualified pipeline) through structured diagnosis and testing. Platform metrics are diagnostics, not the objective.

## Cadence

This is the recurring optimization cadence named in `$google-ads`. What drives it is decision need and data maturity, not habit. Run a cycle when a change is proposed, when a prior change's decision window and conversion lag have matured, when a material metric change appears, or when measurement changes. Do not act on data the prior change has not yet had time to produce. No fixed frequency is implied. A scheduled recurring loop belongs to `$marketing-operations` and stays `designed` until its runtime is verified.

## Workflow

1. **Frame the decision.** Name the primary business outcome, source of truth, profit level or lead stage, date range and comparison, and the decision this cycle supports.
2. **Validate measurement.** Check conversion goals, their included conversion actions, each action's Primary/Secondary status, campaign goal selection, counting, values, attribution, lag, and agreement with the business source of truth. Route defects to `$tracking-measurement` before optimizing.
3. **Review the data.** Spend, conversions, CPA, ROAS, CTR, conversion rate, and search terms or items, compared like for like, with volume, efficiency, mix, and measurement effects kept separate.
4. **Diagnose.** Identify whether the constraint is query intent or traffic, offer, creative or assets, landing page, tracking, feed or eligibility, or bidding and budget. Keep competing explanations open until the evidence separates them. Route offer to `$offer-strategy`, landing page to `$cro`, and unexplained cross-channel change to `$performance-diagnostics`.
5. **Propose the smallest interpretable change.** Name the exact entity, current and proposed state, rationale, expected effect, risk, protected brand, query, and product coverage, and a rollback or stop rule.
6. **Approval gate.** Nothing is changed in the account until the owner explicitly approves that exact change and scope. Record the approval.
7. **Test.** Measure impact against the original hypothesis and the business source of truth once the decision window and conversion lag have matured. `$tracking-measurement` checks validity before direction is read.
8. **Learn.** Record a scoped learning: account, campaign type, query or product set, period, spend range, and evidence level. Update the system only with learnings stated in scope, never as universal best practices.
9. **Scaling is a separate decision.** Any budget, target, or coverage expansion goes through the `$optimization-scaling` readiness, economics, constraint, marginal-evidence, capacity, guardrail, and authorization gates.

## Guardrails

- Validate tracking before optimization.
- Avoid reacting to insufficient or immature data.
- Prioritize business outcomes over platform metrics.
- Preserve valuable coverage unless evidence supports removal.
- Do not claim an undocumented "Google algorithm change"; label documented, account-visible, experimental, inferred, and unknown separately.

## Cycle record

Label every entry `observed`, `calculated`, `inferred`, `assumed`, or `unknown`.

- Primary business outcome and source of truth:
- Measurement status:
- Diagnosed constraint and evidence:
- Proposed change: entity, current state, proposed state, rollback or stop rule:
- Approval status and scope:
- Exact status: draft | approved | saved | published | live | processing | verified (use only the states that apply; `processing` means live while results or conversion lag have not matured; never infer a later state from an earlier one)
