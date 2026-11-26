---
name: 15-churn-prevention
description: Diagnose churn and design save, pause and dunning flows. Use for churn analysis, cancellations, failed payments, exit surveys, save offers, customer success. Not for PMF (use 04-pmf-check).
metadata:
  section: "15 Retention"
  covers: "Churn analysis; Churn reason coding & save verification; Customer success; Dunning / failed-payment recovery; Exit surveys / save offers"
---
# Churn prevention

Churn falls when the reason customers leave is fixed. Diagnosis comes first: voluntary cancellation, involuntary loss from failed payments, quiet lapse, and active risk are different problems with different fixes. It works when the exit reasons are counted, failed payments are recovered with notice and retries, customers who need a break can pause, save offers match a diagnosed reason, and the result is checked over the months that matter. It fails when cancellation is hidden or made hard, a discount is the default answer, consent or suppression is overridden, or a delayed cancellation is counted as a save.

Save the churn plan as a Markdown file in `work/15-retention/` when the required inputs are present (unless withholding under Owner commitments). Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. If present, cohort, cancellation, exit-reason and failed-payment data in `inputs/` are the evidence; customer and offer context add the why.
- If present, read **every** file in `inputs/` (billing exports, cohorts, cancellations, exit answers, failed payments, cost/margin/retention notes, tickets, support notes) before marking costs, margins or dunning status unknown, plus `context/customer.md` → Jobs to be done, Pains, desires and fears, Voice of customer, ICP and personas; `context/offer.md` → Price and model, Core offer, Guarantee; and any work in `work/15-retention/15-onboarding-*.md` or `15-lifecycle-*.md`.
- **No data:** Without cohort, cancellation or exit-reason data, ask for it (billing export, cancel reasons, failed-payment counts) and say what each would show and how to provide it (drop files in `inputs/` or paste into chat). Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Save offers, discounts, free months and credits are the owner's commitments; use only offers in `offer.md`.
  - If the request asks solely to build a save flow around an unconfirmed offer (e.g. give everyone a free month automatically) rather than a full churn diagnosis and plan, **stop and withhold all deliverable files** (write nothing to `work/15-retention/`): compute margin cost from `inputs/` / `offer.md`, ask the owner to confirm exact terms, explain why a blanket offer misses non-price causes, keep cancellation easy, and end with **Principle, framework, source**.
  - If the request asks for a full churn plan from `inputs/`, even while proposing an unconfirmed discount or moving cancellation to support email: **refuse cancellation obstruction** (date rules or mark *to confirm*; keep cancel one step) and mark any discount not in `offer.md` *owner to set* (not the default), and **write the complete churn plan file** (`work/15-retention/15-churn-prevention-<YYYY-MM-DD>-<slug>.md`). Address **involuntary churn first** (including both recovered and auto-cancelled failed charges), label exit-survey answers as **self-reported** with respondents vs total cancellations, map **every counted exit reason** (including taste and travel -> pause/skip) to an honest response, and specify a **decision-relevant verification window** (e.g. later boxes) against a comparison group.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/churn-guide.md](references/churn-guide.md) for churn types, the diagnosis, dunning, pause and save design, and what is never allowed, and [references/retention-reason-coding-and-saves.md](references/retention-reason-coding-and-saves.md) for structured churn reason coding, reason-matched honest save flows, verification windows, and targeted win-back.

1. **Measure churn by type.** From `inputs/`, compute retention by cohort and churn by type (voluntary, involuntary from failed payments, lapse) with [scripts/sum_by.py](scripts/sum_by.py) or [scripts/tally.py](scripts/tally.py), each figure labelled. State the denominator and the window.
2. **Churn analysis.** Count exit reasons and ticket groups; note how many customers answered and that answers are self-reported. Separate fit (wrong customers), product or service failure, operations, price-value, and life events. Each reason gets its owner.
3. **Involuntary churn first.** Dunning / failed-payment recovery: notice before a card expires, an email or text when a payment fails (with consent for SMS), several retries spaced over days, an easy card update, and a grace period. Count what is lost today.
4. **Exit surveys / save offers.** A short required or optional reason question on the cancel flow; for each reason, the honest response: a pause or skip for too much stock or travel, a cadence change, a fix for delivery, a fitting cheaper option if the offer has one. A discount only where price is the diagnosed reason and the owner sets it. Cancellation stays easy and one step.
5. **Customer success.** For B2B or high-value accounts: who watches risk signals (usage drops, missed reviews, complaints) and what they do.
6. **Verify saves.** A save counts only if the customer is still active and paying after the decision-relevant window (for example two more boxes), compared with similar customers who weren't offered it.
7. **Approval.** The plan is a draft. Changing the cancel flow, payment retries, messages or offers needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no churn rates, reasons, results or offers that aren't in `context/` or `inputs/`. Never propose hiding, delaying or obstructing cancellation, or contacting customers against their consent or suppression. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/15-retention/15-churn-prevention-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Churn plan: <business, period>
Skill: 15-churn-prevention · Date: <YYYY-MM-DD> · Framework: Churn analysis, dunning, exit surveys and honest save offers
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing changed
## Churn by type
| Type | Count | Denominator and window | Label |
| --- | --- | --- | --- |
## Why customers leave
| Reason | Count (source) | Cause | Owner |
| --- | --- | --- | --- |
## Failed-payment recovery
## Cancel flow: reason, pause and save
## Customer success (if B2B or high value)
## How saves are verified
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/15-retention/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, churn by type with counts, the top reasons, the dunning fix, and the cancel-flow design, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Churn is split by type with denominators and windows; exit answers are labelled self-reported with the response count.
- [ ] Each reason has a cause and an owner; fit, product, operations and price are separated.
- [ ] Failed-payment recovery has notice, retries, an easy update and a grace period.
- [ ] Cancellation stays easy; no hidden button, forced call or obstruction; save offers match a diagnosed reason; discounts are *owner to set*.
- [ ] Saves are verified over the decision-relevant window against a comparison; nothing changes without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Diagnose why customers leave before you try to keep them: recover failed payments, let people pause, fix the real reason, keep cancelling easy, and count a save only when the customer stays. Churn analysis, Dunning / failed-payment recovery and Exit surveys / save offers, The Complete Marketing System, section 15 Retention (Servidad, 2026); FTC guidance on negative option and click-to-cancel practices (to verify for current status).
