---
name: 07-offer-design
description: Design or rebuild the core offer with the Value Equation and Grand Slam Offer. Use for packaging, deliverables, what should I sell, or leads not buying. Not for price or bonuses (use 07-pricing).
metadata:
  section: "07 Offer"
  covers: "Best-prospect offer test; Bundles; Dream outcome; Grand Slam Offer; Irresistible Offer (Joyner); MAGIC naming; Offer stack; Reason to Buy; Value Equation"
---
# Offer design

People buy when the perceived value is clearly greater than the price. Sell the destination, not the vehicle: nobody wants the modules; they want what happens after. This skill builds the core offer from the customer's own problems and outcomes, and scores it with the Value Equation. Pricing, the guarantee, bonuses, urgency and the ladder each have their own skill and build on it.

## Needs (read before writing)

- `context/customer.md`, with at least one of these present (drafted or confirmed, with content):
  - **Pains, desires and fears**, written by `02-customer-research`;
  - **Voice of customer**, written by `02-voc-mining`.
- If present, also read:
  - from `context/customer.md`: Beliefs, objections and drivers (`02-buyer-psychology`); Current alternatives (`02-customer-research`); Jobs to be done; ICP and personas;
  - `context/positioning.md` → Unique mechanism (`06-unique-mechanism`).
- Read what the business delivers today (the user's message, `inputs/`, an existing `context/offer.md`). The offer is built from what the business can actually deliver.
- If both Pains, desires and fears and Voice of customer are missing:
  - **Raw customer evidence supplied** (interview notes, reviews, call notes): run `02-customer-research` or `02-voc-mining` first, then continue. If that skill is not loaded, stop and say: enable mkt-q1-audience.
  - **Nothing supplied:** stop. Name the missing sections and those skills, and ask for customer evidence. If they are not loaded, say: enable mkt-q1-audience. Do not design an offer around imagined pains. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Dream outcome.** State the result the buyer wants in their terms, from the evidence. It is the destination, not the deliverables.
2. **List every problem on the way.** Draw them from pains, objections, alternatives and the jobs: before, during and after the purchase. Include the problems that stop people from starting, such as effort, setup and trust.
   - Give every belief, objection and risk in `customer.md` → Beliefs, objections and drivers its own problem row, with its source ID. That includes a belief that the business is the wrong kind of provider and a risk about the start, such as a late first delivery. Do not fold an objection into a pain row.
   - If that section says an objection should not be acted on (for example a buyer to disqualify), leave it out and say why in the trim notes.
3. **Write a solution and a delivery vehicle for each problem.** The vehicle is how it is delivered: done for you, done with you, a tool, a call, a template. Use only what the business can deliver; mark new deliverables as proposals.
4. **Trim and stack.** Keep the solutions that are high in value to the buyer and low in cost to deliver. Move the rest to bonuses (for `07-bonuses-urgency`) or drop them. See [references/value-equation.md](references/value-equation.md).
   - **Offer stack:** itemise every component, state its value to the buyer with reasoning, and anchor the total against the price. An invented "worth $X" or a was-price never charged is not evidence; mark estimates `(assumption)`.
   - **Bundles:** package components together only when the evidence shows buyers want them together; say what the bundle replaces and keep each component's value visible.
5. **Score the Value Equation.** Value = (dream outcome × perceived likelihood) ÷ (time delay × effort and sacrifice). For each term:
   - say what raises or lowers it in this offer, with evidence;
   - name the change that would improve it most.

   Then run the **Best-prospect offer test**: would your 100 best prospects say yes without a sales call? Answer from evidence (past closes, reviews, call notes); with none, write unknown and the evidence that would answer it, never a guessed yes.
6. **Name it.** Write a name and a one-liner using MAGIC: magnet, avatar, goal, interval, container. Label the name as a proposal until it is tested. Add the **Reason to Buy**: one line on why this buyer should choose this offer, from their evidence. It is a different job from the reason to believe (proof, owned by `08-proof-stack`).
7. **Check before saving.** Re-read the draft against the Checks and fix any failure.

## Output

Write these sections of `context/offer.md`, replacing each body and leaving every other section exactly as it was:

- `## Dream outcome`: one or two sentences, with evidence.
- `## Core offer`: a table with columns Problem on the way, Solution, Delivery vehicle, and Status (exists / proposed). Add trim notes beneath it.
- `## Value equation`: four terms, each with its rating, evidence and the improvement that matters most.
- `## Name and one-liner`: the name (proposal) and the one-liner.

Format each section the same way:
- It starts with `Status: draft (<YYYY-MM-DD>, 07-offer-design)`, then `Written by: 07-offer-design, <YYYY-MM-DD>`.
- It ends with `Evidence:` and `Method: Value Equation; Grand Slam Offer, $100M Offers (Hormozi)`. Evidence names every source, including any other context file a timing or claim was taken from (for example `context/message.md`).
- Mark anything not traced to a source `(assumption)`.
- Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/offer.md` does not exist, first copy [assets/offer.md](assets/offer.md) to `context/offer.md`, then write your sections.

Leave price, guarantee, bonuses, urgency and the ladder to their own skills. Do not write those sections.

Reply with:
- the offer in one line;
- the weakest Value Equation term;
- the next skill: `07-pricing`, then `07-guarantee-risk-reversal`.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The dream outcome is stated as a result, not as deliverables, in the buyer's terms with evidence.
- [ ] Every belief, objection and risk in Beliefs, objections and drivers has its own problem row with its ID, or a trim note saying why it was left out.
- [ ] Every problem has a solution and a delivery vehicle. Each deliverable is marked as existing or proposed, and nothing is presented as existing that the business has not said it delivers.
- [ ] Each Value Equation term is rated with evidence and has its improvement.
- [ ] Price, guarantee, bonuses, urgency and the ladder are left to their skills.
- [ ] Quotation marks hold only words copied exactly from a source. The name, the one-liner and proposed copy are written without them.
- [ ] No unmarked inference: results, timings or costs the evidence doesn't give are marked `(assumption)`.
- [ ] Only the four owned sections changed. Each has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

Make what they get worth clearly more than what they give up: sell the destination, not the vehicle, and raise perceived likelihood while cutting time delay and effort. Value Equation and Grand Slam Offer, $100M Offers (Alex Hormozi); the Irresistible Offer (Mark Joyner); The Complete Marketing System, section 7 Offer (Servidad, 2026).
