---
name: 05-distinctive-assets
description: Audit and build the colours, shapes, sounds and characters buyers recognise as yours, from recognition evidence. Use for distinctive brand assets, brand recognition, mental availability.
metadata:
  section: "05 Brand"
  covers: "Distinctive assets; How Brands Grow (Sharp); Inherent Drama (Burnett); Mental / physical availability"
---
# Distinctive assets

Distinctive beats different: buyers must recognise the brand before they can be persuaded by it. A distinctive asset is any sensory cue (a colour, a shape, a line, a sound, a character) that buyers link to this brand and to no other. Assets earn that link through consistent use over years, so most of the work is choosing a few, using them everywhere and not throwing them away. This skill audits what the brand already has, scores it on evidence, and decides what to protect, build, pair or drop.

## Needs (read before writing)

- Required (drafted or confirmed, with content): `context/brand.md` → **Brand foundation**, written by `05-brand-foundation`.
- If present, also read: `context/brand.md` → Voice and Naming; `context/customer.md` → Voice of customer and ICP and personas; `context/market.md` → Competitors and alternatives.
- The asset material, if supplied in `inputs/`: an inventory of current assets (where used, since when, how consistently), recognition or recall survey results, competitor observations with dates, brand guidelines.
- If Brand foundation is missing:
  - **The customer evidence for it exists** (`customer.md` → ICP and personas is present): run `05-brand-foundation` first, then continue.
  - **It doesn't:** stop. Name the missing section, `brand.md` → Brand foundation, and its owner `05-brand-foundation`, plus `customer.md` → ICP and personas and `02-icp-persona` if that is missing too. Ask for customer evidence and any existing assets. A stop reply writes nothing and still ends with the **Principle, framework, source** block.
- No asset inventory and no recognition data? Do not invent either. Build the list of candidate assets from the foundation, mark every one *unmeasured*, and make the recognition test the first step.

## Process

Use the method in [references/asset-audit.md](references/asset-audit.md) alongside Leo Burnett's Inherent Drama and brand-character rules in [references/burnett-inherent-drama.md](references/burnett-inherent-drama.md).

1. **Inventory.** List every asset in use: what it is, where it appears, since when, and how consistently. Note inconsistencies (two colours, three taglines) from the material.
2. **Score fame and uniqueness** from recognition data only. Run [scripts/asset_grid.py](scripts/asset_grid.py) on the survey file (`python3 <this skill's folder>/scripts/asset_grid.py inputs/<survey>.csv`) and copy its numbers; never compute percentages by eye.
   - **Fame:** the share of category buyers who link the asset to the brand.
   - **Uniqueness:** of those who link it to any brand, the share who name this one.
   - State the sample: who was asked, how many, how recruited, and the bias (for example, an audience already exposed to the brand). Small bases make a position tentative.
   - Without data, mark the asset *unmeasured*; do not rank it.
3. **Place each asset on the grid** (Romaniuk's Distinctive Asset Grid; the 50% cut-offs are a heuristic):
   - high fame, high uniqueness → **use or lose**: protect, use everywhere;
   - low fame, high uniqueness → **investment potential**: use consistently to build fame;
   - high fame, low uniqueness → **avoid solo use**: always pair with the brand name;
   - low on both → **ignore or test**: drop, or test before investing.
4. **Check against the alternatives.** An asset shared with a competitor or common across the category (a generic phrase, the category's default colour) cannot become distinctive. Use dated competitor observations only; never assert a competitor's current branding from memory.
5. **Check fit with the foundation.** Assets should express the archetype and promise, but distinctiveness comes first: a well-known, unique asset is not dropped for a better story.
6. **Decide.** For each asset: protect, build, pair with the name, fix inconsistency, or drop. Pick a small core set (the strongest few) and the rule for using them together. Name new candidate assets only where the evidence shows a gap, each with how it will be tested.
7. **Changes are the owner's decision.** A rebrand, logo change or retirement of an asset is a recommendation. For every asset the owner proposes to change, rank the risk from its scores: high where fame or uniqueness is high, low where both are low (so changing a weak asset risks less than changing a strong one). Say what would be lost (fame built so far), what it would cost to rebuild, and how to test before switching. Never present a redesign as approved.
8. **Measure.** Name the next recognition check: who to ask (category buyers, not only fans), sample, the question (*which company is this?*), and when to repeat it, so progress is tracked.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure. Run the quote check below.

**Nothing the material doesn't support.** No recognition figures, competitor colours, trademark status, design costs or survey results that aren't in `context/` or `inputs/`. Trademark or registration status is unknown unless a source says otherwise; recommend a clearance check by a qualified professional before investing in a new asset.

## Output

Write `context/brand.md` → `## Distinctive assets`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Distinctive assets
Status: draft (<YYYY-MM-DD>, 05-distinctive-assets)
Written by: 05-distinctive-assets, <YYYY-MM-DD>
Built from: <Brand foundation status; asset inventory; survey; competitor observations with date>
Sample: <who was asked, how many, how recruited, bias> or *no recognition data: every asset unmeasured*
| Asset | Where used, since | Fame | Uniqueness | Grid position | Decision |
| --- | --- | --- | --- | --- | --- |
Core set: <the few assets to use together everywhere, and the rule for using them>
Fix: <inconsistencies to resolve, with where>
Drop or pair: <asset — why>
Candidates to build: <new asset — the gap it fills — how it will be tested> (only where evidence shows a gap)
Owner decisions: <rebrand, colour or logo changes, with what would be lost and the test before switching>
Next recognition check: <who, sample size, question, when>
Evidence: <files and IDs>
Method: Distinctive asset audit and grid (Romaniuk, Building Distinctive Brand Assets); How Brands Grow (Sharp)
```

Describe assets in plain text inside the table (for example *Tagline A, books/agency line*), not in quotation marks, unless you copy the asset's exact words from the source. Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py context/brand.md`). For every line it prints, copy the exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with:
- the core set and the single biggest decision (protect, build or drop);
- what the owner must decide before any redesign;
- the next skill: `05-brand-voice` or `09-creative-brief`.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Fame and uniqueness come from recognition data copied from `asset_grid.py`, with the sample and its bias stated; unmeasured assets are marked *unmeasured*, not ranked.
- [ ] Every asset has a grid position (or *unmeasured*) and a decision: protect, build, pair, fix or drop.
- [ ] Assets shared with competitors or generic to the category are not treated as distinctive; competitor observations carry their date and source.
- [ ] A known, unique asset is never dropped for a new design without the owner's decision, the cost of lost fame and a test.
- [ ] A next recognition check is named: who, how many, the question, when.
- [ ] No invented recognition figures, competitor facts, trademark status or costs. Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] Only `## Distinctive assets` changed. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

Distinctive beats different: pick the few cues buyers already link to you and to no one else, use them everywhere for years, and measure before you change them. Distinctive Asset Grid (Jenni Romaniuk, Building Distinctive Brand Assets); mental availability (Byron Sharp, How Brands Grow, Ehrenberg-Bass Institute); Inherent Drama and brand characters (Leo Burnett); The Complete Marketing System, section 5 Brand (Servidad, 2026).
