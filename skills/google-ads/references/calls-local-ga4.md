# Google Ads: Merchant Center, Calls, Local Services Ads and GA4

**Last verified:** 2026-11-18  
**Freshness class:** High-change; recheck within 30 days or whenever current behavior affects a decision.  
**Source:** The 2026 Google Ads and Meta Ads Playbooks (Vince Servidad), condensed; their platform sections were read against Google's and Meta's help pages on 2026-11-18.

Read this reference for Merchant Center feed and image rules, call conversion setup, Local Services Ads and its migration, or the GA4 link and key-event imports. Apply the root `library/contracts/PLATFORM-CURRENCY.md` contract before treating any rule here as current in a specific account. "Google says" and "Meta says" mark platform claims, not expected account results. Not legal advice.

## Merchant Center and online stores

- Fix account issues first. Every product needs a GTIN, or brand plus MPN.
- Images: under 500 x 500 pixels disapproved from 2027-01-31. Aim for 1500 x 1500 or more, no text on the main image. Up to 10 additional images, 1 lifestyle image, up to 10 videos.
- Fill in the Q&A attribute, shipping, return policy, promotion dates and product ratings.
- Campaign choice: for reach, Performance Max, Search with AI Max, Demand Gen; for control, Search with AI Max, Standard Shopping, Demand Gen.
- Performance Max does not always beat Standard Shopping on the same product; higher Ad Rank shows. Put each product in one campaign for control.
- Google says Black Friday demand can be 3 to 7 times a normal day.

## Call conversions

| Type | What counts |
|---|---|
| Calls from ads | Call and location assets, call ads |
| Calls to a website number | Google forwarding number replaces yours for ad clickers |
| Clicks on a mobile-site number | The click, not the call |
| Clicks on call ads and assets | No forwarding number; Google estimates whether a call followed |
| Imported CRM calls | Only calls that became sales, with value |

- Call reporting (Account settings > Call reporting) uses Google forwarding numbers in 30 countries, including the UK and US. It logs start, duration, connection and caller number for calls over 15 seconds. Turning it off stops call tracking.
- Set the minimum call length to the time a real enquiry takes; check it against call logs. Count one conversion per call for leads.
- For lead gen, bid to calls imported as qualified leads or sales, not every call.
- Clicks on the ad's number are paid; numbers dialed by hand are free.

## Local Services Ads

- Pay per valid lead (calls, messages, bookings), not per click. Keywordless, by service category and area, on Search and Maps only. Badge: Google Verified. Missed calls and slow replies can lower ranking. Lead credits: US and Canada.
- Migration into Google Ads as Performance Max with pay-per-lead goals: select US home and storefront services from August 2026, service-area businesses and custom setups late 2026, non-US accounts 2027. Budgets become daily (weekly / 7), manual bidding ends, Target CPA moves to campaign level.
- Past reports do not migrate: download lead totals and screenshot reports first. Keep Google Business Profile details correct; a name or address change can trigger a review that pauses the campaign.
- Search and Local Services Ads can catch the same caller. Count leads by source in the CRM before judging either.

## GA4

- Link: GA4 Admin > Product links > Google Ads links. Needs GA4 Editor or above and Google Ads Admin. A manager-account link counts as one and shares imported data with client accounts.
- Linking enables key-event imports, Google Ads data in GA4 within 48 hours, and GA4 audiences for remarketing (needs Google signals or user-provided data, with personalized advertising on).
- Import: Google Ads > Create > Conversion action > Import > Google Analytics 4 properties. Only key events import; new ones can take 24 to 48 hours to appear.
- One source per goal. If a GA4 import and a Google tag action count the same purchase or lead, keep one as Primary and the other Secondary. Google marks GA4-based actions Secondary when the account already has goals from that property.
- EEA, UK and Switzerland: without consent signals, GA4 audiences in Google Ads include only people outside the EEA (Google, since March 2024). See [competitor, consent and risk](competitor-consent-risk.md).
