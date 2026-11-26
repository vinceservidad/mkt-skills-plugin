---
name: 10-email-copy
description: Write one marketing email with subject lines, preview text, body, CTA and P.S. Use for broadcasts, promos, newsletters and win-back emails. Not for multi-email sequences (use 12-email-sequences).
metadata:
  section: "10 Copywriting"
---
# Email copy

One email, one idea, one action. An email is read by someone who already gave permission, so it can be personal and direct, but it still has to earn the open, the read and the click. This skill writes single emails from the message and the reader's stage, with every claim traceable.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/message.md` → **Promise**, from `08-message-doc`.
- `context/awareness.md` → **Awareness map**, from `03-awareness-map`.
- `context/awareness.md` → **Journey**, from `03-journey-map`.
  (Awareness map or Journey: at least one)
- If present, also read `context/brand.md` → Voice (`05-brand-voice`); `context/offer.md` for real terms; `context/message.md` → Proof stack, Objection map and Story; Voice of customer.
- If a required section is missing:
  - **The upstream evidence exists:** run the skill that fills it first, then continue. If that skill is not loaded, stop and say: enable mkt-q1-audience.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Promise → `08-message-doc`; Awareness map → `03-awareness-map`, or Journey → `03-journey-map`), and what the user should bring. Do not write copy on an invented offer, promise or proof. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Define the send.** For a re-engagement or win-back email, read the evidenced reasons people left or stalled (Beliefs, objections and drivers; Voice of customer) and answer the top ones with offer elements that `offer.md` lists as existing. Proposed or planned elements must not be implied. In the file, list every evidenced reason as *answered by <element>* or *can't answer yet*. Then define: who receives it (segment, stage or awareness level), its one purpose (announce, promote, educate, re-engage), and its one action.
2. **Choose the structure,** using [references/email.md](references/email.md): PAS, BAB, story-lesson-offer, a news announcement or a plain-text letter. Every part of the structure you name must show in the body. PAS needs all three: the problem, an agitate line on what it costs the reader (from the evidence, not invented), then the solution. A list of problems each followed by its fix is not PAS.
3. **Write three to five subject lines and the preview text.** Specific beats clever. No misleading subjects ("Re:", "Your order") and no false urgency.
4. **Write the body:** short paragraphs, one idea and one call to action, and a P.S. that restates the action. Use real offer terms only. Use deadlines only if `offer.md` → Urgency and scarcity has them. A capacity limit is stated as a limit (*we take four new agencies a month*), never as demand or slots already taken (*four agencies start next month*) unless the context says so.
   Write nothing in the copy that the context doesn't support: no illustrative guidance, no generalisations such as *many people* or *most customers*, and no delivery terms, timings or conditions beyond what `offer.md` says. If the copy needs it, put it under Open questions instead.
   Present each source as what it is: two lines from one review are one customer, never *one customer… another said…*.
5. **Note the compliance basics:** the sender, an unsubscribe link, and a real postal address where the law requires one. The send itself happens in the user's email tool, with the user's approval.
6. **Run the Anti-AI second pass** in [references/anti-ai-check.md](references/anti-ai-check.md): name the reader, fix the 6 whole-piece rules (max 4 items per sentence list, one point one proof, varied paragraph shape) and all 13 sentence issues (0 em dashes, no mid-sentence bold, no buzzwords, no colon reveals, no recap endings), and reread once as the reader.
7. **Check before saving.** Re-read the draft against the Checks and fix any failure.

## Output

Write `work/10-copywriting/10-email-copy-<YYYY-MM-DD>.md`. When you write more than one the same day, add `-<slug>` after the date, for example `work/10-copywriting/10-email-copy-2026-11-13-<slug>.md`:

```markdown
# Email: <what it is for>
Skill: 10-email-copy · Date: <YYYY-MM-DD> · Awareness level: <level> · Framework: <name>
Built from: <context sections used, with their status (draft or confirmed)>
## Copy
<the copy>
## Claims and proof
| Claim in the copy | Proof or source |
| --- | --- |
Reasons (re-engagement only): <reason — answered by … / can't answer yet>
Subject lines: <3–5 options>
Preview text: <…>
## Principle, framework, source
```

Change nothing in `context/`. Copy is a deliverable, not a decision.

**Quotation marks are evidence.** In the copy, quotation marks hold only words that appear exactly in a source, such as a testimonial from the proof stack or a review in `inputs/`, with its source in the claims table. Do not wrap your own headlines or lines in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/10-copywriting/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the key choice made (structure, angle or level) and what is still missing. Your final reply message must end with the **Principle, framework, source** block, after the still-missing list, on a build and on a stop; nothing comes after it. Writing the block in the file does not replace it in the reply:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] One email, one idea, one call to action, for a named segment or stage.
- [ ] Subject lines are specific and honest. No fake reply or forward prefixes, and no false urgency.
- [ ] Offer terms, deadlines and proof match context exactly, and are listed in the claims table.
- [ ] The Anti-AI second pass in `references/anti-ai-check.md` (reader check, 6 whole-piece rules, 13 sentence fixes with 0 em dashes, and final reread) is completed.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] Unsubscribe and sender requirements are noted. Sending is left to the user.
- [ ] No file in `context/` changed.
- [ ] The reply (not just the file) ends with the **Principle / Framework / Source** block, after the still-missing list.

## Principle and source

One email, one idea, one action: earn the open with an honest, specific subject and the click with a reason the reader cares about now. PAS and BAB structures; Copywriting Secrets (Jim Edwards); The Boron Letters (Gary Halbert); The Complete Marketing System, section 10 Copywriting (Servidad, 2026).
