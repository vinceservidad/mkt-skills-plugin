# Ad formats: all 14 paid channels (what to confirm before writing)

Platform limits, asset counts and policies change frequently. Confirm the current values in the platform's own official help pages or the live ad account before writing, and record where each was checked. If you cannot verify a limit during the run, mark it *to confirm* — never state a character limit from memory as current.

## Channel matrix (fields, native copy rules and policy checks)

| Channel | Fields to confirm | Native copy & hook rules | Policy areas to check |
| --- | --- | --- | --- |
| **Google Search (RSAs)** | Headline count & char limit, description count & char limit, display path fields, asset extensions (sitelinks, callouts) | Match active search intent directly; every headline must make sense in any combination (no broken halves unless pinned intentionally); pair concrete offer/mechanism with a clean CTA | Trademarks, unsubstantiated superlatives (*#1*, *best*), excessive caps/punctuation, misleading pricing or claims |
| **Google Performance Max (PMax) & Demand Gen** | Short headlines, long headlines, descriptions, business name, CTA button, optional video/image hooks | Write modular headlines that work standalone across Search, Shopping, YouTube, Discover and Gmail; keep visual + copy promise identical to the landing page | Same Google Ads editorial/claims rules plus feed price/availability parity (hand Shopping feed titles to `11-shopping-feeds`) |
| **Microsoft / Bing Ads** | RSA headlines & descriptions, multimedia ad headline/description, path & extension fields | Mirror high-intent search structure; note older/desktop/B2B skew when matching tone and proof | Same search editorial, trademark and healthcare/finance policy rules |
| **YouTube Ads (In-Stream, Shorts, In-Feed)** | Video script opening 5s hook, headline, long headline, description, companion banner / CTA overlay | Follow **ABCD** (Attract in first 5 seconds before Skip, Brand early, Connect via problem/proof, Direct with clear spoken + visual CTA); write for sound-on AND sound-off captions | Claims substantiation, regulated categories (finance/health), landing-page match |
| **Meta (Facebook & Instagram)** | Primary text (visible lines before *See more*), headline, link description, CTA button | Lead with a scroll-stopping first line in third person or product/story framing; match cold vs. warm temperature cleanly | **Personal attributes** (never assert or ask about personal traits/struggles like *Are you struggling with…?*, *Working from home?*), before/after body/health claims, Special Ad Categories |
| **TikTok & TikTok Shop Ads** | Caption length, on-screen text hook, display name, Shop product anchor / CTA | Speak in fast, conversational native phrasing; front-load the visual + spoken hook in the first 2 seconds; keep captions short so they do not cover key visuals (hand full creator scripts to `09-ugc-brief`) | Unverified claims, exaggerated before/afters, music/commercial audio rights, TikTok Shop offer/price accuracy |
| **LinkedIn Ads** | Introductory text (visible before *see more*), headline, description, Lead Gen Form headline/copy | Write like a peer sharing an operational insight or concrete diagnostic; route cold job-title/company audiences to a checklist, teardown or guide rather than a hard sales call | Professional/financial/ROI claims, data & Lead Gen privacy disclosures |
| **Pinterest Ads (Search, Browse & Catalog Pins)** | Pin title, Pin description, vertical 2:3 clean image text overlay, destination URL | Match visual-search planning intent (clear product/outcome keywords buyers actually search and save); keep text overlay clean and minimal — avoid loud *SALE NOW* clutter; align landing page visually to the exact pin | Misleading links, low-quality/clickbait overlays, feed price/availability parity for Catalog Pins |
| **Reddit Ads** | Post headline, optional body copy (free-form/conversation ads), CTA button, comments on/off setting | Write like an honest practitioner or founder: concrete problem, real mechanism, plain language, zero corporate hype or buzzwords; assume high reader skepticism and write headlines that hold up if comments are open | Editorial honesty, community guidelines, landing-page transparency, regulated industries |
| **X (Twitter) Ads** | Post text length, website card headline, CTA | One sharp idea, contrarian observation or concrete proof per post; conversational native style with zero hashtag stuffing | Claims substantiation, misleading engagement bait, brand/trademark rules |
| **Snapchat Ads** | Brand name, ultra-short headline/caption, 3-second vertical opening hook, attachment CTA | Instant visual comprehension in under 3 seconds; short, punchy mobile copy with one unmistakable tap/swipe action | Age-appropriate content, claims/health restrictions, clear landing-page load speed |
| **Amazon & Marketplace Ads (Sponsored Brands / Display)** | Custom headline length (Sponsored Brands / Display), brand logo & landing store/ASIN match | Lead with clear product category + primary buyer benefit from verified reviews/catalog; keep tone factual and retail-ready (hand listing SEO and ACoS/TACoS structure to `11-marketplace-retail-media`) | **Strict Amazon ad policy:** no unsubstantiated *best*, *#1*, *top-rated* or promotional *save / discount / free shipping* phrasing in headlines unless explicitly permitted by current Amazon Ads Creative Acceptance Policy |
| **Native Ads (Taboola / Outbrain)** | Editorial headline length, brand/sponsor name, thumbnail + advertorial/bridge page match | Use honest curiosity-gap or diagnostic editorial headlines that feel native beside news articles — never bait-and-switch; the landing page must immediately deliver what the headline promised | Native network anti-clickbait rules, sensational/health/finance claims, clear sponsor disclosure |
| **Programmatic / Display Banners (GDN, DSPs)** | Short headline, long headline, short description, CTA button across responsive & static banner sizes | One value proposition + one proof cue + one clear CTA readable at a glance (no dense paragraphs); pair tightly with retargeting stage (`12-retargeting`) | Banner clutter/animation limits, misleading UI buttons (fake close/play buttons), clear brand identification |

## Angles

- **Outcome:** what they get.
- **Problem:** what stops now.
- **Mechanism:** why this works.
- **Proof:** who it worked for.
- **Identity:** for people like you.
- **Objection:** the doubt, answered.

## SLAP: Stop, Look, Act, Purchase

Use SLAP as the shape of every ad regardless of channel:
- **Stop:** the first line, headline or opening 2–5 seconds halts the scroll (or directly answers the active search query).
- **Look:** the next lines hold attention with the single specific reason to care (mechanism, proof or contrast).
- **Act:** one unambiguous call to action matching the buyer's awareness stage.
- **Purchase:** the click lands on a destination carrying the exact same promise, visual cue and offer terms toward conversion.

Check every ad for all four steps before testing variants.

## Testing

Change strictly **one** element per variant (the hook, the angle, the proof line or the call to action) and name that single variable in the variant log. Decide in advance the business metric and minimum sample that settles the test, and pass test execution to `18-creative-testing`.
