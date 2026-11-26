# Signal Validation, Browser/Server Deduplication and Offline CRM Conversions

Distilled from official 2026 Meta Blueprint study guides (Media Buying Feb 2026, Associate Jan 2026) and Google Ads conversion/offline import verification workflows. Always confirm current API payload fields, Meta Event Match Quality diagnostics, and Google Data Manager settings against live platform documentation (*to confirm*).

## 1. The 11-column source-to-business event map

Map every commercial conversion event from the real customer action all the way back to the system of record:

`real action | originating system | event / trigger | connector (browser / server / CRM) | dataset or conversion action | value and currency | consent basis | receipt | deduplication key | platform view | reconciled source-of-truth record`

- **Collection defect vs. attribution difference:** A Meta custom conversion rule or an inflated Pixel trigger does not create real orders. Always check the store or CRM record separately before trusting ad-platform reporting.
- **Avoid firing Purchases on non-purchase views:** Renewal emails, thank-you page bookmarks, or order-status refreshes firing `Purchase` pixels double-count existing customers as new acquisitions (`19-scale-paid` and `11-paid-social` treat this as a hard measurement defect).

## 2. Browser + server deduplication and signal validation

When running browser + server-side tracking together (Meta Pixel + Conversions API; Google tag + Enhanced Conversions / server-side GTM):
1. **Shared unique `event_id` and order ID:** Transmit matching `event_id` / `transaction_id` values on both browser and server payloads for the exact same customer action so the platform deduplicates 36 transmissions for 18 real orders back down to 18 conversions.
2. **Event Match Quality (EMQ) vs. semantic accuracy:** High EMQ measures identifier hashing coverage (email, phone, click ID, external ID); it never proves the event fired on the right page, carried net revenue excluding refunds, or deduplicated cleanly.
3. **Never sum platform-credited conversions across channels:** Google Ads and Meta Ads routinely claim overlapping credit for the same order (`17-attribution`, `17-incrementality`). Reconcile both against non-duplicated store orders or CRM closed-won rows (`scripts/sum_by.py`).

## 3. Offline CRM conversion validation (Meta Conversion Leads and Google OCI / Data Manager)

When a form submission or booked call is not the final sale:
1. **Preserve acquisition identifiers at capture:** Store click/lead IDs (`gclid`, `wbraid`, `gbraid`, Meta `fbc`, `fbp`, and 15-17 digit Lead ID) alongside consent status and UTC timestamps in the CRM on initial lead creation.
2. **Map explicit CRM stages:** Separate `submitted` -> `contacted` -> `qualified (SQL)` -> `won (customer)` so platforms optimize on downstream qualified outcomes instead of junk form fills (`11-paid-social`, `11-paid-search`). Document qualification lag and late/refunded outcome adjustments cleanly.
3. **Audit loss across 5 layers:** Compare row counts at (a) uncaptured IDs, (b) missing consent, (c) schema/formatting errors, (d) rejected platform imports, and (e) attribution/conversion lag gaps.
4. **Strict privacy and consent boundary:** Hashing (`SHA-256`) helps matching; it never exempts unconsented users, restricted health/sensitive datasets, or opt-out flags (`20-compliance`). Test with synthetic data first and get explicit owner approval before modifying live pixels or conversion goals.

## Sources

Meta Media Buying study guide (Feb 2026) and Associate study guide (Jan 2026); Google Ads Enhanced Conversions for Leads and Data Manager documentation (to confirm URLs and dates against current docs).
