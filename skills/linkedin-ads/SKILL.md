---
name: linkedin-ads
description: Plan, audit, or diagnose LinkedIn B2B advertising — account-based and firmographic targeting, format selection, Lead Gen Forms, and cost-structure economics; not for consumer/demographic-targeted channels, and not for the underlying sales-cycle or CRM ownership.
---

# LinkedIn Ads

Classify each model, targeting decision, or economics claim with [`KNOWLEDGE-TAXONOMY.md`](../../library/contracts/KNOWLEDGE-TAXONOMY.md). LinkedIn's targeting unit is frequently the buying account or the buying committee, not the individual consumer — a fundamentally different targeting logic than Meta, TikTok, or YouTube, and one that should be built from `$icp-jtbd` evidence about buying situations and buyer roles, not demographic proxies.

Ad formats, targeting attributes, buying options, and regional availability are platform facts that change. Apply [`PLATFORM-CURRENCY.md`](../../library/contracts/PLATFORM-CURRENCY.md): cite LinkedIn's own documentation with its check date, or state the claim as a check to perform, and confirm availability in the account before an account-specific plan. There is deliberately no LinkedIn registry. This skill carries no cost benchmark: no platform's typical cost per click or cost per lead is evidence about this account.

## Required inputs

Primary business outcome and lead-stage definitions per `$marketing-intake`, since a cost conclusion is meaningless without the qualified-lead, opportunity, or pipeline economics behind it; target account list or firmographic criteria if account-based marketing is in use; buyer roles and buying-committee structure per `$icp-jtbd`; available formats and creative fit for each — LinkedIn lists Sponsored Content, Sponsored Messaging (message ads and conversation ads), Text ads, and Dynamic ads (first-party: https://www.linkedin.com/help/lms/answer/a421454, checked 2026-09-26), and Lead Gen Forms that work with Sponsored Content and messaging ad sets (first-party: https://www.linkedin.com/help/lms/answer/a423447, checked 2026-09-26); confirm current format availability for the objective and account per `library/contracts/PLATFORM-CURRENCY.md`; and sales-cycle length, since a lead generated today frequently will not show revenue for months.

## Method

1. Establish whether targeting is account-based (a defined target account list, matched via account targeting) or attribute-based (job title, seniority, function, industry, company size) — state which and why; see [Account and firmographic targeting](references/account-and-firmographic-targeting.md).
2. Select ad format to fit the funnel stage and buying-committee role being reached; a Sponsored Messaging ad to a senior decision-maker and a Lead Gen Form to a research-stage individual contributor are different mechanisms for different roles, not interchangeable defaults. Check reach constraints before planning Sponsored Messaging: LinkedIn states that in the European Economic Area and Switzerland only members who agreed to see Sponsored Messaging ads in their inbox receive them (first-party: https://www.linkedin.com/help/lms/answer/a421454, checked 2026-09-26).
3. Assess Lead Gen Forms (native, pre-filled, lower-friction) against an off-platform landing page (higher friction, potentially higher intent signal) for the specific offer; the friction/quality tradeoff is a real decision, not a default.
4. Set cost expectations from the account's own cost per qualified outcome — qualified lead, opportunity, pipeline, or revenue, per `$marketing-intake` definitions — against its economics, not from another platform's figures or an unsourced LinkedIn benchmark. For Lead Gen Form ads, cost per lead is a calculation (spend divided by leads), not a billed unit: LinkedIn states that ads with Lead Gen Forms are bought on a cost-per-click or cost-per-impression basis and that cost-per-lead buying is not available (first-party: https://www.linkedin.com/help/lms/answer/a421181, checked 2026-09-26).
5. Define the measurement plan against the actual sales cycle: lead volume and immediate cost-per-lead are early, weak signals; route to `$retention-economics`'s lead-to-revenue cohort method for a maturity-honest read, and do not treat an early cohort's incomplete pipeline as a final quality verdict. See [Lead quality and sales cycle](references/lead-quality-and-sales-cycle.md) for format- and role-segmented quality discipline.
6. Rank actions by expected pipeline impact, confidence, reversibility, and the account's actual budget tolerance for this channel's cost structure.

## Rules

- Do not evaluate LinkedIn cost-per-click or cost-per-lead against another platform's benchmark, and do not state that LinkedIn costs are higher or lower than another platform's as a fact; the platforms serve different audiences and buying contexts, no benchmark in this system supports such a claim, and the account's own cost per qualified outcome against its economics is the decision-relevant figure.
- Do not treat lead volume as the business outcome; for a long sales cycle, immediate lead metrics are a weak, early signal and a business-outcome conclusion requires the lead-to-revenue cohort maturity check `$retention-economics` provides.
- Do not build attribute-based targeting from an assumed persona when `$icp-jtbd` has actual buying-committee and buyer-role evidence available; use the evidence.
- Do not treat every buyer role identically; a campaign reaching only one role in a multi-stakeholder buying committee is reaching part of the decision, and the plan should state which role or roles it targets and which it does not.
- Do not claim account-based targeting reached a target account without confirming the platform's actual match rate for that account list; a low match rate means the campaign is reaching a different, broader audience than the plan states.
- Do not conflate Lead Gen Form volume with off-platform landing-page volume when comparing cost per lead; the two carry different friction and can carry different downstream qualification rates, so measure each path's qualification from this account's CRM rather than assuming the direction.
- Do not state a current ad format, targeting attribute, buying option, or regional restriction from memory; cite LinkedIn's first-party documentation with its check date or label it unverified per `library/contracts/PLATFORM-CURRENCY.md`.

## Output

Plan: targeting approach (account-based or attribute-based) with rationale; format selection matched to buying-committee role and funnel stage; Lead Gen Form versus landing-page decision; cost expectations against this account's own economics; measurement plan matched to sales-cycle length; capacity required; exact status.

Diagnosis: observed change; competing explanations (targeting-match-rate shift, format change, seasonality tied to B2B budget cycles, sales-cycle-stage immaturity misread as a decline) considered before attributing a cause; evidence level; recommended action.

## QA

Confirm targeting approach and its rationale are stated; format matches the buying-committee role and funnel stage rather than defaulting to one format; cost conclusions are checked against this account's own cost per qualified outcome and economics, with no cross-platform or unsourced cost benchmark asserted; format and targeting claims are cited from LinkedIn's first-party documentation with a check date or labeled unverified; lead-quality claims route through `$retention-economics`'s maturity-honest cohort method rather than asserting a final read on an immature cohort; and account-based match rate is confirmed rather than assumed.
