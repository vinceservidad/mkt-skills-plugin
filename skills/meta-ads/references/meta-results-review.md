# Meta results review: from report fields to a bounded decision

```yaml
artifact_type: playbook
decision: interpret a Meta report at the correct entity and result definition, then return an evidence-backed next action
scope: single-channel Meta review and reporting handoff, not cross-channel reconciliation or a causal experiment
owner: meta-ads
inputs: full report scope, metric definitions, settings, comparison period, business outcomes and prior changes
evidence_status: inferred
confidence: not-assessed
freshness: live-check
dependencies: tracking-measurement, performance-diagnostics, economics and scaling owners
authorization: read-only
rollback_or_stop: stop incomplete totals, mixed-result arithmetic, invented diagnosis or recommendations reported as executed
```

## Source basis

BUY-2026-02 pages 84-87 align business goal, campaign objective and performance goal with metrics and give a six-step analysis sequence. Pages 88-90 separate reporting from experiments. ASSOC-2026-01 pages 99-104 cover entity levels, result definitions, filters, breakdowns and export/report options. [Source record](meta-2026-guides-source-notes.md).

The source sequence is: inspect results; inspect other relevant metrics; inspect setup; evaluate those together; repeat and compare ad sets; identify optimization opportunities. The safeguards, arithmetic and report example below are original MKT applications.

## Establish the report contract

Record source file/account, export date, entity grain and IDs, date range, comparison, timezone, currency, filters, attribution setting, conversion location/event, result type and completeness. A filtered screenshot, newest-page result or partial export is not an account total. Never infer missing rows are zero.

For each campaign, resolve what Results actually counts. Purchases, installs, raw leads, qualified leads, conversations and video views cannot share one combined result total or blended CPR. Distinguish all clicks, link/outbound clicks and landing-page views. Retain returned metric labels and disclose missing definitions.

Compute ratios from compatible totals, not an unweighted average of row ratios. Use spent/results for the named result and attributed value/spent for attributed ROAS. For ROAS, zero spend makes the ratio undefined; for cost per result, zero results makes the ratio undefined. A missing required input prevents calculation. Zero verified spend with a positive verified result count gives a computed cost per result of zero, but does not establish free incremental acquisition or complete paid-data coverage. Positive spend with zero observed purchase value gives zero attributed ROAS, not evidence of a measurement defect by itself.

## Apply the six-step review

Start with the goal-aligned result and its quality/value, then examine supporting delivery, response, visit and conversion measures. Connect each finding to actual creative IDs, audience/placement settings, budget/bid choices and the destination. Compare matched windows and disclose changes to definitions, attribution, offer or tracking.

Use entity breakdowns to form hypotheses, not causal verdicts. The system's unequal allocation, audience mix, lag and small samples can explain apparent winners. Do not pause a profitable ad solely for low CTR, pronounce fatigue from frequency alone, or claim an algorithm change from volatility. The guide's example is illustrative, not benchmark evidence for the user's account.

For each material row return `observed result | calculation | interpretation/confidence | competing explanation | proposed action or hold | validation needed | owner | status`.

**Original synthetic example:** a purchase campaign spends GBP 180 for 12 attributed purchases and GBP 720 attributed purchase value: CPA GBP 15 and ROAS 4.0x. A separate lead campaign spends GBP 120 for 20 form leads, of which a matched CRM cohort verifies eight qualified leads: raw CPL GBP 6 and qualified CPL GBP 15. Keep the 12 purchases and 20 form leads separate; do not report 32 equivalent conversions at GBP 9.38 CPR. The cost total is GBP 300 if scope/currency match. Profit and incrementality are still unknown.

A usable bounded update would state the purchase result and qualified-lead result separately, preserve any tracking or cohort uncertainty, and report the actual hold/proposal state. Do not invent a pause, budget increase, completed test or message sent to a stakeholder.

## Finish with the decision the evidence supports

Rank the most consequential issue, including a justified hold or measurement repair. Route deeper unexplained change to `$performance-diagnostics`, source reconciliation/causality to `$tracking-measurement` and existing-system budget or coverage expansion to `$optimization-scaling`. `$marketing-reporting` combines finished findings across channels without taking over this Meta decision. `$marketing-operations` owns any recurring decision process beyond the communication artifact.

**Return:** a clean campaign table or requested short update with spend, precisely named outcomes, relevant value/return, confidence, next action, owner and exact status. A report schedule in a guide is a documented option, not a configured subscription or active background monitor.
