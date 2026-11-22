---
name: youtube-ads
description: Plan, audit, or diagnose YouTube video advertising — format selection, audience targeting, view-through measurement, and creative fit for skippable and non-skippable in-stream, bumper, in-feed, and Shorts formats; not for Search, Shopping, or Performance Max, and not for organic YouTube content strategy.
---

# YouTube Ads

Classify each model, format decision, or measurement method with [`KNOWLEDGE-TAXONOMY.md`](../../library/contracts/KNOWLEDGE-TAXONOMY.md). YouTube runs through the Google Ads platform but is a distinct discipline from Search, Shopping, and Performance Max: it is a video medium whose campaigns may serve awareness, consideration, or direct-response objectives, with different attention economics, format constraints, and measurement norms. Route Search/Shopping/PMax structure, bidding, and account mechanics to `$google-ads`; route organic YouTube content, posting cadence, community management, and channel growth to `$organic-social`, which owns unpaid, algorithmically distributed content — this skill covers paid placement only, including the paid decision to promote an organic video.

Format specifications, placements, audience segment types, and targeting controls are high-change platform facts. Apply [`PLATFORM-CURRENCY.md`](../../library/contracts/PLATFORM-CURRENCY.md) before any current format or targeting-availability claim: cite Google's first-party documentation with its check date, or state it as a check to perform, and confirm account visibility before an account-specific plan. There is deliberately no YouTube registry; [Format selection](references/format-selection.md) carries the dated first-party citations.

## Required inputs

Primary business outcome and where in the funnel this campaign is expected to work — awareness, consideration, or direct response — since format, targeting, and measurement all depend on that answer; available video creative assets and their length/format fit; audience data available — your data segments such as Customer Match and website or app visitors, plus affinity, in-market, and custom segments, which is how Google Ads currently labels these segment types and lists all of them as available for Video campaigns (first-party: https://support.google.com/google-ads/answer/2497941, checked 2026-09-26) — confirmed for the campaign type in the account; brand safety and content-adjacency requirements; and whether brand lift or view-through purchase behavior needs to be measured.

## Method

1. State the funnel objective explicitly before selecting a format; a direct-response objective on a bumper ad or a brand-awareness objective evaluated on last-click conversion rate is a measurement mismatch, not a performance problem.
2. Select ad format to fit the objective and the creative actually available. See [Format selection](references/format-selection.md).
3. Build audience targeting from evidence — first-party lists and observed in-market/affinity behavior — before reaching for broad demographic or interest targeting; state which layer is doing the work, and confirm the segment types and targeting controls available to the campaign type per `library/contracts/PLATFORM-CURRENCY.md`.
4. Assess creative fit before launch: whether the asset communicates its message in the format's actual attention window, not the length the business happened to produce. Route to `$creative-strategy` for concept and hook development if the creative itself needs work.
5. Define the measurement plan before launch, matched to the funnel objective: brand lift study for awareness objectives, view-through and assisted-conversion tracking for consideration, direct conversion tracking for response — see [Measurement fit](references/measurement-fit.md) and route method selection and evidence grading to `$tracking-measurement`.
6. Rank actions by expected business impact, confidence, reversibility, and creative production capacity.

For an annotated creative review or production handoff, use [Google ABCD video review](references/google-abcd-video-review.md); concepts and hooks stay with `$creative-strategy`, and current placement requirements still need verification.

## Rules

- Do not evaluate an awareness-objective campaign on direct-response metrics, or a direct-response campaign on view-through reach; state the objective and hold the campaign to its own measurement standard.
- Do not present view-through conversions as equivalent to click-through conversions; a view-through credit means the ad was shown, not that it was necessarily seen, attended to, or causal — grade the claim per the causal evidence ladder in `$tracking-measurement`.
- Do not recommend a skippable in-stream format for a message that requires the full asset to land; the documented skip option appears after 5 seconds (see [Format selection](references/format-selection.md) for the dated first-party citation), so design the pre-skip window accordingly, or select a non-skippable or bumper format that matches the message's actual requirement.
- Do not state a format length, skip window, placement, segment type, or targeting control from memory or from a third-party summary; cite the first-party source with its check date or label it unverified per `library/contracts/PLATFORM-CURRENCY.md`.
- Do not reuse a Search or Shopping conversion definition unmodified for a video-campaign objective; state the definition explicitly per the funnel stage this campaign targets.
- Preserve brand-safety and content-adjacency settings; do not loosen them to expand reach without explicit approval, since a brand-safety incident carries a cost this system cannot quantify or reverse after the fact.
- A view count, watch time, or completion rate is a delivery and engagement signal, not the business outcome; require a business-outcome measurement for any performance claim beyond delivery.

## Output

Plan: funnel objective; format selection with rationale; audience targeting layers; creative fit assessment; measurement plan matched to objective; capacity required; exact status.

Diagnosis: observed change; funnel objective it should be measured against; competing explanations (creative fatigue, audience saturation, seasonality, format mismatch, measurement change) considered before attributing a cause; evidence level; recommended action.

## QA

Confirm the funnel objective is stated and the campaign is measured against its own objective; format specifications and targeting availability are cited from first-party documentation with a check date or labeled unverified per `library/contracts/PLATFORM-CURRENCY.md`; format matches the message's actual attention requirement; audience targeting states which evidence layer is doing the work; view-through claims are graded rather than treated as equivalent to click-through; brand-safety settings are preserved absent explicit approval to change them; and no delivery or engagement metric is presented as the business outcome.
