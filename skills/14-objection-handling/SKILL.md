---
name: 14-objection-handling
description: Prepare live answers to sales objections and the order to handle them in. Use for handling objections on calls, too expensive, not ready, need to think about it, talk to my partner.
metadata:
  section: "14 Sales"
  covers: "Objection handling (live)"
---
# Objection handling

An objection on a call is usually a question the buyer hasn't been able to ask yet. Live objection handling works when the seller acknowledges it, asks what is behind it, answers the real concern with something true, and checks it landed. It fails when the seller argues, answers the wrong objection, repeats a canned line, discounts the moment price comes up, or pushes past a clear no. The written objection map (which beliefs to rebuild in copy) belongs to `08-objection-map`; this skill prepares what is said live, in what order, and when to walk away.

Save the objection playbook as a Markdown file in `work/14-sales/` when the required inputs are present and the commercial terms are confirmed. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/message.md` → **Objection map** (from `08-objection-map`) or `context/customer.md` → **Beliefs, objections and drivers**, from `02-buyer-psychology`: the objections buyers raise and the beliefs behind them.
- If present, also read `context/offer.md` → Core offer, Price and model, Guarantee, Bonuses, Urgency and scarcity; `context/message.md` → Proof stack, Story; `context/customer.md` → Voice of customer, Current alternatives; call notes, lost reasons and how objections are handled today in `inputs/`; any work in `work/14-sales/14-sales-script-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (call notes, sales notes or interviews in `inputs/`): run `02-buyer-psychology` (or `08-objection-map` if the beliefs exist) first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Objection map → `08-objection-map`; Beliefs, objections and drivers → `02-buyer-psychology`), and ask for evidence, not a description. Write nothing and do **not** include a generic objection-handling approach or partial playbook in the reply. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Discounts, payment plans, fee waivers, extra guarantees and free extras offered to answer an objection are the owner's commitments. Use only what `offer.md` holds; if the request asks to include a new concession or payment plan not in `offer.md`, **stop and withhold the deliverable file** (write nothing to `work/14-sales/`): ask the owner to confirm the exact terms (schedule, eligibility, fee waiver, margin impact) before writing it, and never discount by default. End the stop reply with the **Principle, framework, source** block.
- If `08-objection-map` is not loaded, stop and say: enable mkt-q3-message.
- If `02-buyer-psychology` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/objection-guide.md](references/objection-guide.md) for the acknowledge, ask, answer, check pattern, objection types and when to walk away.

1. **Rank objections by evidence.** Count objections and lost reasons from `inputs/` and context with [scripts/tally.py](scripts/tally.py). Order the playbook by how often each appears and how often it ends a deal.
2. **Classify each.** Real misfit (the buyer is outside the ICP or needs something the offer doesn't do), missing information, a belief to rebuild, a risk to reverse, timing, or a stall hiding another objection. The handling differs; say which.
3. **Prevent before answering.** For the top objections, name where in the call or the materials it should be answered before it comes up (discovery question, proof shown early, guarantee stated).
4. **Live answer per objection.** Acknowledge, ask what is behind it (one question), answer with something true from context (proof that exists, the guarantee as written, the mechanism, the cost of the problem the buyer stated), and check it landed. Write it as a short guide, not a script to read.
5. **Price.** Explore value and the cost of the problem first; compare with the buyer's real alternatives from context. Use only the price bands, guarantee and payment options in `offer.md`. No reflex discount.
6. **Not ready and think about it.** Ask what would need to be true to decide, and what waiting costs. Agree a dated next step or close the file politely.
7. **Other deciders.** Offer to meet the other person and give the champion what they need; don't close around them.
8. **Walk away.** When the objection is a real misfit, say so plainly and recommend what fits instead.
9. **Approval.** The playbook is a draft. Using it on calls or offering any concession needs the owner's explicit approval.
10. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no proof, results, client names, guarantees, discounts or buyer quotes that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/14-sales/14-objection-handling-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Objection playbook: <business, offer>
Skill: 14-objection-handling · Date: <YYYY-MM-DD> · Framework: Objection handling (live): acknowledge, ask, answer, check
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; not yet used on calls
## Objections ranked
| Objection | Count (source) | Type | Ends deals? |
| --- | --- | --- | --- |
## Prevent it earlier
## Live answers
## Price
## Not ready, think about it, other deciders
## When to walk away
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/14-sales/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the top objections with counts, the live answer for each, and where each is prevented earlier, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Objections are ranked by counts from the evidence, with their type.
- [ ] Each live answer acknowledges, asks, answers with something true, and checks.
- [ ] Price answers explore value and real alternatives; no discount or concession outside `offer.md`.
- [ ] Not ready and other-decider objections get a dated next step or a meeting with the decider; misfits get a polite exit.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Treat every objection as a question: find what is behind it, answer it with something true, and walk away from a real misfit. Objection handling (live), The Complete Marketing System, section 14 Sales (Servidad, 2026); acknowledge-ask-answer from consultative selling; Hormozi's CLOSER (Explain away concerns).
