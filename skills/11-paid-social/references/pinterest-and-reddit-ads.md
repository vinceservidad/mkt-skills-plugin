# Pinterest Ads and Reddit Ads guide

Paid social is not uniform across platforms. Meta and TikTok are pure interruption feeds; **Pinterest** behaves like a visual search and planning engine; **Reddit** behaves like skeptical, topic-organized communities. Respect each platform's native intent, creative format and attribution horizon.

## 1. Pinterest Ads (Visual Search & Planning)

### How buyers behave on Pinterest
- **High planning intent, longer conversion lag:** Pinners search and save ideas weeks before buying (home, apparel, gifts, beauty, food, weddings, DIY, lifestyle). Judging a Pinterest cold campaign on 1-day click ROAS kills winners early; pair 7-day / 30-day click and view/save signals (verify current Pinterest attribution window options in official docs) with CRM / GA4 cohort checks (`17-attribution`).
- **Hybrid targeting (Search + Browse + Catalog):**
  - **Keyword + Interest campaigns:** Separate **Search-only** placements (capturing active visual search intent, with negative keywords) from **Browse/Home feed** placements (algorithmic discovery) when volume allows, or review placement breakdowns explicitly before scaling.
  - **Catalog / Shopping Pins:** Connect a clean regional product feed (`11-shopping-feeds`) with accurate price, stock and vertical product imagery for Shopping and Dynamic Retargeting (`12-retargeting`).
- **Creative rules (native vertical pins):**
  - Vertical aspect ratio (2:3 standard — verify current Pinterest Ads specs in official docs), crisp product-in-context photography or quick demo video, minimal clean text overlay naming the outcome/use case, clear brand cue without loud "SALE NOW" clutter.
  - Match the landing page visually and contextually to the exact pin (product page for Shopping/product-aware pins; guide/collection page for planning/problem-aware pins).
- **Tracking & audit prerequisites:**
  - Verify **Pinterest Tag + Conversions API (CAPI)** deduplication (`event_id`), Enhanced Match, and checkout value/currency accuracy (`17-tracking-plan`) before trusting platform ROAS.
  - Check **Outbound Clicks** (clicks to your site) vs. **Pin Clicks** (zooming in on the pin inside Pinterest) — never confuse Pin Clicks with website traffic.
  - Audit checklist when reviewing an existing Pinterest ad account: (1) Tag/CAPI event health & deduplication, (2) Catalog feed errors / out-of-stock pins, (3) Pin Clicks vs. Outbound Clicks & landing-page view drop-off, (4) Search vs. Browse placement split and wasted search terms, (5) creative fatigue & vertical format compliance, (6) attribution window alignment with actual store conversion lag.

## 2. Reddit Ads (High-Skepticism Communities)

### How buyers behave on Reddit
- **Extreme ad skepticism & high research intent:** Redditors actively read subreddits to compare tools, diagnose problems and spot fake hype. Glossy corporate ad copy gets ignored or roasted; transparent, plain-English, proof-backed posts written like a real practitioner outperform traditional ads.
- **Targeting architecture:**
  - **Subreddit targeting:** Group closely related subreddits into focused ad groups so the copy speaks the exact vocabulary of that community (never lump 40 unrelated subreddits under generic copy).
  - **Keyword & Interest targeting:** Capture active comparison threads (especially strong for B2B SaaS, developer tools, finance, health/fitness, niche hobbies and high-consideration consumer gear).
  - **Placements:** Separate Feed placements vs. Conversation placements (ads inside active comment threads, where buyer intent is highest) when reviewing efficiency.
- **Creative & comments rules:**
  - Write like a helpful founder or operator: concrete problem, real mechanism, honest trade-offs, plain language, zero buzzwords.
  - **Comments policy (decide deliberately):** Leave comments **open** ONLY if a knowledgeable human will monitor and reply transparently within hours (great replies often double trust); turn comments **off** if nobody can staff real replies. Never delete legitimate critical questions or use fake shill accounts.
  - Link directly to an honest, fast-loading landing page or comparison/demo page that answers technical questions immediately (no bloated hype funnels).
- **Tracking & audit prerequisites:**
  - Verify **Reddit Pixel + Conversions API (CAPI)** with deduplication and clean UTMs (`17-tracking-plan`).
  - Watch **click-to-landing-page-view drop-off** (mobile app accidental taps can inflate raw CTR); judge strictly on qualified business outcomes (qualified calls, sign-ups, purchases) in CRM/analytics, never raw clicks or upvotes.

## 3. Platform facts rule

Pinterest Ads attribution windows, placement controls, catalog requirements, pin aspect specs, and Reddit Ads CAPI parameters, conversation placement specs and subreddit targeting minimums change. Always verify against current official Pinterest Business Help and Reddit Ads Help documentation (cite URL + date) or mark *to confirm*.
