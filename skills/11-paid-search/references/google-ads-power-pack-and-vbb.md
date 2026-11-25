# Google Ads AI Power Pack, Value-Based Bidding & Experiments Playbook

Distilled from official `@GoogleAds` playbooks (Google Marketing Live 2025/2026, *Ads Decoded*, *Value-based bidding for lead gen*, and *Budget & Bidding Controls*). Platform mechanics, eligibility thresholds and UI names evolve — verify current Google Ads Help documentation (cite URL and access date) or mark *to confirm* before treating any capability as live in an account.

## 1. The AI Power Pack: How Google's 3 AI Campaign Types Work Together

Rather than forcing one campaign type to do every job, separate campaign roles cleanly by buyer intent and funnel stage:

| Campaign type | Primary job | Key guardrails & controls |
| --- | --- | --- |
| **Demand Gen** | Create visual demand at top/mid funnel (YouTube In-Stream, Shorts, Discover, Gmail) | Configure **Ad-Group Channel Controls** (All Google vs. Owned & Operated only to omit third-party Display vs. granular isolation such as YouTube Shorts-only for 9:16 vertical creative). Require creative variety (`09-ad-creative`). |
| **AI Max for Search** | Expand Search intent capture into complex, multi-word and conversational queries (successor to legacy DSA) | Enable only on Search campaigns backed by clean conversion signals (never low-quality click/form-fill spam). Retain Search guardrails: negative keywords, brand exclusions/inclusions, URL exclusions and search-term intent review. |
| **Performance Max (PMax)** | Capture cross-channel conversions across Search, Shopping, YouTube, Discover, Gmail and Maps | Audit spend and conversion splits via **Channel Performance Reporting** (verify availability in the account), apply brand exclusions and campaign-level negatives, and pair with clean feeds (`11-shopping-feeds`) for e-commerce. |

## 2. Value-Based Bidding (VBB) for Lead Gen & AI-Qualified Calls

Bidding on raw form fills or raw phone clicks teaches Smart Bidding to buy the cheapest people who submit forms — often spam, students or unqualified buyers.

- **Map the real lead-to-revenue funnel:** Identify every stage in the CRM (e.g., Raw Lead → Marketing Qualified → Sales Qualified / Booked Call → Closed Won) with observed stage-to-close conversion rates and average deal value from the business's own CRM (never invented industry averages).
- **Assign proxy stage values cleanly:**
  - `Stage Value = Observed Close Rate from that Stage × Average Customer Value (or Contribution Margin)`.
  - If CRM volume for Closed Won is too sparse for weekly bidding feedback, optimize on the **closest reliable qualified stage** (e.g., SQL / Qualified Call) while still importing Closed Won for reconciliation.
- **Feedback speed matters:** Import offline conversions on a consistent, frequent cadence via **Google Ads Data Manager** or Enhanced Conversions for Leads (`17-tracking-plan`) so Smart Bidding sees qualified outcomes within the conversion window.
- **AI-Qualified Call Leads:** When phone calls are a primary conversion path, separate raw call clicks from genuinely qualified calls (duration thresholds or Google Ads AI-qualified call conversion tracking — verify current eligibility/region support in official docs) before bidding on calls.

## 3. Budget Pacing, Spending Limits & Learning Hygiene

- **Daily vs. monthly spending limits:** Under Google Ads standard daily budget pacing, a campaign may spend up to 2× its average daily budget on high-demand days while staying capped at `average daily budget × 30.4` over a billing month (verify current Google Ads Help billing-limit documentation).
- **Avoid starving Smart Bidding:** Setting a daily budget far below the realistic cost per business outcome prevents algorithms from collecting enough conversion signal to exit learning. Check budget sufficiency against actual allowable CPA/target ROAS before blaming creative or keywords; hand scale-up decisions to `19-scale-paid`.
- **Destination hygiene:** Before increasing spend or debugging sudden drops, check for *"Destination not working"* or policy/serving disapprovals across landing pages (HTTP errors, geo-blocks, slow mobile timeouts).

## 4. Proving Changes with Google Ads Experiments (A/B Testing)

Never judge a major bidding, match-type, AI Max or landing-page change from simple before-vs-after date comparisons (seasonality, competition and demand shift week to week).
- Use native **Google Ads Experiments** (cookie-based or search-based 50/50 clean split) to test **one variable at a time** (e.g., Broad Match + Smart Bidding vs. existing match types, AI Max on vs. off, tCPA vs. VBB/tROAS).
- Define the business outcome, minimum duration/sample (accounting for conversion lag) and decision rule up front (`18-ab-testing`), and require owner approval before applying any winning experiment arm.
