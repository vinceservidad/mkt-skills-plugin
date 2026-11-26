---
name: 12-upsell-path
description: Design order bumps, upsells, downsells and cross-sells from the value ladder, presented honestly, with take rates. Use for order bumps, one-click upsells, average order value or post-purchase offers.
metadata:
  section: "12 Funnel"
  covers: "Order bump / upsell / downsell"
---
# Upsell path

The best moment to offer the next step is right after someone decides to buy. An order bump, upsell or downsell raises order value only if it is the logical next step for this buyer, comes from the value ladder, and is presented honestly. A pre-checked box or a guilt-trip button buys revenue with trust and refunds.

Save the requested plan or asset as a Markdown file in `work/12-funnel/` (file name under Output) when the required inputs are present. Creating this deliverable is part of the task, including requests worded as planning or design. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Value ladder**, from `07-value-ladder` (plugin mkt-q2-offer).
- If present, also read `context/offer.md` → Core offer, and Price and model; `context/customer.md` → Segments and Beliefs, objections and drivers; any average order value or take-rate data in `inputs/`.
- If a required section is missing:
  - **The upstream evidence exists:** run the skill that fills it first, then continue. If that skill is not loaded, stop and say: enable mkt-q2-offer. Price and guarantee are the owner's commitments: never generate them yourself; stop and ask, or offer the owning skill's proposal for approval.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Value ladder → `07-value-ladder`, in mkt-q2-offer), the plugin to enable if that skill is not loaded,, and what the user should bring. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Find the next logical step** after each purchase on the value ladder: what problem does buying create or reveal? That is the upsell. Use only offers that exist or that the ladder marks proposed (and label them).
2. **Place each offer,** using [references/upsells.md](references/upsells.md):
   - **Order bump:** small, related, at checkout.
   - **One-click upsell:** after purchase, bigger, the next problem.
   - **Downsell:** a lighter version if the upsell is declined.
   - **Cross-sell:** related, in onboarding.
3. **Present them honestly:** unchecked boxes, plain decline options (no confirmshaming), clear total prices, and easy refunds as the policy allows.
4. **Price from `offer.md`** or mark prices "not set → 07-pricing". Never invent prices.
5. **Set the metrics:** take rate per offer, average order value, and refund rate, with baselines or "unknown".
6. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features, platform capabilities or delivery terms that aren't in `context/` or `inputs/`. Mark inferences `(assumption)`, and list what is needed under Open questions. Describe each source only as it reads: no outcome, motive or behaviour the source doesn't state. In the founder's or brand's voice, add no habits, promises or operational details (who reads replies, what a call covers) that context doesn't contain.

## Output

Write `work/12-funnel/12-upsell-path-<YYYY-MM-DD>.md`, adding `-<slug>` after the date when more than one is written the same day:

```markdown
# Upsell path: <what it is for>
Skill: 12-upsell-path · Date: <YYYY-MM-DD> · Framework: <name>
Built from: <context sections used, with their status>
## Offers
| After | Type | Offer (exists or proposed) | Why it's the next step | Price (or not set) | Metric |
| --- | --- | --- | --- | --- | --- |
## Presentation rules
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. This is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a review, an interview, a testimonial in the proof stack), with the source named. Write your own lines, proposals and copy in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py <file>`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the key decision, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Each offer is the logical next step after the purchase and comes from the value ladder (proposed ones labelled).
- [ ] Prices come from `offer.md` or are marked not set. None is invented.
- [ ] Presentation is honest: no pre-checked boxes, confirmshaming or hidden totals.
- [ ] Take rate, order value and refunds are measured, with baselines or unknown.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Offer the next logical step at the moment of decision, from the value ladder, presented honestly: the order value it adds is worth less than the trust a dark pattern costs. Order bumps, upsells and downsells, DotCom Secrets (Russell Brunson); Customer Value Optimization (DigitalMarketer); The Complete Marketing System, section 12 Funnel (Servidad, 2026).
