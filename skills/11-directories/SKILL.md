---
name: 11-directories
description: List the product on directories, marketplaces and launch platforms the buyer actually uses. Use for directory submissions, Product Hunt launches, marketplace listings, review sites, listing sites.
metadata:
  section: "11 Distribution"
  covers: "Directory submissions; Product Hunt / launch platforms"
---
# Directories and launch platforms

A directory listing is worth having when the buyer searches there, compares there, or the listing earns trust or a link the buyer sees. Directory submissions fail when the goal is "every directory there is" (most send nothing and some hurt), when a launch platform is chosen because a friend did well there although its audience is not the buyer, or when profiles are left half-filled. This skill picks the few places that fit, fills each profile with true, consistent facts, and judges each on leads or customers it sends. Product Hunt and other launch platforms are judged the same way: on whether the people there are the buyer.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/positioning.md` → **Positioning statement** (from `06-positioning-statement`) or `context/customer.md` → **ICP and personas** (from `02-icp-persona`): who the listing must reach and what it says.
- If present, also read `context/customer.md` → Buying triggers and process (where buyers look); `context/market.md` → Competitors and alternatives (where competitors are listed); `context/message.md` → Proof stack; `context/brand.md` → Reputation; `context/offer.md` → Core offer, Price and model; directory, listing, review and rate-card notes in `inputs/`.
- If the required section is missing:
  - **The upstream evidence exists** (interviews, sales notes or reviews in `inputs/`): run `02-icp-persona` first, then continue.
  - **It doesn't:** stop. Name the missing section with the skill that fills it (Positioning statement → `06-positioning-statement`; ICP and personas → `02-icp-persona`) and ask for evidence. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If neither section has content and `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.
- If neither section has content and `06-positioning-statement` is not loaded, stop and say: enable mkt-q2-offer.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/directories-guide.md](references/directories-guide.md) for directory types, the fit test, profiles, reviews and launch platforms.

1. **Outcome.** Name what listings are for (leads, trust at the comparison step, local search, a backlink the buyer sees) and how each listing is judged (leads or customers it sends, with counts, recorded by a source field or a unique link).
2. **Candidates by type.** List the places that could matter: local listings (a business profile on maps), category and review directories for the buyer's industry, software or platform partner directories, marketplaces, trade-publication directories, launch platforms. Use only places named in `inputs/` or obvious categories marked *to check*; never invent a directory, its traffic or its rules.
3. **Fit test for each.** Does the ICP search or compare there (evidence from Buying triggers, discovery calls, sales notes)? Do competitors appear there? Does the listing need reviews the business has or can ask for? What does it cost (rate card with date)? A place whose audience is not the buyer is a no, with the reason, however many upvotes someone else got.
4. **Launch platforms.** Judge Product Hunt and similar platforms on audience fit (they skew to makers, tech and early adopters) and on what the business sells: a service for a non-tech buyer rarely gets customers there. If it fits, plan the launch (date, assets, who answers comments) without buying votes or asking for upvotes in ways the platform bans. Platform rules are facts to cite with URL and date or mark *to confirm*.
5. **The profile.** Name, address and phone consistent everywhere, category, the positioning line, the real offer and price model if the directory shows them, proof that exists, and photos or screenshots. Write it once and adapt per directory.
6. **Reviews on directories.** Ask real customers at a good moment, reply to every review, never pay for or gate reviews (asking only happy customers where the platform forbids it). Review solicitation rules differ by platform and law: cite or mark *to confirm*. The review system itself belongs to `16-reviews`.
7. **Paid placements.** A featured or paid listing is an owner decision with its cost and a test period; judge it on leads per dollar against the free listing.
8. **Approval.** The plan is a draft. Creating or claiming listings, paying for placements or launching needs the owner's explicit approval.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no directory traffic, rankings, review counts, ratings, certifications or awards that aren't in `context/` or `inputs/`. A certification the owner has not verified is *to confirm*. Count from files with [scripts/tally.py](scripts/tally.py), never by eye. Mark inferences `(assumption)` and list what is needed under Open questions.

## Output

Write `work/11-distribution/11-directories-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Directory and launch plan: <business, date>
Skill: 11-directories · Date: <YYYY-MM-DD> · Framework: Directory submissions and launch platforms (fit before reach)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing listed, paid or launched
## Outcome and how each listing is judged
## Candidates
| Place | Type | Buyer fit (evidence) | Cost (dated) | Decision and reason |
| --- | --- | --- | --- | --- |
## Launch platforms
## The profile
## Reviews on directories
## Paid placements
## Platform facts
| Fact the plan relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Titles of books, essays or talks, including in the Principle, framework, source block, go in italics, never in quotation marks. Write proposed profile text in italics or a plain block. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`) and fix every line it prints until it reports every quotation matches.

Reply with the file path, the places chosen and rejected with the reason, the launch-platform verdict, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every place is judged on evidence that the buyer searches or compares there; misfits are rejected with the reason; no "list everywhere".
- [ ] No directory, traffic figure, rule or certification is invented; unverified items are *to check* or *to confirm*.
- [ ] Launch platforms are judged on audience fit to the ICP; no bought or solicited votes against platform rules.
- [ ] The profile is consistent and uses only true facts and proof that exists.
- [ ] Reviews are asked of real customers, never paid or gated; review rules are dated or *to confirm*.
- [ ] Paid placements carry a dated cost and a test; each listing is judged on leads or customers with counts.
- [ ] The plan says nothing is listed, paid or launched without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Be listed where your buyer looks and compares, with a complete and honest profile, and judge each listing on the customers it sends. Directory submissions and Product Hunt / launch platforms, The Complete Marketing System, section 11 Distribution (Servidad, 2026); Traction (Gabriel Weinberg and Justin Mares) for testing channels on fit before scale.
