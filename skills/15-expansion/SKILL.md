---
name: 15-expansion
description: Plan upsell, cross-sell, fee-band moves and account expansion from usage and value ladder. Use for upselling, cross-sell, moving clients up a tier or fee band, account growth, B2B account management.
metadata:
  section: "15 Retention"
  covers: "Account management (B2B); Expansion playbook (upsell / cross-sell)"
---
# Expansion

Expansion grows revenue from customers who are already getting value: a higher tier, an added service, more seats. It works when the offer matches a need the customer has shown (a question they asked, growth in usage, a new problem), the timing follows a success rather than a renewal threat, the next offer exists and can be delivered, and the result is counted in net revenue retained. It fails when everyone is pushed the same upsell, an offer with no price or capacity is sold, or expansion targets customers who are not yet getting the core value.

Save the expansion playbook as a Markdown file in `work/15-retention/` when the required inputs are present and the commercial terms are confirmed. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Value ladder**, from `07-value-ladder`: what customers can move up to and what moves them.
- If present, also read `context/offer.md` → Core offer, Price and model, Guarantee; `context/customer.md` → Jobs to be done, Segments, ICP and personas, Voice of customer; account data, usage, questions asked, renewal terms and capacity in `inputs/`; any work in `work/15-retention/15-churn-prevention-*.md` or `work/14-sales/`.
- If a required section is missing:
  - **The upstream evidence exists** (account data, sales notes or interviews in `inputs/`): run `07-value-ladder` first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Value ladder → `07-value-ladder`), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Prices for new tiers or services, discounts, contract changes and delivery capacity are the owner's commitments. If the next step on the ladder has no price or definition, stop before selling it, ask for the exact terms, and plan the triggers and a pilot without it.
- If `07-value-ladder` is not loaded, stop and say: enable mkt-q2-offer.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/expansion-guide.md](references/expansion-guide.md) for expansion signals, account management, the offer conversation and net revenue retention.

1. **Who is ready.** From account data in `inputs/`, list accounts with expansion signals (asked about the next offer, usage or size growth, a band change, high engagement) and those that are not yet getting core value (low engagement, recent problems). Count with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py).
2. **Is the next step real?** Check the Value ladder: is the upsell or cross-sell defined, priced and deliverable within capacity? If not, design a small pilot with a few ready accounts and leave the price to the owner.
3. **Triggers.** For each expansion path: the signal that starts it, who acts (the account manager, the founder), the conversation, and the next step. Tie each to a success moment (a good quarter, a goal reached), not a renewal or a complaint.
4. **Account management (B2B).** For key accounts: owner, review rhythm, health signals, and a simple account plan (goals, risks, opportunities).
5. **Contract terms.** Apply existing terms honestly (a fee change at renewal when revenue moves up a band, as the contract says); no surprise price rises.
6. **Measure.** Expansion revenue, contraction and churn per period; net revenue retention computed from the accounts with the arithmetic shown; accepted versus declined offers.
7. **Approval.** The playbook is a draft. Offering anything to a client, changing prices or contracts needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no prices, account facts, results or capacity that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/15-retention/15-expansion-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Expansion playbook: <business, period>
Skill: 15-expansion · Date: <YYYY-MM-DD> · Framework: Expansion playbook (upsell / cross-sell) and account management
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing offered or changed
## Accounts by readiness
| Account | Signals (evidence) | Getting core value? | Ready for |
| --- | --- | --- | --- |
## Is the next step real?
## Triggers and conversations
## Account management
## Contract terms
## How we measure it
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/15-retention/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the accounts ready to expand and why, whether the next offer is ready to sell, and the first pilot or trigger, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Readiness comes from account signals, counted; accounts not getting core value are excluded.
- [ ] The next offer is defined, priced and deliverable, or a pilot is proposed with the price left to the owner.
- [ ] Triggers follow success moments; existing contract terms are applied as written.
- [ ] Measurement covers expansion, contraction, churn and net revenue retention with the arithmetic shown; nothing is offered without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Offer more only to customers already getting value, when they have shown the need, with an offer that is real and deliverable, and measure net revenue kept. Expansion playbook and account management, The Complete Marketing System, section 15 Retention (Servidad, 2026); Value Ladder (Russell Brunson, DotCom Secrets).
