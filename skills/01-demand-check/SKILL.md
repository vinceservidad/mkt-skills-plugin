---
name: 01-demand-check
description: Measure existing demand from keyword exports, ad presence, competitor count and price bands. Use for is there demand, search volume, who bids. Not for market size (use 01-market-assessment).
metadata:
  section: "01 Market"
  covers: "Demand analysis"
---
# Demand check

Selling into existing demand is fast and cheap; creating demand is slow and expensive. This skill finds out which one this business faces. It reads the traces buyers and competitors leave: what people search for and how often, who pays to show up on those searches, how many providers serve the need, and what they charge. Then it decides whether the job is to capture demand that exists or to create it, and for which terms.

## Needs (read before writing)

- **Demand evidence**, in `inputs/`, elsewhere in the project, or pasted by the user. Any of these counts:
  - a keyword export (terms, estimated monthly searches, competition, bid ranges, trend), with the tool, location and export date;
  - search-result or ad-library observations, with dates;
  - competitor notes with prices;
  - the business's own demand data: inbound leads by source, search-console queries, waitlists, sales.
- If present, also read:
  - `context/market.md` → Market definition, from `01-market-assessment`: whose demand you are measuring. Also Competitors and alternatives, from `01-competitor-profiling`: reuse its prices and players.
  - `context/customer.md` → Voice of customer and Buying triggers and process: the words buyers use, to check the terms against.
  - `context/offer.md` → Core offer and Price and model.
- Nothing upstream is required. If there is no demand evidence at all, the material is missing, so stop before writing any context section. Write the collection plan described under Output instead.
  - Never state a search volume, bid, ad count or price from memory or as "typical".
  - Look up public sources only when the user asks you to and a web tool is available. Then record what you saw, where and when.

## Process

Use [references/demand-signals.md](references/demand-signals.md) for the detail of each signal and its limits.

1. **Group the terms by intent.** Sort every term into:
   - **Solution, specific:** names this kind of solution for this buyer (*bookkeeping for agencies*).
   - **Solution, generic:** the category without the buyer (*online bookkeeping services*).
   - **Problem or DIY:** the problem, a template or how-to (*cash flow forecast template*).
   - **Alternative:** another way to solve it (*fractional CFO*).

   Total each group with `scripts/tally.py` or `python3`, never by eye. Say which group is this business's demand and which is only adjacent.
2. **Read each signal for what it is.**
   - **Search volume:** the tool's estimate for its location and date, not a count of buyers. Low volume for a specific term can still be valuable; high volume for a generic term mostly belongs to other buyers.
   - **Bid ranges and competition:** what the tool estimates advertisers pay. They signal commercial interest, not profit.
   - **Ads seen:** who was advertising on which search or in which ad library, on which date. Report every ad observation in the evidence against the term group it belongs to, including ad-library searches, not only search-result ads. Presence is not spend. If no spend figures were shown, spend is *unknown*.
   - **Competitor count and price bands:** how many providers serve it, and the low, middle and high price observed.
   - **Own data:** leads by source and close rates beat every proxy.
3. **Check the buyer's words.** Do buyers search the way they talk in interviews and calls? A gap between the two (they describe a *payroll scare*; nobody searches it) means demand exists as pain but not as search. That is a content or referral route, not a paid-search route.
4. **Decide.** For each intent group, say whether demand is:
   - **Existing, capturable:** people search for this solution and others pay to reach them.
   - **Existing as pain, not as search:** the problem is real (customer evidence) but buyers don't search for the solution.
   - **To be created:** no search, no ads and few providers. Slow and expensive; say so.
   - **Unknown:** the evidence doesn't say.

   Then say what that means for the next step: capture (search, comparison pages), educate (content and lead magnets on the problem terms), or create (category work, outbound). Leave channel choice to `11-channel-selection`.
5. **Name the limits.** One export, one date, one location; estimates; terms not checked. List the gaps and how to fill them.
6. **Check before saving.** Re-read the draft against every item under Checks, and run `scripts/check_quotes.py` on it. Fix any failure before you save.

**Platform facts.** Do not state how a keyword tool, search engine or ad library currently works (how it estimates, buckets or hides data, who it shows) unless you have checked the platform's own documentation and cite it as `(first-party: <URL>, checked YYYY-MM-DD)`. Otherwise describe only what the export or observation shows, and mark anything else *unverified*.

**Labels.** Every number is copied from a named export or note (with its date), *calculated* from named inputs (show the formula), or marked `(assumption)`. No unmarked inference.

**Denominators.** Every count keeps its own denominator, checked against the source: lost deals are out of lost deals (*6 of 29 lost deals*), not out of all calls; closed deals out of closed deals; leads out of leads. Recheck each "x of y" against the file before saving.

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from a source. Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py context/market.md`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches. Totals come from [scripts/tally.py](scripts/tally.py) (`python3 <this skill's folder>/scripts/tally.py inputs/keywords.csv`) or `python3`.

## Output

**With evidence**, write `context/market.md` → `## Demand`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Demand
Status: draft (<YYYY-MM-DD>, 01-demand-check)
Written by: 01-demand-check, <YYYY-MM-DD>
| Intent group | Terms (est. monthly searches) | Group total | Bid range | Ads seen (date) | Reading |
| --- | --- | --- | --- | --- | --- |
Providers and price bands: <count of providers observed; low / middle / high price with source and date>
Buyer words vs search: <match or gap, with evidence>
Verdict: <existing, capturable | existing as pain, not search | to be created | unknown> for <groups> — <what it means for the next step>
Limits and gaps: <tool, location, date, estimates; what to collect next>
Evidence: <files, tools, dates>
Method: Demand analysis (search volume, ad presence, competitor count, price bands)
```

Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/market.md` does not exist, first copy [assets/market.md](assets/market.md) to `context/market.md`, then write your section into it.

**Without evidence**, write `work/01-market/01-demand-check-<YYYY-MM-DD>-plan.md`: the seed terms to research in each intent group (from the buyer's words where known), what to export from a keyword tool (volume, competition, bids, trend, location, date), what to observe in search results and ad libraries, which competitors and prices to log, and which own-data sources to pull. Leave `context/` unchanged.

Reply, without evidence, with the plan's path and a plain list of the material to bring (a keyword export with tool, location and date; dated notes of ads and competitors with prices; own leads, inquiries or search-console queries) and how to provide it: save the files in `inputs/` or paste them into the conversation, then ask again.

Reply, with evidence, with:
- the verdict, by intent group, in one or two lines;
- the most important limit of the evidence;
- the next skill: `01-market-assessment` (is it worth it), `01-competitor-profiling`, or `11-channel-selection`.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Terms are grouped by intent, and the business's own demand is separated from adjacent or generic demand.
- [ ] Every volume, bid, ad count and price names its source and date. Group totals are calculated, not eyeballed, and every "x of y" uses the source's own denominator.
- [ ] Every ad observation in the evidence (search results and ad libraries) is reported against its term group.
- [ ] Search volume is called an estimate, bids are not called profit, and ad presence is not called spend or success.
- [ ] Buyer words from research are compared with search terms, and a gap is named where it exists.
- [ ] The verdict separates capturable demand, pain without search, demand to create, and unknown.
- [ ] No current platform behaviour is asserted without a first-party citation and date.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] Without evidence, no context section was written and no number was stated.
- [ ] Only `## Demand` changed. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

Sell into existing demand where you can: creating demand is slow and expensive, so measure what buyers already search for and pay to solve before deciding to capture, educate or create. Demand analysis (search volume, ad-spend signals, competitor count, price bands); a starving crowd beats a great product (Gary Halbert); The Complete Marketing System, section 1 Market (Servidad, 2026).
