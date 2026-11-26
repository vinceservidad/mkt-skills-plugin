---
name: 17-unit-economics
description: Model CAC, LTV, payback, contribution margin, MER and ROAS from the business's own numbers. Use for unit economics, CAC, lifetime value, payback, break-even ROAS, can we afford to scale.
metadata:
  section: "17 Measurement"
  covers: "CAC / LTV / payback; Lead-to-revenue cohorts; MER; ROAS; Unit economics"
---
# Unit economics

Unit economics says whether each customer makes money and how fast. It works when contribution margin is built from real costs, LTV uses retention the business has observed (and says how far it extrapolates), CAC uses the source system's customer count, payback is in the business's own billing periods, and blended and channel views are kept apart. It fails when LTV is revenue times a guessed lifetime, platform ROAS is the profit test, discounts and refunds are double counted, or "profit" is used without saying which costs are in it.

Save the unit economics model as a Markdown file in `work/17-measurement/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Price and model**, from `07-pricing`: price, billing model and what a customer pays over time.
- If present, also read `context/offer.md` → Core offer, Guarantee, Value ladder; cost, fee, refund, retention and spend data in `inputs/`; source-system customer counts; any work in `work/17-measurement/17-attribution-*.md` or `work/15-retention/`.
- If a required section is missing:
  - **The upstream evidence exists** (price lists or billing exports in `inputs/`): run `07-pricing` first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Price and model → `07-pricing`), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If `07-pricing` is not loaded, stop and say: enable mkt-q2-offer.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/unit-economics-guide.md](references/unit-economics-guide.md) for contribution margin, CAC, LTV with observed retention, payback, MER, break-even ROAS and their traps, and [references/cohort-ltv-and-lead-revenue.md](references/cohort-ltv-and-lead-revenue.md) for fixed acquisition-month cohort LTV, billing-period payback discipline, and B2B lead-to-revenue cohorts with open pipeline share.

1. **Contribution margin per order.** Price minus variable costs (product, fulfilment, shipping, payment fees, refunds if not already in net revenue), with each input labelled *observed*, *owner's estimate* or *calculated*. Name the profit level (contribution margin before marketing, after marketing).
2. **Retention and LTV.** Use observed retention from cohorts; compute contribution per customer over the observed window first, then any extrapolation as a labelled scenario. Never revenue × a guessed lifetime.
3. **CAC.** Blended CAC = total marketing spend ÷ new customers from the system of record for the same period. Channel CAC uses a stated attribution view and its bias. Compute with [scripts/sum_by.py](scripts/sum_by.py).
4. **Payback.** CAC ÷ contribution per period, in billing periods; compare with observed retention: payback beyond the observed window is a risk.
5. **MER and ROAS.** MER = total revenue ÷ total marketing spend. Break-even ROAS = 1 ÷ contribution margin rate on first-order revenue (or on the LTV window chosen). Platform ROAS is a platform view, not profit.
6. **What it means.** Which channel or blended level is profitable, on which window, and what would change the answer; scaling questions go to `19-scale-paid`.
7. **Approval.** The model is a draft. Budget, price or bid changes based on it need the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no costs, margins, retention, CAC or LTV that aren't in `context/` or `inputs/` or computed from them. Do not use 'profit' without naming the level and costs included. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/17-measurement/17-unit-economics-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Unit economics: <business, period>
Skill: 17-unit-economics · Date: <YYYY-MM-DD> · Framework: Unit economics (contribution margin, CAC / LTV / payback, MER, ROAS)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's review; nothing changed
## Contribution margin per order
| Item | Value | Label | Source |
| --- | --- | --- | --- |
## Retention and LTV (observed window, then scenarios)
## CAC (blended and by channel)
## Payback
## MER and break-even ROAS
## What it means
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/17-measurement/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, contribution per order, LTV over the observed window, blended and channel CAC, payback, MER and break-even ROAS, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Contribution margin lists every variable cost with labels; the profit level is named; nothing is double counted.
- [ ] LTV uses observed retention first; extrapolation is a labelled scenario.
- [ ] CAC uses source-system customer counts; channel CAC states its attribution view.
- [ ] Payback is compared with observed retention; MER and break-even ROAS are computed; platform ROAS is not called profit.
- [ ] All arithmetic is shown; nothing changes without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Know what one customer earns you after variable costs, over the retention you have actually seen, against what it cost to win them, and never mistake a platform's ROAS for profit. Unit economics, CAC / LTV / payback, MER and ROAS, The Complete Marketing System, section 17 Measurement (Servidad, 2026).
