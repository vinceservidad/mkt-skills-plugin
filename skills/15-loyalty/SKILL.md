---
name: 15-loyalty
description: Design a loyalty program with points, tiers, perks and surprise that the margin can carry. Use for loyalty programs, rewards, points, VIP tiers, customer perks, repeat purchase incentives.
metadata:
  section: "15 Retention"
  covers: "Loyalty program"
---
# Loyalty

A loyalty program pays customers for behaviour the business already wants: buying again, staying, referring. It works when the reward is valued by the customer, its cost fits the margin, the rules are simple and honest, and the program is judged on extra repeat purchases compared with customers who aren't in it. It fails when points are copied from a big retailer, the cost is never modelled, rewards go to customers who would buy anyway with no change in behaviour, or rules hide how points expire. Surprise perks often do more than points for a small business.

Save the loyalty design as a Markdown file in `work/15-retention/` when the required inputs are present and the commercial terms are confirmed. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Order, margin and retention data in `inputs/` are the evidence; offer and segment context add what customers value.
- If present, also read `context/offer.md` → Value ladder, Price and model, Bonuses; `context/customer.md` → Segments, Voice of customer, Jobs to be done; `context/brand.md` → Voice; margin, cost, cohort, repeat-purchase and survey data in `inputs/`; any work in `work/15-retention/15-lifecycle-*.md` or `work/16-referral-community/16-referral-program-*.md`.
- **No data:** Without order, margin or retention data, ask for it (repeat rates, margin per order, how customers buy), say what each decides, and explicitly state **how to provide it** (save exports or notes in `inputs/` or paste the numbers into the conversation). Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Reward values, earn rates, tiers, perks and expiry are the owner's commitments. The design proposes options with their cost; the owner sets the numbers.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/loyalty-guide.md](references/loyalty-guide.md) for program types, the cost model, rules, perks and how to measure lift.

1. **Goal behaviour.** Name the behaviour the program should change (a second order, staying past the drop-off box, a larger order, a referral) and the evidence that it matters (cohort drops, repeat rates).
2. **Cost model.** From margin and price in `inputs/`, compute the effective cost of each proposed reward as a share of revenue and of margin, with the arithmetic shown and labelled *owner's estimate* or *calculated*. Include breakage (points never redeemed) only as an assumption.
3. **Design.** Choose the simplest program type that drives the behaviour: surprise and delight perks, a milestone reward (at the box where customers drop), points, tiers or a paid membership. Write the earn rule, the reward, eligibility and expiry in plain words.
4. **What customers value.** Use Voice of customer and survey comments to pick rewards (a perk they mention) over discounts by default.
5. **Honest rules.** Clear terms, no hidden expiry, no changes that take away earned rewards without notice. Rules are legal facts to verify for the country or mark *to confirm*.
6. **Measure lift.** Compare repeat purchase or retention of members with a holdout or matched non-members over the decision-relevant window; count reward cost against the extra margin.
7. **Approval.** The design is a draft. Launching a program, promising rewards or changing terms needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no costs, rates, margins or customer preferences that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/15-retention/15-loyalty-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Loyalty design: <business, date>
Skill: 15-loyalty · Date: <YYYY-MM-DD> · Framework: Loyalty program (behaviour, cost model, honest rules, measured lift)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing launched or promised
## The behaviour to change (evidence)
## Cost model
| Option | Earn rule | Reward | Cost as % of revenue | Cost as % of margin | Label |
| --- | --- | --- | --- | --- | --- |
## Recommended design
## Rules
## How we measure lift
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/15-retention/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the behaviour targeted, the cost of the owner's idea and the alternatives, and the recommended design, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The target behaviour is tied to evidence such as a cohort drop.
- [ ] Every reward is costed as a share of revenue and margin with the arithmetic shown.
- [ ] The simplest design that drives the behaviour is chosen; rewards come from what customers value.
- [ ] Rules are plain and honest; legal facts are dated or *to confirm*.
- [ ] Lift is measured against a holdout or matched group; nothing launches without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Reward the behaviour you need, at a cost your margin can carry, with rules a customer can read in one breath, and check that members actually buy more than they would have. Loyalty program, The Complete Marketing System, section 15 Retention (Servidad, 2026); Byron Sharp, How Brands Grow, on loyalty programs mostly rewarding existing buyers.
