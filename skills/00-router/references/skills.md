# Skill index

Generated from `catalog.json` by `tools/build.py`; do not edit by hand. Status `built` means the skill exists in this library; `planned` means the section's frameworks apply but the skill has not shipped yet. A skill is invoked as `/<plugin>:<skill>`; when a built skill is not loaded, name its plugin so the user can enable it.

Columns: what the skill is for, what it writes, what it requires before it will write (alternatives separated by "or"), and what it reads if present.

## Q1. Who are we selling to, in what market?

### 01 Market

Job: choose a market where demand exists, you can win, and the economics work. Plugin: `mkt-q1-audience`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `01-market-assessment` | built | Judge whether a market is worth entering: demand, size, forces, timing and what buyers can pay. | `market.md#Market definition`, `market.md#Size`, `market.md#Forces and timing` | nothing | `customer.md#ICP and personas` |
| `01-demand-check` | built | Measure existing demand from search volume, ad spend, competitor count and price bands. | `market.md#Demand` | nothing | `market.md#Market definition` |
| `01-sophistication-stage` | built | Place the market on Schwartz's five sophistication stages and pick the claim type that still works. | `market.md#Market sophistication` | `market.md#Competitors and alternatives` | nothing |
| `01-competitor-profiling` | built | Profile competitors and the real alternatives, including doing nothing or a spreadsheet. | `market.md#Competitors and alternatives` | nothing | `market.md#Market definition`; `customer.md#Current alternatives` |

### 02 Customer

Job: know the buyer better than they know themselves, in their own words. Plugin: `mkt-q1-audience`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `02-customer-research` | built | Plan and run customer interviews and surveys, then synthesize pains, desires, alternatives and buying triggers. | `customer.md#Research log`, `customer.md#Pains, desires and fears`, `customer.md#Current alternatives`, `customer.md#Buying triggers and process` | nothing | `market.md#Market definition` |
| `02-icp-persona` | built | Define who buys, decides, pays and uses, and who to disqualify, as an ICP and personas. | `customer.md#ICP and personas` | `customer.md#Research log` or `customer.md#Voice of customer` | `customer.md#Segments`; `customer.md#Jobs to be done` |
| `02-jobs-to-be-done` | built | Map the functional, emotional and social jobs and the forces that make buyers switch. | `customer.md#Jobs to be done` | `customer.md#Research log` or `customer.md#Voice of customer` | `customer.md#ICP and personas` |
| `02-buyer-psychology` | built | Map the beliefs, objections and decision drivers that block or speed the sale. | `customer.md#Beliefs, objections and drivers` | `customer.md#Research log` or `customer.md#Voice of customer` | `customer.md#ICP and personas`; `customer.md#Jobs to be done` |
| `02-segmentation` | built | Split the market into segments that respond differently and choose which to target (STP). | `customer.md#Segments` | `customer.md#Research log` or `customer.md#Voice of customer` | `market.md#Size` |
| `02-voc-mining` | built | Mine reviews, tickets, forums and call notes for verbatim customer language, with sources. | `customer.md#Voice of customer` | nothing | nothing |

### 03 Awareness

Job: match what you say to what the buyer already knows. Plugin: `mkt-q1-audience`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `03-awareness-map` | built | Map buyers across Schwartz's five awareness levels and set the entry message, proof and offer for each. | `awareness.md#Awareness map` | `customer.md#ICP and personas`; `customer.md#Pains, desires and fears` or `customer.md#Jobs to be done` | `market.md#Market sophistication`; `customer.md#Voice of customer` |
| `03-journey-map` | built | Map journey stages, the buyer's questions, touchpoints and content gaps (See-Think-Do-Care). | `awareness.md#Journey` | `customer.md#ICP and personas`; `awareness.md#Awareness map` | `customer.md#Buying triggers and process` |
| `03-traffic-temperature` | built | Give every traffic source a temperature and the page, offer and call to action it should get. | `awareness.md#Traffic temperature` | `awareness.md#Awareness map` | `offer.md#Value ladder`; `awareness.md#Journey` |

## Q2. What are we selling, and why would they choose it?

### 04 Product

Job: make sure the thing being sold actually delivers the result, before marketing amplifies it. Plugin: `mkt-q2-offer`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `04-pmf-check` | built | Test product-market fit with the Sean Ellis survey, retention curves and word of mouth. | `work/04-product/` | nothing | `customer.md#ICP and personas` |
| `04-plg-audit` | built | Audit a free or self-serve product as the acquisition and conversion engine. | `work/04-product/` | nothing | `customer.md#Jobs to be done`; `offer.md#Price and model` |

### 05 Brand

Job: be remembered and preferred before the buyer is ready, so that when they are, you are the first and easiest choice. Plugin: `mkt-q2-offer`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `05-brand-foundation` | built | Define the brand promise, story, values, personality and archetype on one page. | `brand.md#Brand foundation` | `customer.md#ICP and personas` | `positioning.md#Positioning statement` |
| `05-distinctive-assets` | built | Audit and build the colors, shapes, sounds and characters buyers recognize as yours. | `brand.md#Distinctive assets` | `brand.md#Brand foundation` | nothing |
| `05-brand-voice` | built | Define the brand voice, tone by context, and words to use and avoid. | `brand.md#Voice` | `brand.md#Brand foundation` | `customer.md#Voice of customer` |
| `05-reputation` | built | Monitor and manage reputation, review responses and crisis communications. | `brand.md#Reputation` | nothing | `brand.md#Brand foundation` |
| `05-naming` | built | Name a brand, product or feature and check the name is clear, ownable and available. | `brand.md#Naming` | `brand.md#Brand foundation` or `positioning.md#Positioning statement` | nothing |

### 06 Positioning

Job: own one clear place in the buyer's mind relative to the alternatives. Plugin: `mkt-q2-offer`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `06-positioning-statement` | built | Position the product against the real alternatives: unique attributes, value, best-fit customers and category. | `positioning.md#Category`, `positioning.md#Target customer`, `positioning.md#Competitive alternatives`, `positioning.md#Differentiation`, `positioning.md#Positioning statement` | `customer.md#ICP and personas`; `customer.md#Current alternatives` or `market.md#Competitors and alternatives` | `customer.md#Jobs to be done` |
| `06-unique-mechanism` | built | Name the mechanism that makes the result happen, as the strongest reason to believe. | `positioning.md#Unique mechanism` | `positioning.md#Differentiation` | `market.md#Market sophistication` |
| `06-competitor-pages` | built | Write comparison and alternative pages that hold the position honestly. | `work/06-positioning/` | `positioning.md#Positioning statement`; `market.md#Competitors and alternatives` | nothing |
| `06-category-design` | built | Name and own a new problem and category instead of competing in an old one. | `positioning.md#Category design` | `positioning.md#Positioning statement`; `market.md#Competitors and alternatives` | nothing |

### 07 Offer

Job: make what they get worth clearly more than what they give up, and make choosing it feel safe and urgent. Plugin: `mkt-q2-offer`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `07-offer-design` | built | Design or rebuild the core offer with the Value Equation and Grand Slam Offer method. | `offer.md#Dream outcome`, `offer.md#Core offer`, `offer.md#Value equation`, `offer.md#Name and one-liner` | `customer.md#Pains, desires and fears` or `customer.md#Voice of customer` | `customer.md#Beliefs, objections and drivers`; `customer.md#Current alternatives`; `positioning.md#Unique mechanism` |
| `07-pricing` | built | Set the price and pricing model from value, alternatives and evidence of willingness to pay. | `offer.md#Price and model` | `offer.md#Core offer`; `offer.md#Dream outcome` | `customer.md#Current alternatives`; `market.md#Competitors and alternatives`; `customer.md#Segments` |
| `07-guarantee-risk-reversal` | built | Design a guarantee that shifts risk to the seller without breaking the economics. | `offer.md#Guarantee` | `offer.md#Core offer`; `customer.md#Beliefs, objections and drivers` | `offer.md#Price and model` |
| `07-bonuses-urgency` | built | Add bonuses that each kill the next objection, and urgency and scarcity that are true. | `offer.md#Bonuses`, `offer.md#Urgency and scarcity` | `offer.md#Core offer`; `customer.md#Beliefs, objections and drivers` | `offer.md#Price and model` |
| `07-value-ladder` | built | Lay out the offers from free to high-ticket and continuity, and how buyers move up. | `offer.md#Value ladder` | `offer.md#Core offer`; `offer.md#Price and model` | `customer.md#Segments` |

## Q3. What do we say?

### 08 Message

Job: decide the one idea, the promise, and the reasons that make it believable, before any ad or page is written. Plugin: `mkt-q3-message`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `08-message-doc` | built | Write the message document: big idea, promise, mechanism, reason why, enemy and message house. | `message.md#Big idea`, `message.md#Promise`, `message.md#Mechanism`, `message.md#Reason why`, `message.md#Enemy`, `message.md#Message house` | `offer.md#Dream outcome`; `offer.md#Core offer`; `awareness.md#Awareness map` | `positioning.md#Unique mechanism`; `customer.md#Voice of customer` |
| `08-objection-map` | built | Pair every reason not to buy with the answer and the proof. | `message.md#Objection map` | `customer.md#Beliefs, objections and drivers` | `message.md#Proof stack` |
| `08-proof-stack` | built | Assemble proof under every claim: results, testimonials, data, demos and authority. | `message.md#Proof stack` | `message.md#Promise` or `offer.md#Dream outcome` | nothing |
| `08-story-epiphany-bridge` | built | Write the discovery story that rebuilds the buyer's vehicle, internal and external beliefs. | `message.md#Story` | `customer.md#Beliefs, objections and drivers`; `offer.md#Core offer` | nothing |

### 09 Creative Strategy

Job: turn the message into ideas that stop the scroll for a specific audience at a specific awareness level, in a specific format. Plugin: `mkt-q3-message`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `09-angle-matrix` | built | Generate angles across awareness level, emotional driver and format; every cell is a test. | `work/09-creative-strategy/` | `message.md#Promise`; `awareness.md#Awareness map` | `customer.md#Voice of customer` |
| `09-creative-brief` | built | Write a creative brief: audience, awareness, insight, single message, proof, format and CTA. | `work/09-creative-strategy/` | `message.md#Message house` or `message.md#Promise`; `awareness.md#Awareness map`; `offer.md#Core offer` | nothing |
| `09-hooks` | built | Write hooks for ads, videos and posts from the hook library, matched to awareness. | `work/09-creative-strategy/` | `message.md#Promise`; `customer.md#Voice of customer` or `awareness.md#Awareness map` | nothing |
| `09-ad-creative` | built | Produce ad concepts, variations and iterations for paid social and display (Hook-Story-Offer). | `work/09-creative-strategy/` | `message.md#Promise`; `awareness.md#Awareness map`; `offer.md#Core offer` | nothing |
| `09-ugc-brief` | built | Brief creators for UGC: problem-solution, testimonial, unboxing, day-in-the-life, before-after. | `work/09-creative-strategy/` | `message.md#Promise`; `customer.md#Voice of customer` | nothing |
| `09-image-video` | built | Direct or generate image and video assets that carry the message and the brand's assets. | `work/09-creative-strategy/` | `message.md#Promise` | `brand.md#Distinctive assets` |

### 10 Copywriting

Job: write words that move the reader to the next action. This is where the small, famous frameworks live. Plugin: `mkt-q3-message`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `10-page-copy` | built | Write or rewrite web page copy: home, about, product and feature pages. | `work/10-copywriting/` | `offer.md#Core offer`; `message.md#Promise`; `awareness.md#Awareness map` | `customer.md#Voice of customer`; `brand.md#Voice` |
| `10-headlines` | built | Write headlines and leads chosen by awareness level (Caples, Great Leads, 4 Us). | `work/10-copywriting/` | `message.md#Promise`; `awareness.md#Awareness map` | `customer.md#Voice of customer` |
| `10-sales-page` | built | Write a long-form sales page from offer, proof and objections. | `work/10-copywriting/` | `offer.md#Core offer`; `offer.md#Price and model`; `offer.md#Guarantee`; `message.md#Proof stack`; `message.md#Objection map`; `awareness.md#Awareness map` | `message.md#Story` |
| `10-email-copy` | built | Write individual emails: broadcasts, promotions and announcements. | `work/10-copywriting/` | `message.md#Promise`; `awareness.md#Awareness map` or `awareness.md#Journey` | `brand.md#Voice` |
| `10-ad-copy` | built | Write ad copy for search and social, matched to awareness and platform limits. | `work/10-copywriting/` | `message.md#Promise`; `awareness.md#Awareness map`; `offer.md#Core offer` | nothing |
| `10-vsl-script` | built | Write a video sales letter or webinar script (Perfect Webinar). | `work/10-copywriting/` | `offer.md#Core offer`; `message.md#Story` or `message.md#Big idea`; `message.md#Proof stack` | nothing |
| `10-copy-editing` | built | Edit copy for clarity, specificity, proof and flow without changing the offer. | `work/10-copywriting/` | nothing | `message.md#Promise`; `brand.md#Voice` |
| `10-swipe-file` | built | Build and use a swipe file of proven ads, headlines and pages, filed by section and awareness. | `work/10-copywriting/` | nothing | nothing |

## Q4. How do we reach them?

### 11 Distribution

Job: put the message in front of the right people, at a cost that works, in channels you can grow. Plugin: `mkt-q4-reach`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `11-channel-selection` | built | Choose one or two channels to win with the Bullseye method, from all paid, owned and earned options. | `work/11-distribution/` | `customer.md#ICP and personas`; `offer.md#Core offer` or `offer.md#Price and model` | `awareness.md#Traffic temperature` |
| `11-seo` | built | Plan SEO: keyword research by intent, on-page, technical health, links and topical authority. | `work/11-distribution/` | `customer.md#ICP and personas` | `awareness.md#Journey` |
| `11-local-seo` | built | Plan Local SEO and Google Business Profile: Map Pack visibility, NAP citations and local pages. | `work/11-distribution/` | `customer.md#ICP and personas` | `offer.md#Core offer`; `brand.md#Reputation` |
| `11-ai-seo-geo` | built | Get the brand cited in AI search answers (generative engine optimization). | `work/11-distribution/` | `positioning.md#Positioning statement` or `customer.md#ICP and personas` | nothing |
| `11-programmatic-seo` | built | Build templated pages at scale from a data set, without thin or duplicate content. | `work/11-distribution/` | `customer.md#ICP and personas` | nothing |
| `11-site-architecture` | built | Design site structure and internal linking so pages are found and rank. | `work/11-distribution/` | nothing | `awareness.md#Journey` |
| `11-schema` | built | Add structured data that matches visible content and earns rich results. | `work/11-distribution/` | nothing | nothing |
| `11-paid-search` | built | Plan paid search to capture intent: keywords, match types, ad groups and bidding. | `work/11-distribution/` | `offer.md#Core offer`; `awareness.md#Awareness map` | nothing |
| `11-shopping-feeds` | built | Plan Google Shopping, Merchant Center and supplemental product feeds: titles, hygiene and SKU segmentation. | `work/11-distribution/` | `offer.md#Core offer`; `awareness.md#Awareness map` | `offer.md#Price and model` |
| `11-paid-social` | built | Plan paid social: creative-led campaigns, broad targeting and algorithm learning. | `work/11-distribution/` | `offer.md#Core offer`; `awareness.md#Awareness map` | `message.md#Promise` |
| `11-marketplace-retail-media` | built | Plan marketplace and retail media (Amazon Ads, TikTok Shop, Etsy, Walmart): retail readiness, Buy Box and TACoS. | `work/11-distribution/` | `offer.md#Core offer`; `awareness.md#Awareness map` | `offer.md#Price and model` |
| `11-content-strategy` | built | Plan content pillars, clusters, repurposing and distribution against the journey. | `work/11-distribution/` | `customer.md#ICP and personas`; `awareness.md#Journey` or `awareness.md#Awareness map` | nothing |
| `11-social` | built | Plan organic social: platform choice, formats, cadence and community replies. | `work/11-distribution/` | `customer.md#ICP and personas` | `brand.md#Voice` |
| `11-influencer` | built | Plan influencer and creator programs: seeding, sponsorship, affiliate and whitelisting. | `work/11-distribution/` | `customer.md#ICP and personas`; `offer.md#Core offer` | nothing |
| `11-affiliate-jv` | built | Design affiliate and JV programs that pay on performance. | `work/11-distribution/` | `offer.md#Core offer`; `offer.md#Price and model` | nothing |
| `11-cold-email` | built | Run cold outreach and account-based plays: list, first line, value, soft ask, follow-up. | `work/11-distribution/` | `customer.md#ICP and personas`; `offer.md#Core offer` | nothing |
| `11-email-channel` | built | Run email as a channel: list growth, deliverability and the broadcast calendar. | `work/11-distribution/` | `customer.md#ICP and personas` | `offer.md#Core offer`; `brand.md#Voice` |
| `11-pr` | built | Earn press with newsjacking, data stories and the founder story. | `work/11-distribution/` | `message.md#Big idea` or `message.md#Story` | nothing |
| `11-co-marketing` | built | Borrow audiences through partnerships, the Dream 100 and newsletter sponsorships. | `work/11-distribution/` | `customer.md#ICP and personas` | nothing |
| `11-events` | built | Use events, trade shows and speaking to meet buyers and book conversations. | `work/11-distribution/` | `customer.md#ICP and personas` | nothing |
| `11-aso` | built | Optimize an app store listing for search and conversion. | `work/11-distribution/` | `positioning.md#Positioning statement` or `customer.md#ICP and personas` | nothing |
| `11-directories` | built | List the product on directories, marketplaces and launch platforms. | `work/11-distribution/` | `positioning.md#Positioning statement` or `customer.md#ICP and personas` | nothing |
| `11-free-tools` | built | Build free tools that attract buyers and lead to the core offer (engineering as marketing). | `work/11-distribution/` | `customer.md#Jobs to be done` | nothing |
| `11-podcast-video` | built | Use podcasts, guesting and video (YouTube) as a distribution channel. | `work/11-distribution/` | `customer.md#ICP and personas` | `message.md#Story` |
| `11-sms` | built | Plan SMS as an owned channel: consent, cadence and message types. | `work/11-distribution/` | `awareness.md#Journey` or `awareness.md#Awareness map` | `offer.md#Core offer` |
| `11-whatsapp` | built | Plan WhatsApp Business Platform and conversational messaging: explicit opt-in, Utility vs Marketing templates and flows. | `work/11-distribution/` | `awareness.md#Journey` or `awareness.md#Awareness map` | `offer.md#Core offer` |

### 12 Funnel

Job: design the path from first touch to purchase (and beyond) so each step earns the next one. Plugin: `mkt-q4-reach`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `12-funnel-design` | built | Design the path from first touch to purchase and back-end, one job per step. | `work/12-funnel/` | `offer.md#Value ladder` or `offer.md#Core offer`; `awareness.md#Traffic temperature` or `awareness.md#Awareness map` | nothing |
| `12-lead-magnet` | built | Design a lead magnet that is specific, fast, valuable and leads to the core offer. | `work/12-funnel/` | `offer.md#Core offer`; `customer.md#Pains, desires and fears` | nothing |
| `12-landing-page` | built | Build a landing page for one traffic source and one offer. | `work/12-funnel/` | `offer.md#Core offer`; `message.md#Promise`; `awareness.md#Traffic temperature` or `awareness.md#Awareness map` | nothing |
| `12-email-sequences` | built | Write email sequences: welcome, nurture (Soap Opera), launch and sales. | `work/12-funnel/` | `offer.md#Core offer`; `message.md#Story` or `message.md#Promise`; `awareness.md#Journey` or `awareness.md#Awareness map` | nothing |
| `12-retargeting` | built | Build the retargeting ladder: visitors, engaged, cart and buyers, each with its own message. | `work/12-funnel/` | `awareness.md#Traffic temperature`; `offer.md#Core offer` | nothing |
| `12-launch` | built | Run a launch funnel with built-in urgency (Product Launch Formula). | `work/12-funnel/` | `offer.md#Core offer`; `offer.md#Urgency and scarcity`; `message.md#Big idea` | nothing |
| `12-webinar-challenge` | built | Design a webinar or challenge funnel that converts on a live event. | `work/12-funnel/` | `offer.md#Core offer`; `message.md#Story` or `message.md#Big idea` | nothing |
| `12-upsell-path` | built | Design order bumps, upsells and downsells that raise order value. | `work/12-funnel/` | `offer.md#Value ladder` | nothing |

## Q5. How do they decide?

### 13 Conversion

Job: turn the visitors you already have into leads and buyers, without buying more traffic. Plugin: `mkt-q5-decide`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `13-cro-audit` | built | Audit a page for clarity, relevance, friction, anxiety and proof, and rank the fixes. | `work/13-conversion/` | `offer.md#Core offer` or `message.md#Promise` | `awareness.md#Awareness map` |
| `13-checkout` | built | Optimize checkout: fields, guest checkout, payment options, progress and order bumps. | `work/13-conversion/` | nothing | `offer.md#Price and model` |
| `13-signup` | built | Optimize signup and registration flows for completion and activation. | `work/13-conversion/` | nothing | `customer.md#Jobs to be done` |
| `13-popups` | built | Design popups and slide-ins that capture without annoying. | `work/13-conversion/` | `offer.md#Core offer` or `offer.md#Value ladder` | nothing |
| `13-paywalls` | built | Design paywalls and upgrade prompts in the product. | `work/13-conversion/` | `offer.md#Price and model` | nothing |
| `13-pricing-page` | built | Design the pricing page: plans, anchors, comparison and risk reversal. | `work/13-conversion/` | `offer.md#Price and model` | `offer.md#Guarantee` |
| `13-trust-signals` | built | Place the trust stack: reviews, logos, guarantees, real people and specific numbers. | `work/13-conversion/` | `message.md#Proof stack` or `customer.md#Beliefs, objections and drivers` | nothing |
| `13-cart-recovery` | built | Write the cart and checkout recovery sequence with an escalating reason to return. | `work/13-conversion/` | `customer.md#Beliefs, objections and drivers` | `offer.md#Guarantee` |

### 14 Sales

Job: close higher-ticket or complex deals in conversation, where a page cannot do the whole job. Plugin: `mkt-q5-decide`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `14-sales-script` | built | Write a sales call script that sells the outcome and closes (CLOSER, Challenger). | `work/14-sales/` | `offer.md#Core offer`; `customer.md#Beliefs, objections and drivers` | nothing |
| `14-discovery-spin` | built | Run discovery that makes the prospect state the gap (SPIN, Gap Selling, MEDDIC). | `work/14-sales/` | `customer.md#Pains, desires and fears`; `customer.md#ICP and personas` | nothing |
| `14-objection-handling` | built | Prepare answers to sales objections and the order to handle them in. | `work/14-sales/` | `message.md#Objection map` or `customer.md#Beliefs, objections and drivers` | nothing |
| `14-prospecting` | built | Build prospect lists and a prospecting cadence for the ICP. | `work/14-sales/` | `customer.md#ICP and personas` | nothing |
| `14-lead-scoring` | built | Score and qualify leads (BANT, fit and intent) and route them to sales. | `work/14-sales/` | `customer.md#ICP and personas` | nothing |
| `14-sales-enablement` | built | Build battle cards, one-pagers and decks that sales actually uses. | `work/14-sales/` | `positioning.md#Competitive alternatives` or `market.md#Competitors and alternatives`; `message.md#Proof stack` or `message.md#Objection map` | nothing |
| `14-dm-selling` | built | Sell in DMs and chat: open, qualify, invite, close. | `work/14-sales/` | `offer.md#Core offer`; `customer.md#ICP and personas` | nothing |

## Q6. What happens after?

### 15 Retention

Job: get the customer to the promised result, keep them, and grow what they spend. Plugin: `mkt-q6-after`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `15-onboarding` | built | Onboard customers to the first result, not the features (activation and the aha moment). | `work/15-retention/` | `offer.md#Dream outcome`; `customer.md#Jobs to be done` | nothing |
| `15-lifecycle` | built | Plan lifecycle email, SMS and push: welcome, post-purchase, replenishment, win-back. | `work/15-retention/` | `awareness.md#Journey` or `customer.md#Segments` | `offer.md#Value ladder` |
| `15-churn-prevention` | built | Diagnose churn and design save, pause and dunning flows that keep customers. | `work/15-retention/` | nothing | `customer.md#Jobs to be done`; `offer.md#Price and model` |
| `15-loyalty` | built | Design a loyalty program: points, tiers, perks and surprise. | `work/15-retention/` | nothing | `offer.md#Value ladder`; `customer.md#Segments` |
| `15-expansion` | built | Plan upsell, cross-sell and account expansion triggers. | `work/15-retention/` | `offer.md#Value ladder` | nothing |
| `15-nps-feedback` | built | Run NPS, CSAT and CES and route the feedback to Product and Offer. | `work/15-retention/` | nothing | `customer.md#ICP and personas` |

### 16 Referral and Community

Job: turn customers into the acquisition channel. Plugin: `mkt-q6-after`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `16-referral-program` | built | Design a referral program: reward, timing, ask and tracking. | `work/16-referral-community/` | `offer.md#Core offer` | `customer.md#Buying triggers and process` |
| `16-reviews` | built | Build a review generation system: ask at delight, one click, respond to every review. | `work/16-referral-community/` | nothing | `brand.md#Reputation` |
| `16-testimonials-case-studies` | built | Collect testimonials and case studies with before, after, specific result and objection beaten. | `work/16-referral-community/` | `offer.md#Dream outcome`; `customer.md#Beliefs, objections and drivers` | nothing |
| `16-community` | built | Build a community with a purpose, rituals and a value exchange, measured by engagement. | `work/16-referral-community/` | `customer.md#ICP and personas`; `customer.md#Jobs to be done` | nothing |
| `16-ugc-program` | built | Run a UGC program: prompts, contests, creator seeding and featuring customers. | `work/16-referral-community/` | `customer.md#ICP and personas` | `brand.md#Distinctive assets` |
| `16-viral-loop` | built | Design sharing mechanics and measure the viral loop (K-factor). | `work/16-referral-community/` | nothing | `offer.md#Core offer` |

## Q7. How do we know, and how do we improve?

### 17 Measurement

Job: know what is working, what it costs, and what it returns, at every stage. Plugin: `mkt-q7-improve`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `17-tracking-plan` | built | Write the tracking plan: events, UTMs, pixels, server-side and CRM fields. | `work/17-measurement/` | nothing | `awareness.md#Journey`; `offer.md#Value ladder` |
| `17-analytics` | built | Answer a business question from funnel and cohort data. | `work/17-measurement/` | nothing | nothing |
| `17-attribution` | built | Choose and caveat an attribution model, from last click to MMM. | `work/17-measurement/` | nothing | nothing |
| `17-unit-economics` | built | Model CAC, LTV, payback, contribution margin and MER. | `work/17-measurement/` | `offer.md#Price and model` | nothing |
| `17-dashboard` | built | Design a dashboard around the north star and its input metrics. | `work/17-measurement/` | nothing | nothing |
| `17-incrementality` | built | Design holdout and geo-lift tests that measure what spend really adds. | `work/17-measurement/` | nothing | nothing |

### 18 Experimentation

Job: replace opinions with evidence, in order of expected impact. Plugin: `mkt-q7-improve`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `18-hypothesis` | built | Write test hypotheses and prioritize them (ICE, PIE, RICE). | `work/18-experimentation/` | nothing | nothing |
| `18-ab-testing` | built | Design an A/B test: one variable, sample size, duration and decision rule. | `work/18-experimentation/` | nothing | nothing |
| `18-creative-testing` | built | Test creative concepts, then variations, then iterations. | `work/18-experimentation/` | `message.md#Promise` or `awareness.md#Awareness map` | nothing |
| `18-price-testing` | built | Test price by cohort, geography or offer variant without breaking trust. | `work/18-experimentation/` | `offer.md#Price and model` | nothing |
| `18-experiment-log` | built | Keep the learning log: hypothesis, result, insight, next step. | `work/18-experimentation/` | nothing | nothing |

### 19 Growth

Job: take what works and make it bigger without breaking it, in the right order. Plugin: `mkt-q7-improve`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `19-constraint-finder` | built | Find the growth stage and the one constraint to fix now. | `work/19-growth/` | nothing | nothing |
| `19-growth-model` | built | Build a growth model and forecast from the funnel's rates and volumes. | `work/19-growth/` | nothing | nothing |
| `19-scale-paid` | built | Scale paid media: budget steps, creative volume, broad targeting and new placements. | `work/19-growth/` | nothing | `offer.md#Price and model` |
| `19-horizontal-expansion` | built | Expand to new channels, offers, segments or markets once the core is stable. | `work/19-growth/` | `customer.md#Segments` or `customer.md#ICP and personas`; `offer.md#Value ladder` or `offer.md#Core offer` | nothing |
| `19-growth-loops` | built | Design loops where each cycle's output feeds the next (viral, content, paid, sales). | `work/19-growth/` | nothing | `offer.md#Core offer` |

## Q8. How do we run it?

### 20 Operations

Job: give the system people, money, tools, process and rules so it runs every week without you. Plugin: `mkt-q8-run`.

| Skill | Status | Purpose | Writes | Requires | Reads if present |
| --- | --- | --- | --- | --- | --- |
| `20-marketing-plan` | built | Write the one-page marketing plan with owners, budget, KPIs and calendar. | `work/20-operations/` | `customer.md#ICP and personas`; `offer.md#Core offer` | `message.md#Promise` |
| `20-budget` | built | Allocate and pace the marketing budget (70/20/10, brand vs activation). | `work/20-operations/` | nothing | nothing |
| `20-sops` | built | Turn a process that worked twice into an SOP with steps, examples and checks. | `work/20-operations/` | nothing | nothing |
| `20-content-calendar` | built | Plan the content calendar: what ships when, who owns it. | `work/20-operations/` | nothing | `awareness.md#Journey`; `brand.md#Voice` |
| `20-martech` | built | Map the martech stack: what each tool does, connects to and who owns it. | `work/20-operations/` | nothing | nothing |
| `20-compliance` | built | Check marketing against ad policies, privacy law and claim-substantiation rules. | `work/20-operations/` | nothing | `offer.md#Guarantee`; `message.md#Proof stack` |
| `20-marketing-council` | built | Review a plan or asset from several expert perspectives before it ships. | `work/20-operations/` | nothing | nothing |
| `20-campaign-review` | built | Run a post-mortem: what happened, why, what to keep and what to change. | `work/20-operations/` | nothing | nothing |
