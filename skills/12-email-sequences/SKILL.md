---
name: 12-email-sequences
description: Plan and write pre-purchase email sequences (welcome, Soap Opera nurture, launch, follow-up) with timing and exit rules. Use for a drip or welcome series. Not for one email (use 10-email-copy).
metadata:
  section: "12 Funnel"
  covers: "Seinfeld emails; Soap Opera Sequence"
---
# Email sequences

Most buyers don't buy on first contact; the money is in the follow-up. A sequence moves a new lead from opt-in to the next step in a planned order. It opens loops, tells the story, shows proof and makes the offer, with one goal per email and a clear exit when they buy or opt out.

Save the requested plan or asset as a Markdown file in `work/12-funnel/` (file name under Output) when the required inputs are present. Creating this deliverable is part of the task, including requests worded as planning or design. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Core offer**, from `07-offer-design` (plugin mkt-q2-offer).
- `context/message.md` → **Story**, from `08-story-epiphany-bridge` (plugin mkt-q3-message).
- `context/message.md` → **Promise**, from `08-message-doc` (plugin mkt-q3-message).
- `context/awareness.md` → **Journey**, from `03-journey-map` (plugin mkt-q1-audience).
- `context/awareness.md` → **Awareness map**, from `03-awareness-map` (plugin mkt-q1-audience).
  (Story or Promise: at least one; Journey or Awareness map: at least one)
- If present, also read `context/message.md` → Proof stack and Objection map; `context/offer.md` → Price and model, Guarantee, Bonuses, and Urgency and scarcity; `context/brand.md` → Voice; the lead magnet or entry point.
- If a required section is missing:
  - **The upstream evidence exists:** run the skill that fills it first, then continue. If that skill is not loaded, stop and say: enable mkt-q2-offer (Core offer), mkt-q3-message (Story, Promise) or mkt-q1-audience (Journey, Awareness map). Price and guarantee are the owner's commitments: never generate them yourself; stop and ask, or offer the owning skill's proposal for approval.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Core offer → `07-offer-design`, in mkt-q2-offer; Story → `08-story-epiphany-bridge`, or Promise → `08-message-doc`, both in mkt-q3-message; Journey → `03-journey-map`, or Awareness map → `03-awareness-map`, both in mkt-q1-audience), the plugin to enable if that skill is not loaded,, and what the user should bring. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Define the sequence:** the trigger (opt-in, purchase, webinar), the reader's awareness level, the goal (book a call, buy, activate), the number of emails and the timing, and the exit rules (stop on purchase or unsubscribe).
2. **Choose the structure,** using [references/sequences.md](references/sequences.md):
   - **Welcome and Soap Opera:** set the stage, high drama, epiphany, hidden benefits, urgency and call to action.
   - **Seinfeld emails (Brunson):** after the Soap Opera Sequence, a daily broadcast of short story-led emails. Plan it only with consent and a frequency the owner approves, and take its stories from Story or the inputs.
   - **Nurture.**
   - **Launch.**
   - **Sales.**
   - **Follow-up.**
3. **Plan each email:** its one job, the subject line, the core idea, and the call to action. Stories come only from Story or the inputs; proof only from the proof stack; offer terms, deadlines and bonuses only from `offer.md`.
4. **Write the emails:** plain, personal, one idea each. Describe the lead magnet or entry point only as far as context describes its contents; if context doesn't, refer to it by name and list its contents under Open questions. In sendable copy, also add none of these unless context states them:
   - a number, even as an example, a time estimate or a hypothetical (*about ten minutes*, *paid 60 days late*);
   - a sourced number reworded beyond its source: keep its exact count and population (*10 of 12 closed deals*, not *our last 12*);
   - what the founder has seen, what most owners do, or what people ask or say, beyond the sourced count (*the pattern is nearly always the same*, *two things people ask*);
   - a bonus, term or process that context says is unproven or not to be advertised yet, stated as settled;
   - who reads replies or what a call covers, including a *hit reply and tell me* call to action, which promises that someone reads replies;
   - the founder's preferences or feelings (*I'd rather you know now*), or what the lead magnet is for or contains.

   Use a link or booking call to action instead, and put each idea under Open questions.
5. **Note the compliance basics:** consent, sender identity, unsubscribe, and a postal address where required. List them as items for the owner to check; don't state what a specific law requires unless context or a cited official source says so. Sending and automation stay in the user's tool, with their approval.
6. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features, platform capabilities or delivery terms that aren't in `context/` or `inputs/`. Mark inferences `(assumption)`, and list what is needed under Open questions. Describe each source only as it reads: no outcome, motive or behaviour the source doesn't state. In the founder's or brand's voice, add no habits, promises or operational details (who reads replies, what a call covers) that context doesn't contain.

## Output

Write `work/12-funnel/12-email-sequences-<YYYY-MM-DD>.md`, adding `-<slug>` after the date when more than one is written the same day:

```markdown
# Email sequence: <what it is for>
Skill: 12-email-sequences · Date: <YYYY-MM-DD> · Framework: <name>
Built from: <context sections used, with their status>
Trigger: <…> · Goal: <…> · Exit rules: <…>
## Plan
| # | Day | Job | Subject | Call to action |
| --- | --- | --- | --- | --- |
## Emails
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

- [ ] The trigger, goal, timing and exit rules are defined, and each email has one job and one call to action.
- [ ] Stories, proof and offer terms come only from context. No invented stories, results, deadlines or discounts.
- [ ] Sendable copy contains no founder habits or observations, reply handling, call contents, lead-magnet contents, example or hypothetical numbers, or reworded statistics that are not in context. An inline *check before sending* note does not make one acceptable: remove the line from the copy and list it under Open questions.
- [ ] The sequence moves the reader one awareness step at a time toward the goal.
- [ ] Consent and unsubscribe basics are noted. Sending is left to the user.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

The money is in the follow-up: a planned sequence with one job per email moves a lead from opt-in to the next step, using true stories and real proof. Soap Opera Sequence, DotCom Secrets (Russell Brunson); email follow-up (Dan Kennedy); The Complete Marketing System, section 12 Funnel (Servidad, 2026).
