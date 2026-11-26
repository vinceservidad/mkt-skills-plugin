---
name: 19-horizontal-expansion
description: Choose the next segment, offer or market to expand into once the core is stable. Use for new markets, new products, new segments, international expansion, what comes after the core offer.
metadata:
  section: "19 Growth"
  covers: "Ansoff Matrix; Core–Adjacent–Transformational; Crossing the Chasm; Horizontal scale paths"
---
# Horizontal expansion

Horizontal expansion adds a new segment, offer, channel or market next to a core that already works. It works when the core is stable first, each option is placed by how far it moves from what the business knows (same customers or new, same offer or new), the closest options with evidence of demand go first, and each comes with a small test and a stop rule. It fails when expansion is used to escape a leaking core, the farthest and most exciting option goes first, the team's capacity is ignored, or a new market is entered on a hunch.

Save the expansion options as a Markdown file in `work/19-growth/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **Segments** or **ICP and personas**, from `02-segmentation`: who the core serves and which segments were set aside.
- `context/offer.md` → **Value ladder** or **Core offer**, from `07-value-ladder`: what the core sells and which steps are empty.
- If present, also read `context/customer.md` → Jobs to be done; `context/offer.md` → Price and model; growth, retention, capacity and demand evidence in `inputs/`; any work in `work/19-growth/19-constraint-finder-*.md` or `work/01-market/`.
- If a required section is missing:
  - **The upstream evidence exists** (reviews, tickets, sales or customer notes in `inputs/`): run `02-segmentation` or `07-value-ladder` first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Segments or ICP and personas → `02-segmentation` (or `02-icp-persona`); Value ladder or Core offer → `07-value-ladder` (or `07-offer-design`)), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If `02-segmentation` is not loaded, stop and say: enable mkt-q1-audience.
- If `07-value-ladder` is not loaded, stop and say: enable mkt-q2-offer.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/expansion-guide.md](references/expansion-guide.md) for core stability checks, the Ansoff Matrix, core–adjacent–transformational, crossing the chasm and horizontal scale paths, and [references/international-localization-playbook.md](references/international-localization-playbook.md) when any option involves international or multi-region expansion (landed-cost/VAT/duties math, DDP shipping, localization, local payments, country-separated feeds/ad accounts and hreflang).

1. **Is the core stable?** Retention, delivery and constraint from `inputs/` and `19-constraint-finder`; if the core is leaking, expansion waits and the reason is stated.
2. **List options.** From the owner's ideas and the evidence: new segments (from Segments set aside), new offers (empty ladder steps, product gaps), new channels, new markets.
3. **Ansoff Matrix.** Place each: market penetration, product development, market development, diversification.
4. **Core–Adjacent–Transformational.** Rate distance from what the business knows; closer goes first unless evidence says otherwise.
5. **Crossing the Chasm.** For a new segment, check whether it buys for different reasons and needs a different whole product or proof; name the beachhead.
6. **Horizontal scale paths.** For each top option: evidence of demand, what it needs (product, operations, legal, team), capacity, cost (or *unknown*), the smallest test and its stop rule. Market facts (rules, duties, shipping) are cited with URL and date or *to confirm*.
7. **Approval.** The options are a draft. Launching products, entering markets or committing money needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no market sizes, demand, costs or regulations that aren't in `context/` or `inputs/` or cited with a date. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/19-growth/19-horizontal-expansion-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Expansion options: <business, date>
Skill: 19-horizontal-expansion · Date: <YYYY-MM-DD> · Framework: Ansoff Matrix; Core–Adjacent–Transformational; Crossing the Chasm; Horizontal scale paths
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval
## Is the core stable?
## Options
| Option | Ansoff quadrant | Core, adjacent or transformational | Evidence of demand | Needs | Capacity | Cost |
| --- | --- | --- | --- | --- | --- | --- |
## Order and why
## Smallest test and stop rule for the first option
## Not now
## Facts to confirm
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/19-growth/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, whether the core is ready, the first option and its test, and what waits and why, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Core stability is checked first; a leaking core delays expansion with the reason.
- [ ] Every option is placed on Ansoff and by distance, with evidence of demand or *none*.
- [ ] New segments are checked for different buying reasons and whole product (beachhead named).
- [ ] The first option has needs, capacity, cost or *unknown*, a smallest test and a stop rule; market facts are dated or *to confirm*.
- [ ] Non-priorities are explicit; nothing launches without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Stabilise the core, then expand to the nearest option with evidence of demand, test it small, and leave the farthest bets until the closer ones are proven. Ansoff Matrix (Igor Ansoff), Core–Adjacent–Transformational (Nagji and Tuff), Crossing the Chasm (Geoffrey Moore); The Complete Marketing System, section 19 Growth (Servidad, 2026).
