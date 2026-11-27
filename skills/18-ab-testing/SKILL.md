---
name: 18-ab-testing
description: Design and read A/B or multivariate tests with sample size, duration and decision rules. Use for A/B tests, split tests, sample size, test duration, is an A/B result statistically significant.
metadata:
  section: "18 Experimentation"
  covers: "A/B testing; Beat-the-control testing (Bencivenga); Keyed-ad testing (Hopkins); Multivariate testing; Sequential / Bayesian testing"
---
# A/B testing

An A/B test compares two versions on the same traffic at the same time so the difference can be credited to the change. It works when one change is tested against one primary metric, the sample size and duration are set from the baseline and the smallest effect worth acting on, the decision rule is written before launch, and the test runs to its planned end through full weekly cycles. It fails when tests are stopped the moment a tool says "winning", several metrics are checked until one looks good, traffic is too small to detect the effect, or a result from one season is treated as permanent.

Save the test design as a Markdown file in `work/18-experimentation/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Baseline traffic and conversion for the page or step in `inputs/` are the evidence.
- If present, also read `context/customer.md` → Beliefs, objections and drivers; `context/offer.md` → Core offer; traffic, conversion, past tests and tool notes in `inputs/`; any work in `work/18-experimentation/18-hypothesis-*.md` or `work/13-conversion/`.
- **No data:** Without baseline traffic and conversion, give the sample-size method and design structure in the reply, ask for visitors per day and the current conversion rate for the step tested, explain how to provide them (drop exports in `inputs/` or paste into chat), and state no sample size or duration. Write no test-design file until it arrives. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/ab-testing-guide.md](references/ab-testing-guide.md) for sample size, duration, decision rules, peeking, sequential and Bayesian options, and multivariate tests, and [references/testing-classics.md](references/testing-classics.md) for Hopkins's keyed-ad tracking and Bencivenga's beat-the-control testing discipline.

1. **One change, one metric.** Name the change, the audience and page, the primary metric (with its denominator) and guardrail metrics (for example refunds, cancellations).
2. **Sample size.** From the baseline rate and the minimum detectable effect worth acting on, compute visitors per arm by hand with the two-proportion formula (two-sided alpha 0.05, power 0.8: target rate = baseline × (1 + relative MDE); average rate = (baseline + target) ÷ 2; visitors per arm = (1.96 × √(2 × average × (1 − average)) + 0.84 × √(baseline × (1 − baseline) + target × (1 − target)))² ÷ (target − baseline)², rounded up), then duration from daily traffic, rounded up to whole weeks. If it takes too long, say so and propose a bigger change, a higher-traffic step or another method.
3. **Decision rule before launch.** Fixed-horizon (read once at the planned end, at the chosen significance and power), or a sequential or Bayesian method if the tool supports it properly; write the rule and what each outcome triggers.
4. **Read past tests honestly.** If a past test stopped early or was underpowered, say what it can and can't support.
5. **Multivariate testing.** Only when traffic supports every combination; usually not for small sites.
6. **QA and run.** Check both versions render and track before launch; no changes mid-test; note seasonality and promotions.
7. **Read.** Effect with its interval, the guardrails, and the decision per the rule; scope the learning to the conditions tested and log it (`18-experiment-log`).
8. **Approval.** The design is a draft. Launching the test or shipping a variant needs the owner's explicit approval.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, lifts, rates or significance that aren't computed from `inputs/`. Expected effects are assumptions. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with a hand tally (one line per item, counted one by one) or hand group totals (add each numeric column within the group, then divide for each ratio; a zero denominator is n/a), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/18-experimentation/18-ab-testing-<YYYY-MM-DD>-<slug>.md`:

```markdown
# A/B test design: <page, change>
Skill: 18-ab-testing · Date: <YYYY-MM-DD> · Framework: A/B testing (fixed horizon, or sequential / Bayesian with a written rule)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; not launched
## Change, audience, metrics
## Sample size and duration
| Baseline | Minimum detectable effect | Visitors per arm | Daily traffic | Weeks |
| --- | --- | --- | --- | --- |
## Decision rule
## Past tests: what they support
## QA and run rules
## How to read and log it
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, check every quotation in your file by hand: any quotation of four or more words must appear word for word in `inputs/` or another context file, ignoring case and punctuation (for an ellipsis or a [bracketed] insert, each part must appear). For every quotation that does not match, copy the source's exact words or drop the quotation marks, and check again until every quotation matches.

Reply with the file path, the sample size and duration with the arithmetic, the decision rule, and whether the traffic can decide this test, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] One change and one primary metric with guardrails.
- [ ] Sample size comes from baseline and minimum detectable effect via the two-proportion formula; duration is in whole weeks; undecidable tests change method.
- [ ] The decision rule is written before launch; no stopping on a tool's early winner unless a proper sequential method is used.
- [ ] Past underpowered or early-stopped tests are labelled as weak evidence.
- [ ] Learning is scoped and logged; nothing launches without approval.
- [ ] Quotation marks hold only exact source words, and every quotation was checked word for word against a source.
- [ ] No file in `context/` changed.

## Principle and source

Test one change against one metric, size the test before you start, decide how you will read it in advance, and run it to the end. A/B testing, Multivariate testing and Sequential / Bayesian testing, The Complete Marketing System, section 18 Experimentation (Servidad, 2026); keyed-ad testing, Scientific Advertising (Claude Hopkins); beat-the-control discipline (Gary Bencivenga); Trustworthy Online Controlled Experiments (Kohavi, Tang and Xu).
