# Cohort LTV, Payback Discipline and B2B Lead-to-Revenue Cohorts

Use alongside [unit-economics-guide.md](unit-economics-guide.md) when computing LTV from observed retention, checking cash payback risk before scaling, or evaluating long-sales-cycle lead generation channels (LinkedIn, outbound, organic search) where closed revenue lags ad spend by weeks or quarters.

## 1. Cohort retention and observed contribution LTV

1. **Group customers by first-purchase / activation month** from the billing system or store ledger, keeping fixed acquisition cohorts untouched over time rather than blending new and old buyers into monthly averages.
2. **Track surviving paying customers and net contribution per period** (`price - COGS - fulfilment - shipping - fees - refunds` per order * realized orders per starting customer in month `0, 1, 2...`).
3. **Separate observed LTV from extrapolated LTV:** Report cumulative contribution over the **actually observed retention window** first (e.g., 4-month observed contribution LTV). Any extension past observed cohort history (assuming month-6 churn holds to month 24) must be labeled an *extrapolated scenario*, never presented as realized LTV.
4. **Compare cohorts by acquisition channel and offer:** Discounted or aggressive trial cohorts frequently retain worse than full-price cohorts; evaluate channel CAC against that channel's own cohort retention (`15-churn-prevention`).

## 2. Payback period discipline

Compute payback in the business's **actual billing periods** (`channel or blended CAC / cumulative net contribution per period`):
- Flag any channel whose payback period extends beyond the **observed retention window** or strains working capital before scaling spend (`19-scale-paid`).
- Never compute payback against gross revenue instead of post-fulfilment contribution margin; doing so hides variable delivery costs and overstates allowable CPA.

## 3. B2B Lead-to-Revenue cohorts (long sales cycles)

Standard ecommerce payback breaks on B2B lead generation when closing a deal takes 30 to 180+ days:
1. **Cohort strictly by lead-creation date:** Never cohort by opportunity-creation or close date (survivorship bias hides dead leads created in the same month).
2. **Keep every stage and the open share visible:** Track `created leads -> MQL -> SQL -> opportunity -> closed-won -> closed-lost -> open share %` side by side (`scripts/sum_by.py` from CRM exports). Never treat an open pipeline lead as won or lost.
3. **Judge maturity before killing a channel:** Recent cohorts appear weaker simply because open pipeline has not closed yet. State the *open share %* alongside interim cost per SQL and revenue per lead, and define a maturity threshold (e.g., open share < `15%` or full typical cycle elapsed) before cutting or scaling slow-cycle channels like LinkedIn (`11-paid-social`) or ABM (`14-prospecting`).
4. **Separate velocity from revenue lag:** One channel can advance prospects to discovery calls faster while another closes larger retainers slower; reconcile pipeline speed separately from realized cash (`19-scale-paid` checks conversion-lag readiness before budget jumps).

## Sources

The Complete Marketing System, section 17 Measurement (Servidad, 2026); cohort accounting and B2B CRM pipeline economics principles.
