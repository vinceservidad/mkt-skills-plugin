---
name: 04-pmf-check
description: Test product-market fit by segment with Sean Ellis survey, cohort retention and word of mouth. Use for PMF, are customers sticking around, product vs marketing problem, ready to scale.
metadata:
  section: "04 Product"
  covers: "4Ps (McCarthy); 7Ps (services mix); Five Product Levels and 4Cs (Kotler); Kano model; Lean Startup / MVP; Product–market fit; Sean Ellis PMF test"
---
# PMF check

Fit is measured by retention and word of mouth, not by sales. Sales can be bought; customers who stay, who would be very disappointed to lose the product and who bring others cannot. This skill reads that evidence segment by segment, checks the product delivers the result it promises, and says where fit is strong, partial, absent or unknown, so marketing is pointed at customers the product already wins and is not used to speed up the refunds.

## Needs (read before writing)

- **Fit evidence**, in `inputs/`, elsewhere in the project, or pasted by the user. Any of these counts, and more kinds give a firmer verdict:
  - **Survey:** Sean Ellis survey responses (the disappointment question, ideally with main benefit, who benefits and improvements), with who was asked, when and how many answered;
  - **Retention:** a customer, subscriber or account log with start and end dates (or a cohort table), with the export date; reasons for leaving if recorded; revenue retention if there are fees;
  - **Word of mouth:** lead or signup sources (referral share), "have you recommended us" answers, unprompted reviews;
  - **Delivery:** evidence the core result happens: a service log, defect or support tickets, refunds, usage of the key feature.
- If present, also read:
  - `context/offer.md` → Core offer and Dream outcome, from `07-offer-design`: the product and the result whose fit you are testing.
  - `context/customer.md` → Segments (`02-segmentation`) and ICP and personas (`02-icp-persona`): the groups to split every signal by. Also Voice of customer and Research log.
  - Founder or owner claims (tenure, satisfaction, results): treat them as claims to check against the logs, not as evidence.
- Nothing upstream is required. If there is no fit evidence at all, the material is missing: write no verdict and no number, and write the measurement plan described under Output instead. Never state a survey score, retention rate, churn rate or referral share from memory, from a "typical" benchmark or from the user's impression.

## Process

Use [references/pmf-signals.md](references/pmf-signals.md) for the survey questions, how to read each signal, its limits and the verdict ladder, and [references/kotler-product-levels.md](references/kotler-product-levels.md) for Kotler's Five Product Levels and 4Ps-to-4Cs translation.

1. **Name what is being tested.** The product and its promised result (from `offer.md` if present, otherwise as the user states it, marked), the unit (customer, account, subscriber) and the segments to split by. Fit is for a product *and* a segment, never for the business in general.
2. **Score the survey,** if there is one, with [scripts/pmf_score.py](scripts/pmf_score.py) (`python3 <this skill's folder>/scripts/pmf_score.py <survey.csv> <answer column> <segment column>`), never by eye.
   - Report the very-disappointed share overall *and by segment*, each with its n and interval, the number asked, the response rate and who did not answer.
   - Check who was asked: people who have experienced the core product. Very new customers, churned customers and non-users answer different questions; say how many of each are in the sample.
   - The 40% line is Ellis's heuristic, not a law and not proof. Compare against it, name it as a heuristic, and say when the sample is too small to tell (an interval that straddles it).
   - Read the main benefit and the "who benefits" answers *of the very-disappointed group*: that is the result the fit rests on and the customer it rests with.
3. **Read retention** with [scripts/retention.py](scripts/retention.py) (`python3 <this skill's folder>/scripts/retention.py <log.csv> <YYYY-MM as-of> <segment column>`).
   - Per start cohort, retention at each age counted only over customers old enough to reach it (show the denominator). Cohorts too young to judge are *too young*, not good.
   - Look at the shape: a curve that flattens means a core that stays; one heading to zero means no fit yet for that group.
   - Sort the reasons for leaving: fit or price for the segment, product or delivery failure, external events (acquired, closed, hired in-house), involuntary (payment). Only fit and failure reasons speak to PMF.
   - Revenue retention needs fees by customer and month; if they are not there, say *unknown*.
   - Reproduce any claimed figure (median tenure, churn) from the log, or show why it cannot be reproduced, with both definitions. Keep the contradiction visible; do not pick the nicer number.
4. **Read word of mouth.** Referral share of new leads or signups, the referred close rate, the recommendation answers, unprompted reviews. Every share keeps its own denominator and period from the source.
5. **Check the product delivers.** Does the core result happen reliably (service log, defects, refunds, delivery or quality tickets)? For a service, check people, process and physical evidence too (7Ps). Sort improvement requests with the Kano model: a missing *basic* (it breaks trust) is a product fix before any marketing; *performance* and *delight* requests are roadmap input. Route price and packaging requests to `07-pricing`, and onboarding or activation friction to `15-onboarding`, without solving them here.
6. **Give the verdict by segment,** triangulating the signals:
   - **Strong signal:** survey at or above the heuristic with a usable n, a flattening retention curve, and real word of mouth, all in the same segment.
   - **Partial:** some signals agree, others are thin, young or contradictory.
   - **Not yet:** signals say this segment does not stay, would not miss it, or does not refer.
   - **Unknown:** the evidence does not say.

   Each verdict names its evidence and its biggest limit. A strong signal in one segment is not fit for the whole customer base. Say what it means for marketing: which segment to aim at and which to stop pulling in, and what to fix first (product, offer or onboarding owners). A verdict here is not permission to scale spend: scaling needs `19-scale-paid`'s readiness, economics and authorization gates.
7. **Plan the next read.** What would move each unknown or partial verdict: survey the segment again at a larger n, wait for a cohort to reach 12 months, record reasons for leaving, collect fees for revenue retention. Treat changes to the product as Lean Startup experiments (build, measure, learn) owned by `18-hypothesis`.
8. **Check before saving.** Re-read the draft against every item under Checks, and run `scripts/check_quotes.py` on it. Fix any failure before you save.

**Labels.** Every number is copied from a named source (with its date), *calculated* from named inputs by the bundled scripts or `python3` (show the formula or the command), or marked `(assumption)`. No unmarked inference; frequency words (*most*, *often*) need a count.

**Denominators.** Every "x of y" uses the source's own population and period: very disappointed out of respondents, respondents out of those asked, referrals out of that quarter's calls.

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from a source, with the source ID. Survey questions you propose, your own lines, labels for data you lack, and the titles of books, essays or talks (including in the Principle, framework, source block) go in italics, never in quotation marks. Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py <file>`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches. Counts of rows come from [scripts/tally.py](scripts/tally.py).

## Output

**With evidence**, write `work/04-product/04-pmf-check-<YYYY-MM-DD>-pmf.md`:

```markdown
# PMF check: <product> (<date>)
Skill: 04-pmf-check · Framework: Sean Ellis PMF survey; cohort retention; Product–Market Fit (Andreessen, Rachleff)
Product and promise tested: <from offer.md Core offer / Dream outcome, or as stated (assumption)>
Built from: <files and context sections used, with dates and status>
## Verdict by segment
| Segment | Survey (very disappointed, n, interval) | Retention | Word of mouth | Delivery | Verdict | Biggest limit |
| --- | --- | --- | --- | --- | --- | --- |
## Survey
<asked, answered, response rate, who is in the sample; scores by segment; the very-disappointed group's main benefit and who they say benefits; 40% as Ellis's heuristic>
## Retention
<cohort table with denominators; too-young cohorts; shape; reasons for leaving sorted; revenue retention known or unknown; claimed figures reproduced or not>
## Word of mouth
## Does the product deliver?
<core result evidence; 7Ps for services; Kano sort of requests; routed to owners>
## What this means for marketing
<segment to aim at, segment to stop pulling in, what to fix first and its owner skill; not a scaling decision>
## Contradictions and open questions
## Next read
<what to collect, when, and what would change each verdict>
## Claims and sources
| Claim or number | Source or calculation |
| --- | --- |
## Principle, framework, source
```

**Without evidence**, write `work/04-product/04-pmf-check-<YYYY-MM-DD>-plan.md`: the product and segments to test, the survey to send (the questions in italics, who to send it to, what n to aim for and why), the retention data to export (customer log with start and end dates, reasons for leaving, fees), the word-of-mouth signals to pull (lead sources, reviews), and how each will be read. State no score, rate or share.

Change nothing in `context/`. This is a diagnosis, not a context decision; segment, offer and pricing changes go to their owners.

Reply, with evidence, with:
- the verdict by segment in one or two lines;
- the most important limit of the evidence;
- the one thing to fix or measure next, and its owner skill.

Reply, without evidence, with the plan's path and a plain list of the material to bring (survey responses with who was asked; a customer log with start and end dates; lead sources or referral counts; delivery records) and how to provide it: save the files in `inputs/` or paste them, then ask again.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every signal is split by segment, and the verdict is per segment, never one verdict for the whole business.
- [ ] The survey score comes from `pmf_score.py` with n, interval, number asked and response rate; the 40% line is called Ellis's heuristic, and a small or skewed sample is named.
- [ ] Retention is by cohort with eligible denominators; too-young cohorts are labelled, reasons for leaving are sorted, and revenue retention is stated or marked unknown.
- [ ] Owner or founder claims are reproduced from the data or shown not to reproduce, with the contradiction kept visible.
- [ ] Word-of-mouth shares keep their source's denominator and period.
- [ ] Delivery of the core result is checked; product, price and onboarding issues are routed to their owner skills, not solved here.
- [ ] No verdict is turned into a scaling or spend decision.
- [ ] No score, rate or benchmark is invented; without evidence, the file is a plan with no numbers.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Fit is measured by retention and word of mouth, not by sales: find the segment that would be very disappointed to lose the product, stays and brings others, make sure the product delivers its result there, and only then let marketing amplify it. Sean Ellis PMF survey (Sean Ellis; Hacking Growth, Ellis & Brown); Product–Market Fit (Marc Andreessen, "The only thing that matters"; Andy Rachleff); Five Product Levels and 4Ps-to-4Cs (Philip Kotler, Marketing Management); The Complete Marketing System, section 4 Product (Servidad, 2026).
