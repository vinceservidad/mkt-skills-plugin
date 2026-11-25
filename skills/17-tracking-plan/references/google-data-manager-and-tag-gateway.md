# Google Ads Data Manager & Google Tag Gateway Guide

Distilled from official `@GoogleAds` tagging and measurement playbooks (*Data Manager: Verify & Activate Connections*, *Google Tagging Tutorials*, *Drive better lead gen with first-party data*). Platform UI flows, connector lists and legal consent obligations change — verify current official Google Ads Help docs (cite URL + date) or mark *to confirm*, and never cite Google's aggregate lift averages as expected results for a specific business.

## 1. Google Ads Data Manager (First-Party Signal Hub)

Smart Bidding and Value-Based Bidding perform only as well as the verified first-party outcomes fed back into them. **Google Ads Data Manager** centralizes connecting CRMs, e-commerce platforms, warehouses and file sources into Google Ads without fragile one-off manual CSV uploads.

- **Core use cases:**
  - **Offline Conversion Imports (OCI) & Enhanced Conversions for Leads:** Stream CRM stages (Qualified Call, SQL, Closed Won) with real deal values (`11-paid-search` Value-Based Bidding) matched via hashed first-party identifiers (email/phone) and/or click IDs (`gclid`, `wbraid`, `gbraid`).
  - **Customer Match:** Keep consented customer, high-LTV and existing-buyer exclusion lists refreshed automatically (always exclude current subscribers/customers from cold acquisition where relevant).
- **Verify & activate checklist (do not assume a connected source is working):**
  1. Confirm field mapping (timestamp with timezone, currency code, conversion value, order/lead ID for deduplication, hashed PII normalized cleanly).
  2. Verify active ingestion status, recent row count and match-rate health inside Data Manager diagnostics.
  3. Reconcile imported conversion totals against the source CRM/store before switching bidding strategies onto the new action.

## 2. Google Tag Gateway (First-Party Tagging Infrastructure)

Third-party browser tracking loses signal to ad blockers, ITP and browser cookie limits. **Google Tag Gateway** (serving the Google tag through your own first-party domain via CDN/edge proxy such as Cloudflare or server-side GTM — verify exact supported setups in official docs) strengthens first-party measurement durability alongside:
- **Enhanced Conversions (Web & Leads):** Sends SHA-256 hashed consented first-party customer data (email, phone, address) alongside conversion events to recover observable cross-device/browser conversions.
- **Consent Mode v2:** Passes explicit user consent signals (`ad_storage`, `analytics_storage`, `ad_user_data`, `ad_personalization`) from a certified CMP so tags respect regional law (GDPR/EEA/UK) and behavioral/conversion modeling activates only where legally permitted (flag legal/privacy review with the owner).

## 3. Rollout discipline

- Never flip a live bidding campaign onto a brand-new server-side or Data Manager conversion action on day one: run it as **Secondary (observe-only)** first, reconcile counts and deduplication (`transaction_id` / `order_id`) against the store or CRM over at least 1–2 conversion cycles, then promote to **Primary** only with the owner's explicit approval.
