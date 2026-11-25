# Diagnosis

Results fail at one of the eight questions. Start at the symptom, inspect the "check first" sections, and only then the "then" sections. Fix the first section that is empty, weak or contradicted by the numbers; downstream fixes on top of an upstream gap waste money.

| Symptom | Check first | Then |
| --- | --- | --- |
| Ads run, nobody clicks | Creative Strategy (hook, angle) | Customer (wrong audience), Distribution (wrong channel) |
| Clicks, no leads | Awareness (message too advanced), Funnel (landing page) | Conversion (friction, trust) |
| Leads, no sales | Offer (value, risk reversal) | Sales, Conversion, Message (reason to believe) |
| Sales, no profit | Measurement (CAC, LTV, margin) | Offer (price), Distribution (channel cost) |
| Sales, no repeat | Product (does it deliver?) | Retention (onboarding, activation) |
| Works, but cannot grow | Growth (vertical vs horizontal) | Distribution (new channels), Operations (team, budget) |
| Growth stalls after scaling | Market (saturation, sophistication) | Brand (no memory, price pressure) |

## How users describe each row

| Row | Phrases that mean it |
| --- | --- |
| Ads run, nobody clicks | low CTR, ads get impressions but no clicks, thumb-stop rate is bad, creative is fatiguing, CPMs fine but CPC terrible |
| Clicks, no leads | landing page doesn't convert, high bounce, people visit but don't sign up, cost per lead too high with normal CPC |
| Leads, no sales | leads don't buy, calls don't close, trials don't convert, lots of inquiries but no purchases, people say it's too expensive |
| Sales, no profit | ROAS looks fine but we lose money, CAC too high, margins disappear after ads, unit economics don't work |
| Sales, no repeat | customers don't come back, high churn, refunds, no second purchase, cancellations after month one |
| Works, but cannot grow | spend more and CPA explodes, maxed out the channel, plateaued, can't hire fast enough |
| Growth stalls after scaling | it worked then stopped, everyone copies us, prices under pressure, claims no longer land |

## What "weak" means in each check-first section

Use the context file first; use the user's numbers to confirm.

- **Creative Strategy:** no angle matrix or brief behind the ads; one angle tested; hooks not matched to the audience's awareness level.
- **Awareness:** `awareness.md` → Awareness map empty, or the ad or page speaks to a more advanced level than the traffic (a product pitch to problem-aware strangers).
- **Funnel:** no defined path for this traffic temperature; the landing page serves several jobs or several offers.
- **Offer:** `offer.md` → Core offer, Value equation or Guarantee empty; price set without evidence; deliverables listed instead of an outcome; no reason to buy now.
- **Measurement:** no CAC, LTV, payback or contribution margin on record; decisions made on platform ROAS alone.
- **Product:** no PMF signal (Sean Ellis survey, retention curve, word of mouth); refunds or churn concentrated in the first weeks.
- **Growth:** scaling before the system is stable, or adding channels before the first channel is saturated.
- **Market:** `market.md` → Market sophistication or Competitors empty; claims that worked are now made by everyone.

## Order of fixes

Upstream before downstream: Customer → Awareness → Offer → Message → Copywriting → Funnel → Distribution → Conversion → Sales → Retention → Measurement. When two sections are both weak, fix the earlier one first unless the user's numbers isolate the later one (for example, a strong offer with a 0.2% landing-page conversion rate on warm traffic points at the page).

## Where do I start

No symptom and no existing context: start with `02-customer-research`, then follow the order of fixes above. Market work (`01-market-assessment`) comes after customer research, not first. If `02-customer-research` is not loaded, say enable mkt-q1-audience.
