# Causal Evidence Ladder (C0 to C5) and Lift Study Selection

Use when grading marketing claims, choosing an incrementality test design, or deciding whether reported results are strong enough to justify a budget jump or channel exit. Causal evidence complements `17-attribution` and Meridian MMM (`references/measurement-trifecta-and-meridian.md`).

## 1. The Causal Evidence Ladder (C0 to C5)

Classify every performance claim honestly by its weakest structural link:

| Level | Underlying evidence | What decision it supports |
| --- | --- | --- |
| C0 | Platform-attributed conversions or ROAS (no control) | Delivery and creative triage only; never proof of incremental lift regardless of sample size |
| C1 | Multi-source correlation or uncontrolled before-and-after | Hypotheses and test prioritization |
| C2 | Modeled attribution or uncalibrated MMM with explicit assumptions | Directional planning, revisable as real tests run |
| C3 | Quasi-experiment (matched geo markets, synthetic control, interrupted time series) | Provisional causal estimate inside the tested scope |
| C4 | Randomized controlled experiment (user holdout, randomized geo-lift, switchback, validated platform lift) | Causal estimate inside the tested population, offer, and window |
| C5 | Replicated randomized experiments across periods, geographies, or channels | Standing strategic rule within established boundaries |

Match the required evidence level to the cost of being wrong: reversible low-spend tests only need `C1-C2`, whereas sustained scaling steps or cutting a core channel warrant `C3` minimum and `C4` preferred (`19-scale-paid`).

## 2. Lift study selector (User Holdout vs. Geo-Lift vs. Platform Lift)

| Method | Best fit | Primary watch-outs |
| --- | --- | --- |
| Geo-lift experiment | Channel-level incrementality (Meta, YouTube, Search, multi-channel) | Avoid choosing "best" and "worst" cities after launch; balance pre-test regional variance and run long enough for power |
| User holdout / PSA | High-volume single-platform accounts with native holdout support | Guard against cookie loss, cross-device leakage, and spillover between household/account users |
| Platform lift studies (Meta Conversion Lift / Brand Lift, Google Lift) | Validated ad-account lift when eligible (*to confirm* current minimums/tools) | Apply seller-grades-own-work scrutiny: reconcile conversions in the store/CRM rather than platform events alone, verify unexposed control integrity |

## 3. Meta Blueprint lift-study guardrails (distilled from 2026 guides)

- Compare the **assigned opportunity-to-see (test)** population against the **assigned unexposed (control)** population, never comparing only users who clicked or viewed against everyone else (selection bias invalidates lift).
- Hold creative, bidding, and major budget changes steady mid-test, wait out post-exposure purchase lag, and compute incremental CAC as `test spend / net incremental customers` in the system of record.
- Never scale a `C4` result automatically into a different season, higher CPM tier, or new offer without confirming unit economics (`17-unit-economics`) and operational capacity (`19-scale-paid`).

## Sources

Meta Media Buying (Feb 2026) and Creative Strategy Professional (July 2026) study guides; Google Ads incrementality documentation; The Complete Marketing System, section 17 Measurement (Servidad, 2026).
