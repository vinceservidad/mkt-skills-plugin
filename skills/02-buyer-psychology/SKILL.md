---
name: 02-buyer-psychology
description: Map the beliefs, objections and drivers that block the sale (Cialdini, loss aversion). Use for why people hesitate, say it is too expensive, or churn. Not for writing answers (use 08-objection-map).
metadata:
  section: "02 Customer"
  covers: "Behavioral economics (Kahneman, Ariely); Belief mapping; Buyer psychology; Cialdini's principles; Life-Force 8 (Whitman)"
---
# Buyer psychology

Decisions are made emotionally first and justified rationally after, and a sale is blocked by a belief more often than by a missing feature. This skill names the beliefs and objections that stop this buyer, from evidence, and the drivers that actually move them. That way the offer can remove the risk and the message can answer the belief, instead of applying every persuasion trick at once.

## Needs (read before writing)

- `context/customer.md`, with at least one of these present (drafted or confirmed, with content):
  - **Research log**, written by `02-customer-research`;
  - **Voice of customer**, written by `02-voc-mining`.

  Also read:
  - Pains, desires and fears;
  - Current alternatives;
  - Buying triggers and process;
  - lost-deal, churn and review evidence in `inputs/`.
- `context/customer.md` → ICP and personas (`02-icp-persona`) and Jobs to be done (`02-jobs-to-be-done`), if present. Objections differ by role, and the anxiety and habit forces feed this map.
- When both Research log and Voice of customer are missing:
  - **Raw material supplied** (call notes, lost-deal reasons, reviews or interviews): run `02-customer-research` or `02-voc-mining` on it first, then continue.
  - **Nothing supplied:** stop. Name the missing sections and those skills. Ask for lost-deal reasons, sales-call notes, cancellation reasons or critical reviews. Never list "likely objections" from imagination. End the reply with the **Principle, framework, source** block (see Output), even when you stop.

## Process

1. **Collect every hesitation in the evidence.** Sources include:
   - lost-deal reasons;
   - churn reasons;
   - questions asked on calls;
   - critical and mixed reviews;
   - "almost didn't buy because…" lines.

   Keep the source and count for each one. Every hesitation gets its own row, including confusion about what to buy or how to use it, even when it also appears as an ICP disqualifier. In a note-taker's summary, quote only the words inside the note's own quotation marks: from a note reading all "promised the same thing", quote "promised the same thing" and leave *all* outside.
2. **Classify each hesitation** with [references/belief-types.md](references/belief-types.md):
   - **Vehicle:** "this kind of solution won't work for me".
   - **Internal:** "I can't do it" or "I'll lose control".
   - **External:** "something outside stops me".
   - **Price or value, trust, risk, fit, timing.**

   When a hesitation fits both a false-belief type and a practical type (fear of losing control is internal and also a risk), record both, such as Internal / risk.
3. **Rank them.** Use frequency in the evidence × how often each one kills a deal. Separate what buyers say in public, which is often price, from what the evidence shows decided it, which is often trust, risk or category. Check deals lost on price against the ICP disqualifiers: if those buyers fall outside the ICP, say so, because the objection may be fit, not price.
4. **Name the belief that would flip it** and the proof it needs:
   - a demonstration;
   - a peer case;
   - a guarantee;
   - a sample using the buyer's own data;
   - a lighter plan.

   Do not write the answer copy. Note where each one is handled downstream:
   - risk → `07-guarantee-risk-reversal`;
   - objection-killing bonuses → `07-bonuses-urgency`;
   - answers → `08-objection-map`;
   - wrong-fit buyers → disqualify (ICP).
5. **Choose the drivers that genuinely apply.** For each driver, cite the evidence that it moves this buyer. Drivers to consider:
   - social proof, authority, reciprocity, commitment and consistency, liking, scarcity (Cialdini);
   - behavioral economics: loss aversion, anchoring (Kahneman, Ariely);
   - motivation–ability–prompt (Fogg);
   - core desires (Whitman's Life-Force 8).

   Leave the rest out. Scarcity and urgency count only when true.

## Output

Write `context/customer.md` → `## Beliefs, objections and drivers`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Beliefs, objections and drivers
Status: draft (<YYYY-MM-DD>, 02-buyer-psychology)
Written by: 02-buyer-psychology, <YYYY-MM-DD>
| Belief or objection (a plain statement without quotation marks; a verbatim quote goes in Evidence with its ID) | Type | Evidence and count | Kills deals? | Flips with | Handled in |
| --- | --- | --- | --- | --- | --- |
Drivers that apply: <driver — evidence it moves this buyer>
Drivers not to use: <driver — why (no evidence, or not true here); name the claim to avoid without quotation marks>
Core desire: <Life-Force 8 or core desire, with evidence or (assumption)>
Evidence: <files and IDs>
Method: Belief mapping (Brunson's false beliefs); Cialdini's principles; Kahneman and Ariely; Fogg Behavior Model
```

- Put quotes in quotation marks only when they are verbatim, with their source. Paraphrase without quotation marks: write the belief as a plain statement, such as This kind of service won't work for a business my size, and put the customer's own words, quoted with their ID, in the Evidence column.
- Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/customer.md` does not exist, first copy [assets/customer.md](assets/customer.md) to `context/customer.md`, then write your section into it.

Reply with:
- the two beliefs that kill the most deals;
- the next skill: `07-offer-design`, or `07-guarantee-risk-reversal` when risk tops the list.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every objection is traced to evidence with a count. None is a generic "common objection" from outside the evidence.
- [ ] Each objection is classified (vehicle, internal, external, price, trust, risk, fit or timing). What buyers say is separated from what decided the deal.
- [ ] Each high-ranked objection names the belief or proof that would flip it and the downstream section that handles it.
- [ ] Drivers are tied to evidence for this buyer. Unsupported drivers are listed under "not to use". No false scarcity or manipulation.
- [ ] No unmarked inference: any statement about buyers that the evidence does not state (a motive, a habit, a frequency word such as "often" or "most", which group an unlabelled review came from, a rate for a channel the notes don't give) carries `(assumption)` or is left out.
- [ ] Quotation marks hold only words copied exactly from a source (no added or moved words). Paraphrases, inferences, labels and suggested questions go without quotation marks (use italics for a suggested question).
- [ ] Only `## Beliefs, objections and drivers` changed. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

Decisions are emotional first and justified rationally after, and a sale is blocked by a belief more often than a feature: find the vehicle, internal and external false beliefs and the real risk, then use only the persuasion drivers the evidence shows move this buyer. Belief mapping and the Epiphany Bridge, Expert Secrets (Russell Brunson); Influence (Robert Cialdini); Thinking, Fast and Slow (Daniel Kahneman); Predictably Irrational (Dan Ariely); Fogg Behavior Model (BJ Fogg); Cashvertising's Life-Force 8 (Drew Eric Whitman).
