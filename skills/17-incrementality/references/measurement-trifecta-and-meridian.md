# The Modern Measurement Trifecta & Meridian MMM Guide

Distilled from official `@GoogleAds` measurement playbooks (*Attribution, incrementality & MMM: The modern measurement trifecta* and *One year testing Meridian*). Platform experiment thresholds and Meridian features change — verify current official Google Ads Help and Meridian documentation (cite URL + date) or mark *to confirm*.

## 1. Why One Measurement Method Is Never Enough (The Trifecta)

Every measurement method answers a different question and has a distinct blind spot. Combine all three rather than asking one tool to do all three jobs:

| Pillar | Question it answers | Cadence & granularity | Blind spot |
| --- | --- | --- | --- |
| **Attribution** (`17-attribution`) | Which campaigns, ads and keywords should get daily bid/creative adjustments? | Daily / weekly; campaign & ad level | Over-credits lower-funnel/brand/retargeting touches; misses offline & non-clickable media. |
| **Incrementality / Lift Experiments** (`17-incrementality`) | Did this channel or campaign actually cause net-new revenue/customers that would not have happened anyway? | Periodic tests (weeks); channel / geo / campaign level | Point-in-time snapshot; tests one lever at a time; needs clean holdout or geo controls. |
| **Marketing Mix Modeling (MMM — e.g., Meridian)** | How should next quarter's total budget split across all channels (paid, brand, offline, seasonal) for maximum marginal ROI? | Quarterly / annual; channel & macro level | Needs sufficient historical time-series data; uncalibrated MMMs can misestimate digital causality. |

## 2. Lower-Threshold Incrementality Testing

Historically, formal platform lift studies required very large budgets, locking small and mid-sized advertisers out of causal proof.
- Modern geo-based and platform-native incrementality experiments (including Google Ads' lowered-threshold incrementality tests — verify current minimum spend requirements and eligibility in official Google Ads Help docs) make causal testing feasible for mid-sized accounts.
- Still check statistical power FIRST against the business's own baseline sales variance by region: a smaller budget threshold does not override basic math if baseline volume is too noisy to detect the minimum profitable lift.

## 3. Calibrating MMM with Incrementality Priors (Meridian)

Google's open-source Bayesian MMM framework (**Meridian**, with **Meridian GeoX** geo-experiment design) solves the classic MMM vs. attribution split by **calibrating the model with incrementality results**:
- Run a clean geo-lift or holdout experiment on a core channel first (`17-incrementality`), measuring net-new orders/revenue in the store or CRM.
- Feed the measured incremental ROI and its uncertainty interval into the MMM as a **Bayesian prior** so the model anchors channel elasticity to real causal evidence rather than pure historical correlation.
- Use scenario planning to inspect diminishing-returns saturation curves before shifting quarterly budgets (`19-scale-paid`, `20-budget`).
- **Readiness gate:** Do not recommend building an MMM for an early-stage business with thin spend or less than ~1–2 years of clean weekly channel spend and outcome history; start with clean source-of-truth tracking (`17-tracking-plan`), unit economics (`17-unit-economics`) and focused holdout/geo tests first.
