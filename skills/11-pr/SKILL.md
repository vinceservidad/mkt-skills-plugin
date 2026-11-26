---
name: 11-pr
description: Earn press with newsjacking, data stories and the founder story, pitched to outlets the buyer reads. Use for PR, press coverage, media pitches, getting featured, journalist outreach.
metadata:
  section: "11 Distribution"
  covers: "Earned publicity showmanship (Barnum); News-event PR and third-party authority (Bernays); Newsjacking; PR / earned media"
---
# PR

Earned media works when a story is true, new and useful to one outlet's readers, and those readers are the buyer. It fails when the pitch is an announcement nobody asked for, the "data" is a handful of customers sold as an industry finding, a person's story is told without their permission, the target is a famous outlet the buyer never reads, or a news hook is forced onto a tragedy. The plan's job is to find the stories the business can stand behind, match each to outlets its buyers follow, and pitch them so a journalist or host can say yes.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/message.md` → **Big idea** (from `08-message-doc`) or **Story** (from `08-story-epiphany-bridge`): the idea or story the coverage carries.
- If present, also read `context/customer.md` → ICP and personas (whose outlets count), Voice of customer; `context/message.md` → Promise, Proof stack, Enemy; `context/brand.md` → Voice, Reputation; `context/positioning.md` → Positioning statement; data, outlet, permission and capacity notes in `inputs/`; any work in `work/11-distribution/11-channel-selection-*.md` or `work/11-distribution/11-podcast-video-*.md`.
- If the required section is missing:
  - **The upstream evidence exists** (founder notes, interviews or sales notes in `inputs/` but no Big idea or Story): run `08-story-epiphany-bridge` or `08-message-doc` first, then continue.
  - **It doesn't:** stop. Name the missing section with the skills that fill it (Big idea → `08-message-doc`; Story → `08-story-epiphany-bridge`), and ask for evidence (founder notes, customer interviews), not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Permissions.** A named customer, a family member's or partner's story, and customer data (even anonymised totals) can be used only with the permission the owner holds. If a story needs a permission the notes don't record, the plan may prepare it but marks it *blocked until permission*, with the exact question to ask.
- If `08-message-doc` and `08-story-epiphany-bridge` are both not loaded, stop and say: enable mkt-q3-message.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/pr-guide.md](references/pr-guide.md) for story types, outlet fit, the pitch, data stories and newsjacking rules, and [references/pr-classics.md](references/pr-classics.md) for Bernays's news-event engineering and third-party authority and Barnum's truth-grounded publicity showmanship.

1. **Goal and outcome.** Name what coverage is for (reach the buyer, borrowed trust for the proof stack, links, booked conversations) and what judges it (leads or calls traced to a story, with counts). Mentions and impressions are signals.
2. **Story inventory.** List every story the business can tell, each with its source: the founder story (from Story), data the business owns, a contrarian view from the Big idea or Enemy, customer results with permission, a dated real event. For each, record what is true, what is still missing and what permission it needs.
3. **Data stories.** Count and describe data only as it is: who it covers, how many, when, and how it was pulled. A business's own customers are its customers, not the industry: say so in the headline, never "agencies wait 41 days" from 24 clients. Check whether publishing even anonymised totals is allowed by the customer agreement and ask the owner; until then the story is *blocked until permission*. Count from files with [scripts/tally.py](scripts/tally.py), never by eye.
4. **Outlets by buyer fit.** Choose outlets the ICP reads, listens to or watches, with the evidence (discovery calls, interviews, the owner's reading). Order by fit and by how reachable they are (a host who already knows the founder first). A famous outlet the buyer doesn't read is a stretch goal, not the plan; say why. Never look up, invent or add journalists' names or contact details.
5. **Pitches.** One pitch per outlet and story: a subject that says the story, why it matters to that outlet's readers now, the evidence, what the founder can offer (an interview, the data, a guest piece), and a short close. Plain and specific; no press-release boilerplate, no claim the context doesn't hold.
6. **Newsjacking.** Tie a story to news only when the news is real, dated in `inputs/` or cited with a URL and date, and the business has something useful to add. Never use a tragedy, disaster or someone's harm as a hook. Without a real current event, write the rule for when to use it and leave the hook empty.
7. **Capacity and calendar.** Fit pitches and interviews to the founder's stated time (interviews a month, blocked weeks). Space follow-ups by days; one follow-up, then stop.
8. **Tracking.** Record each pitch (outlet, story, date, reply, result) and each piece of coverage (date, link, leads or calls attributed, with how attribution was recorded). Coverage is not proof of incrementality.
9. **Approval.** The plan is a draft. Sending any pitch, publishing data, naming a customer or person, or agreeing to an interview needs the owner's explicit approval.
10. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, quotes, customer names, coverage, awards or credentials that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. A story with a missing beat stays missing; never fill it with invented detail. No third-party benchmark (a "typical" pitch reply rate) is evidence.

## Output

Write `work/11-distribution/11-pr-<YYYY-MM-DD>-<slug>.md`:

```markdown
# PR plan: <business, period>
Skill: 11-pr · Date: <YYYY-MM-DD> · Framework: PR / earned media (founder story, data stories, newsjacking)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing pitched or published
## Goal and the outcome that decides
## Story inventory
| Story | What is true (source) | Missing | Permission needed | Status (ready / blocked until permission) |
| --- | --- | --- | --- | --- |
## Data story
## Outlets
| Outlet | Buyer fit (evidence) | Reachability | Story | Priority |
| --- | --- | --- | --- | --- |
## Pitches
## Newsjacking rule
## Calendar and capacity
## Tracking and how we judge it
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (an interview, a review, the owner's notes), with the source named. Titles of books, essays or talks, including in the Principle, framework, source block, go in italics, never in quotation marks. Write pitch drafts in italics or a plain block, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the stories ready now and those blocked with the permission each needs, the outlets in order with the reason, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every story has its source, what is missing and the permission it needs; stories needing an unrecorded permission are marked blocked with the question to ask.
- [ ] Data is described as what it is (whose, how many, when); a business's own customers are never presented as an industry finding; publishing customer data waits for permission.
- [ ] Outlets are chosen on evidence the buyer follows them; famous outlets outside that evidence are a stretch goal with the reason; no journalist names or contacts are invented.
- [ ] Each pitch fits one outlet's readers, carries only supported claims and has one follow-up.
- [ ] News hooks are real and dated; no tragedy is used as a hook.
- [ ] Pitches and interviews fit the founder's stated capacity.
- [ ] Coverage is judged on leads or calls with counts; the plan says nothing is pitched or published without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Pitch a true story to the outlets your buyers already trust, with evidence you are allowed to share, and judge PR on the conversations it starts. PR / earned media and Newsjacking, The Complete Marketing System, section 11 Distribution (Servidad, 2026); Crystallizing Public Opinion (Edward Bernays); earned publicity demonstrations (P.T. Barnum, within strict proof rules); Newsjacking (David Meerman Scott); Trust Me, I'm Lying (Ryan Holiday) as a warning about manufactured stories.
