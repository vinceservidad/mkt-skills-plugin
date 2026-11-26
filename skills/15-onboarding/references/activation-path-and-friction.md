# Activation path-to-value audit and cohort experiments

Use alongside [onboarding-guide.md](onboarding-guide.md) to validate whether the activation metric predicts real retention, strip unnecessary onboarding friction without deleting mandatory setup, and test activation fixes cleanly across cohorts.

## 1. Validating the activation definition

A valid activation metric proves two things in historical cohorts (`inputs/`):
1. **Real customer value (`Dream outcome` + `02-jobs-to-be-done`):** The buyer has actually achieved the first meaningful outcome they paid for (e.g., brewed and dialed in their first specialty cup, published their first reconciled monthly report, ran their first live workflow), not merely opened an email or finished a tooltip tour.
2. **Retention separation across cohorts:** Compare day-30 / month-2 retention of customers who hit the proposed activation event inside the target window against those who did not (`scripts/sum_by.py` from cohorts). If both groups churn identically, the event is a vanity milestone rather than true activation.

## 2. Step-by-step path-to-value friction audit

Walk chronologically from payment/signup to the activation event and classify every step into one of three buckets:

| Classification | Criteria | Action |
| --- | --- | --- |
| Essential setup | Result, billing, safety, or qualification literally fails without it | Keep step; clarify instructions, defaults, and inline progress |
| Product or operations gap | Customer stalls because the product breaks, shipping lags, or expectations were unclear | Hand root fix to `04-pmf-check`, `07-offer-design`, or operations |
| Unnecessary friction | Internal form fields, duplicate confirmations, long feature tours, or non-essential choices | Remove, automate from earlier inputs, or defer until after first value |

Never remove mandatory qualification, setup, or expectation-setting steps solely to boost day-1 completion percentage if doing so shifts failures into month-1 churn. Map every week-1 nudge, guide, or check-in (`15-onboarding`) directly to a counted support ticket cluster or measured drop-off step.

## 3. Cohort experiments and upstream/downstream handoffs

- **Equal-window cohort testing:** Measure activation rate (`activated within N days / starting new customers`), median time-to-first-value, and early cohort retention before and after a single flow change across matched maturity windows (never compare an incomplete week against a closed month).
- **Root-cause handoffs:** Route bad-fit buyers who cannot activate despite clear onboarding back to `02-icp-persona` and `11-paid-social` / `11-paid-search` targeting filters; pass customers who activate cleanly but drop later to `15-lifecycle` and `15-churn-prevention`.

## Sources

The Complete Marketing System, section 15 Retention (Servidad, 2026); Lincoln Murphy desired-outcome onboarding and cohort activation analysis principles.
