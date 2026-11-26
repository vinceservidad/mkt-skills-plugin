# Paid social: decision rules

## The outcome chain

Every paid social plan names four things, in this order:

1. **Primary business outcome**: what the business is paid for or what reliably leads to it (a qualified discovery call, a paying subscriber who stays past the second delivery, a first order with margin).
2. **Optimisation event**: what the platform's delivery system is told to find. It must be tracked reliably and happen often enough for the platform to learn; how often is a platform rule to verify, not a number to state from memory. When the outcome is too rare, step one stage up the funnel (a sample-report request rather than a closed deal), and say what that proxy can get wrong (it can fill up with unqualified people).
3. **Delivery signals**: impressions, frequency, CTR, CPC, engagement, platform leads. Useful for diagnosis (is the ad being seen, is it fatiguing), never for the keep or stop decision on their own.
4. **Economics**: the allowable cost per outcome, from price, margin and retention in `offer.md` or `inputs/`. If margin or retention is unknown, the allowable cost is unknown: write the formula and ask the owner, do not pick a number.

## Reading results that already ran

- Total by concept with `scripts/sum_by.py`. Report spend, platform-reported results and business outcomes side by side, and the cost per business outcome with its count (n).
- Small counts decide nothing on their own. With one or two outcomes per concept, say the read is directional (heuristic) and name the spend or count that would make it decidable.
- Platform-reported leads and CRM outcomes disagree routinely. Keep them in separate columns; never substitute one for the other.
- When a cheap-click concept brings the wrong buyers (the wrong company size, freelancers instead of owners), that is a qualification failure in the creative or the audience, not a winner to scale.
- Frequency rising while CTR falls is a pattern consistent with fatigue. It is not proof; a fresh version of the same concept is the test.
- Never reward the concept with the most likes, comments or clicks with more budget; route any budget increase to `19-scale-paid`.

## Platform choice

- Start from where the evidence puts the buyer: lead sources, journey touchpoints, channel-selection output. A platform the business has never tested is a hypothesis.
- B2B buyers defined by company size and role need a platform that can reach that role at that size, and the gap between the platform's company-size bands and the ICP is a known source of waste to name.
- Consumer products with visual demonstration or a daily ritual usually suit short video and image feeds (heuristic; verify formats and placements).
- One or two platforms done well beat five done badly (Weinberg & Mares). Add a platform only after the first has a readable result.

## Structure

- **Cold:** one awareness level per campaign, the awareness map's entry message, an offer that fits that level (free education for unaware and problem-aware, proof and a low-risk next step for solution-aware). Name the audience approach as a hypothesis: broad with creative doing the qualification, or defined filters where the buyer must be a specific role or company size.
- **Warm:** visitors, engagers, leads and abandoners belong to the retargeting ladder (`12-retargeting`). The paid-social plan names the hand-off and the exclusions, not the rungs.
- **Exclusions:** existing customers out of acquisition; disqualified segments (for example studios under 8 staff) out wherever the platform allows it.

## Creative concepts

- A concept is an angle plus a format, not a colour change. Each tests one thing: the angle, the hook, the format or the offer.
- Source each angle from the awareness map, a pain, belief or objection with its evidence ID, or proof that exists with permission.
- Production belongs to `09-creative-strategy` (`ad-creative`, `ugc-brief`, `image-video`). Copy belongs to `10-ad-copy`.
- A concept that ran unchanged for weeks has not been tested against a fresh version of itself; say so before calling it dead.

## Pre-launch build order (before spending $1)

1. **Gate 1 (Strategy and economics):** Lock the core offer (`07-offer-design`), target segment and exclusions (`02-segmentation`), promise and proof (`08-message-doc`), and allowable cost per business outcome (`17-unit-economics`, or owner-set tolerance).
2. **Gate 2 (Destination QA):** Publish and test the landing page on mobile and desktop so the page load, headline, offer, and CTA match the campaign's awareness level (`12-landing-page`).
3. **Gate 3 (Tracking and CAPI verification):** Configure browser Pixel plus Conversions API deduplication, verify domain and dataset permissions, connect CRM offline events or Conversion Leads if lead-gen, and lock UTMs (`17-tracking-plan`).
4. **Gate 4 (Compliance and billing):** Confirm billing, Special Ad Category declarations, consent flags, and policy rules (`20-compliance`).

Build inside Ads Manager in this order (every object stays paused or in draft until owner approval):

1. Account, billing, consent, and Special Ad Category check.
2. Published destination URL verified live.
3. Tracking events, CAPI deduplication, and UTMs tested.
4. Creative concepts and copy checked against placement safe zones (`09-ad-creative`, `09-image-video`, `10-ad-copy`).
5. Draft Campaign (objective, CBO/ABO) -> Ad Set (optimization event, audience and exclusions, placements, schedule, budget) -> Ads (concepts, copy, UTMs, final URL).
6. Pre-publish QA and explicit owner approval.
7. Publish, confirm active delivery, and verify live event firing in Events Manager.

## Budget, learning and stop rules

- The owner sets the budget. The plan proposes how to split a test budget across concepts and the minimum spend or outcome count before a call; label any such threshold a heuristic.
- Keep rule and stop rule are both written in cost per business outcome against the allowable cost (or the owner's tolerance where economics are unknown).
- Scaling: no universal rule (no "raise 20% every three days"). Hand it to `19-scale-paid`, which checks readiness, economics, constraints, marginal evidence, capacity, guardrails and authorisation. Capacity in `offer.md` (onboarding slots, roasting capacity) caps scale whatever the ads do.

## Platform claims

Platform formats, specifications, audience options and minimum sizes, optimisation events and their volume needs, learning-phase behaviour, special ad categories, consent requirements and ad policies change often. For each one the plan relies on:

- **Documented:** checked in the platform's own current help or developer documentation during this run, cited as `(first-party: <URL>, checked YYYY-MM-DD)` next to the claim, with its scope.
- **Account-visible:** seen in this business's ad account, with the date.
- **To confirm:** everything else, written as a check to perform, not as a fact.

Do not use third-party benchmarks or another platform's documentation as evidence about this account.

## Authorisation

The plan is advice and a draft. Creating campaigns, changing budgets, bids, audiences or conversion events, pausing ads or launching new ones needs the owner's explicit approval. After any approved change, verify it in the account and record the state (draft, saved, published, live, verified).
