# Churn reason coding & save verification playbook

Use alongside [churn-guide.md](churn-guide.md) to separate involuntary vs. voluntary churn, code exit interviews and support logs cleanly, build unobstructed honest save flows, and verify whether saved customers stay active past the verification window.

## 1. Retention diagnosis and structured reason coding

Before proposing any save incentive or email flow, segment losses into four distinct buckets from billing and product/order logs (`scripts/tally.py` / `scripts/sum_by.py`):
1. **Involuntary churn (failed payments):** Track hard vs. soft declines, recovery rate, and silent cancellations after dunning exhaustion. Fix here first because failed-card recovery saves willing customers without margin loss.
2. **Early-cohort churn (pre-habit drop-off):** Customers cancelling in cycle 1 or 2 usually reflect acquisition/fit mismatch (`02-icp-persona`, ad promises) or unmet activation (`15-onboarding`).
3. **Voluntary mature churn (explicit cancel):** Code exit-survey answers and support tickets into mutually exclusive root causes (`oversupply / cadence too fast`, `taste or product quality`, `late/damaged fulfilment`, `price vs. perceived value`, `temporary travel/pause`, `fit / competitor switch`), explicitly recording sample coverage (`answered N of M cancels`) and reminding the team that exit surveys are **self-reported**.
4. **Silent lapse (non-subscription repeat drop):** Track inter-purchase interval lengthening before customers go dark (`15-lifecycle` RFM triggers).

## 2. Reason-matched honest save architecture

Always keep cancellation visible, simple, and one-step (no dark patterns, forced phone calls, or hidden buttons; verify local negative-option rules *to confirm* via `20-compliance`). Match each coded exit reason to the honest fix:

| Diagnosed reason | Honest intervention | Owner and check |
| --- | --- | --- |
| Too much product / travel | One-click **Skip next delivery**, **Extend cadence**, or **Pause** option | Retention + fulfilment settings |
| Wrong fit / taste / feature confusion | Product switch recommendation, troubleshooting guide, or concise human help | `15-onboarding` / `04-pmf-check` |
| Delivery / ops failure | Proactive delay alert + replacement/repair workflow | Operations |
| Price (confirmed root cause) | Smaller existing tier from `offer.md`, OR an **owner-set** targeted save credit with margin cap and expiration | Owner commitment only (`07-pricing`) |

Never fire a default "50% off to stay" popup at every canceller; blanket discounts erode margin on customers who only needed a skip button.

## 3. Save verification and targeted win-back

- **Decision-relevant verification window:** Count a "save" as real only if the customer remains active and billed across subsequent cycles (e.g., box 2 or month 3 after intervention) relative to an untreated or baseline cohort, never counting a delayed cancel two weeks later as a win.
- **Reason-based win-back (`15-lifecycle`):** Mail lapsed/cancelled users only where explicit marketing consent exists (`11-email-channel`), leading with proof that their original exit reason changed (new cadence control, resolved stock/delivery issue, updated formula) rather than endless generic coupons.

## Sources

The Complete Marketing System, section 15 Retention (Servidad, 2026); FTC Negative Option / Click-to-Cancel compliance guidance (to confirm current jurisdiction rules).
