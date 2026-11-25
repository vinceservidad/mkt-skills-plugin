# Meta Performance 5, Delivery Alignment and Results Validation

Use when planning, reviewing, or restructuring Meta Ads campaigns. Platform labels, controls, and eligibility change frequently: cite official Meta docs with URL and date checked, confirm in the live account, or mark *to confirm*.

## 1. End-to-end creative delivery alignment row

Construct one alignment row before debating creative or bidding tweaks; leave unconfirmed settings blank under Open questions:

`business outcome | customer action | campaign objective | conversion location | performance goal | event/dataset | value/counting basis | audience controls | creative promise | destination | measurement window`

Never relabel a Traffic click, video view, or Engagement reaction as a purchase or qualified lead.

## 2. Meta Performance 5 five-row review (operational framing)

Score observed evidence across Meta's five pillars without recommending universal rules or blanket automation:

| Pillar | What to inspect | Decision guardrail |
| --- | --- | --- |
| Account simplification | Redundant ad-set splits dividing conversion volume | Consolidate only demonstrated overlap; preserve needed splits (country, language, distinct margins, offer, or compliance) |
| Automation | Advantage+ audience/placements/campaign settings | Verify hard constraints (location, age, language, Custom Audience exclusions) vs soft suggestions |
| Creative diversification | Distinct concepts, angles, formats, and buyers | Resizing, background color swaps, or headline synonyms are adaptations, not strategic diversity (hand concept design to `09-ad-creative`) |
| Data quality | Pixel/dataset match rate, CAPI deduplication, attribution window | Route pixel/server tracking gaps to `17-tracking-plan` before trusting automated bidding |
| Results validation | Platform-attributed conversions vs CRM/order outcomes | Separate Meta credit from store/CRM business truth; route causal tests to `17-incrementality` |

## 3. Compatible results arithmetic contract

- Keep Meta attribution settings identical across any comparison window (e.g., 7-day click / 1-day view); flag window changes explicitly.
- **Never pool incompatible outcomes:** never merge raw leads + qualified SQLs + purchases into one blended cost per result (`use sum_by.py` by campaign/ad/outcome type separately).
- High CTR, thumb-stop rate, or Opportunity Score never justifies scaling spend on a poor business-outcome ad, nor pausing a profitable high-CPA prospect campaign prematurely without CRM margin proof.

## 4. Current Meta product naming (*to confirm* against Docs / account)

- **Advantage+ Sales:** current name replacing legacy Advantage+ Shopping Campaigns (ASC).
- **Advantage+ Leads / App:** Advantage+ setup defaults when campaign budget, Advantage+ audience, and Advantage+ placements remain active.
- **Advantage+ audience:** treats targeting preferences as suggestions except hard exclusions (location, minimum age, language, Custom Audience exclusions — *to confirm* in current ad set controls).
- Never explain delivery volatility as an unverified algorithm change; decompose auction/CPM, creative fatigue, audience saturation, tracking loss, offer, and seasonality separately.
