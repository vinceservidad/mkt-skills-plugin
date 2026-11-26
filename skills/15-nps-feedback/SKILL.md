---
name: 15-nps-feedback
description: Run NPS, CSAT and CES surveys and route the feedback to fixes, product and offer. Use for NPS, customer satisfaction surveys, CSAT, customer effort score, closing the loop on feedback.
metadata:
  section: "15 Retention"
  covers: "CSAT / CES; NPS"
---
# NPS and feedback

A satisfaction score is only worth collecting if someone acts on it. NPS, CSAT and CES each answer a different question (would you recommend us, were you happy with this, how easy was this), and each is noisy on its own. Feedback works when the right question is asked at the right moment, response rates and who answered are reported with the score, comments are tagged and counted, detractors and unhappy customers get a reply, and themes go to the team that can fix them. It fails when the score becomes the goal, surveys go out too often, comments are never read, or a small sample is treated as everyone.

Save the feedback plan as a Markdown file in `work/15-retention/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Survey results, comments, tickets and reviews in `inputs/` are the evidence.
- If present, also read `context/customer.md` → ICP and personas, Voice of customer, Segments; `context/offer.md` → Core offer; survey exports, comments, tickets and reviews in `inputs/`; any work in `work/15-retention/15-churn-prevention-*.md` or `work/16-referral-community/16-reviews-*.md`.
- **No data:** When `inputs/` has no survey results or NPS comments yet (even if `inputs/` already holds sample reviews or ticket notes), write no deliverable file; design the first survey (question, moment, audience, frequency, detractor reply plan) in the reply, ask for the full ticket/support exports and any survey results or reviews needed to work on, and explicitly state **in the reply itself how to provide the material** (save exports in `inputs/` or paste them into chat); invent no score or response rate. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/feedback-guide.md](references/feedback-guide.md) for when to use NPS, CSAT or CES, survey timing and frequency, scoring, tagging and closing the loop.

1. **Read the results.** Compute the score from the counts (NPS = % promoters − % detractors) with the arithmetic shown, the response rate and the sample, using [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py). Label who answered (self-selected) and what that can and can't show.
2. **Themes.** Tag and count comments by theme; link each theme to the evidence elsewhere (tickets, exit reasons) and to its owner (operations, product, offer, onboarding).
3. **Choose the measures.** NPS for the overall relationship, at a steady interval; CSAT right after a specific interaction; CES after a task (support, setup, cancel). Say which and why; no business needs all three at once.
4. **Timing and frequency.** Survey each customer at most at the interval the plan sets, not every month by default; transactional surveys follow the event.
5. **Close the loop.** Who replies to detractors and unhappy customers, how fast and with what; when promoters are asked for a review or referral (`16-reviews`, `16-referral-program`).
6. **Route and report.** Themes to owners with counts each period; the score trend with response rates; what changed because of feedback. Never drop comment themes or mark them owner-only even if asked to report only the score: state plainly that the score alone never shows what to fix, keep every counted theme in the main team report and plan, and assign an owner to every theme row (including "Other" -> triage owner).
7. **Approval.** The plan is a draft. Sending surveys or contacting customers needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no scores, response rates, themes or quotes that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/15-retention/15-nps-feedback-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Feedback plan: <business, period>
Skill: 15-nps-feedback · Date: <YYYY-MM-DD> · Framework: NPS, CSAT and CES (ask, tag, route, close the loop)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing sent
## Results
| Measure | Score (calculated) | Responses / sent | Who answered |
| --- | --- | --- | --- |
## Themes
| Theme | Count | Also seen in | Owner |
| --- | --- | --- | --- |
## Which measures, when
## Frequency
## Closing the loop
## Routing and reporting
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/15-retention/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the score with its arithmetic and response rate, the top themes and owners, and the survey rhythm, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The score is calculated from counts with the response rate and sample labelled.
- [ ] Comments are tagged and counted, linked to other evidence and given owners.
- [ ] Each measure (NPS, CSAT, CES) is used for its own question and moment; frequency is limited.
- [ ] Detractors get a reply with an owner and a time; promoters are routed to reviews or referrals.
- [ ] Reporting shows trend, response rate and actions taken; nothing is sent without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Ask the right question at the right moment, report who answered, read every comment, reply to the unhappy, and send each theme to the team that can fix it. NPS (Fred Reichheld, The Ultimate Question), CSAT and CES (Dixon, Freeman and Toman, Stop Trying to Delight Your Customers); The Complete Marketing System, section 15 Retention (Servidad, 2026).
