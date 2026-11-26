---
name: 11-social
description: Plan organic social platforms, formats, cadence and community replies. Use for social media strategy, organic posting plans, Instagram, LinkedIn or TikTok, or posts getting likes without leads.
metadata:
  section: "11 Distribution"
  covers: "Social media marketing"
---
# Social

Organic social is borrowed attention on a platform you don't control. It works when the business shows up where its buyers already are, in the platform's native format, gives useful things far more often than it asks, answers the people who reply, and turns the attention into subscribers it owns. It fails when a business posts everywhere, chases reach from the wrong audience, or keeps a cadence for six weeks and then goes silent.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`.
- If present, also read `context/brand.md` → **Voice** (from `05-brand-voice`); `context/customer.md` → Pains, desires and fears, Jobs to be done, Voice of customer and Segments; `context/awareness.md` → Journey, Awareness map and Traffic temperature; `context/offer.md` → Core offer and Value ladder (free steps that exist); `context/message.md` → Big idea, Message house and Story; any post analytics, follower data, comment logs or capacity notes in `inputs/`; any work in `work/11-distribution/11-content-strategy-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (interviews, reviews or call notes in `inputs/` but no ICP): run `02-icp-persona` first, then continue.
  - **It doesn't:** stop. Name the missing section with the skill that fills it (ICP and personas → `02-icp-persona`), and ask for evidence (interviews, reviews, sales-call notes), not a description of the buyer. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- No `brand.md` Voice: say *no brand voice on file*, keep to what the evidence supports (the buyer's own words, words customers distrust), and suggest `05-brand-voice`.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/social-guide.md](references/social-guide.md) for the analytics read, the series and reply rules, and platform claims, and [references/meta-organic-and-algorithm-fit.md](references/meta-organic-and-algorithm-fit.md) for Facebook Page, Instagram Profile and Business Suite readiness, communication jobs, distribution fit, and the organic-to-paid creative bridge.

1. **Platforms.** Choose one or two where the evidence puts the ICP (lead sources, journey touchpoints, where reviews or forum posts come from). Say what each platform is for. Name the ones left out and why.
2. **Read what already ran,** when `inputs/` holds post analytics. Total by format and topic with [scripts/sum_by.py](scripts/sum_by.py) (`python3 <this skill's folder>/scripts/sum_by.py <file> format`), not by eye. Rank by the outcome columns (downloads, sign-ups, calls) before reach or reactions, show counts, and note who engaged where the notes say (right buyer or not). One post that went viral is one data point: do not build a pillar on it until a second version repeats the result.
3. **Series and the give-to-ask mix.** Set 2 to 4 recurring series, each from an evidenced pain, job or belief (or a content-strategy pillar), each in the platform's native format. Most posts give (teach, show, tell the true story); a minority ask, and every ask points to a free step or offer that exists in `offer.md`. Name the mix as a heuristic.
4. **Voice.** Write in the brand voice if one is on file; otherwise in the buyer's plain words. Example posts are your own lines, in italics.
5. **Cadence and capacity.** Set a cadence the stated hours and people can keep, including weeks the business is known to be busy. If capacity isn't in `inputs/`, mark the cadence *(assumption)* and ask who writes, designs and replies, and how many hours a week. Dates go to `20-content-calendar`.
6. **Community and replies.** Who replies, how fast (a proposal for the owner to confirm), what gets answered publicly, what moves to direct messages or support, and what is escalated. Product or service complaints go to support and, when they are public reputation issues, to `05-reputation`. Never argue, never delete fair criticism, never promise what `offer.md` doesn't hold.
7. **Capture.** Every series has a path to something the business owns: a lead magnet, a newsletter, a sample. Paid amplification of a post is handed to `11-paid-social`; direct-message selling to `14-dm-selling`.
8. **Measurement.** Per series: the outcome metric (sign-ups, downloads, sourced calls or orders) with its attribution method (UTM, sign-up source, CRM field), and the signals (reach, reactions) labelled as signals.
9. **Platform claims.** Ranking or distribution behaviour, format specs, best times to post and feature availability are platform claims: cite the platform's own documentation with a date, or label them account-observed (from the supplied analytics), inferred or unknown. No third-party "best time to post" or engagement benchmark.
10. **Approval.** The plan and its example posts are drafts. Publishing, replying on the business's behalf, or changing profiles needs the owner's approval.
11. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, follower counts, offers, features or claims that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Describe each source only as it reads. In the founder's or brand's voice, add no habits, promises or operational details (who reads replies, how fast) that context doesn't contain; propose them for the owner to confirm.

## Output

Write `work/11-distribution/11-social-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Social plan: <business, platforms, period>
Skill: 11-social · Date: <YYYY-MM-DD> · Framework: Organic social with Jab, Jab, Jab, Right Hook
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing posted
## Platforms and their job
## What has worked so far (if analytics supplied)
| Format or topic | Posts | Reach (signal) | Outcome columns | Who engaged | Read |
| --- | --- | --- | --- | --- | --- |
## Series
| Series | Evidence | Native format | Give or ask | Next step (exists or gap) | Example (italics) |
| --- | --- | --- | --- | --- | --- |
## Cadence and capacity
## Community and replies
## Capture and hand-offs
## Measurement
## Platform claims
| Claim | Status (documented with URL and date / account-observed / inferred / unknown) |
| --- | --- |
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a review, a comment log, a post export), with the source named. Write your own post ideas and lines in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the platforms and series chosen, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] One or two platforms, chosen from evidence of where the ICP is, each with a stated job.
- [ ] Supplied analytics are totalled with `sum_by.py` and ranked by outcome before reach; one viral post is not made a pillar.
- [ ] Each series comes from evidence, is native to its platform, and every ask points to a real offer or a named gap.
- [ ] Cadence and reply commitments fit stated capacity, or are marked *(assumption)* for the owner to confirm.
- [ ] Platform behaviour claims are cited with a dated first-party source or labelled account-observed, inferred or unknown; no third-party benchmark.
- [ ] Reach and reactions are labelled signals; each series has an outcome metric and attribution method or gap.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Show up where your buyers already are, in the platform's own format, give far more than you ask, answer the people who reply, and turn borrowed attention into an audience you own. Organic social; Jab, Jab, Jab, Right Hook (Gary Vaynerchuk); Traction (Weinberg & Mares); The Complete Marketing System, section 11 Distribution (Servidad, 2026).
