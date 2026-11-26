---
name: 02-icp-persona
description: Define the ideal customer profile and buyer personas with an empathy map, from evidence. Use for ICP, ideal customer, avatar, dream buyer, who decides. Not for market splits (use 02-segmentation).
metadata:
  section: "02 Customer"
  covers: "Empathy map; ICP / persona"
---
# ICP and personas

Every downstream skill writes for someone. The ICP says which accounts or people to pursue and which to turn away. Personas say how each role in the purchase thinks and talks. Both are built from the customers who succeeded, compared with those who churned or never bought, not from a stereotype.

## Needs (read before writing)

- `context/customer.md`, with at least one of these present (drafted or confirmed, with content):
  - **Research log**, written by `02-customer-research`;
  - **Voice of customer**, written by `02-voc-mining`.

  Also read Pains, desires and fears, Current alternatives, and Buying triggers and process.
- `context/customer.md` → Segments, from `02-segmentation`, if present. Build the ICP for the target segment, and treat "not now" segments as disqualifiers. Keep the target segment's bounds (size band, type) in the ICP filters; if the evidence seems to argue for other bounds, keep the segment's and note the conflict for `02-segmentation` to settle.
- `context/customer.md` → Jobs to be done, from `02-jobs-to-be-done`, if present. Use it to sharpen the persona's goals.
- When both Research log and Voice of customer are missing:
  - **Raw material supplied** (interview notes, call notes, reviews or tickets in `inputs/` or the conversation): run `02-customer-research` (or `02-voc-mining` for review-type text) on it first, then continue.
  - **Nothing supplied:** stop. Say the ICP needs upstream customer context, name each missing section in `context/customer.md` and the skill that fills it (`Research log` → `02-customer-research`, `Voice of customer` → `02-voc-mining`), and list what to bring: notes from 5–10 conversations with recent buyers, churned customers and lost deals, or a review export. Never write an ICP or persona from assumptions about "typical" buyers. End the reply with the **Principle, framework, source** block (see Output), even when you stop.

## Process

1. **Compare best and worst.** From the evidence, list what the customers who bought and stayed share. Then list what the churned, lost or poor-fit ones share. Only attributes that separate the two groups belong in the ICP.
2. **Write the ICP as filters.** Use observable attributes someone could apply to a list:
   - **B2B:** industry, size, revenue model, stage, tools used, recent trigger event.
   - **B2C:** situation, behaviour, current alternative, trigger. Use demographics only where evidence shows they matter.

   Tie each attribute to evidence.
3. **Map the roles.** Who finds, decides, pays, uses and influences. In B2C one person may hold every role; say so.
4. **Write the disqualifiers.** Who to turn away, and why, with evidence: price mismatch, wrong job, cannot be served well. Disqualifiers save more money than the ICP.
5. **Build one persona per role that matters.**
   - Use an empathy map: think, feel, say, do, pains, gains. Use [references/persona-template.md](references/persona-template.md).
   - Fill "say" with verbatim quotes from the evidence. In a note-taker's summary, only the words inside the note's own quotation marks are the customer's: from a note reading all "promised the same thing", quote "promised the same thing" and leave *all* outside.
   - Describe a situation, not a stock photo. No invented age, hobbies or names, unless the evidence states them. A role label such as "Studio owner" is enough.
6. **Where they gather.** List the places, people and media the evidence shows they already use: referral sources, podcasts, communities, events. This is the start of a Dream 100 list. Mark inferred places `(assumption)`.

## Output

Write `context/customer.md` → `## ICP and personas`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## ICP and personas
Status: draft (<YYYY-MM-DD>, 02-icp-persona)
Written by: 02-icp-persona, <YYYY-MM-DD>
ICP (filters): <attribute — evidence>; <attribute — evidence>; trigger: <event — evidence>
Roles: finds <…> · decides <…> · pays <…> · uses <…> · influences <…>
Disqualify: <who — why — evidence>
Persona — <role label>: situation; goals; think / feel; says: "<verbatim>" — <source>; does; pains; gains; objections
Where they gather: <channels and people — evidence or (assumption)>
Evidence: <files and IDs>
Method: ICP and persona; empathy map; Dream Buyer (Kennedy)
```

Mark any attribute not traced to a source `(assumption)`. A question to ask next goes in italics alone, with no quotation marks: *Who else signs off on this spend?* Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/customer.md` does not exist, first copy [assets/customer.md](assets/customer.md) to `context/customer.md`, then write your section into it.
- If you ran an upstream skill first, it writes its own sections the way it always does.

Reply with:
- the ICP in one sentence;
- the disqualifiers;
- the next skill: `03-awareness-map`, or `02-jobs-to-be-done` if the jobs are still missing.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every ICP attribute is observable (someone could filter a list with it) and separates good customers from poor-fit ones, with evidence.
- [ ] Finder, decider, payer and user are distinguished, or explicitly the same person.
- [ ] Disqualifiers are listed with reasons and evidence.
- [ ] Personas are built from quotes and behaviour. No invented names, ages, hobbies or demographics.
- [ ] No unmarked inference: any statement about buyers that the evidence does not state (a motive, a habit, a frequency word such as "often" or "most", which group an unlabelled review came from, a rate for a channel the notes don't give) carries `(assumption)` or is left out.
- [ ] Quotation marks hold only words copied exactly from a source (no added or moved words, not even a leading *who*). Paraphrases, inferences, labels and suggested questions go without quotation marks (use italics for a suggested question). Before saving, copy your section into a scratch file outside `context/` and run [scripts/check_quotes.py](scripts/check_quotes.py) on it (`python3 <this skill's folder>/scripts/check_quotes.py <scratch file>`); fix every line it prints.
- [ ] Quotes are verbatim with a source; no personal data.
- [ ] Only `## ICP and personas` changed (plus any upstream sections written by an upstream skill run first). It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

Describe the buyer precisely enough to find them and to turn the wrong ones away. A niche you can describe beats a market you cannot, and who decides, pays and uses can be different people. ICP and persona, with the empathy map (Dave Gray, XPLANE); Dream Buyer (Dan Kennedy; Russell Brunson's Dream 100, Traffic Secrets); The Complete Marketing System, section 2 Customer (Servidad, 2026).
