# Ecommerce Growth Playbook

## Knowledge metadata

- Primary type: playbook
- Secondary type: diagnostic map / routing
- Decision: which ecommerce constraint to diagnose next, and which specialist owns the resulting decision
- Owner: `$cro` loads it; the cross-business priority decision belongs to `$growth-strategy`, and paid-media scaling belongs to `$optimization-scaling`
- Evidence status: repeatable diagnostic structure; order, product, and contribution economics must be supplied
- Freshness: stable; current platform controls require first-party checks

## Purpose

Diagnose what currently limits ecommerce contribution profit (stated before or after media) and route each constraint to its owner. This is not a fixed sequence or a channel checklist.

## Start from the outcome

1. Name the primary business outcome, its profit level and included costs, the baseline, the horizon, and the source of truth.
2. Reconcile orders, net or gross revenue, discounts, refunds, COGS, variable fulfillment, payment fees, and media spend. Never subtract discounts or refunds twice.
3. Mark missing economics. Give a break-even table or sensitivity range instead of a profitability verdict.

## Diagnose the limiting constraint

The areas have no fixed order. Evidence decides which constraint binds. Several may co-limit, and some may stay unresolved.

| Diagnosis area | Owner of the resulting decision |
|---|---|
| Market, customer, and buying situation | `$customer-research`, `$icp-jtbd` |
| Product-market fit and offer strength | `$offer-strategy` |
| Price, package, or discount architecture | `$pricing-monetization` |
| Creative performance | `$creative-strategy` with the channel skill |
| Landing page, product page, and checkout friction | `$cro` |
| Tracking accuracy and attribution | `$tracking-measurement` |
| Repeat purchase, lapse, and win-back | `$retention-strategy`; cohort and lifetime value economics in `$retention-economics` |
| Paid-channel efficiency | `$google-ads`, `$meta-ads` |
| Unexplained metric change | `$performance-diagnostics` |

## Growth levers

Model: ecommerce revenue = traffic × conversion rate × AOV, with revenue and AOV on one stated basis (gross sales or net revenue, and tax and shipping treatment). Contribution profit also depends on COGS, variable fulfillment, payment fees, refunds not already deducted in net revenue, and, after media, media spend. Each lever is a hypothesis for a diagnosed constraint, not a priority list:

- Increase qualified traffic
- Improve conversion of qualified visitors
- Increase average order value without eroding contribution margin before media or raising refunds
- Improve repeat purchase rate
- Reduce wasted spend

## Decision rules

- `$growth-strategy` decides which constraint or opportunity to pursue first across the business, and records explicit non-priorities.
- Do not scale traffic before tracking, economics, and conversion fundamentals are confirmed. Every paid-media expansion goes through the `$optimization-scaling` gates.
- A lever that raises conversion rate, AOV, or attributed revenue while lowering contribution profit after media is not growth.
- Live budget, price, offer, page, and campaign changes require explicit approval.
