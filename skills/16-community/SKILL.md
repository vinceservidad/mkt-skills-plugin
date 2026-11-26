---
name: 16-community
description: Build a community with a purpose, rituals and a value exchange, measured by engagement and outcomes. Use for customer community, Slack or Discord groups, ambassador programs, customer advisory boards.
metadata:
  section: "16 Referral and Community"
  covers: "Ambassador programs; Community-led growth; Customer advisory boards"
---
# Community

A community is people who come back because they get something from each other, not just from the business. Community-led growth works when the community has a clear purpose for a defined group, a ritual that gives people a reason to show up, a value exchange members feel, a host with time to run it, and a measure beyond member count. It fails when it is a broadcast channel with a group name, the founder promises daily posts they can't keep, it is open to everyone and so to no one, or success is the number of sign-ups. Ambassador programs and customer advisory boards are small, deliberate forms that often fit better.

Save the community plan as a Markdown file in `work/16-referral-community/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: who the community is for.
- `context/customer.md` → **Jobs to be done**, from `02-jobs-to-be-done`: what members come to get done together.
- If present, also read `context/customer.md` → Voice of customer, Segments; `context/offer.md` → Core offer, Value ladder; `context/brand.md` → Voice; requests from customers, existing groups, host time and platform notes in `inputs/`; any work in `work/16-referral-community/` or `work/11-distribution/11-co-marketing-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (interviews, sales notes or reviews in `inputs/`): run the skill that fills the missing section (`02-icp-persona` or `02-jobs-to-be-done`) first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (ICP and personas → `02-icp-persona`; Jobs to be done → `02-jobs-to-be-done`), and ask for evidence, not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.
- If `02-jobs-to-be-done` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/community-guide.md](references/community-guide.md) for community types, purpose, rituals, the value exchange, host capacity and engagement measures.

1. **Evidence of demand.** What customers have asked for (to meet peers, to learn, to share), counted from `inputs/` with [scripts/tally.py](scripts/tally.py). No demand evidence means start small and test.
2. **Purpose and members.** One purpose tied to a job, for a defined group (customers only, the ICP, or a wider audience), with who is not a member and why.
3. **Format.** Choose the smallest form that serves the purpose: a monthly call, a customer advisory board, an ambassador program, an event series, or an online group. A platform comes last; platform features are facts to cite or mark *to confirm*.
4. **Rituals.** A regular moment members come for (a monthly session, a teardown, a peer round), at a cadence the host can keep.
5. **Value exchange.** What members get, what they give, and what the business gets, stated plainly. No hidden selling.
6. **Host capacity.** Who runs it, hours a month, and what happens when they're busy; promises scaled to that.
7. **Rules and privacy.** Simple member rules, moderation, and what members share (confidential business numbers stay private unless members choose).
8. **Measure.** Active members (attended or posted in the period), repeat attendance, member-to-member replies, and outcomes (retention of members versus non-members, referrals), with counts. Member count alone is not a result.
9. **Approval.** The plan is a draft. Launching a community, inviting customers or creating channels needs the owner's explicit approval.
10. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no member counts, engagement figures, results or quotes that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/16-referral-community/16-community-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Community plan: <business, date>
Skill: 16-community · Date: <YYYY-MM-DD> · Framework: Community-led growth (purpose, ritual, value exchange)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing launched, nobody invited
## Evidence of demand
## Purpose and members
## Format
## Rituals
## Value exchange
## Host capacity
## Rules and privacy
## How we measure it
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/16-referral-community/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the purpose and members, the format and ritual, the host's time, and how success is measured, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Demand evidence is counted; weak evidence leads to a small test.
- [ ] The community has one purpose tied to a job and a defined membership.
- [ ] The smallest fitting format is chosen; rituals fit the host's stated time.
- [ ] The value exchange is explicit; member data and business numbers stay private by default.
- [ ] Success is active members, repeat attendance and outcomes with counts, not sign-ups; nothing launches without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Give a defined group a reason to come back to each other, at a rhythm the host can keep, and measure what members do, not how many joined. Community-led growth, Ambassador programs and Customer advisory boards, The Complete Marketing System, section 16 Referral and Community (Servidad, 2026); The Business of Belonging (David Spinks).
