---
name: 18-creative-testing
description: Test ad creative concepts first, then variations and iterations, and read results honestly. Use for creative testing, ad testing, which ad concepts to test next, ad fatigue, testing hooks/angles.
metadata:
  section: "18 Experimentation"
  covers: "Creative testing"
---
# Creative testing

Creative testing finds which messages and formats bring customers, then improves them. It works in layers: test different concepts (the idea, angle or format) first, then variations within the winning concept (hooks, openings, visuals), then small iterations. It works when each test has a hypothesis from the message and awareness map, budget is set so each concept gets a fair read, results are judged on the business outcome rather than clicks, and platform delivery skew is acknowledged. It fails when six captions on the same photo count as six concepts, the algorithm's spend split is taken as a verdict, or winners are declared on a handful of conversions.

Save the creative test plan as a Markdown file in `work/18-experimentation/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/message.md` → **Promise** (from `08-message-doc`) or `context/awareness.md` → **Awareness map**, from `03-awareness-map`: the messages and awareness levels concepts are built from.
- If present, also read `context/message.md` → Big idea, Proof stack, Objection map; `context/customer.md` → Voice of customer, Pains, desires and fears; `context/brand.md` → Distinctive assets; ad results, spend, outcomes and creative lists in `inputs/`; any work in `work/09-creative-strategy/` or `work/11-distribution/11-paid-social-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (reviews, tickets or interviews in `inputs/`): run `08-message-doc` or `03-awareness-map` first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Promise → `08-message-doc`; Awareness map → `03-awareness-map`), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If `08-message-doc` is not loaded, stop and say: enable mkt-q3-message.
- If `03-awareness-map` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/creative-testing-guide.md](references/creative-testing-guide.md) for concept, variation and iteration layers, budget per read, outcome metrics, platform delivery and fatigue.

1. **Read what ran.** From `inputs/`, list ads with spend, outcomes (cost per business outcome in the stated view) and how different they really are; count with [scripts/sum_by.py](scripts/sum_by.py). Say whether past tests compared concepts or only variations.
2. **Concepts first.** Draft three to five distinct concepts from the Promise, Big idea, Proof stack and the awareness levels (for example a problem-aware comparison, a product-aware review, a how-it-works demo), each with a hypothesis.
3. **Fair read.** Budget and structure so each concept gets enough spend for a read on the business outcome (a stated number of conversions), not only clicks. Note that platforms skew delivery toward early favourites; use separate ad sets or the platform's own A/B test tool (for example Meta's A/B test tool, marked *to confirm* or cited with URL and date) as fair-read options. Platform testing features are facts to cite with URL and date or mark *to confirm*.
4. **Then variations and iterations.** Within the winning concept: hooks, openings, visuals; then small edits. Each layer has its own hypothesis and read.
5. **Outcome and fatigue.** Check `inputs/` for any known tracking or pixel defects (such as a pixel firing on renewals) that inflate platform-reported counts and flag them before reading cost per outcome. Judge on cost per business outcome in a stated attribution view, plus a guardrail (customer quality, retention); watch frequency and falling results for fatigue.
6. **Log.** Record each test and what was learned (`18-experiment-log`); production briefs go to `09-creative-brief` or `09-ugc-brief`.
7. **Approval.** The plan is a draft. Launching ads or changing budgets needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, costs, conversion counts or platform behaviour that aren't in `context/` or `inputs/` or cited with a date. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/18-experimentation/18-creative-testing-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Creative test plan: <business, platform, period>
Skill: 18-creative-testing · Date: <YYYY-MM-DD> · Framework: Creative testing (concepts, then variations, then iterations)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; no ad launched, no budget changed
## What ran and what it shows
## Concepts to test
| Concept | Awareness level | Message source | Hypothesis |
| --- | --- | --- | --- |
## Structure and budget for a fair read
## Variations and iterations after a winner
## Outcome, guardrails and fatigue
## Platform facts
| Fact the plan relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/18-experimentation/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, what past ads did and didn't test, the concepts to test with hypotheses, and the budget and read rule, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Past ads are read for what they actually compared; variations are not called concepts.
- [ ] New concepts come from the Promise, proof and awareness levels, each with a hypothesis.
- [ ] Each concept gets a fair read on the business outcome; platform delivery skew is addressed; platform facts are dated or *to confirm*.
- [ ] Variations and iterations follow a winning concept.
- [ ] Results are judged on cost per business outcome with a guardrail; nothing launches without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Test big differences before small ones, give each idea a fair read on the outcome you are paid for, and do not let the algorithm's early spend split pick the winner. Creative testing, The Complete Marketing System, section 18 Experimentation (Servidad, 2026); Breakthrough Advertising (Eugene Schwartz) for awareness-level concepts.
