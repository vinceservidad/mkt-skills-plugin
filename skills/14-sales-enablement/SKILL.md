---
name: 14-sales-enablement
description: Build battle cards, one-pagers and decks that sales actually uses, from positioning, proof and objections. Use for battle cards, sales one-pager, sales deck, competitor comparisons for sales.
metadata:
  section: "14 Sales"
  covers: "Battle cards / sales enablement"
---
# Sales enablement

Sales enablement gives the people on calls what they need at the moment a buyer asks: how we differ from the alternative they're weighing, the proof that answers a doubt, a one-pager to forward to the person who signs. It works when each asset answers a question buyers actually ask, every claim has a source, competitor facts are dated and fair, and the asset is short enough to use live. It fails when decks are built for the brand rather than the buyer, battle cards trash competitors with guesses, or proof is borrowed without permission.

Save the enablement kit as a Markdown file in `work/14-sales/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- One of: `context/positioning.md` → **Competitive alternatives** (from `06-positioning-statement`), `context/market.md` → **Competitors and alternatives** (from `01-competitor-profiling`), or `context/customer.md` → **Current alternatives** (from `02-customer-research`): what buyers compare the offer against.
- `context/message.md` → **Proof stack** (from `08-proof-stack`) or `context/message.md` → **Objection map**, from `08-objection-map`: the proof and the answers the assets carry.
- If present, also read `context/positioning.md` → Positioning statement; `context/offer.md` → Core offer, Price and model, Guarantee; `context/customer.md` → Voice of customer, Beliefs, objections and drivers; `context/brand.md` → Voice, Distinctive assets; sales notes, the questions prospects ask, existing materials and permission notes in `inputs/`; any work in `work/06-positioning/06-competitor-pages-*.md` or `work/14-sales/`.
- If **any** of `context/positioning.md` → Competitive alternatives, `context/market.md` → Competitors and alternatives, or `context/customer.md` → Current alternatives already has content (and **either** Proof stack **or** Objection map has content), all required upstream sections are already satisfied: **do NOT invoke `01-competitor-profiling` or any other upstream skill, and do NOT modify any file in `context/`** — write ONLY to `work/14-sales/`.
- Only when **all three** alternatives sections are empty, or both proof/objection sections are empty:
  - **The upstream evidence exists** (competitor notes, sales notes or reviews in `inputs/`): run the skill that fills the missing section (`01-competitor-profiling`, `06-positioning-statement`, `08-proof-stack` or `08-objection-map`) first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Competitive alternatives → `06-positioning-statement`; Competitors and alternatives → `01-competitor-profiling`; Proof stack → `08-proof-stack`; Objection map → `08-objection-map`), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If `06-positioning-statement` is not loaded, stop and say: enable mkt-q2-offer.
- If `01-competitor-profiling` is not loaded, stop and say: enable mkt-q1-audience.
- If `08-proof-stack` is not loaded, stop and say: enable mkt-q3-message.
- If `08-objection-map` is not loaded, stop and say: enable mkt-q3-message.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/enablement-guide.md](references/enablement-guide.md) for battle card structure, one-pager and deck rules, competitor fairness and proof permissions.

1. **Questions first.** List the questions prospects ask most, with counts from `inputs/` ([scripts/tally.py](scripts/tally.py)), and which asset answers each. Build only assets that answer a real question.
2. **Battle cards.** One per alternative buyers weigh (including doing nothing): when buyers choose it, where it is genuinely better, where the offer is better and why, the proof, the question to ask, and the trap to avoid. Competitor facts are dated with a source or marked *to confirm*; no guesses about their prices or quality.
3. **One-pager.** For the person who signs and wasn't on the call: the problem in the buyer's words, what the offer does, price model as in `offer.md`, the guarantee as written, proof that exists in context or `inputs/` (including founder-reported operational metrics clearly labelled as founder-reported, plus sourced quotes), and the next step. State explicitly if there is no published client case study with written permission yet, and mark any willing reference clients or unapproved quotes as needing written permission before sharing.
4. **Deck (only if needed).** A few slides that follow the call, not a brand tour: their situation, the gap, how the offer closes it, proof, price and next step.
5. **Proof rules.** Use only proof in Proof stack or `inputs/` with the permission it has; client names and quotes need permission; reviews are quoted exactly with the source.
6. **Keep it current.** Who owns each asset, when it is reviewed, and what triggers an update (a competitor change, a new proof point).
7. **Approval.** The kit is a draft. Sharing assets with prospects or publishing competitor comparisons needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no competitor facts, prices, results, client names, quotes or claims that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/14-sales/14-sales-enablement-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Sales enablement kit: <business, date>
Skill: 14-sales-enablement · Date: <YYYY-MM-DD> · Framework: Battle cards / sales enablement
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing shared with prospects
## Questions buyers ask
| Question | Count (source) | Asset that answers it |
| --- | --- | --- |
## Battle cards
## One-pager
## Deck outline (if needed)
## Proof and permissions
## Owners and review dates
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/14-sales/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the assets built and the question each answers, the battle cards, and which proof needs permission, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every asset answers a counted buyer question.
- [ ] Battle cards are fair, say where the alternative is better, and date or mark *to confirm* every competitor fact.
- [ ] The one-pager carries price, guarantee and next step exactly as in `offer.md`.
- [ ] Proof is only what exists, with permissions stated; nothing is shared without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Give sales short, sourced answers to the questions buyers actually ask, be fair about the alternatives, and keep every asset current. Battle cards / sales enablement, The Complete Marketing System, section 14 Sales (Servidad, 2026); Obviously Awesome (April Dunford) for competitive alternatives.
