---
name: 12-lead-magnet
description: Design a lead magnet that solves one narrow problem fast and leads to the core offer, with outline, title and next step. Use for a freebie, opt-in incentive, content upgrade or more email subscribers.
metadata:
  section: "12 Funnel"
  covers: "Lead magnet"
---
# Lead magnet

A lead magnet trades something specific and fast for contact details. A good one solves one narrow problem the buyer already has, delivers a quick win, and makes the core offer the obvious next step. A bad one is a long ebook nobody finishes, or a freebie for people who will never buy.

Save the requested plan or asset as a Markdown file in `work/12-funnel/` (file name under Output) when the required inputs are present. Creating this deliverable is part of the task, including requests worded as planning or design. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Core offer**, from `07-offer-design` (plugin mkt-q2-offer).
- `context/customer.md` → **Pains, desires and fears**, from `02-customer-research` (plugin mkt-q1-audience).
- If present, also read `context/awareness.md` → Awareness map; `context/customer.md` → Voice of customer and Jobs to be done; `context/offer.md` → Value ladder (any existing free step).
- If a required section is missing:
  - **The upstream evidence exists:** run the skill that fills it first, then continue. If that skill is not loaded, stop and say: enable mkt-q2-offer (Core offer) or mkt-q1-audience (Pains, desires and fears). Price and guarantee are the owner's commitments: never generate them yourself; stop and ask, or offer the owning skill's proposal for approval.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Core offer → `07-offer-design`, in mkt-q2-offer; Pains, desires and fears → `02-customer-research`, in mkt-q1-audience), the plugin to enable if that skill is not loaded,, and what the user should bring. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Pick the problem.** Choose one narrow, urgent problem from the pains (with evidence) whose solution points to the core offer. Solving it should create the next problem the core offer solves.
2. **Choose the format** using [references/lead-magnet-formats.md](references/lead-magnet-formats.md): checklist, template, calculator, quiz, sample on their data, mini-course or guide. The rule is that it can be consumed in minutes.
3. **Score it** against Hormozi's tests (specific, fast, valuable, leads to the offer) and the awareness level it serves.
4. **Outline it:** title (specific, in buyer language), promise, sections or fields, and the quick win.
5. **Define the next step after opt-in:** the thank-you page offer and the nurture. Use only real offers.
6. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features, platform capabilities or delivery terms that aren't in `context/` or `inputs/`. Mark inferences `(assumption)`, and list what is needed under Open questions. Describe each source only as it reads: no outcome, motive or behaviour the source doesn't state. In the founder's or brand's voice, add no habits, promises or operational details (who reads replies, what a call covers) that context doesn't contain.

## Output

Write `work/12-funnel/12-lead-magnet-<YYYY-MM-DD>.md`, adding `-<slug>` after the date when more than one is written the same day:

```markdown
# Lead magnet: <what it is for>
Skill: 12-lead-magnet · Date: <YYYY-MM-DD> · Framework: <name>
Built from: <context sections used, with their status>
## Problem it solves (evidence)
## Format, title and promise
## Outline
## Scores: specific / fast / valuable / leads to offer
## After opt-in
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. This is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a review, an interview, a testimonial in the proof stack), with the source named. Write your own lines, proposals and copy in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py <file>`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the key decision, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The magnet solves one narrow, evidenced problem, and solving it points to the core offer.
- [ ] It can be consumed in minutes, and its title is specific and in the buyer's language.
- [ ] The next step after opt-in uses a real offer or a named gap.
- [ ] No invented statistics, results or testimonials in the magnet or its promise.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Give away a specific, fast win on one real problem whose solution makes the core offer the obvious next step. Lead magnets, $100M Leads (Alex Hormozi); DotCom Secrets (Russell Brunson); The Complete Marketing System, section 12 Funnel (Servidad, 2026).
