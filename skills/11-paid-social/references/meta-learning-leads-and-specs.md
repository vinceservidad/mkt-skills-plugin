# Meta Learning, Lead Quality, Budgeting, Policies and Specs

Use when planning budgets/bidding, diagnosing learning-limited or underdelivery states, improving Instant/website lead quality, auditing Ads Manager exports, or checking Specs / Regulated categories (*to confirm* against current Meta docs and the account). Not legal advice.

## 1. Learning phase and significant edits (*to confirm* in Meta Help / account)

- **Learning heuristic:** Meta documentation cites roughly ~50 optimization events per week as a typical learning-exit guideline (not an account guarantee; Shops ads have separate documented rules *to confirm*).
- **Significant edits that can restart learning:** changing targeting, creative, optimization event, bid strategy, adding new ads, pausing `>= 7` days, or making large budget/bid-goal jumps.
- **Campaign budget advantage:** under CBO, budget shifts across ad sets, single ad-set edits, or adding an ad set typically leave sibling ad sets unaffected, whereas campaign-level bid or large budget shifts can reset multiple sets (*to confirm*).
- **Learning-limited order of options:** never jump straight to higher spend. Inspect consolidation of redundant ad sets, broader audience constraints, bid/cost-cap constraints, or an upstream higher-frequency validated event; hand any budget increase on an existing system to `19-scale-paid`.

## 2. Lead quality & Conversion Leads workflow

- When lead volume looks cheap in Ads Manager while sales close rates collapse:
  1. Connect CRM stages back via **Conversions API** preserving Meta's 15–17 digit Lead ID (*Conversion Leads* integration; *to confirm* setup availability).
  2. Optimize toward the **Conversion leads** performance goal or CRM-qualified website lead event rather than unvetted lead submits (`17-tracking-plan` owns wiring).
  3. Add qualifying multiple-choice or work-email/budget questions on Instant forms (or pre-qualifying page copy) to filter mismatched inquiries cleanly without making unverified lift predictions.

## 3. Budget, bid strategy and underdelivery planning

| Choice | When appropriate | Critical caveat |
| --- | --- | --- |
| CBO vs ABO | CBO when ad sets share equivalent outcome/margin targets; ABO when testing disparate audiences/geos requiring protected spend | Do not merge different margins/markets just to hit a volume label |
| Daily vs Lifetime | Daily for steady pacing and open-ended learning; Lifetime for strict fixed end-date schedules | Daily budget paces weekly and can fluctuate day to day (*to confirm*) |
| Spend-based (`Highest volume/value`) | Priority is spending authorized budget efficiently within broad pool | More spend is not proof of profit; verify marginal CPA/ROAS |
| Goal-based (`Cost per result` / `ROAS goal`) | Strict allowable cost per outcome from unit economics must hold | Tight goals restrict delivery rather than guaranteeing every conversion hits target |
| Bid cap | Account holds proven auction bid model | Auction bid cap is not a cap on reported CPA |

- **Underdelivery triage order:** check account/payment/billing limits -> active policy rejections -> schedule/audience/placement restrictions -> conversion event rarity -> overly tight bid/cost caps -> creative limited/fatigued flags. Propose the smallest reversible fix with a review window.

## 4. Policies, consent, regulated categories and data pulls (*to confirm*)

- **Special Ad Categories:** Financial products/services (US replacement for Credit), Employment, Housing require category declaration and restrict age, gender, ZIP/postal targeting, lookalikes, and some exclusions; social/election ads require authorization and *Paid for by* disclosures (restricted in the EU).
- **Health, datasets & privacy:** Meta dataset categorization (e.g., Health & Wellness) restricts custom parameters and standard optimization events until configured; apply GDPR consent signals (`fbq('consent', 'revoke')` before init until grant) and US state Limited Data Use (LDU) flags with legal/privacy review (`20-compliance`). Reject any cures/unrealistic timed outcome claims or negative personal-attribute callouts.
- **Specs & 9:16 safe zones (Meta Ads Guide reference — *to confirm* before final export):** verify latest Feed (`4:5`), Stories/Reels (`9:16` leaving ~`14%` top, ~`35%` bottom, `6%` side UI clearance), Square (`1:1`), Carousel, and Right Column limits in Ads Manager before creative delivery (`09-ad-creative`, `09-image-video`).
- **Required Ads Manager / Events Manager pull fields:** compare equal date windows (`30d` vs prior `30d`), state attribution window once, capture Campaign/Ad set (`Delivery`, `Objective`, `Performance goal`, `Bid strategy`, `Budget`, `Spend`, `Results`, `CPR`, `ROAS`, `Frequency`, `Reach`, `Last significant edit`), Creative (`Format`, `Spend`, `Results`, `CPR`, `Link CTR`, `3s plays / Impressions`, `ThruPlays`, `Diversity/Fatigue status`), Events Manager (`browser vs server`, `dedup`, `EMQ`), and 14-day Activity history. Name missing columns explicitly; never invent them.
