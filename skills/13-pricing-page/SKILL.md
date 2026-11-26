---
name: 13-pricing-page
description: Design the pricing page with plans, anchors, comparison and risk reversal. Use for pricing page layout, show prices vs contact us, plan table, recommended tier. Not for setting prices (07-pricing).
metadata:
  section: "13 Conversion"
  covers: "Pricing page design"
---
# Pricing page

A pricing page turns a price that is already decided into a choice the buyer can make with confidence. It shows the plans or bands clearly, anchors them against the right alternative, says what each includes, removes the risk, answers the price objections, and gives one next step. It publishes nothing the owner hasn't decided: no new tiers, decoys, discounts, annual deals or guarantees. Pricing decisions belong to `07-pricing`; this skill presents them, and changes nothing live.

Save the design as a Markdown file in `work/13-conversion/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Price and model**, from `07-pricing`.

A section counts only when its `Status:` line says drafted or confirmed and it has content under it. A file that exists with `Status: empty` (the installer's template) is missing. Check this first, before asking for page or other material: a missing upstream section is a stop, not a baseline.

If present, also read:
- `context/offer.md` → **Guarantee**, from `07-guarantee-risk-reversal`; Core offer (what each plan includes, and what is only proposed); Bonuses; Urgency and scarcity; Value ladder;
- `context/message.md` → Objection map, Proof stack; `context/customer.md` → Beliefs, objections and drivers, Segments;
- the current pricing page and any numbers for it, in `inputs/` or pasted.

If something is missing:
- **Price and model missing:** stop. Name Price and model → `07-pricing` and say what to bring (the prices and model the owner has set). Price and guarantee are the owner's commitments: never generate them yourself. A stop reply still ends with the **Principle, framework, source** block.
- **Guarantee missing or not approved:** design the page without one and list it under Open questions with `07-guarantee-risk-reversal`.
- If `07-pricing` is not loaded, stop and say: enable mkt-q2-offer.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/pricing-page-anatomy.md](references/pricing-page-anatomy.md) for the sections, anchoring and decoy rules, and what may be published.

1. **Sort what may be published.** From Price and model and the rest of `offer.md`, list each price, plan, term, inclusion, guarantee and incentive as *decided* (drafted or confirmed with a source), *assumption or proposed* (marked so in `offer.md`), or *not decided*. Only decided items go on the page; the rest go under Open questions. Say that drafted prices are recommendations until the owner confirms them.
2. **Decide what the page must do.** Let the buyer choose a plan and buy, or choose a band and book a call. Showing prices versus *contact us* is the owner's decision: give the evidence for each (price questions, lost-on-price counts, how the price is set before a call) and recommend.
3. **Lay out the plans:** order, the value metric in the buyer's words (why the price differs: revenue band, bags, seats), what each includes from the Core offer, and a recommended plan only if evidence shows which one fits most buyers. No new tier, no decoy that the business would not sell honestly.
4. **Anchor honestly:** against the alternative named in Price and model (a hire, a higher-priced option, the cost of the problem), with sourced figures only. No invented "was" prices or competitor prices.
5. **Comparison and inclusions:** a short table of what each plan includes, with proposed items left out.
6. **Risk reversal:** the guarantee exactly as `offer.md` states it and with its status, marked *owner to approve wording before publishing* unless confirmed; cancellation and renewal terms that exist today. Proposed clauses (for example an automatic refund rule not yet built) are held.
7. **FAQ:** the price and risk objections from the Objection map or Beliefs, answered only with what is true now.
8. **Next step:** one call to action per plan, and what happens after it.
9. **Urgency:** only what Urgency and scarcity says is true (a real capacity limit, stated plainly). No countdowns, no invented demand.
10. **Measure:** primary outcome (paid orders or qualified calls from the page, by plan), guardrails (refunds, wrong-band calls, support questions about price), each change as a test with a window and stopping rule. Hand price experiments to `18-price-testing`, page copy to `10-page-copy`, trust elements to `13-trust-signals`.
11. **Authorization.** Publishing prices, terms or a guarantee needs the owner's approval and a check afterwards against the baseline.
12. **Check before saving.** Re-read the draft against the Checks, run `scripts/check_quotes.py`, and fix any failure.

**Nothing the context doesn't support.** Write no prices, discounts, annual deals, tiers, inclusions, guarantee terms, deadlines or customer numbers that aren't decided in `context/` or `inputs/`. Anything marked `(assumption)` or proposed in `offer.md` stays off the page. Show the whole price the buyer pays (shipping, fees, the condition on any free-shipping or free-trial claim).

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from a source, with the source named. Your plan names, headlines and FAQ answers go in italics. Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py <file>`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches.

## Output

Write `work/13-conversion/13-pricing-page-<YYYY-MM-DD>-pricing-page.md`:

```markdown
# Pricing page: <business> (<date>)
Skill: 13-pricing-page · Framework: Pricing page anatomy; anchoring and honest decoys (Kahneman, Ariely)
Built from: <context sections and inputs used, with status>
## What may be published
| Item | Status (decided / assumption or proposed / not decided) | Source |
| --- | --- | --- |
## What the page must do (and show prices or not)
## Page, section by section
<headline direction, plans, anchor, inclusions table, risk reversal, FAQ, next step>
## Plans
| Plan or band | Price (exactly as set) | For whom | Includes | Call to action |
| --- | --- | --- | --- | --- |
## Metrics and tests (owner approval needed to publish)
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/` and nothing live.

Reply with the file path, the main layout decision, every item held back for the owner (prices still in draft, a guarantee to approve, assumptions), and a reminder that publishing needs the owner's approval.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every price, plan, term and inclusion on the page is copied exactly from `offer.md` and marked decided; assumptions and proposed items are held under Open questions.
- [ ] No new tier, decoy, discount, annual deal, "was" price or competitor price is invented; the anchor uses a sourced alternative.
- [ ] The guarantee appears only as `offer.md` states it, with its approval status, and proposed clauses are held.
- [ ] The whole price is shown, with the condition on any free-shipping or free-trial claim.
- [ ] Objections in the FAQ come from context and are answered only with what is true now; urgency is true or absent.
- [ ] One next step per plan; tests have metric, guardrails, window and stopping rule; publishing needs the owner's approval.
- [ ] Every test is written out on its own: metric, guardrails, window and stopping rule (when to stop early or call it), none blank or deferred to another test.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

A pricing page presents decided prices so the buyer can choose with confidence: anchor against the real alternative, show the whole price, remove the risk with terms that exist, and publish nothing the owner hasn't decided. Anchoring and decoy effects (Kahneman, Thinking, Fast and Slow; Ariely, Predictably Irrational); $100M Offers (Alex Hormozi); The Complete Marketing System, section 13 Conversion (Servidad, 2026).
