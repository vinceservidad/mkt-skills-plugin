---
name: 07-guarantee-risk-reversal
description: Design a guarantee or risk reversal that answers the buyer's top fear and fits the economics. Use for money-back terms, what if it fails. Not for refund policy pages, legal terms or bonuses.
metadata:
  section: "07 Offer"
  covers: "Guarantee / risk reversal"
---
# Guarantee and risk reversal

Every risk you remove is a sale you didn't lose. A good guarantee answers the specific fear that stops this buyer, which is often not "I want my money back". It shifts that risk to the seller, and it costs less than the sales it wins. This skill designs that guarantee and states its exposure honestly.

## Needs (read before writing)

- `context/offer.md` → **Core offer**, written by `07-offer-design`. It must be present (drafted or confirmed, with content): it defines what is guaranteed.
- `context/customer.md` → **Beliefs, objections and drivers**, written by `02-buyer-psychology`. It must be present: it holds the risk the guarantee must answer.
- If present, also read:
  - `context/offer.md` → Price and model (`07-pricing`), for the cost exposure;
  - Dream outcome;
  - delivery data in `inputs/`: on-time rates, refund history, results.
- If a required section is missing:
  - **Upstream evidence exists:** for example, customer evidence but no objection map. Run the missing skill first (`02-buyer-psychology` or `07-offer-design`), then continue. If `02-buyer-psychology` is not loaded, stop and say: enable mkt-q1-audience.
  - **It doesn't:** stop. Name the missing sections and the skills that fill them. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Find the risk to reverse.** From Beliefs, objections and drivers, pick the fear that most often stops or delays the sale, with evidence: a late delivery, no results, losing control, wasting money. The guarantee answers that fear in the buyer's terms. State the fear in your own words, without quotation marks, and cite its source ID. Quote only words copied exactly from the source, with the ID.
2. **Choose the type,** using [references/guarantee-types.md](references/guarantee-types.md):
   - **Unconditional:** money back, no questions.
   - **Conditional:** money back if X, provided the buyer did Y.
   - **Service:** if we miss Z, you get W.
   - **Results-based** or **better-than-money-back.**
   - **Anti-guarantee:** "all sales final", with a stated reason.

   Match the type to what the business can control and measure.
3. **Write the terms plainly.** Cover:
   - what is promised;
   - the time limit;
   - what the buyer must do;
   - what they get if it's missed;
   - how to claim.

   No hidden conditions.
4. **Cost the exposure.** Estimate the worst-case cost per customer and the likely claim rate, using delivery or refund data if supplied. Always give a claim-rate figure: from the data, or a stated estimate marked `(assumption)`; never leave the rate as unknown. Only the volume (how many clients or sales) may be unknown. State cost per customer or per client-month; give an annual or total figure only when the number of clients or sales comes from an input, naming it. Never pick a client count yourself: cumulative figures such as agencies served since a year are not the current client base. If it is unknown, write `unknown, ask <owner>` for the total. Compare that with the sales the guarantee could win. If the business can't absorb the worst case, tighten the condition or choose a service guarantee.
5. **Name it and state it in one line.** For example: *Five-day close or the month is free.* Write it as a proposal, without quotation marks. The same goes for any wording you consider or reject, such as a taste-only promise: describe it in plain text, never in quotation marks.
6. **Approval.** A guarantee is a commercial and legal commitment. Say that the owner approves the wording before it is published, and that local consumer law applies.
7. **Check before saving.** Re-read the draft against the Checks and fix any failure.

## Output

Write `context/offer.md` → `## Guarantee`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Guarantee
Status: draft (<YYYY-MM-DD>, 07-guarantee-risk-reversal)
Written by: 07-guarantee-risk-reversal, <YYYY-MM-DD>
Risk it reverses: <fear, paraphrased without quotation marks — source IDs and count>
Type: <type and why it fits what the business controls>
Terms: <promise · time limit · what the buyer does · what they get · how to claim>
One-line version: <proposal>
Exposure: worst case <…> per customer; likely claim rate <a figure, with its source or `(assumption)`>; annual total only with a sourced client count, otherwise `unknown, ask <owner>`; worth it because <…>
Approval: owner approves the wording before publishing; check local consumer law.
Evidence: <sources>
Method: Risk reversal (Jay Abraham); guarantees, $100M Offers (Hormozi)
```

Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/offer.md` does not exist, first copy [assets/offer.md](assets/offer.md) to `context/offer.md`, then write your section.

Reply with:
- the guarantee in one line;
- its worst-case cost;
- the next skill: `07-bonuses-urgency`.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The guarantee answers the buyer's top evidenced risk, not a generic refund.
- [ ] The terms are complete and plain: the promise, time limit, buyer's part, remedy and how to claim. No hidden conditions.
- [ ] The business can control and measure what it promises.
- [ ] The worst-case exposure is estimated, with data or `(assumption)`, no client count or volume that no input supplies, and weighed against what the guarantee wins.
- [ ] The owner's approval and consumer law are flagged before publishing.
- [ ] No unmarked inference. Quotation marks hold only words copied exactly from a source, never proposed, considered or rejected guarantee wording.
- [ ] Only `## Guarantee` changed. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

Every risk you remove is a sale you didn't lose: shift the buyer's biggest evidenced fear onto the seller, on terms the business controls and can afford. Risk reversal (Jay Abraham, Getting Everything You Can Out of All You've Got); guarantees in $100M Offers (Alex Hormozi); The Complete Marketing System, section 7 Offer (Servidad, 2026).
