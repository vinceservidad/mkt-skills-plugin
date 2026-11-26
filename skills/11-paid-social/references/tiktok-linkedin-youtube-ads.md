# TikTok Ads, LinkedIn Ads and YouTube Ads Buying Playbook

Use alongside [paid-social-guide.md](paid-social-guide.md) when planning or auditing non-Meta paid social and video channels. Platform UI labels, minimum audience thresholds, format limits, and automated campaign names change frequently; verify in official platform help docs (cite URL and date) or mark *to confirm*.

## 1. TikTok Ads (native fit, Spark Ads and fatigue triage)

- **Creative and native fit hypothesis:** Test full-screen vertical (`9:16`) assets built in the visual language of the feed (native captions, natural pacing, 1-to-2-second pattern-interrupt or spoken hook, trending or creator voice audio) against polished brand cuts as an empirical hypothesis (`09-ad-creative`, `09-hooks`), rather than assuming cropped horizontal spots perform identically.
- **Spark Ads vs. standard In-Feed ads:** Spark Ads boost an authorized organic TikTok post using the creator's or brand's handle, preserving organic social engagement while carrying paid tracking. Verify handle authorization codes, paid-usage duration, and disclosure rules via `11-influencer` before launch. Inspect Smart+ automation vs. manual ad-group structure and Search Ads Toggle against current TikTok Ads Manager controls (*to confirm*).
- **Creative-level fatigue cadence:** Track frequency, CTR, and cost per business outcome **at the individual video ID level** (campaign averages hide dying winners propped up by newer ads). Set refresh triggers from the account's own observed decay curve rather than importing fixed Meta schedules; when replacing a fatigued video, change the concept, angle, or opening hook (`18-creative-testing`) rather than only re-uploading the same edit.

## 2. LinkedIn Ads (ABM, firmographic targeting and lead maturity)

- **Account-based targeting and match rates:** When targeting a defined ABM account list (`02-icp-persona`), confirm the uploaded company/contact match rate (LinkedIn Help documents 7-day matched-audience refresh windows and member privacy controls; verify current specs) before projecting reach or spend. Layer seniority, job function, or vetted titles inside matched accounts so budget concentrates on actual buying-committee roles instead of entire companies.
- **Firmographic attribute stacking:** Combine function, seniority, industry, and verified company-size bands (`10-40` vs. LinkedIn `11-50` bands can leak smaller firms unless job titles or exclusions filter them). Avoid stacking so many filters that estimated audience size drops below minimum delivery thresholds (verify LinkedIn's documented 300-member minimum audience rule).
- **Formats and Thought Leader Ads:** Choose formats by buyer communication job (`Single Image`, `Document / Carousel` for frameworks/checklists, `Video`, `Thought Leader Ads` sponsoring an executive/subject-matter post, `Conversation Ads` *to confirm*).
- **Lead quality and cohort maturity:** Keep **Lead Gen Form** leads and **website landing-page** leads in separate reporting rows with separate CRM conversion rates. On long B2B cycles, evaluate LinkedIn via CRM **lead-to-revenue cohorts** with open pipeline share visible (`17-unit-economics`) instead of judging prematurely on raw CPL or early closed deals.

## 3. YouTube Ads format selection and objective-matched measurement

Creative scripting and ABCD production rules live in `09-ad-creative` (`references/demand-gen-and-youtube-creative.md`). Use this matrix for buying, campaign objective alignment, and measurement:

| Format (*to confirm* in Google Ads) | Skip and length profile | Buying fit and measurement rule |
| --- | --- | --- |
| Skippable in-stream | Skip after 5s; <3 min recommended | Broad controlled reach or DR action; hook and value proposition must register inside seconds 1 to 5 |
| Non-skippable in-stream | No skip; 15s to 60s by subtype | Reserved for messages requiring full completion; never use non-skippable to force weak creative |
| Bumper | No skip; 5s to 6s | Single-point recall reinforcement alongside longer formats, not complex education |
| In-feed video | Thumbnail + title in Search/Watch Next/Home | Evaluated like intent browse: title and thumbnail control click-to-watch performance |
| YouTube Shorts | Vertical feed; instant swipe skip | Mobile-native vertical creative with zero guaranteed viewing window |
| Masthead | Reservation via Google rep (autoplay muted) | Mass timed launches only; verify reservation commitments and sound-off comprehension |

**YouTube measurement fit (never blend conversion types):**
- *Awareness:* Brand Lift (apply independent scrutiny and holdout verification; `17-incrementality`).
- *Consideration:* Directional engaged-view and assisted-conversion signals (graded `C1-C2`, never causal proof).
- *Direct response:* Verified store or CRM conversions; never sum view-through and click-through conversions into one "incremental conversions" column.

## Sources

TikTok Business Help Center, LinkedIn Marketing Solutions Help (Matched Audiences and Targeting specifications), and Google Ads Help (About video ad formats; verify current specs with URL and date).
