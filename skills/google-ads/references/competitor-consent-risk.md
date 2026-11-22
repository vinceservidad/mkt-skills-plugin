# Google Ads: Competitor Research, Consent, Account Health and Regulated Industries

**Last verified:** 2026-11-18  
**Freshness class:** High-change; recheck within 30 days or whenever current behavior affects a decision.  
**Source:** The 2026 Google Ads and Meta Ads Playbooks (Vince Servidad), condensed; their platform sections were read against Google's and Meta's help pages on 2026-11-18.

Read this reference for competitor ad research, consent requirements, suspensions and appeals, or a regulated product or market. Apply the root `library/contracts/PLATFORM-CURRENCY.md` contract before treating any rule here as current in a specific account. "Google says" and "Meta says" mark platform claims, not expected account results. Not legal advice.

## Competitor research

- Google Ads Transparency Center (adstransparency.google.com): search by advertiser or site; filter by region, date, platform and format. Shows ads run on Search, YouTube, Display and Gmail.
- Meta Ad Library (facebook.com/ads/library): active Meta ads by keyword or Page and country. Ads that reached the UK or EU stay one year after last impression, with dates, targeting and reach; social-issue, election and political ads stay 7 years with spend and reach.
- Log per competitor: offer, angle, format, first-seen date, landing page, source and check date. A long-running ad is a hint, not proof, that it works. Take angles and gaps, never the words.
- Look up the client too: verified advertiser name, and no old or stray ads still running.
- Findings feed `$creative-strategy`; they are evidence about competitors, not customer truth.

## Consent

- Google's EU user consent policy covers the EEA, UK and Switzerland: consent for cookies where required and for ad personalization, kept records, and withdrawal.
- Consent mode signals: `ad_storage`, `analytics_storage`, `ad_user_data`, `ad_personalization`. `ad_user_data` is required for conversion tracking and enhanced conversions.
- Basic mode blocks tags until the visitor chooses. Advanced mode loads tags and sends cookieless pings when consent is denied, so Google can model conversions.
- Google says that without consent signals you cannot keep using its tags for measurement, personalization and remarketing for EEA users. Customer Match in the EEA needs `ad_user_data` and `ad_personalization` both granted.
- Meta consent and data-source rules: see the meta-ads [leads, health and specs reference](../../meta-ads/references/meta-leads-health-specs.md).

## Account health

- Google suspends at once, without warning, for egregious violations (circumventing systems, counterfeit goods, malicious software and others) and can suspend for billing problems (chargebacks, suspicious payments, unpaid balances). Other repeat violations get at least 7 days' warning. A suspension can reach related and new accounts.
- Strikes (some policies): warning; strike 1 = 3-day hold; strike 2 within 90 days = 7-day hold; strike 3 within 90 days = suspension.
- Appeal from Contact us in the account notice: one at a time, honest and complete, within at least 6 months. Some advertisers must pass verification first; 3 failed attempts end the appeal. Never open new accounts while one is suspended.
- Advertiser verification: every advertiser eventually, by a Google-set deadline; missing it can restrict ads or pause the account. The verified name shows in ad disclosures and the Transparency Center.
- EU political ads: every campaign must declare. Campaigns that say yes stop serving in the EU. Check with query 6 in [GAQL data pulls](gaql-data-pulls.md).

## Regulated industries

Flag a regulated account to the user and read the full policy for the product and country before launch.

- Healthcare and medicines: certification for prescription drug services (online pharmacies, telemedicine), pharmaceutical manufacturers, addiction services and abortion ads (US, UK, Ireland). UK online pharmacies: GPhC registration plus Google certification, no prescription drugs in ads or landing pages. UK telemedicine: LegitScript plus Google certification. HIV home tests: US (FDA approved), France, the Netherlands, UK only. Birth control, fertility and STI testing restricted in some locations. No speculative treatments, unapproved substances, or unapproved cure claims.
- Personalized ads: health, alcohol, gambling, birth control, negative financial status and other sensitive categories cannot use advertiser-curated audiences (Customer Match, your data segments, lookalike segments, audience expansion); Google's predefined audiences are allowed. No personalized ads to under-18s. US and Canada housing, employment and consumer finance: no targeting by gender, age, parental status, marital status or ZIP code.
- Financial services: verification in some locations; disclosures visible without a click. Personal loans: full repayment in 61 days or longer; US APR under 36%. No binary options or credit repair. Debt services need certification. CFDs, spread betting and rolling spot forex only in select locations with approval. Crypto only within certification and local rules.
- Gambling: certification per country; UK operators need a Gambling Commission license. Never target minors. Landing pages show responsible-gambling information, an age warning and license details.
- Political: election-ads verification where required, "Paid for by" disclosures, EU political ads restricted under Regulation 2024/900.
