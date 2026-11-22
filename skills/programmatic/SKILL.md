---
name: programmatic
description: Plan or diagnose demand-side-platform display and video buying across the open exchange — supply-path optimization, inventory quality and fraud screening, and viewability/verification; not for a single walled-garden platform, and not for the underlying creative or audience-strategy decision.
---

# Programmatic

Classify each buying method, verification approach, or economics claim with [`KNOWLEDGE-TAXONOMY.md`](../../library/contracts/KNOWLEDGE-TAXONOMY.md). Programmatic buys inventory aggregated across many sites and apps the buyer has not individually vetted, through a multi-party supply chain — a different risk profile than buying from a single platform that runs its own auction and reports on the inventory it sells (`$meta-ads`, `$tiktok-ads`, `$linkedin-ads`, `$youtube-ads`). That distinction is about who operates and reports on the buy, not a guarantee of quality: a single platform's buy can also extend to third-party sites and apps — for example, YouTube video ads can appear across websites and apps running on Google video partners (first-party: https://support.google.com/google-ads/answer/2375464, checked 2026-09-26). Inventory quality, supply-chain cost, and fraud are the defining concerns here, not creative or targeting alone.

DSP features, identifier availability, verification-vendor methodology and accreditation, and industry-standard definitions change. Apply [`PLATFORM-CURRENCY.md`](../../library/contracts/PLATFORM-CURRENCY.md): cite the DSP's, vendor's, or standards body's own documentation with its check date, or label the claim unverified. There is deliberately no programmatic registry.

## Required inputs

Primary business outcome and funnel objective; demand-side platform in use and its available inventory sources (open exchange, private marketplace, programmatic guaranteed); available first-party or contextual targeting signal, and the current availability of third-party cookies and other cross-site identifiers in the browsers, apps, and DSP in scope — which changes with browser, operating-system, and platform policy, so confirm it from those owners' own documentation and account-visible reach per `library/contracts/PLATFORM-CURRENCY.md` rather than assuming either availability or deprecation; brand-safety and content-adjacency requirements; and whether independent verification (viewability, invalid-traffic, brand-safety measurement) is in place.

## Method

1. Assess the buying method against the objective: open exchange (broadest reach, least curated access route; fraud and quality risk to be measured with independent verification, not assumed), private marketplace (negotiated access to specific publishers, more buyer control over which publishers are bought), and programmatic guaranteed (reserved inventory at a fixed price, most predictable but least flexible) each trade reach against quality and cost predictability differently — state which is used and why.
2. Screen inventory quality and supply-chain cost before scaling spend. See [Supply-path optimization](references/supply-path-optimization.md).
3. Require independent, third-party verification for viewability, invalid traffic, and brand safety rather than accepting the DSP's or a single seller's self-reported figures alone. See [Verification and fraud screening](references/verification-and-fraud-screening.md).
4. Set targeting from available first-party or contextual signal, and state explicitly where third-party-cookie-dependent targeting is degraded or unavailable rather than assuming a targeting configuration still functions as it did in a prior period.
5. Define the measurement plan against the funnel objective, applying the same view-through discipline `$youtube-ads` applies: a served impression is not a caused outcome, and any causal claim should be graded on `$tracking-measurement`'s evidence ladder.
6. Rank actions by expected business impact, confidence, reversibility, and the account's actual capacity to monitor a fragmented, multi-party supply chain on an ongoing basis.

## Rules

- Do not accept a DSP's or single supply-side platform's self-reported viewability, brand-safety, or invalid-traffic figures as sufficient; require independent third-party verification, since the reporting party frequently has a financial interest in favorable numbers.
- Do not treat open-exchange inventory as equivalent in quality to a private marketplace or programmatic-guaranteed deal without evidence; the open exchange is the least curated access route by construction, so measure its fraud and quality risk with independent verification rather than assuming it is equal.
- Do not scale spend into inventory whose supply path has not been screened; an unscreened path can route through multiple resellers each taking a fee, and can include made-for-advertising sites optimized to generate ad calls rather than genuine audience engagement.
- Do not present a served or viewable impression as a caused business outcome; grade any resulting claim on the causal evidence ladder in `$tracking-measurement`, the same discipline `$youtube-ads` applies to view-through.
- Do not assume a targeting configuration that relied on third-party cookies still functions as in a prior period without confirming current signal availability; state degraded or unavailable targeting explicitly rather than reporting reach as if unaffected.
- Do not state a DSP capability, identifier-availability status, verification vendor's methodology or accreditation, or a standard's current definition from memory or from a seller's summary; cite the owner's first-party documentation with its check date or label it unverified per `library/contracts/PLATFORM-CURRENCY.md`.
- Do not conflate cost per impression across supply paths with different fee structures; a lower headline cost per impression through a longer, fee-stacked resale path can be more expensive in total than a shorter, direct path with a higher headline rate.

## Output

Plan: buying method and rationale; supply-path screening approach; verification vendor and metrics in place; targeting signal available and any degradation disclosed; measurement plan with evidence-level expectation; capacity to monitor ongoing supply quality; exact status.

Diagnosis: observed change (cost, viewability, invalid-traffic rate, or outcome); competing explanations (supply-path shift, verification-vendor methodology change, seasonality, targeting-signal degradation) considered before attributing a cause; evidence level; recommended action.

## QA

Confirm the buying method is stated with rationale rather than defaulted; supply-path screening happened before scaling spend; verification relies on an independent third party rather than the seller's self-report; targeting-signal degradation or availability is confirmed from current first-party sources and disclosed rather than assumed either way; no served impression is presented as a caused outcome without evidence-level grading; and total supply-chain cost, not headline cost per impression alone, informs any efficiency conclusion.
