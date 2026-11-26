---
name: 18-hypothesis
description: Write test hypotheses, ICE/PIE/RICE backlogs and minimum viable tests. Use for test ideas, hypotheses, prioritizing experiments, what to test first, smallest test to check an idea, growth backlog.
metadata:
  section: "18 Experimentation"
  covers: "Build–Measure–Learn; Hypothesis format; ICE / RICE / PIE; Minimum Viable Test"
---
# Hypotheses and prioritization

A hypothesis turns an idea into a test someone can lose. It works when it names the change, who sees it, the metric that will move and by how much, and the evidence behind the belief; when ideas are scored on the same scale with the evidence for each score shown; and when the first tests are ones the traffic can actually decide. It fails when the backlog is a list of opinions, button colours outrank customer problems, scores are invented to justify a favourite, or tests are picked that would take a year to read.

Save the test backlog as a Markdown file in `work/18-experimentation/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Ideas, traffic and conversion data, research and past results in `inputs/` and context are the evidence.
- If present, also read `context/customer.md` → Pains, desires and fears, Beliefs, objections and drivers, Voice of customer; `context/message.md` → Objection map; `context/offer.md` → Core offer; idea lists, traffic, conversion, tickets, research and past tests in `inputs/`; any work in `work/18-experimentation/18-experiment-log-*.md` or `work/13-conversion/13-cro-audit-*.md`.
- **No data:** Without an idea list or traffic data in `inputs/`, write no scored backlog file; if `context/` holds evidence, draft starter hypotheses from that evidence only (labelled as context-only drafts) in the reply, give the hypothesis template and scoring rules, ask for the idea list, traffic and conversion by page, and any research, and explain how to provide them (drop files in `inputs/` or paste into chat). End with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/hypothesis-guide.md](references/hypothesis-guide.md) for the hypothesis format, ICE, PIE and RICE scoring, minimum viable tests and what traffic can decide.

1. **Collect and clean.** List every idea; merge duplicates; drop ideas that are not tests (fixes to obvious bugs ship without a test) and say so; flag price or discount ideas as owner commitments and route them to `18-price-testing`.
2. **Hypothesis format.** For each: *Because we see [evidence], we believe [change] for [audience] will move [metric] by [expected size]; we'll know when [measure] after [duration].* The evidence names its source; an idea with none is marked *opinion*. Only mark an idea as evidenced when a specific ticket count, review or data finding in `inputs/` or `context/` directly supports it; mark ideas with no direct evidence (such as FAQ rewrites, hero photos or button colours) as *opinion* — never stretch unrelated tickets as indirect evidence.
3. **Score.** Use one framework for the whole list (ICE: impact, confidence, ease; PIE: potential, importance, ease; RICE: reach, impact, confidence, effort) and show the reason for each score. Confidence comes from evidence, not enthusiasm.
4. **Can the traffic decide it?** For the top ideas, check the sample the metric needs against traffic (see `18-ab-testing`); ideas the traffic can't decide in a reasonable time become a bigger change, a different metric, or a non-A/B method (Minimum Viable Test, qualitative check, before-after with caution).
5. **Minimum Viable Test.** For each top idea, the smallest test that would teach the most (a fake-door, a manual version, a survey, a page variant).
6. **Build–Measure–Learn.** The order to run them and what each result would change next.
7. **Approval.** The backlog is a draft. Launching tests or changing live pages needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no traffic, conversion rates, expected lifts presented as fact, or evidence that isn't in `context/` or `inputs/`. Expected sizes are labelled assumptions. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/18-experimentation/18-hypothesis-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Test backlog: <business, date>
Skill: 18-hypothesis · Date: <YYYY-MM-DD> · Framework: Hypothesis format with ICE / PIE / RICE (<chosen>); Build–Measure–Learn
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; no test launched
## Ideas cleaned
## Hypotheses
| # | Hypothesis | Evidence (source) or opinion | Metric |
| --- | --- | --- | --- |
## Scores
| # | Score parts with reasons | Total |
| --- | --- | --- |
## Can the traffic decide it?
## Minimum viable tests
## Order and what each result changes
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/18-experimentation/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the top three tests with their hypotheses and scores, which ideas the traffic can't decide, and the first minimum viable test, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every idea is a hypothesis with evidence named or marked *opinion*.
- [ ] One scoring framework is used with a reason for each score; confidence comes from evidence.
- [ ] Top ideas are checked against the traffic needed; undecidable ones change method.
- [ ] Each top idea has a minimum viable test and a next step for each outcome.
- [ ] Expected sizes are labelled assumptions; nothing launches without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Turn ideas into hypotheses someone can lose, score them on evidence, run first what your traffic can actually decide, and let each result choose the next test. Build–Measure–Learn (Eric Ries, The Lean Startup), ICE (Sean Ellis), PIE (WiderFunnel), RICE (Intercom); The Complete Marketing System, section 18 Experimentation (Servidad, 2026).
