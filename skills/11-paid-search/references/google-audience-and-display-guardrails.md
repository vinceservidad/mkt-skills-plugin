# Google Customer Match / Audience Observation, Display Guardrails and Programmatic SPO

Use when planning Google Ads audiences (Customer Match, RLSA, remarketing lists), Performance Max audience signals, Google Display Network expansion, or programmatic display/video buys. Verify all Customer Match eligibility minimums, list-expiry caps, and campaign-type controls in current Google Ads documentation (*to confirm*).

## 1. Google audience readiness ledger

Define the exact commercial job before attaching any audience list: acquiring net-new buyers, resolving open purchase objections, expanding existing customer LTV, or observing behavior cleanly.

For each list, document:
`source system | qualifying event | membership window | refresh cadence | consent basis | intended campaign use (Targeting vs. Observation vs. Signal vs. Exclusion)`

**Three operational guardrails:**
1. **Targeting vs. Observation is not neutral:** Under Google Ads *Targeting*, delivery restricts to list members; under *Observation*, delivery continues broadly while reporting on the list. However, Google documents that first-party *Observation* segments can still inform Smart Bidding signals (`11-paid-search` checks current docs). Never treat Observation as zero bidding influence.
2. **PMax audience signals are suggestions, not hard cages:** Audience signals help seed Performance Max exploration and do not restrict PMax delivery strictly to those users. Exclude existing customers at the campaign/customer-acquisition setting level only where new-customer acquisition economics require it (`17-unit-economics`) and current account eligibility confirms.
3. **Consent, hashing and retargeting incrementality:** Never upload unconsented CRM lists to Customer Match; hashing supports matching and never replaces opt-in requirements (`20-compliance`). High ROAS on prior-buyer or branded RLSA campaigns reflects existing purchase momentum, never causal incrementality (`17-incrementality`).

## 2. Display Network and Programmatic Supply-Path Optimization (SPO)

Disable Display Network expansion on Search campaigns by default unless explicitly isolated in its own test campaign. Whenever running standalone Google Display, Demand Gen open web, or DSP programmatic buys, enforce supply-path and verification hygiene:

- **Supply-Path Optimization (SPO):** Audit how many SSP resellers sit between the DSP and the actual publisher (`ads.txt` / `sellers.json` alignment where visible). Judge media cost on **working media rate** (effective CPM after intermediary take rates), not headline CPM, and shift spend progressively toward shorter direct or PMP paths while measuring delivered cost per business outcome.
- **Made-For-Advertising (MFA) and low-intent placement exclusions:** Screen open-exchange logs regularly and exclude MFA sites (aggressive auto-refresh, stacked ad slots, minimal editorial content), mobile gaming apps with accidental clicks, and parked domains before scaling spend.
- **Independent Verification and Invalid Traffic (IVT) Screening:** Separate General IVT (GIVT) from Sophisticated IVT (SIVT) bots, enforce recognized viewability definitions, maintain explicit brand-suitability exclusion lists rather than trusting default checkboxes, and never rely solely on a seller's or DSP's self-reported viewability/fraud scores when discrepancies arise against site analytics.

## Sources

Google Ads Help documentation (Targeting vs. Observation, Customer Match, Performance Max signals; verify current specs with URL and date); ANA / ISBA programmatic SPO and MRC verification principles.
