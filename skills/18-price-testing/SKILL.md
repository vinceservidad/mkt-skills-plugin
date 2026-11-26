---
name: 18-price-testing
description: Test price by cohort, region or offer variant without breaking trust or the law. Use for price testing, testing a price increase, willingness to pay tests, pricing experiments, discount tests.
metadata:
  section: "18 Experimentation"
  covers: "Price testing"
---
# Price testing

A price test measures how buyers respond to a different price or offer, so a pricing decision rests on behaviour rather than opinion. It works when the test compares new buyers in separate cohorts, periods, regions or clearly different offers, measures revenue and margin per visitor plus retention (not just conversion), protects existing customers, and is fair and legal. It fails when two people see different prices for the same thing at the same time without reason, the test is judged on conversion alone, existing subscribers are surprised, or one short test is treated as the permanent price.

Save the price test design as a Markdown file in `work/18-experimentation/` when the required inputs are present and the owner has stated the test prices or confirmed any new discount terms. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Price and model**, from `07-pricing`: the current price, model and what has been tested.
- If present, also read `context/offer.md` → Core offer, Value ladder, Guarantee; `context/customer.md` → Beliefs, objections and drivers, Segments; traffic, conversion, margin, retention and past price changes in `inputs/`; any work in `work/18-experimentation/18-ab-testing-*.md` or `work/17-measurement/17-unit-economics-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (price lists, billing or sales notes in `inputs/`): run `07-pricing` first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Price and model → `07-pricing`), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Every price, discount and offer tested is the owner's commitment. When the owner gives test prices for a full price-test design (with traffic and baseline data present), draft the design file with `Arms (owner to set)` marked pending approval. When asked to add or build a discount, concession or new offer arm not in `context/offer.md` without confirmed terms (amount, end date, eligibility) and margin/cost basis, stop and write no deliverable file: ask the owner to confirm the discount's terms and margin cost first, design no arm on assumed terms, note the arm must be judged on contribution margin and retention per visitor, and end with the **Principle, framework, source** block.
- If `07-pricing` is not loaded, stop and say: enable mkt-q2-offer.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/price-testing-guide.md](references/price-testing-guide.md) for test designs, fairness and legal checks, metrics, sample size and protecting existing customers.

1. **The decision.** The pricing question (raise, lower, restructure, discount) and what would change it, from `offer.md` and unit economics.
2. **Design that stays fair.** Prefer new-buyer cohorts over time, regions, or clearly different offers (different bundle, term or tier) over showing different prices for the identical item to people at the same time. If a simultaneous split is used, say why, how it is disclosed and how buyers are treated fairly (for example honoring the lower price on request). Pricing and consumer-protection rules are legal facts to verify with URL and access date or mark *to confirm*.
3. **Protect existing customers.** Existing subscribers keep their terms unless the owner decides a change with notice; the test is for new buyers.
4. **Metrics.** Revenue and contribution margin per visitor, conversion, and retention or refunds over the window that matters; computed with [scripts/sum_by.py](scripts/sum_by.py). Conversion alone is not the decision.
5. **Size and duration.** Use the sample-size method in `18-ab-testing`; price tests often need long windows to see retention. If traffic can't decide it, use a sequential cohort test or a survey-based estimate labelled as stated preference.
6. **Read.** Observed behaviour, stated preference and inference kept separate; the result applies to the period, audience and offer tested.
7. **Approval.** The design is a draft. Showing any test price or changing live prices needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no prices, elasticities, results or margins that aren't in `context/` or `inputs/` or computed from them. No competitor price or framework default is proof of the right price. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/18-experimentation/18-price-testing-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Price test design: <offer, date>
Skill: 18-price-testing · Date: <YYYY-MM-DD> · Framework: Price testing (cohort, region or offer variant)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; no price shown or changed
## The decision
## Design and fairness
## Existing customers
## Arms (owner to set)
| Arm | Price or offer | Who sees it | When |
| --- | --- | --- | --- |
## Metrics and guardrails
## Size and duration
## Legal checks
## How to read it
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/18-experimentation/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the design and why it is fair, the metrics, the duration, and how existing customers are protected, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The design avoids unexplained simultaneous price differences for the identical item; fairness and legal facts are dated or *to confirm*.
- [ ] Existing customers keep their terms unless the owner decides a change with notice.
- [ ] Metrics include revenue and margin per visitor and retention, not conversion alone.
- [ ] Size and duration are estimated; observed behaviour and stated preference are separated.
- [ ] Prices are the owner's; nothing is shown or changed without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Test price on new buyers in a way you would be comfortable explaining, judge it on margin and retention per visitor, and keep existing customers' trust intact. Price testing, The Complete Marketing System, section 18 Experimentation (Servidad, 2026); Monetizing Innovation (Madhavan Ramanujam and Georg Tacke).
