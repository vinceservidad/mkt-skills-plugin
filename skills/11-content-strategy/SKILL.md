---
name: 11-content-strategy
description: Plan content pillars, clusters, repurposing and distribution against the buyer journey. Use for content strategy, blog plan, content pillars, what content to make and where.
metadata:
  section: "11 Distribution"
  covers: "Content marketing; Content repurposing"
---
# Content strategy

Content earns attention by answering the questions buyers already have, in the order they have them. A strategy picks the few pillars where the business's real expertise meets an evidenced buyer pain, maps each topic to a stage of the journey with a next step, and plans how each piece reaches people and turns them into subscribers the business owns. A list of fifty blog titles is not a strategy; neither is a cadence nobody can keep.

Save the strategy as a Markdown file in `work/11-distribution/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`.
- `context/awareness.md` → **Journey** (from `03-journey-map`) or **Awareness map** (from `03-awareness-map`). Either one is enough; read both if present.
- If present, also read `context/customer.md` → Pains, desires and fears, Jobs to be done and Voice of customer; `context/awareness.md` → Traffic temperature; `context/offer.md` → Core offer and Value ladder (the free steps and lead magnets that exist); `context/message.md` → Big idea, Promise, Message house and Story; `context/brand.md` → Voice; any keyword exports, analytics, existing content lists or capacity notes in `inputs/`; any work in `work/12-funnel/12-lead-magnet-*.md`, `work/11-distribution/11-seo-*.md` or `work/11-distribution/11-channel-selection-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (interviews, reviews or call notes in `inputs/` but no ICP or journey): run the skill that fills it first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (ICP and personas → `02-icp-persona`; Journey → `03-journey-map`, or Awareness map → `03-awareness-map`), and ask for evidence (interviews, reviews, sales-call notes), not a description of the buyer. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.
- If `03-journey-map` is not loaded, stop and say: enable mkt-q1-audience.
- If `03-awareness-map` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/content-guide.md](references/content-guide.md) for pillar tests, cluster fields, repurposing and the search-data rule.

1. **Content mission and tilt.** One sentence: for whom (the ICP), what they get (the outcome of reading), and the business's tilt, the expertise or angle it has that others don't (from offer, message or story, not invented).
2. **Pillars.** Choose 2 to 4. Each pillar is an evidenced buyer pain, job or belief (cite the IDs) where the business has real expertise, and whose topics lead naturally to the core offer. Reject pillars the evidence doesn't support or that attract disqualified buyers, and say why.
3. **Clusters.** Under each pillar, list topics as buyer questions (from the journey, the awareness map, Voice of customer, tickets or call notes) with the journey stage and awareness level each serves, the format, and the next step. Next steps are only free assets and offers that exist in `offer.md` or `work/`; anything else is a named *gap*. Cover every journey stage or say which is deliberately left out.
4. **Search demand,** only where `inputs/` holds keyword or search data. Quote volumes exactly as the export gives them, with its date and tool; never estimate volumes or difficulty. Detailed keyword and on-page work goes to `11-seo`; answer-engine visibility to `11-ai-seo-geo`.
5. **Repurposing map.** For each pillar asset (an article, a podcast episode, a webinar), list the derivatives per channel (posts, carousel, email, short video), starting with assets the business already has.
6. **Distribution and capture.** For each piece, how it reaches people: owned (email, site), earned (guest spots, partners, PR) or paid (promotion handed to `11-paid-social` or `11-paid-search`). Every pillar has a capture point that turns readers into subscribers the business owns (rent-to-own).
7. **Cadence and capacity.** Set a cadence the stated capacity can sustain. If capacity is not in `inputs/`, write the cadence as a proposal *(assumption)* and ask who writes, edits and designs, and how many hours a week. Dates and the editorial calendar go to `20-content-calendar`; organic social posting to `11-social`.
8. **Measurement.** One metric per stage tied to the business outcome (subscribers, lead-magnet downloads, sourced calls or orders), with the attribution method that exists (UTM, "how did you hear about us", sign-up source) or the gap. Views and engagement are signals, not outcomes.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, statistics, testimonials, search volumes, offers, features or claims that aren't in `context/` or `inputs/`. Topic ideas that would need data the business doesn't hold are marked *needs data*. Mark inferences `(assumption)` and list what is needed under Open questions. Describe each source only as it reads. Search-engine and platform behaviour claims need a dated first-party source or *to confirm*. Competitor claims need a dated source or an `(assumption)` label.

## Output

Write `work/11-distribution/11-content-strategy-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Content strategy: <business, period>
Skill: 11-content-strategy · Date: <YYYY-MM-DD> · Framework: Content marketing (pillars, clusters, repurposing, distribution)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval
## Content mission and tilt
## Pillars
| Pillar | Buyer pain, job or belief (evidence) | Why we can own it | Leads to |
| --- | --- | --- | --- |
## Clusters
| Pillar | Topic (buyer question) | Journey stage / awareness level | Evidence | Search data (if supplied) | Format | Next step |
| --- | --- | --- | --- | --- | --- | --- |
## Rejected pillars and why
## Repurposing map
## Distribution and capture
## Cadence and capacity
## Measurement
## Hand-offs
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The strategy is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a review, an interview, a ticket), with the source named. Write your own titles, topics and lines in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches. Count anything you report from files with [scripts/tally.py](scripts/tally.py), not by eye.

Reply with the file path, the pillars chosen, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] 2 to 4 pillars, each tied to an evidenced pain, job or belief with IDs, and to the business's real expertise.
- [ ] Every topic is a buyer question mapped to a journey stage or awareness level, with a next step that exists or a named gap.
- [ ] Search volumes appear only as the supplied export states them, with its date; none is estimated.
- [ ] Every pillar has a repurposing path, a distribution route and an owned capture point.
- [ ] Cadence matches stated capacity, or is marked *(assumption)* with the capacity question asked.
- [ ] Measurement ties each stage to a business outcome with its attribution method or gap; views are not outcomes.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Answer the questions your buyers already ask, in the order they ask them, on the few topics where your expertise is real, and turn every reader you reach into a subscriber you own. Content marketing: pillars, clusters, repurposing and distribution, Epic Content Marketing and Content Inc. (Joe Pulizzi); Everybody Writes (Ann Handley); The Complete Marketing System, section 11 Distribution (Servidad, 2026).
