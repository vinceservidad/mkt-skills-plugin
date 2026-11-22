# CRO Improvement Workflow

## Knowledge metadata

- Primary type: process
- Secondary type: experiment workflow / audit checklist
- Decision: which verified pre-conversion barrier to fix or test, and how its business effect will be judged
- Owner: `$cro`; `$tracking-measurement` owns test validity and the learning record
- Evidence status: heuristic observations are hypothesis inputs; causal claims require a valid test
- Authorization: read-only review; live page, form, or checkout changes require explicit approval

## Objective

Improve the primary business outcome (purchases, qualified leads, or contribution profit, stated before or after media) through the pre-conversion path by removing verified friction and increasing clarity. Conversion rate is a diagnostic, not the objective. A higher rate that comes with worse AOV, refund rate, lead quality, or contribution profit is not an improvement.

## Workflow

1. **Define the outcome and boundary.** Name the primary business outcome, the conversion boundary, and any qualified or supporting conversion. Reserve "Primary conversion action" for the Google Ads setting.
2. **Research users.** Use recordings, surveys, usability evidence, support and sales objections, and technical errors. Label each input as observed, inferred, assumed, or unknown.
3. **Analyze traffic and message scent.** Trace the upstream promise to the page. Segment by source, device, intent, landing page, and new or returning user when the data permits.
4. **Identify the first meaningful leak.** Separate technical failure from persuasion weakness. Fix verified defects before testing persuasion variants.
5. **Form a hypothesis.** State the problem, evidence, expected mechanism, proposed change, primary metric tied to the business outcome, and guardrails. When the change is to copy (headline, body, offer wording, CTA, or microcopy), specify the problem the rewrite must solve and hand it to `$copywriting` as a rewrite brief; CRO does not write the copy.
6. **Prioritize.** Rank by evidence strength, expected impact, effort, risk, and learning value.
7. **Design a valid test with `$tracking-measurement`.** Fix the primary metric, stop rule, sample and duration approach, and conversion lag before launch, and check instrumentation. Choose a focused change that can test the mechanism over a redesign. Copy variants come from `$copywriting`.
8. **Approval gate.** No live page change without explicit approval.
9. **Measure business impact.** Check validity before reading direction, evaluate against the business source of truth and guardrails, and record a scoped learning.

## Review areas

- Message match
- Offer clarity (the offer itself belongs to `$offer-strategy`; price and packaging belong to `$pricing-monetization`)
- Trust elements and traceable proof
- User experience, accessibility, and mobile
- Checkout or lead flow, including necessary qualification, legal, and pricing information that must not be removed to inflate conversion rate

Once the problem starts after the conversion boundary and concerns reaching first value, it goes to `$activation`.
