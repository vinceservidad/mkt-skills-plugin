---
name: 03-awareness-map
description: Map buyers across Schwartz's five awareness levels with an entry message, proof and offer for each. Use for cold vs warm audiences, Breakthrough Advertising. Not for journeys (use 03-journey-map).
metadata:
  section: "03 Awareness"
  covers: "Awareness levels (Schwartz); Awareness × Sophistication grid"
---
# Awareness map

A message two levels ahead of the reader is ignored. Unaware buyers need a story or an identity hook; most-aware buyers need the deal. This skill decides, for this business's buyers, what each awareness level already believes and what the first message, the proof and the offer must be at that level. Every ad, page and email then reads the map instead of guessing.

## Needs (read before writing)

- `context/customer.md` (read only), with these sections present (drafted or confirmed, with content):
  - **ICP and personas**, written by `02-icp-persona`. It defines whose awareness you are mapping.
  - **Pains, desires and fears** (written by `02-customer-research`) or **Jobs to be done** (written by `02-jobs-to-be-done`). At least one; it supplies what each level knows about the problem.
- If present, read:
  - Current alternatives, Buying triggers and process, Voice of customer, and Beliefs, objections and drivers, in `context/customer.md`;
  - `context/market.md` → Market sophistication, from `01-sophistication-stage`. It changes how bold a claim each level will believe.
  - `context/offer.md`, if present (`07-offer-design` and its siblings): the offers, guarantee and proof that actually exist.
  - Lead-source or traffic data in `inputs/`.
- If a required section is missing, follow this order:
  1. **Raw customer evidence supplied** (notes, reviews): run the missing upstream skill first, then continue.
  2. **Nothing supplied:** stop. Name the missing section and the skill that fills it, and what the user should bring. Do not map awareness for an invented buyer.
- A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Define the five Awareness levels (Schwartz) for this buyer.** Write each level in this buyer's terms:
   - **Unaware:** feels symptoms but does not name the problem.
   - **Problem aware:** names the problem, but does not know solutions exist.
   - **Solution aware:** knows solutions, but not this one.
   - **Product aware:** knows this product, but is not convinced.
   - **Most aware:** wants it and needs the deal.

   Use their words from Voice of customer where possible. See [references/levels.md](references/levels.md).
2. **Estimate the share at each level** from evidence: lead sources, questions asked on calls, search terms, how buyers describe the problem. Mark every share without a source `(assumption)`. "Unknown" is acceptable. Never invent percentages as fact.
3. **For each level, set:**
   - **What they already know or believe.**
   - **Entry message:** the first thing to say. At unaware and problem aware, lead with the problem or identity. At solution aware, lead with the mechanism or difference. At product and most aware, lead with proof, offer and terms: the entry message itself opens with the strongest proof or the deal, not only the Proof needed column.
   - **Proof needed:** story, demonstration, comparison, testimonial or guarantee.
   - **Offer or next step to show:** free education at the top, the core offer and deal at the bottom. Each level gets its own step, one rung higher in commitment than the level above; never repeat the same step at two adjacent levels. If no existing offer fits a level, write a gap there. A bonus comes with the core offer, so it is never a standalone free step. Use only offers, guarantees and proof that exist in `context/offer.md`, the inputs or the user's message; write anything else as *Gap: needs …* for `07-offer-design`, never as if it exists. Something a buyer wished for (a lost prospect saying they would have bought if you had shown X) is evidence of a gap, not an offer that exists.
4. **Apply the Awareness × Sophistication grid** if `market.md` → Market sophistication exists: combine each level with the sophistication stage to choose the angle, since each level still needs a claim the buyer has not heard to exhaustion. If it is absent, apply the awareness level alone and note the gap in Evidence.
5. **Name the mismatches.** Note where today's marketing speaks to the wrong level, if the user or inputs describe their ads, pages or calls. For example: a product pitch to problem-aware strangers.

6. **Check before saving.** Re-read the draft against every item under Checks and fix any failure before you write the section. The usual ones are a composed phrase in quotation marks (beliefs, transitions, messages and gap labels you wrote go without them: write *Gap: no free forecast-current check*, with no quotation marks inside), an offer that does not exist, and the same next step at two levels.

## Output

Write `context/awareness.md` → `## Awareness map`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Awareness map
Status: draft (<YYYY-MM-DD>, 03-awareness-map)
Written by: 03-awareness-map, <YYYY-MM-DD>
| Level | Share (source or (assumption)) | What they know or believe | Entry message | Proof needed | Offer or next step |
| --- | --- | --- | --- | --- | --- |
Biggest level to win now: <level and why, with evidence>
Mismatches today: <where current marketing speaks to the wrong level, or "none observed">
Evidence: <sections and inputs used>
Method: Schwartz's five levels of awareness (Breakthrough Advertising)
```

- Entry messages are directions, not finished copy. Copywriting skills write the copy.
- Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/awareness.md` does not exist, first copy [assets/awareness.md](assets/awareness.md) to `context/awareness.md`, then write your section into it.

Reply with:
- the level to win first;
- the biggest mismatch;
- the next skill: `03-journey-map`, or `03-traffic-temperature` when traffic sources are known.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] All five levels are described for this buyer, using their words where the evidence has them.
- [ ] Each level has an entry message, the proof it needs and an offer or next step, and they rise in specificity from unaware to most aware.
- [ ] Each level's next step is a different step (or a labelled gap) from the level above, rising in commitment from free education to the core offer. No step repeats at two adjacent levels, and bonuses appear only with the core offer, never as a free step.
- [ ] Shares cite evidence or are marked `(assumption)` or "unknown". No invented percentages are stated as fact.
- [ ] Each piece of evidence is assigned to one level and used the same way in the table, the summary lines and the reply.
- [ ] Unaware and problem-aware entries lead with the problem, a story or identity, not the product or price. Product-aware and most-aware entries open with proof and the offer.
- [ ] Every offer, guarantee or proof named either exists in `context/offer.md`, the inputs or the user's message, or is labelled as a gap. What a buyer wished for in the inputs is a gap, not an existing offer.
- [ ] Entry messages are directions, not finished copy. No product facts, prices or results are invented.
- [ ] Quotation marks hold only words copied exactly from a source (no added or moved words, and not the note-taker's summary around a quote). Paraphrased buyer questions, labels, proposed messages and calls to action go without quotation marks (use italics for proposed copy).
- [ ] No unmarked inference: any statement about buyers that the evidence does not state (a motive, a frequency word such as "often" or "most", a share or rate the inputs don't give) carries `(assumption)` or is left out.
- [ ] Only `## Awareness map` changed in `context/awareness.md`. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

Lead with what the buyer already believes and take them one step forward: a message two levels ahead of the reader is ignored, so each awareness level needs its own entry message, proof and offer. Five levels of awareness, Breakthrough Advertising (Eugene Schwartz); The Complete Marketing System, section 3 Awareness (Servidad, 2026).
