---
name: marketing-intake
description: Capture and grade the evidence, metric definitions, access, authorization, and reusable project context behind a marketing engagement before substantial audit, diagnosis, planning, or scaling work; use when scope, data provenance, economics, shared context, or approval boundaries are unclear; not for making the specialist decision itself.
---

# Marketing Intake

Record what was actually received, from whom, in what state. Intake does not establish that a claim is true — it establishes what is known, how it is known, and what would reverse the conclusion.

Classify the resulting artifact with [`KNOWLEDGE-TAXONOMY.md`](../../library/contracts/KNOWLEDGE-TAXONOMY.md). An intake record is a process artifact and evidence ledger, never proof of an outcome.

## Required inputs

Required before intake can complete: business model, primary business outcome, account and market scope, date range and comparison period, currency, reporting timezone, data sources supplied, access available, and the system treated as the business source of truth.

Required before any profitability, scaling, or lead-quality conclusion: cost and profit definitions with named profit level, cost of goods sold, discounts, refunds, fulfillment and payment costs, and — for lead generation — lifecycle stage definitions and Customer Relationship Management outcomes.

Intake may proceed with gaps. It may not present a gap as satisfied.

## Method

1. Record engagement context and scope. Separate what the user asserted from what a source system shows. See [Engagement context](references/engagement-context.md).
2. Enter every decision-relevant claim in the evidence register with its source, collection method, and evidence state. See [Evidence register](references/evidence-register.md).
3. Define every metric and lifecycle term before any comparison. Platform labels are not definitions. See [Metric definitions](references/metric-definition-register.md).
4. Record conversion architecture: Google Ads conversion goals, their included conversion actions and Primary or Secondary status; Meta objective, conversion location, performance goal, dataset, and event. Record attribution settings, windows, conversion lag, and known tracking defects.
5. Record capacity — inventory, fulfillment, creative, sales, and service — wherever a recommendation could exceed it.
6. Request only the missing evidence that could change a decision, ranked by decision impact. See [Access and data request](references/access-and-data-request.md).
7. Record the authorization boundary before proposing any change. See [Authorization register](references/authorization-register.md).
8. State which decisions the current evidence can and cannot support, and name the gaps capable of reversing each one.
9. When the project needs reusable cross-skill context, create or update `.agents/marketing-context.md` from [`templates/marketing-context.md`](../../library/templates/marketing-context.md) using [Marketing Context governance](references/marketing-context-governance.md). Preserve provenance, evidence state, contradictions, freshness, and the change log; do not copy unnecessary raw data into it.

## Rules

- Never upgrade an evidence state. A user-reported figure remains `asserted` until observed in a named source; a figure in a supplied document or screenshot remains `document-supplied`, weaker than `observed`, until seen in the named source system or an unedited export from it; an `observed` figure remains `observed` until reconciled with the business source of truth, and `reconciled` until independently confirmed by a second source or check.
- An evidence state is not a causal, scaling-proof, or integration state. Even `verified` does not license a causal claim; grade causality on the causal evidence ladder through `$tracking-measurement`, per [Evidence and proof scales](../../library/contracts/GLOSSARY.md#evidence-and-proof-scales).
- Never fill a gap with a benchmark, an assumed margin, a typical conversion rate, or a platform default. Record it as unknown.
- Do not treat platform attribution as the business outcome, and do not reconcile platforms by addition.
- Do not compare periods, accounts, or channels before their metric definitions are recorded and confirmed compatible.
- Do not request personal data that no decision requires. Record research provenance without exposing identifying detail. Quotations require a traceable supplied source.
- Absence of a supplied cost structure blocks a profitability conclusion; it does not block analysis labeled as efficiency-only.
- Intake authorizes nothing. Recording an approval is not receiving one, and no intake output may imply a live change.
- Do not declare intake complete while a gap capable of reversing the primary decision is open. Declare it partial and name the gap.
- Marketing Context is a reusable summary, not evidence promotion. A statement copied into `.agents/marketing-context.md` keeps the source evidence state and specialist owner.
- Do not make every task load the entire Marketing Context. Downstream work should use only decision-relevant sections.

## Output

Intake record: engagement context; primary business outcome; scope and period; source-of-truth system; evidence register with states; metric and conversion definitions; capacity constraints; authorization boundary; ranked outstanding requests; decisions currently supportable; decisions blocked and what would unblock them; exact status.

Marketing Context when useful: versioned `.agents/marketing-context.md` containing only reusable decision context, source/evidence state, freshness, contradictions, open decisions, and change history.

Access request: named source, specific artifact or export, date range, reason it is decision-changing, and what remains blocked without it.

## Library references

- [`templates/marketing-context.md`](../../library/templates/marketing-context.md) — reusable structure for project-level shared Marketing Context.
- [Marketing Context governance](references/marketing-context-governance.md) — creation, update, freshness, contradiction, and ownership rules.

## QA

Confirm every decision-relevant claim carries a source and evidence state; no state was upgraded without a named source; no gap was filled by assumption; metric definitions precede comparisons; conversion goal and action language follows the glossary; personal data is minimal and provenance is traceable; the authorization boundary is explicit; blocked decisions are listed rather than answered; and any Marketing Context update preserves source, evidence state, contradictions, freshness, and version history.
