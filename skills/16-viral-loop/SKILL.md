---
name: 16-viral-loop
description: Design sharing mechanics, invite loops, forced-share checks and K-factor honestly. Use for going viral, K-factor, invite loops, forced-share/invite gates, network effects, making a product shareable.
metadata:
  section: "16 Referral and Community"
  covers: "K-factor / viral loop; Network effects; Sneezers and IdeaVirus (Godin); STEPPS (Berger)"
---
# Viral loop

A viral loop is when using or buying the product leads people to bring in others, who do the same. It is measured by the K-factor (invites sent per user × the share of invites that become users) and the cycle time. It works when sharing is part of the value (a gift, a shared result, an invite that helps both sides), the mechanics are easy, and the loop is measured from real data. It fails when "going viral" is the goal, K-factor is estimated from hope, sharing is forced or spammy, or a loop is designed for a product people don't talk about. Most products never reach a K-factor above 1; loops still help when they lower acquisition cost.

Save the viral loop design as a Markdown file in `work/16-referral-community/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. Usage, gift, share and referral data in `inputs/` are the evidence; offer context says what can be shared.
- If present, also read `context/offer.md` → Core offer, Value ladder; `context/customer.md` → Jobs to be done, Voice of customer, Segments; gift orders, shares, invites, referral sources and tickets in `inputs/`; any work in `work/16-referral-community/16-referral-program-*.md` or `work/19-growth/19-growth-loops-*.md`.
- **No data:** Without any sharing, gift or referral data, design the loop and the instrumentation to measure it, ask for the data (gifts sold, recipient subscriptions, customer counts), and explicitly state **how to provide it** (drop exports in `inputs/` or paste counts into chat); invent no K-factor. Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/viral-loop-guide.md](references/viral-loop-guide.md) for K-factor and cycle time, STEPPS, network effects, loop mechanics and measurement, and [references/word-of-mouth-classics.md](references/word-of-mouth-classics.md) for Godin's Sneezers and IdeaVirus mechanics and Barnum's truth-grounded talkability triggers.

1. **Is there a natural share?** From `inputs/` and Voice of customer, find where customers already share or give (gifts, posts, recommendations), counted with [scripts/tally.py](scripts/tally.py). Use STEPPS (Berger) to judge why people would share: social currency, triggers, emotion, public, practical value, stories.
2. **Network effects?** Say whether the product gets better for each user as more join (most don't). If not, the loop is word of mouth and sharing, not a network effect.
3. **Loop design.** One loop: the trigger, the share action, what the recipient sees, what makes them act, and how they become a sharer. Make the share part of the value (a gift with a start date, a shared result), never forced or spammy.
4. **Measure honestly.** K-factor = invites (or shares) per user × conversion of those invites, from real counts; cycle time from share to new user. With no data, write the formula and the events to track, and give no K estimate.
5. **What it's worth.** Even with K below 1, each new user brings 1 / (1 − K) users in total; compute the effect on acquisition cost from the business's own figures if K is measured.
6. **Instrument.** The events to record (share, invite sent, opened, converted) and where; hand tracking details to `17-tracking-plan`.
7. **Approval.** The design is a draft. Building features, sending invites or changing the product needs the owner's explicit approval.
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no K-factors, share counts, conversion rates or results that aren't in `context/` or `inputs/`. Never present K above 1 as likely without data. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/16-referral-community/16-viral-loop-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Viral loop design: <business, date>
Skill: 16-viral-loop · Date: <YYYY-MM-DD> · Framework: K-factor / viral loop, STEPPS (Berger), network effects
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing built or sent
## Where customers already share
## Why they would share (STEPPS)
## Network effects
## The loop
## K-factor and cycle time
## What it is worth
## Instrumentation
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/16-referral-community/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, where sharing already happens, the loop design, how K will be measured, and what it could be worth, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Existing sharing is counted; STEPPS is applied to why people would share.
- [ ] Network effects are claimed only if the product improves with more users.
- [ ] The share is part of the value and never forced.
- [ ] K-factor and cycle time come from real counts or are left as a formula with events to track; no hoped-for K.
- [ ] Instrumentation is listed; nothing is built or sent without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Build sharing into the value people already get, measure the loop from real counts, and treat a K-factor above 1 as rare. K-factor / viral loop, Network effects and STEPPS (Jonah Berger, Contagious), The Complete Marketing System, section 16 Referral and Community (Servidad, 2026); Unleashing the IdeaVirus and Purple Cow (Seth Godin); truth-grounded demonstrations (P.T. Barnum); Andrew Chen on viral loops and The Cold Start Problem.
