---
name: 03-journey-map
description: Map the customer journey (See-Think-Do-Care) with each stage's buyer question, intent and gap. Use for buyer's journey, content per stage, search intent. Not for awareness (use 03-awareness-map).
metadata:
  section: "03 Awareness"
  covers: "Buyer's journey; Customer journey map; Search intent; See–Think–Do–Care"
---
# Journey map

A customer journey map shows what the buyer is trying to find out at each stage, and whether anything you own answers it. It sits between the awareness map, which says what they know, and the funnel and content plans, which say what to build. The gaps it finds become content and funnel work, in the order the buyer meets them.

## Needs (read before writing)

- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: whose journey it is.
- `context/awareness.md` → **Awareness map**, from `03-awareness-map`: what each stage already knows and the entry message.
  Both must be present (drafted or confirmed, with content).
- Read **Buying triggers and process** (`02-customer-research`) if present. It holds the real steps, roles and questions.
- Read any evidence of current assets and touchpoints, if supplied: site pages, emails, call scripts, lead sources in `inputs/`.
- If the ICP or the awareness map is missing:
  - **The upstream material exists:** for example, ICP present but no awareness map. Run the missing upstream skill first, then continue.
  - **Nothing upstream:** stop. Name the missing sections and the skills that fill them. Do not draw a generic funnel for an imagined buyer.
- A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Lay out the stages.** Use See, Think, Do and Care. Map them to awareness levels and to awareness, consideration, decision and retention:
   - **See:** the whole addressable audience, unaware or problem aware.
   - **Think:** they have a commercial need and are researching.
   - **Do:** ready to buy.
   - **Care:** existing customers.
2. **Write the buyer's question at each stage**, in their words where the evidence has them. A question you composed is a paraphrase: write it without quotation marks, and put in quotation marks only a line you can find word for word in the inputs or context. This applies in every cell, including gap labels: write *Gap: no page answering which plan fits my team*, with no quotation marks around your own wording. The words around a quote must keep its meaning: do not wrap a verbatim fragment in a summary that changes what the buyer said (a price that seemed too high until X is not a price that felt right). For example, the Do question can be the question asked on sales calls.
   Place each question at the stage where the evidence shows it being asked. Support tickets and existing customers' questions belong in Care, so give every friction group in the tickets (for example each ticket tag) a Care row, even when you also note a pre-purchase version as a Think gap.
3. **Classify intent:** informational, commercial or transactional. Note the searches or places where each question is asked, if the evidence shows them.
4. **List touchpoints and assets that exist today**, from the inputs or the user. Mark an asset as unknown when it is not described. Never assume the business has a page or email it hasn't mentioned.
5. **Find the gaps.** A gap is a stage question with no owned asset answering it, or an asset answering a question nobody at that stage asks. Rank the gaps by where the evidence shows buyers stall or drop:
   - lost-deal reasons;
   - the questions asked on calls;
   - churn timing.
6. **Note emotions and moments of truth** only where the evidence shows them: the trigger, the first close, the first box.

Use [references/stages.md](references/stages.md) for the stage and intent definitions.

## Output

Write `context/awareness.md` → `## Journey`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Journey
Status: draft (<YYYY-MM-DD>, 03-journey-map)
Written by: 03-journey-map, <YYYY-MM-DD>
| Stage | Awareness level | Buyer's question (their words where possible) | Intent | Touchpoints | Asset today | Gap |
| --- | --- | --- | --- | --- | --- | --- |
Moments of truth: <moment — evidence>
Biggest gaps, in order: <gap — why it matters — evidence>
Evidence: <sections and inputs used>
Method: See–Think–Do–Care (Google); buyer's journey (HubSpot); search intent classification
```

- Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/awareness.md` does not exist, first copy [assets/awareness.md](assets/awareness.md) to `context/awareness.md`, then write your section into it.

Reply with:
- the top gaps;
- the next skill: `03-traffic-temperature`, or `12-funnel-design` once the offer exists.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every stage has the buyer's question, intent, touchpoints, today's asset (or "unknown") and the gap.
- [ ] Questions use the buyer's words where the evidence has them.
- [ ] No asset, page, channel or metric is invented. Unknowns are marked.
- [ ] The Care stage (existing customers: onboarding, retention, referral) is included, not just acquisition, and covers every friction group the support or customer evidence shows.
- [ ] Gaps are ranked from evidence of where buyers stall, not by preference.
- [ ] Quotation marks hold only words copied exactly from a source (no added or moved words, and not the note-taker's summary around a quote). Paraphrased buyer questions, labels, proposed messages and calls to action go without quotation marks (use italics for proposed copy).
- [ ] No unmarked inference: any statement about buyers that the evidence does not state (a motive, a frequency word such as "often" or "most", a share or rate the inputs don't give) carries `(assumption)` or is left out.
- [ ] Only `## Journey` changed in `context/awareness.md`. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

Answer the question the buyer is asking at the stage they are in: content and pages work when they match intent, and the journey continues after the sale. See–Think–Do–Care (Avinash Kaushik, Google); the buyer's journey (HubSpot); The Complete Marketing System, section 3 Awareness (Servidad, 2026).
