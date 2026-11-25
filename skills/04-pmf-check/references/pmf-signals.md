# PMF signals: how to collect and read them

Each signal answers one question. None of them alone proves fit; agreement across signals in one segment is the strongest evidence this skill can give. Classify what you write: the Ellis 40% line is a **heuristic**, a retention curve is a **pattern** in observed data, and "product–market fit" is a **framework** for reasoning, not a measured fact.

## 1. Sean Ellis PMF test (the survey): would they miss it?

**The questions** (propose them in italics, never as quotations):
1. *How would you feel if you could no longer use <product>?* Very disappointed · Somewhat disappointed · Not disappointed (it isn't really that useful) · N/A, I no longer use it.
2. *What type of people do you think would most benefit from <product>?*
3. *What is the main benefit you receive from <product>?*
4. *How can we improve <product> for you?*
5. Optional: *What would you use instead if <product> were no longer available?* and *Have you recommended <product> to anyone?*

Questions 2 to 4 follow the version Rahul Vohra described for Superhuman's product-market fit engine; question 1 is Ellis's.

**Who to ask.** People who have experienced the core of the product: for software, active users who have used it more than once recently; for a service, customers who have received the core result at least once (a delivered month, a finished project). Exclude, or report separately, brand-new customers who have not yet had the result, churned customers and people who never used it. Record how many were asked, how many answered and who did not: owners who are unhappy answer surveys less often (assumption: non-response bias runs in either direction; say it is unknown).

**Scoring.** Very-disappointed answers ÷ valid answers (N/A excluded and counted). Run `scripts/pmf_score.py` overall and by segment. Report the 95% interval it prints: with 14 answers, a 71% score has an interval of roughly 45% to 88%; with 4 answers, the interval is too wide to say anything.

**The 40% line.** Ellis reported that products which went on to grow well tended to score at or above 40% very disappointed. It is a heuristic from his experience, not a law, not a peer-reviewed threshold and not proof of fit. Use it as a reference line; never write "PMF achieved" from a score alone.

**What to read next.** The answers of the very-disappointed group to questions 2 and 3 tell you who the product is really for (the high-expectation customer) and what result it rests on. The somewhat-disappointed group's improvement answers are the nearest roadmap; the not-disappointed group often shows a segment to stop pulling in.

## 2. Retention: do they stay?

**Cohorts.** Group customers by start period. For each age (3, 6, 12, 24 months, or weeks for a product used weekly), count retained ÷ customers old enough to reach that age. A cohort that has not reached an age is *too young*, not *100%*. `scripts/retention.py` does this from a log with start and end months.

**Shape.** Plot or read the curve per cohort. A curve that drops and then flattens means a group stays; one that keeps falling toward zero means no fit yet for that group. Do not quote a benchmark retention rate for the category; compare cohorts and segments with each other.

**Reasons for leaving.** Sort them before reading anything into churn:
- *Fit or price for the segment* (too small, needed less): a targeting or packaging signal, often outside the core segment.
- *Product or delivery failure* (late, wrong, broken): a product signal; fix before marketing.
- *External events* (acquired, closed, hired in-house, moved to a different kind of solution): real loss, weak evidence about fit.
- *Involuntary* (failed payment): an operations signal, not fit.

**Tenure.** Tenure of active customers is still growing (censored). A median tenure "to date" is not a lifetime, and it changes with how many new customers just joined. When a claimed figure (say, a founder's median tenure) does not reproduce from the log, show both definitions and keep the gap visible.

**Revenue retention** (net or gross) needs fees per customer per period. Without them it is unknown.

## 3. Word of mouth: do they bring others?

- Share of new leads, calls or signups from referrals, with its period and denominator.
- Close or conversion rate of referred leads against other sources (each with its own denominator).
- "Have you recommended us?" answers, split by the disappointment answer.
- Unprompted reviews or mentions, counted, with dates.

Word of mouth that exists only because of a paid referral incentive is weaker evidence than unprompted referral; say which it is if known.

## 4. Does the product deliver the core result?

Fit cannot survive a product that does not reliably do the thing. Check the delivery record:
- the core result's own log (on-time delivery, closes, shipments, uptime);
- defects, refunds, delivery or quality complaints, with counts and periods;
- usage of the key feature or deliverable.

**4Ps and 7Ps.** The 4Ps (McCarthy) place Product beside Price, Place and Promotion; in this library Price lives in Offer, Place in Distribution and Promotion in Message, so this skill looks only at Product. For services, Booms & Bitner's 7Ps add People (who delivers), Process (how reliably) and Physical evidence (what the client sees: reports, dashboards): check each for the core result.

**Kano model.** Sort requests and complaints:
- *Basic* (must-be): expected; absence causes dissatisfaction, presence earns no credit (a close that is on time, a bag that arrives before the last one runs out). A failing basic is the first fix.
- *Performance*: more is better, linearly (faster answers, more detail).
- *Delight* (attractive): unexpected, creates enthusiasm, absence is not missed.
- *Indifferent* or *reverse*: no effect, or some segments dislike it (too much reporting for a small studio).

Classify from the evidence you have and mark the class `(assumption)` unless a Kano questionnaire was run.

## 5. Verdict ladder

| Verdict | When |
| --- | --- |
| Strong signal | In one segment: survey at or above the heuristic with an interval mostly above it, a retention curve that flattens over cohorts old enough to show it, and real word of mouth. |
| Partial | Some signals agree; others are thin (small n), young (cohorts not old enough) or contradictory. |
| Not yet | This segment would not miss it, does not stay or does not refer. |
| Unknown | The evidence does not cover it. |

Name the biggest limit beside each verdict. Fit in one segment says nothing about another, and it does not authorize spending more: that is a growth and economics decision with its own gates.

## 6. Lean Startup: what to do with a "not yet"

Treat each change to the product as an experiment (Ries): state what you will build or change, the signal that would show it worked (a segment's very-disappointed share, a cohort's 3-month retention), the window, and the stopping rule. The smallest version that tests the assumption is the MVP. Experiment design and logging belong to `18-hypothesis` and `18-experiment-log`.

## Sources

Sean Ellis, the PMF survey (and Hacking Growth, Ellis & Morgan Brown, 2017); Marc Andreessen, "The only thing that matters" (2007); Andy Rachleff on product–market fit; Rahul Vohra, "How Superhuman built an engine to find product/market fit" (First Round Review, 2018); Eric Ries, The Lean Startup (2011); Noriaki Kano, attractive quality and must-be quality (1984); E. Jerome McCarthy, Basic Marketing (1960); Bernard Booms & Mary Jo Bitner (1981).
