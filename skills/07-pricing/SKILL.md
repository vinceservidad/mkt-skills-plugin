---
name: 07-pricing
description: Set the price and pricing model from evidence, with anchoring, decoys, tiers and Van Westendorp. Use for what to charge, too cheap, free trial vs freemium. Not for page (use 13-pricing-page).
metadata:
  section: "07 Offer"
  covers: "Anchoring; Coupons / discounts / promo codes; Decoy pricing; Free trial vs freemium; Price psychology; Pricing strategy; Van Westendorp / Gabor-Granger"
---
# Pricing

Price is a signal, not just a number. It should sit well below the value the buyer perceives and above what it costs to deliver, and be anchored against the right alternative. A price is a decision made from evidence of what buyers already paid and did, kept separate from what they say they would pay, what competitors charge and what you infer. Any live change is the owner's decision, not this skill's.

## Needs (read before writing)

- `context/offer.md`, with both sections present (drafted or confirmed, with content):
  - **Core offer**, written by `07-offer-design`: what is being priced;
  - **Dream outcome**, also by `07-offer-design`: what the price is anchored to.
- If present, also read:
  - `context/customer.md` → Current alternatives (`02-customer-research`), Segments (`02-segmentation`), and Beliefs, objections and drivers;
  - `context/market.md` → Competitors and alternatives (`01-competitor-profiling`).
- Read the price evidence, if supplied: current prices, closed-deal values, lost-on-price counts, conversion by price, churn by plan, delivery cost or margin, survey results.
- Once Core offer and Dream outcome are present, missing cost, margin or volume data is not a reason to stop. Write the section anyway: mark each unknown as unknown and list the data that would change the price. A question such as "is $X the right price?" or "should we discount?" still gets the section written, with the answer in it.
- If Core offer or Dream outcome is missing:
  - **The customer sections exist:** run `07-offer-design` first, then continue.
  - **They don't exist:** stop. Name the missing sections and `07-offer-design`, plus `02-customer-research` if customer evidence is missing too. If that skill is not loaded, say: enable mkt-q1-audience. Give no price, range or benchmark figure in the reply: there is nothing to anchor it to. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Sort the evidence into four kinds.** Keep them apart in the section, using [references/pricing-guide.md](references/pricing-guide.md):
   - **Observed behaviour:** what buyers paid, closed at, churned at, upgraded to.
   - **Stated preference:** what they said they'd pay; survey answers.
   - **Competitor and alternative context:** what other options cost.
   - **Inference:** your reasoning, marked `(assumption)`.

   A competitor's price, a survey answer or a markup rule is context, not proof of the right price.
2. **Choose the pricing strategy and model** (cost-plus, value-based, competitor-based, penetration, premium; tiered, usage, subscription) that fits how the buyer gets value and how the business delivers it:
   - flat or tiered;
   - by a value metric such as size, usage or seats;
   - subscription or one-time;
   - free trial vs freemium, for products: a trial limits time and freemium limits features or usage. Choose from evidence on activation, conversion to paid and the cost of serving free users, not by default.

   Say why, with evidence.
3. **Set the price points.**
   - Anchor against the most relevant alternative the buyer already compares: a hire, a higher-priced option, the cost of the problem.
   - Show the value-to-price gap with the arithmetic from the stated figures. A ratio or comparison must hold across the whole of any range it uses.
   - Respect cost to deliver. If margin is unknown, say so.
   - Decoy pricing (an option added to shift the choice between others) and charm pricing are hypotheses to test, never proof of the best price; use them only when honest and serving the buyer's choice.
4. **Price objections.** Name each objection in your own words, with its source ID. If you quote, copy the source's words exactly, adding or dropping none. This applies to the user's message too: paraphrase what they said unless you copy it word for word. Cite a source only for what it actually says. Decide whether "too expensive" means wrong segment, unproven value or a missing anchor. Base this on the evidence, before lowering anything. Prefer packaging changes, such as a lighter plan for a segment that cannot pay, over blanket discounts.
5. **Plan the test.**
   - What would show the price is right or wrong: a metric, a time window, a stopping rule.
   - Hand experiments to `18-price-testing`.
6. **Approval.** The section is a recommendation. Say that changing live prices needs the owner's approval, and say what to check afterwards: conversion, churn and revenue per customer, against the baseline.
7. **Check before saving.** Re-read the draft against the Checks and fix any failure.

## Output

Write `context/offer.md` → `## Price and model`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Price and model
Status: draft (<YYYY-MM-DD>, 07-pricing)
Written by: 07-pricing, <YYYY-MM-DD>
Model: <model and why, with evidence>
Price points: <price per tier or plan — anchor — value gap>
Evidence by kind: observed <…> · stated <… paraphrased with source IDs; quotation marks only around words copied exactly> · competitor and alternative context <…> · inference <… (assumption)>
Price objections: <each objection in your own words, without quotation marks, with its source ID — what it really is, and the response (packaging, proof, segment), not a blanket discount>
To test: <what, metric, window, stopping rule → 18-price-testing>
Approval: recommendation only; live price changes need the owner's approval and a check of <metrics> afterwards.
Evidence: <sources>
Method: Value-based pricing; anchoring and price psychology (Kahneman, Ariely); <Van Westendorp or Gabor-Granger if used>
```

Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/offer.md` does not exist, first copy [assets/offer.md](assets/offer.md) to `context/offer.md`, then write your section.

Reply with:
- the recommended price and model in one line;
- the evidence that would change it;
- a reminder that live changes need approval;
- the next skill: `07-guarantee-risk-reversal` or `07-value-ladder`.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Observed behaviour, stated preference, competitor context and inference are kept apart. No competitor price, survey answer or markup rule is treated as proof.
- [ ] The price is anchored to a named alternative or to the cost of the problem, with evidence.
- [ ] Price objections are diagnosed (segment, value proof, anchor) before any discount is proposed. No blanket discount is the default.
- [ ] Margin or cost to deliver is used if known, or stated as unknown.
- [ ] The section was written, even if the user only asked a question or cost data is missing.
- [ ] A test with a metric and a stopping rule is named, and live changes are left to the owner's approval.
- [ ] No unmarked inference. Quotation marks hold only words copied exactly from a source.
- [ ] Only `## Price and model` changed. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

Price is a signal, set from what buyers already pay and do, well below the value they perceive and anchored against their real alternative, and changed only by a tested, approved decision. Value-based pricing and price psychology: anchoring (Kahneman, Thinking, Fast and Slow; Ariely, Predictably Irrational); $100M Offers (Alex Hormozi); The Complete Marketing System, section 7 Offer (Servidad, 2026).
