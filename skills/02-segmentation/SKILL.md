---
name: 02-segmentation
description: Split a market into segments, score them and pick who to target first (STP, Kotler). Use for who to focus on, which niche, we sell to everyone. Not for personas (use 02-icp-persona).
metadata:
  section: "02 Customer"
  covers: "Segmentation; STP"
---
# Segmentation

A niche you can describe precisely beats a market you cannot. Segments are only useful if they respond differently: to a different need, message, channel or price. This skill finds those groups in the evidence, chooses the one to win first, and names the ones to leave alone.

## Needs (read before writing)

- `context/customer.md`:
  - **Research log** (from `02-customer-research`) or **Voice of customer** (from `02-voc-mining`). You need at least one present, meaning drafted or confirmed with content.
  - Also read Pains, desires and fears, Current alternatives, and Buying triggers and process, if present.
- `context/market.md` → Size, if present, from `01-market-assessment`. It supplies size signals. Without it, size is a labelled estimate or "unknown".
- If both Research log and Voice of customer are missing, follow this order:
  1. **Raw material supplied** (interview notes, call notes, reviews or tickets in `inputs/` or the conversation): run `02-customer-research` or `02-voc-mining` on it first, then continue.
  2. **Nothing supplied:** stop. Say that segments need customer evidence. Name the skill that collects it and what the user should bring. Do not write segments from assumptions about "typical" buyers.

## Process

1. **Pick the bases that predict response.** Start with what changes behaviour:
   - **Needs-based:** the job, outcome or pain.
   - **Behavioural:** usage, frequency, trigger, current alternative.
   - **Situational or firmographic:** size, stage, model.

   Use demographics only when the evidence shows they predict a difference.
2. **Draft 2–5 segments.** For each, record:
   - who they are, in observable terms;
   - the need or job that sets them apart;
   - their current alternative;
   - what they respond to;
   - what they resist;
   - the evidence IDs and counts.
3. **Test that they differ.** Two segments that want the same thing for the same reason, through the same channel, are one segment. Merge them.
4. **Score each segment.** Use the criteria in [references/scoring.md](references/scoring.md):
   - size signal;
   - pain and urgency;
   - ability to pay;
   - ease of reaching them;
   - fit with what is sold today;
   - strength of evidence.

   Use the evidence, and mark each estimate `(assumption)`.
5. **Target.** Choose one primary segment (two at most), with the reason. Name the segments you are not serving now, and why.
   - Positioning for the target is finished in `06-positioning-statement`; do not write it here.
   - Do not force a target the evidence cannot support. If the evidence is too thin to separate segments, say so and list what research would.

## Output

Write `context/customer.md` → `## Segments`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Segments
Status: draft (<YYYY-MM-DD>, 02-segmentation)
Written by: 02-segmentation, <YYYY-MM-DD>
| Segment | Who (observable) | Need that sets them apart | Current alternative | Responds to | Evidence |
| --- | --- | --- | --- | --- | --- |
Scores: <segment: size, pain, pay, reach, fit, evidence → total>
Target: <segment> because <evidence-based reason>.
Not now: <segment>: <reason>; <segment>: <reason>.
Open questions: <what would change the choice>
Evidence: <files and IDs>
Method: STP (Kotler); needs-based and behavioural segmentation
```

Mark anything not traced to a source `(assumption)`, including size estimates. Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/customer.md` does not exist, first copy [assets/customer.md](assets/customer.md) to `context/customer.md`, then write your section into it.

Reply with:
- the target;
- what you deprioritised;
- the next skill: `02-icp-persona` for the target segment's ICP.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Segments differ in need, behaviour or response, not only in demographics. Look-alike segments were merged.
- [ ] Every segment cites evidence (IDs, counts). Sizes without a source are marked `(assumption)` or "unknown".
- [ ] Exactly one primary target (two at most) is chosen, with an evidence-based reason, or the section says the evidence cannot yet separate segments.
- [ ] "Not now" segments are named with reasons. Saying no is part of the output.
- [ ] No unmarked inference: any statement about buyers that the evidence does not state (a motive, a habit, a frequency word such as "often" or "most", which group an unlabelled review came from, a rate for a channel the notes don't give, one interview generalised to a whole group, such as why several deals were lost) carries `(assumption)` or is left out. Re-read each sentence of the section for this before saving.
- [ ] Quotation marks hold only words copied exactly from a source (no added or moved words). Paraphrases, inferences, labels and suggested questions go without quotation marks (use italics for a suggested question).
- [ ] Positioning is left to `06-positioning-statement`, and offers and pricing to `07-offer-design`.
- [ ] Only `## Segments` changed. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

A segment is a group that responds differently. Pick the one you can describe precisely, reach and win, and say no to the rest, because a niche you can describe beats a market you cannot. STP: segmentation, targeting, positioning (Philip Kotler, Marketing Management); The Complete Marketing System, section 2 Customer (Servidad, 2026).
