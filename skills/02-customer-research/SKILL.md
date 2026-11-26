---
name: 02-customer-research
description: Plan customer interviews (The Mom Test) and surveys, or turn interview notes, reviews and tickets into buyer pains and triggers. Use for who buys and why. Not for exact quotes (use 02-voc-mining).
metadata:
  section: "02 Customer"
  covers: "Customer interviews (Mom Test); Surveys (market research)"
---
# Customer research

People buy to move from a current state to a desired state. This skill finds out, from what customers did rather than what they predict, what that move looks like, what they tried before, and what made them act. Everything downstream reads its four sections: segments, ICP, jobs, awareness and the offer.

## Needs (read before writing)

- **Raw evidence**, in `inputs/`, elsewhere in the project, or pasted by the user. Any of these counts:
  - interview notes or transcripts;
  - sales-call notes;
  - survey results;
  - churn or cancellation reasons;
  - reviews.

  Record each source's type, count, dates and who it covers: customers, churned, lost or prospects.
- `context/customer.md`, if present: Research log (what was already studied) and Voice of customer, written by `02-voc-mining`. Reuse its sourced quotes; do not re-derive them.
- `context/market.md` → Market definition, if present, from `01-market-assessment`. It scopes who to recruit.
- Nothing upstream is required. If there is no raw evidence, the material is missing, so stop before writing any context section. Instead, write the research plan described under Output, and still end the reply with the **Principle, framework, source** block.
  - Never fill a section from your own idea of "typical customers".
  - The founder's beliefs are hypotheses for the plan, not findings.

## Process

**With evidence (synthesize):**

1. **Log the sources.** For each source, note:
   - type and count;
   - dates;
   - mix: customers, churned, lost, prospects;
   - who ran it;
   - its bias: reviews and forum posts are self-selected and skew to extremes or enthusiasts, tickets come from people with a problem, sales notes are the rep's summary, surveys are stated preference.

   Count from a tally of item IDs, never by eye, and recheck every number against the file before writing it.

   Name the gaps. Start with the source types that are missing altogether, said plainly (for example *No interviews or surveys have been done; every source is self-selected or problem-led.*). For each gap write the research that would fill it (for example, interview 5 cancelled subscribers). Write a suggested question in italics, never in quotation marks. Common gaps: no churned customers, no non-buyers, one segment only.
2. **Read for behaviour, not opinion.** Weight what people did and paid over what they say they would do. Mark compliments and hypotheticals ("I'd definitely buy…") as weak evidence. This is The Mom Test applied to existing notes.
3. **Pains, desires and fears.**
   - Group the evidence in the customer's framing.
   - Cite the evidence IDs and counts for each item.
   - Quote only verbatim text, with its source. Copy every quoted word exactly ("shows" stays "shows"); keep words outside a source's quotation marks outside yours; never put your own inference or a suggested question in quotation marks.
4. **Current alternatives.** List what they used before or instead: other providers, DIY, a spreadsheet, a hire, doing nothing. For each one, note the price if stated, why they chose it, and why they left it or stayed.
5. **Buying triggers and process.**
   - The event that started the search: a scare, a deadline, a hire, a season.
   - Who finds, who decides, who pays and who uses. Name a role only where a source says who does it; an interviewee's job title does not show who decides or pays. Otherwise write "not recorded" and list it as a gap.
   - The steps and the questions buyers ask.
   - How long the decision takes.

   Use counts where the notes allow ("23 of 41 calls asked…").
6. **Separate findings from hypotheses.** Anything seen once, or only inferred, is marked `(assumption)` or labelled a single source. A reason, price or motive the source does not state (why someone left, that an option is "free") is an inference: mark it or leave it out.
7. **Know whose words they are.** In notes written by someone else, only the words inside the note's own quotation marks are the customer's; the rest is the note-taker's summary. Quote only the former, or paraphrase without quotation marks: from a note reading all "promised the same thing", quote "promised the same thing" and leave *all* outside.

**Without evidence (plan):**

Write the research plan from [references/interview-guide.md](references/interview-guide.md). It has five parts:
- who to recruit, and how many;
- a screener;
- a Mom Test interview guide about past behaviour;
- an optional survey, only once 30 or more customers exist;
- the existing sources to pull: call notes, tickets, reviews, competitor reviews.

Put the founder's beliefs under "Hypotheses to test". Then ask the user to run the interviews and bring the notes back.

Count with [scripts/tally.py](scripts/tally.py) whenever the material is a file: `python3 <this skill's folder>/scripts/tally.py inputs/reviews.csv` prints rows and per-column counts, and `tally.py notes.md 'R\d+|T-\d+'` counts distinct item IDs. Use its numbers, not counts made by reading.

## Output

**With evidence**, write these four sections of `context/customer.md`, replacing each section's body and leaving every other section exactly as it was:

- `## Research log`: sources (type, count, dates, mix), method, and gaps.
- `## Pains, desires and fears`: three lists, each item with evidence IDs.
- `## Current alternatives`: one line per alternative, covering price if known, why chosen, and why left.
- `## Buying triggers and process`: triggers with counts, roles, steps, questions buyers ask, and decision time.

Format each section the same way:
- It starts with `Status: draft (<YYYY-MM-DD>, 02-customer-research)`, then `Written by: 02-customer-research, <YYYY-MM-DD>`, then the content.
- Each of the four sections, the Research log included, ends with `Evidence:` (the files and IDs used) and `Method: Customer interviews, The Mom Test (Fitzpatrick)`. Add surveys to the Method line if used.
- Anything not traced to a source is marked `(assumption)`.
- Never set `confirmed` unless the user says the section is approved.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/customer.md` does not exist, first copy [assets/customer.md](assets/customer.md) to `context/customer.md`, then write your sections into it.

**Without evidence**, write `work/02-customer/02-customer-research-<YYYY-MM-DD>-plan.md` with these sections: Goal, Hypotheses to test, Who to recruit, Screener, Interview guide, Existing sources to pull, Survey (optional), and How to log notes. Leave `context/` unchanged.

Reply with:
- the three findings that matter most, or the plan's first step;
- the gaps;
- the next skill: `02-segmentation` or `02-icp-persona`. Use `02-voc-mining` instead if raw text still needs mining.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every finding cites evidence (an interview, call, review or survey ID, or a count). Single-source or inferred items are labelled.
- [ ] Every number was recounted from item IDs and matches the source files.
- [ ] In Buying triggers and process, every trigger, role or step backed by fewer than 3 items is labelled thin or single source next to its count.
- [ ] The Research log says plainly which source types are missing (interviews, surveys, churned customers, non-buyers) and names each gap with the research that would fill it.
- [ ] Past behaviour outranks opinions and hypotheticals. Compliments are not counted as demand.
- [ ] Current alternatives include doing nothing or DIY where the evidence shows it, not only named competitors.
- [ ] Buying roles are separated (finder, decider, payer, user) wherever the evidence shows them.
- [ ] Quotation marks hold only words copied exactly from a source (no added or moved words). Paraphrases, inferences, labels and suggested questions go without quotation marks (use italics for a suggested question).
- [ ] Quotes are verbatim with a source; no names or personal data.
- [ ] Without evidence, no context section was written. The plan's questions ask about specific past events, not opinions about the future or the product.
- [ ] Only the four owned sections changed. Each has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

People buy to move from a current state to a desired state, and the only reliable evidence of that move is what they already did: ask about specific past events, never about hypothetical futures. Customer interviews, The Mom Test (Rob Fitzpatrick); current state to desired state ($100M Offers, Hormozi; Sugarman); The Complete Marketing System, section 2 Customer (Servidad, 2026).
