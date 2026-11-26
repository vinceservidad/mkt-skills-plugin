---
name: 02-voc-mining
description: Mine reviews, tickets, surveys and call notes for customers' exact words, themes and a language bank. Use for voice of customer, what customers say about us. Not for interviews (02-customer-research).
metadata:
  section: "02 Customer"
  covers: "Social listening; Voice of Customer"
---
# Voice of customer mining

Copy is assembled from research, not invented. This skill turns raw customer text into a sourced bank of the customer's own words, which every later skill (offer, message, headlines, ads) reads instead of guessing.

## Needs (read before writing)

- **Raw customer text**, from either source:
  - files in `inputs/` or anywhere in the project: reviews, tickets, forum posts, transcripts, survey exports, call notes;
  - text the user pasted into the conversation.

  Note for each source what it is, its date range and how many items it holds.
- `context/customer.md`, if it exists. Read three sections:
  - Research log (sources already used);
  - Segments, and ICP and personas, so quotes can be tagged by segment;
  - Voice of customer, which is your own section; add to it rather than discarding sourced quotes.
- Nothing upstream is required. If there is no raw customer text, the material is missing. Stop. Do not write the section, and never invent or "illustrate" quotes. Tell the user which sources to pull, in order of value:
  1. sales-call notes or transcripts;
  2. support tickets;
  3. reviews of you and of competitors;
  4. forum threads;
  5. survey open-ends.

  You may save that collection plan to `work/02-customer/02-voc-mining-<YYYY-MM-DD>-sources.md`. End the reply with the **Principle, framework, source** block (see Output), even when you stop.

## Process

1. **Inventory the sources.** For each one, record:
   - type and count;
   - date range;
   - who is speaking: customer, prospect, churned or lost;
   - its bias. Review sites skew to extremes, tickets skew to problems, and testimonials are selected.
   - Social listening (public posts, comments, community threads) counts only when the text is supplied; record platform and date, note that it skews to the vocal, and treat handles as personal data.
2. **Extract verbatim snippets.** Read every item. Copy the exact words that express a pain, desire, fear, objection, trigger, outcome, alternative or identity.
   - Keep the item's ID and date with each snippet.
   - Shorten only with `…` and never change words inside quotation marks.
   - Remove people's and pets' names, emails, handles, order numbers and anything else that could identify a private person; write `[Dog]`, `[Owner]` or a role instead.

   [references/coding-guide.md](references/coding-guide.md) has the codes and the extraction table.
3. **Code into themes.** Group the snippets by what they are about, in the customer's framing. Count the items in each theme, per source, from a tally of item IDs rather than by eye.
   - When a source gives category counts (for example, support tags), use those numbers and say so.
   - Every number you write (themes, ratings, totals) must be recounted from the IDs behind it before it goes in the section.
   - A theme that rests on one item is an anecdote; label it that way.
   - **Small samples.** Under about 20 items in total, write counts as "x of n" and call nothing a pattern. Say in the Gaps line what more material to collect before frequencies mean anything.
4. **Rank.** Rank by frequency first, then intensity: strong emotion, money or time lost, a cancellation.
   - Keep negative and neutral voices alongside praise; they hold the objections the offer must answer.
   - Note which segment or rating each theme comes from.
5. **Build the language bank.** Give each phrase the ID of an item it came from.
   - Phrases of 2–6 words that customers repeat, which can be lifted into copy.
   - The words they use for the problem, the outcome and the alternatives.
   - Any jargon of yours that they never use.
6. **Name the gaps.** Note any missing voices: churned customers, non-buyers, a segment. Note any source that was unreadable or skipped.

Count with [scripts/tally.py](scripts/tally.py) whenever the material is a file: `python3 <this skill's folder>/scripts/tally.py inputs/reviews.csv` prints rows and per-column counts, and `tally.py notes.md 'R\d+|T-\d+'` counts distinct item IDs. Use its numbers, not counts made by reading.

## Output

Write `context/customer.md` → `## Voice of customer`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Voice of customer
Status: draft (<YYYY-MM-DD>, 02-voc-mining)
Written by: 02-voc-mining, <YYYY-MM-DD>
Sources: <type, count, dates> · <type, count, dates>
| Theme | Items | Where | Strongest quote |
| --- | --- | --- | --- |
Quotes by theme:
- <Theme>: "<verbatim>" — <source ID, date>
Language bank: "<phrase>" (<ID>), "<phrase>" (<ID>), …
Their words, not ours: <customer word> (not "<our word>")
Gaps: <voices or sources missing>
Evidence: <files and sources used>
Method: Voice of Customer mining (review and ticket coding); Mom Test weighting of past behaviour (Fitzpatrick)
```

- Start the section with `Status: draft (<date>, 02-voc-mining)`. Set `confirmed` only if the user says it is approved.
- In the frontmatter, set `status: draft` (unless it is already `confirmed`) and `updated: <date>`, and append one line to `## Change log`.
- If `context/customer.md` does not exist, first copy [assets/customer.md](assets/customer.md) to `context/customer.md`, then write your section into it.
- Quotation marks are only for customer words. Counts, labels and notes go without them: write Counts: reviews x of 15, tickets x of 10 sampled, not "x of 15".
- When there are more than about 40 snippets, also save the full coded extraction to `work/02-customer/02-voc-mining-<YYYY-MM-DD>-extract.md`. In that case keep the context section to the strongest 8–15 quotes.

Reply with:
- the top themes;
- the gaps;
- the next skill: `02-buyer-psychology` for objections, or `02-icp-persona` for who is speaking.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every quotation is copied character for character from a named source, and carries an ID or date. Nothing paraphrased sits inside quotation marks.
- [ ] Quotation marks hold only words copied exactly from a source (no added or moved words). Paraphrases, inferences, labels and suggested questions go without quotation marks (use italics for a suggested question).
- [ ] No people's or pets' names, emails, handles, order numbers or other personal data appear, inside quotes or out.
- [ ] Every language-bank phrase carries the ID of an item it came from.
- [ ] Theme counts come from the material (or a source's own category counts, labelled as such), not from impressions. Every number was recounted from item IDs. Single-item themes are labelled as anecdotes.
- [ ] With fewer than about 20 items, counts read "x of n", no theme is called a pattern, and the Gaps line says what to collect next.
- [ ] Complaints, cancellations and neutral voices are included, not only praise.
- [ ] The language bank uses the customers' words, not marketing language.
- [ ] Gaps in the sources are named.
- [ ] Only `## Voice of customer` changed in `context/`. It has a Status line, Evidence and Method lines and a change-log line, and is not marked confirmed.

## Principle and source

The customer's words beat your words: copy is assembled from research, not invented, and what people did and complained about outweighs what they say they would do. Voice of Customer mining and review mining (Joanna Wiebe, Copyhackers); weighting past behaviour over opinion, The Mom Test (Rob Fitzpatrick); The Complete Marketing System, section 2 Customer (Servidad, 2026).
