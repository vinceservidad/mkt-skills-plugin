---
name: 16-ugc-program
description: Run a UGC program with prompts, contests, creator seeding and featuring customers, with rights and rules. Use for user-generated content, customer photos, giveaways, contests, hashtag campaigns.
metadata:
  section: "16 Referral and Community"
  covers: "Giveaways / contests"
---
# UGC program

User-generated content is what customers make and share on their own: photos, videos, posts. A UGC program makes that easier and more frequent, and lets the business feature it. It works when the prompt fits a moment customers already enjoy, sharing is easy, the business asks before reusing anything, giveaways follow the law and platform rules, and the program is judged on reach to new buyers and sales, not likes. It fails when photos are reposted without permission, contests require tagging friends in ways platforms forbid, giveaways skip legal rules, or seeded customers are expected to post without disclosure. Briefs for content the business commissions belong to `09-ugc-brief`.

Save the UGC program plan as a Markdown file in `work/16-referral-community/` when the required inputs are present and the commercial terms are confirmed. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: whose content and whose audience matter.
- If present, also read `context/brand.md` → Distinctive assets, Voice; `context/customer.md` → Voice of customer; `context/offer.md` → Core offer, Bonuses; post counts, tags, permissions, giveaway ideas and budgets in `inputs/`; any work in `work/09-creative-strategy/09-ugc-brief-*.md` or `work/11-distribution/11-influencer-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (reviews, tickets or social posts in `inputs/`): run `02-icp-persona` first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (ICP and personas → `02-icp-persona`), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Prizes, free products for seeding, discounts and contest dates are the owner's commitments; the plan costs them and the owner sets them.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/ugc-guide.md](references/ugc-guide.md) for prompts, permissions and rights, giveaway and contest rules, seeding with disclosure, and measurement.

1. **What customers already post.** Count posts and tags from `inputs/` with [scripts/tally.py](scripts/tally.py) and note the moments they post (unboxing, first cup, a result).
2. **Prompts.** One or two prompts tied to those moments, with an easy way to share (a card in the box, a hashtag, a short ask in an email).
3. **Permission and rights.** Before reusing any post on the site, in emails or ads: ask the creator, record their yes, credit them, and state where it will run. Paid use in ads needs explicit rights.
4. **Featuring customers.** Where and how featured content appears, chosen for buyers who fit the ICP.
5. **Giveaways / contests.** If the owner wants one: entry method, eligibility, prize and its cost, dates, official rules, no purchase necessary where required, and platform promotion rules (for example limits on tag-a-friend or share-to-enter). Laws on sweepstakes and contests differ by place; verify and mark *to confirm*; flag legal review.
6. **Creator seeding.** Free product to customers who post often: no posting obligation, or if there is one, clear disclosure of the gift. Larger creator deals go to `11-influencer`.
7. **Measure.** Posts, reach to non-followers where the platform shows it, visits and orders from featured content or unique links, with counts; likes are signals.
8. **Approval.** The plan is a draft. Reusing posts, launching contests, shipping free product or contacting customers needs the owner's explicit approval.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no post counts, reach, results, prizes or customer content that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/16-referral-community/16-ugc-program-<YYYY-MM-DD>-<slug>.md`:

```markdown
# UGC program: <business, period>
Skill: 16-ugc-program · Date: <YYYY-MM-DD> · Framework: UGC program (prompts, permission, giveaways / contests, seeding)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing reused, launched or shipped
## What customers already post
## Prompts
## Permission and rights
## Featuring customers
## Giveaways and contests
## Seeding
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

Reply with the file path, what customers already post, the prompt, the permission process, the giveaway verdict, and the seeding rules, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Existing posts are counted and the moments they happen named.
- [ ] No content is reused without the creator's recorded permission; ad use needs explicit rights.
- [ ] Giveaways have official rules, costs and platform checks; laws are dated or *to confirm*; legal review is flagged.
- [ ] Seeding carries no undisclosed posting obligation.
- [ ] Success is reach to new buyers and orders with counts; nothing is launched without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Make it easy for customers to share the moments they already enjoy, ask before you reuse anything, run giveaways by the rules, and judge the program on new buyers reached. Giveaways / contests and UGC, The Complete Marketing System, section 16 Referral and Community (Servidad, 2026); platform promotion guidelines and FTC endorsement guidance (verify current versions).
