---
name: 11-podcast-video
description: Use podcasts, guesting and video (YouTube) as a distribution channel. Use for podcast guest spots, starting a podcast, YouTube channel plans, video content strategy, pitching podcast hosts.
metadata:
  section: "11 Distribution"
  covers: "Podcast marketing / guesting; YouTube / video marketing"
---
# Podcast and video

Podcasts and video let a buyer spend twenty minutes with the founder before they ever talk. Guesting on shows the buyer already follows borrows a trusted host's audience and costs only time; running a channel or show builds an asset but needs a cadence the business can keep for months. The channel works when shows and topics are chosen for the ICP, every episode teaches something the buyer needs, and the work is judged on leads and clients it brings. It fails when a channel starts at a cadence nobody can sustain, shows are picked by size, private client material is reused, or views are the goal.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: whose shows and searches count.
- If present, also read `context/message.md` → Story, Big idea, Proof stack; `context/customer.md` → Jobs to be done, Pains, desires and fears, Voice of customer; `context/brand.md` → Voice; `context/offer.md` → Core offer; past episodes, lead sources, outlets, time and equipment notes in `inputs/`; any work in `work/11-distribution/11-content-strategy-*.md`, `11-pr-*.md` or `11-social-*.md`.
- If the required section is missing:
  - **The upstream evidence exists** (interviews, sales notes in `inputs/`): run `02-icp-persona` first, then continue.
  - **It doesn't:** stop. Name the missing section with the skill that fills it (ICP and personas → `02-icp-persona`) and ask for evidence. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/podcast-video-guide.md](references/podcast-video-guide.md) for guesting, running a show or channel, topics, repurposing and platform facts.

1. **Outcome and evidence so far.** Name the outcome (leads, booked calls, clients) and read what podcasts or video have already produced, counted from `inputs/` with [scripts/tally.py](scripts/tally.py): leads and clients by show, with how the source was recorded.
2. **Guest or own?** Start with guesting when the business has no audience: it borrows one now and costs only time. Recommend an own show or channel only when the founder's stated hours can sustain a steady cadence for months and topics are deep enough; scale the cadence to those hours, never the reverse.
3. **Shows to pitch.** Shows the ICP follows, with the evidence (discovery calls, lead sources, the owner's knowledge); a host who already had the founder on comes first. Describe hosts by role; never look up or add real names or contacts. Show size claims are the host's.
4. **Topics.** Episode topics from the buyer's jobs and pains and the founder's Story and Big idea, each with what the listener learns. Customer stories and client material appear only with permission; private client work is never reused.
5. **The pitch and the episode.** A short pitch per show with a specific topic for its audience; a guest one-pager; one clear next step for listeners (a resource that exists, a page with a unique link).
6. **Own channel (if chosen).** Format, length, cadence within capacity, recording setup the owner has, titles and thumbnails built on searchable jobs (for YouTube), and a review point after a fixed number of episodes. Platform features and requirements are facts to cite with URL and date or mark *to confirm*.
7. **Repurposing.** Clips, posts and newsletter items from each episode, handed to `11-social` and `11-content-strategy`.
8. **Measure.** Per show or video: leads and clients by source with counts, plus listens or views as signals. A source field under-counts; add a unique link or a "where did you hear about us" question.
9. **Approval.** The plan is a draft. Pitching hosts, publishing or using any client material needs the owner's explicit approval.
10. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no audience sizes, results, guests, quotes or client stories that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. No benchmark download or view count is evidence.

## Output

Write `work/11-distribution/11-podcast-video-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Podcast and video plan: <business, period>
Skill: 11-podcast-video · Date: <YYYY-MM-DD> · Framework: Podcast marketing / guesting and YouTube / video marketing
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing pitched or published
## Outcome and what has worked so far
| Show or channel | Leads | Clients | How recorded |
| --- | --- | --- | --- |
## Guest or own: the decision
## Shows to pitch
| Show | Buyer fit (evidence) | Reachability | Topic |
| --- | --- | --- | --- |
## Topics
## Pitch and guest one-pager
## Own channel (if chosen)
## Repurposing
## How we judge it
## Platform facts
| Fact the plan relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Titles of books, essays or talks, including in the Principle, framework, source block, go in italics, never in quotation marks. Write pitch drafts in italics or a plain block. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`) and fix every line it prints until it reports every quotation matches.

Reply with the file path, the guest-or-own decision and why, the first shows to pitch, the cadence, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Past results are counted by show with how they were recorded.
- [ ] The guest-or-own decision follows the founder's stated hours; any cadence fits them.
- [ ] Shows are chosen on buyer fit with evidence; no host names or contacts are invented.
- [ ] Topics come from the buyer's jobs and the founder's story; no client material without permission.
- [ ] Each episode has one next step with a way to count leads.
- [ ] Platform facts are dated or *to confirm*; the plan says nothing is pitched or published without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Borrow trusted hosts' audiences first, teach the buyer something real every time, only start your own show at a cadence you can keep, and count the clients each show brings. Podcast marketing / guesting and YouTube / video marketing, The Complete Marketing System, section 11 Distribution (Servidad, 2026); Traffic Secrets (Russell Brunson) on working your way into the Dream 100's shows.
