---
name: 07-bonuses-urgency
description: Add bonuses that each remove an objection, plus true urgency and scarcity. Use for bonus stacks, limited spots, deadlines, flash sales, buy now. Not for the core offer (use 07-offer-design).
metadata:
  section: "07 Offer"
  covers: "Bonuses; Flash sales; Scarcity / urgency"
---
# Bonuses and urgency

Each bonus should answer the next objection in line. A bonus that answers nothing is clutter. Urgency and scarcity work only when they are true: a fake deadline or a fake "3 spots left" costs trust, and in many places it breaks consumer law. This skill adds bonuses that remove objections, and a reason to act now that the business can stand behind.

## Needs (read before writing)

- `context/offer.md` → **Core offer**, written by `07-offer-design`. It must be present (drafted or confirmed, with content).
- `context/customer.md` → **Beliefs, objections and drivers**, written by `02-buyer-psychology`. It must be present: bonuses are chosen from it.
- If present, also read:
  - `context/offer.md` → Price and model (`07-pricing`) and Guarantee (`07-guarantee-risk-reversal`);
  - capacity, season or deadline facts in `inputs/` or the user's message.
- If a required section is missing:
  - **The evidence exists:** run the missing skill first (`02-buyer-psychology` or `07-offer-design`), then continue. If `02-buyer-psychology` is not loaded, stop and say: enable mkt-q1-audience.
  - **It doesn't:** stop. Name the missing sections and the skills that fill them. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **List the objections still standing** after the core offer and the guarantee, ranked by evidence: effort, *will it work for me*, proof, timing.
2. **Design one bonus per objection,** using [references/bonus-urgency-guide.md](references/bonus-urgency-guide.md). A good bonus is cheap to deliver, valuable to this buyer, and named for what it solves.
   - Use deliverables the business can provide. Mark new ones as proposed.
   - State any value you assign a bonus as the value to the buyer, with reasoning. Never present an invented "worth $X" as fact.
3. **Find the true urgency and scarcity:**
   - **Capacity:** how many new customers the business can actually take per period.
   - **Time:** a real deadline, a cohort start, a seasonal reason, a price change already decided.
   - **Cost of waiting:** what the buyer loses by delaying, from evidence.

   Flash sales (short, time-limited sales) count only when the start, end and price are real and hold afterwards: no resetting countdown, no was-price never charged.

   If none is true, say so. Recommend a cost-of-waiting reason instead of a fake deadline.
4. **Write each in one line,** as a proposal without quotation marks, and say where it shows: the offer page, the call or the email. In the objection column, paraphrase the objection and cite its ID (*onboarding is a slog, review 3*). Use quotation marks only for words that appear exactly in the source, never for the note-taker's summary around a quote. Name rejected tactics in italics (*only 3 spots left*), not in quotation marks.
5. **Check before saving.** Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file you wrote (`python3 <this skill's folder>/scripts/check_quotes.py context/offer.md`). For every line it prints, copy the exact words from the source or drop the quotation marks and use italics, then run it again until it reports every quotation matches. This includes objection labels and category names in table cells: a label you coined (*will it work for us*) is italics, not quotation marks. Then re-read the draft against the Checks and fix any failure.

## Output

Write two sections of `context/offer.md`, replacing each body and leaving every other section exactly as it was.

```markdown
## Bonuses
Status: draft (<YYYY-MM-DD>, 07-bonuses-urgency)
Written by: 07-bonuses-urgency, <YYYY-MM-DD>
| Bonus | Objection it removes (evidence) | Exists or proposed | Cost to deliver | Value to the buyer |
| --- | --- | --- | --- | --- |
Evidence: <sources>
Method: Bonuses that kill objections, $100M Offers (Hormozi)

## Urgency and scarcity
Status: draft (<YYYY-MM-DD>, 07-bonuses-urgency)
Written by: 07-bonuses-urgency, <YYYY-MM-DD>
True scarcity: <capacity fact and source, or "none">
True urgency: <deadline or season and source, or "none">
Cost of waiting: <what delay costs the buyer, from evidence>
Not to use: <any fake urgency considered and rejected>
Evidence: <sources>
Method: Scarcity and urgency that are true (Hormozi; Cialdini)
```

Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/offer.md` does not exist, first copy [assets/offer.md](assets/offer.md) to `context/offer.md`, then write your section.

Reply with:
- the bonus stack;
- the reason to act now;
- the next skill: `07-value-ladder`, or `08-message-doc`.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every bonus names the evidenced objection it removes. None is filler.
- [ ] Bonus values are the buyer's value with reasoning, never an invented price tag stated as fact. Deliverables are marked as existing or proposed.
- [ ] Scarcity and urgency are true and sourced. If none exists, the section says so and offers a cost-of-waiting reason instead.
- [ ] Rejected fake-urgency tactics are listed under "Not to use".
- [ ] No unmarked inference. Quotation marks hold only words copied exactly from a source, and `check_quotes.py` reports every quotation matches.
- [ ] Only `## Bonuses` and `## Urgency and scarcity` changed. Each has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

Each bonus should remove the next objection in line, and urgency and scarcity work only when they are true: a fake deadline trades a sale today for trust tomorrow. Bonuses, scarcity and urgency, $100M Offers (Alex Hormozi); scarcity, Influence (Robert Cialdini); The Complete Marketing System, section 7 Offer (Servidad, 2026).
