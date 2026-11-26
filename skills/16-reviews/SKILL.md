---
name: 16-reviews
description: Build review systems, one-click asks, Trustpilot/Google bad-review replies. Use for review plans, getting reviews, Trustpilot replies, or refusing/replacing staff or fake review requests.
metadata:
  section: "16 Referral and Community"
  covers: "Reviews"
---
# Reviews

Reviews are proof buyers trust more than anything the business says. A review system works when every customer is asked at a moment they have felt the value, leaving a review takes one click, every review gets a reply (the bad ones most of all), and complaints feed fixes. It fails when only happy customers are asked where the platform forbids it, reviews are bought or rewarded for being positive, fake or staff reviews are posted, or criticism is ignored. Platform rules and consumer-protection law on reviews are strict.

Save the review system as a Markdown file in `work/16-referral-community/` when the required inputs are present and the commercial terms are confirmed. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Existing reviews, ratings, ticket themes and the customer journey in `inputs/` and context are the evidence.
- If present, also read `context/brand.md` → Reputation, Voice; `context/awareness.md` → Journey (the moment of value); `context/customer.md` → Voice of customer; review exports, ratings, platforms, NPS results and tickets in `inputs/`; any work in `work/15-retention/15-nps-feedback-*.md` or `work/05-brand/05-reputation-*.md`.
- **No data:** Without existing reviews or customer data, still design the complete review request system (moment, channel, one-click link, wording, reply plan, and rules against review gating, fake/staff reviews, and incentives) in the reply or `work/16-referral-community/16-reviews-<YYYY-MM-DD>-plan.md` while inventing no ratings or counts. Ask where reviews live today and how to provide any exports (drop files in `inputs/` or paste into chat). End with the **Principle, framework, source** block.
- **Owner commitments.** Any incentive tied to reviews is the owner's commitment and must be checked against platform rules and law before it is used; never one that depends on the review being positive.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/reviews-guide.md](references/reviews-guide.md) for where reviews matter, the ask, one-click links, replies, and what platforms and law forbid.

1. **Where reviews are.** Count reviews and ratings by platform and stars from `inputs/` with [scripts/tally.py](scripts/tally.py); note which are unanswered and which platforms buyers see.
2. **The moment.** Pick the moment of felt value from the Journey or NPS data and ask then, by the channel the customer agreed to.
3. **Ask everyone.** Ask all customers at that moment, not only promoters, where the platform forbids review gating; never filter who is asked by what they will say. Platform rules on solicitation are facts to cite with URL and date or mark *to confirm*.
4. **One click.** A direct link to the review form, a short ask in the brand's voice, one reminder at most.
5. **Incentives.** No reward for positive reviews; many platforms forbid any incentive. If the owner wants an incentive, check platform rules and law first and mark *to confirm*.
6. **Reply to every review.** Thank positive ones specifically; answer negative ones publicly with the fix or a way to reach a person, without arguing or sharing private details. Route complaint themes to their owners.
7. **Measure.** Reviews per 100 customers asked, rating trend, reply rate and time, complaint themes fixed.
8. **Approval.** The system is a draft. Sending review requests, posting replies or offering incentives needs the owner's explicit approval.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no reviews, ratings, review counts or customer words that aren't in `context/` or `inputs/`. Never write reviews for customers or staff to post: if asked to write fake or staff reviews to add to the review plan, still write the review system deliverable file in `work/16-referral-community/` refusing the fake/staff reviews (marking FTC/platform rules with verified official URLs and dates or *to confirm*), counting real reviews from `inputs/`, and planning honest replies to negative reviews plus an all-customer ask at a moment of value (with zero fabricated review text). Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/16-referral-community/16-reviews-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Review system: <business, date>
Skill: 16-reviews · Date: <YYYY-MM-DD> · Framework: Reviews (ask at delight, one click, reply to every review)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing sent or posted
## Where reviews are
| Platform | Reviews | Rating | Unanswered | Buyers see it? |
| --- | --- | --- | --- | --- |
## When and how we ask
## The request
## Incentives and rules
## Replies
## Complaint themes and owners
## Platform and legal facts
| Fact the plan relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## How we measure it
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/16-referral-community/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, where reviews stand, the moment and channel for the ask, the reply plan, and any rule that blocks the owner's idea, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Reviews are counted by platform and stars; unanswered reviews are listed.
- [ ] Everyone is asked at the moment of value where gating is forbidden; nobody is filtered by expected sentiment.
- [ ] No reward for positive reviews; incentives are checked against rules or marked *to confirm*.
- [ ] Every review gets a reply; negative ones get a public fix or contact without private details.
- [ ] Platform and legal facts are dated or *to confirm*; nothing is sent or posted without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Ask every customer at the moment they feel the value, make it one click, reply to every review, and never buy, filter or fake them. Reviews, The Complete Marketing System, section 16 Referral and Community (Servidad, 2026); FTC rule on fake reviews and testimonials (2024; verify current status) and platform review policies.
