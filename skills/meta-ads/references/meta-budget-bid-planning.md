# Meta budget and bid planning: a decision with explicit assumptions

```yaml
artifact_type: playbook
decision: choose a justified budget structure and bidding approach, and produce a costed planning scenario
scope: Meta planning and underdelivery review; existing-system expansion remains with optimization-scaling
owner: meta-ads
inputs: business goal, order or lead value, outcome cost, time horizon, constraints, observed configuration and performance
evidence_status: inferred
confidence: not-assessed
freshness: live-check
dependencies: economics, measurement integrity, current platform controls and explicit authorization
authorization: draft
rollback_or_stop: stop invented values, guaranteed forecasts or unapproved budget and bidding changes
```

## Source basis

BUY-2026-02 pages 29-38 separate auction/reservation, campaign/ad-set budgets, daily/lifetime distribution, pacing and spend-based/goal-based/manual bidding. PLAN-2026-02 pages 16-22 explain bid tradeoffs; pages 37-50 give budget-selection criteria and two estimation methods. [Source record and unresolved instruction differences](meta-2026-guides-source-notes.md).

The following decision process, sensitivity analysis and examples are original MKT applications, not measured improvements or current UI instructions.

## Make the decision before selecting a field

Record `business outcome | result definition | value/cost basis | horizon | total authorized exposure | hard constraints | observed setup | proposed change | verification`.

A budget controls intended spend; a bid strategy controls how delivery pursues outcomes within its constraints. Neither proves unit economics. Separate initial planning from a request to increase an existing system's budget or coverage; the latter must go to `$optimization-scaling` and its full gates.

| Decision | Planning logic |
|---|---|
| Auction or reservation | Compare flexibility and outcome optimization with advance reach/frequency planning. Reservation eligibility, supported objectives and delivery commitments require current verification. A forecast is not booked inventory. |
| Campaign or ad-set budget | Consider campaign-level outcome equivalence and spend flexibility versus protected allocations, materially different goals, values, bid strategies or constraints. Do not merge budgets only to obtain an automation badge. |
| Daily or lifetime | Match an average-daily plan versus a total-period constraint to cash exposure, schedule and opportunity variability. A daily budget is not a guaranteed identical daily charge. Verify actual spending controls before configuring a hard cap. |
| Spend-based | Candidate when maximizing outcome count or validated value within the authorized budget is the priority. More spend is not a business success by itself. |
| Goal-based | Candidate when an economically supported outcome-cost or return objective matters more than full delivery. A tight goal may constrain spend; it is not a guarantee of each conversion's cost. |
| Manual bid cap | Candidate only with an evidenced model of auction bids and outcomes. Do not equate an auction bid ceiling with a ceiling on reported CPA. |

Use the source's terms for source recall. For an implementation handoff, separately verify the actual performance goal, bid control, attribution and value inputs in the account. The guide's ambiguous CPM/setup rows are not a substitute for that check.

## Calculate scenarios, not promises

For a sales-goal scenario, use matching periods and units:

`required orders = target revenue / expected average order value`

`scenario ad spend = required orders * assumed cost per purchase`

Identify whether revenue is total business revenue or an explicitly scoped paid-attributed target. Do not silently assign all organic or returning-customer revenue to advertising. An allowable maximum CPA is a constraint, not a measured expected CPA. The guide's estimated-minimum wording does not prove attainability.

**Original synthetic example:** a 10-day paid-revenue planning target of GBP 12,000 and expected order value GBP 60 implies 200 orders. At CPA scenarios of GBP 12, 15 and 18, modeled spend is GBP 2,400, 3,000 and 3,600. The base scenario implies 4.0x revenue/ad spend, not profit or incremental return. Without margins and other relevant costs, affordability is unknown. Verify capacity for the modeled orders and show which assumptions require evidence.

For a reach/frequency planning scenario:

`impressions = audience size * target reach fraction * frequency per interval * number of matching intervals`

`scenario spend = impressions / 1000 * CPM`

**Original synthetic example:** 400,000 eligible people, 60% target reach, two impressions per reached person per week for three weeks and GBP 4 CPM implies 1,440,000 impressions and GBP 5,760 modeled spend. If frequency is already a campaign-total six, do not multiply by three again. This assumes a consistent reached-population basis; changing weekly cohorts require a clearer reach model. Actual reach, frequency, eligibility and delivery remain unverified.

Never divide by a zero or unknown order value. Keep rates' denominators explicit. A click-to-purchase rate plus CPM alone cannot establish purchase CPA without a link between impressions and clicks; do not insert an assumed CTR to complete missing data.

## Diagnose underdelivery without reflexive expansion

Check status, review/billing/access issues, schedule, source integrity, outcome volume, audience and placement constraints, bid/value goals and recent edits. Separate available budget from budget actually spent. A learning-limited label does not automatically justify more spend, a weaker optimization event or removal of protected constraints. Propose the smallest evidence-supported intervention with a review window and rollback condition. A written budget schedule is not scheduled execution.

**Return:** selected structure and bid rationale; alternatives rejected; scenario table with sources/assumptions; exposure and commercial constraints; unresolved checks; one next decision and its owner; exact draft/approval status. Reuse the existing campaign brief and channel/scaling workflow rather than create a parallel budgeting system.
