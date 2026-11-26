---
name: 10-swipe-file
description: Build and use a swipe file of supplied ads, headlines, emails and pages, filed by awareness level and structure. Use for saved or competitor examples to model. Not for new ads (use 10-ad-copy).
metadata:
  section: "10 Copywriting"
  covers: "Swipe file"
---
# Swipe file

A swipe file is a library of real examples, filed so the right model can be found when writing. Its value is in the analysis: why an example works, for which reader at which awareness level. Its risk is in false claims: an example is only "proven" if its source shows the results.

## Needs (read before writing)

- Nothing upstream is required. Read examples supplied by the user (pasted, files in `inputs/`, screenshots described in text); `context/awareness.md` → Awareness map and `context/message.md` → Promise, to choose relevant models for a new piece.
- If the material this skill works on is missing, stop and ask for it; never invent it. Write no swipe file. The stop reply has this shape:
  1. Say that no examples were supplied, so no swipe file was built.
  2. List where to collect real examples: the Meta Ad Library, the LinkedIn Ad Library and Google Ads Transparency Center, competitors' pages and emails, the user's own best performers, and books, cited by title and page.
  3. Optionally, name at most three classics, each with its structure only: no copy text and no claimed results.
  4. End with the **Principle, framework, source** block.

## Process

1. **Collect only real examples.** Use what the user supplies or points to, with its source (brand, channel, date, link if any). If no examples are supplied, the material is missing: say so, list where to collect them (ad libraries, competitors' pages, the user's own best performers), and write no examples. Don't reproduce famous ads from memory. A classic can be named and its structure described; reproduce its text only from a supplied source.
2. **File each example** using [references/filing.md](references/filing.md): type, section (offer, message, headline, page), awareness level, structure (PAS, story, offer lead…), the angle, and what makes it work, in one line.
3. **Record performance only if the source shows it.** Otherwise write "performance unknown". A long-running ad in an ad library is a signal, not proof. A competitor's ad is evidence only that the competitor ran it, not that the tactic works; say so in the file for each competitor example.
4. **For a new piece, pull models:** choose two or three examples that match the reader's awareness level and the structure needed, and say what to borrow (structure, angle, rhythm) and what not to copy (the words, the brand, claims).
5. **Check before saving.** Re-read the draft against the Checks and fix any failure.

## Output

Write `work/10-copywriting/10-swipe-file-<YYYY-MM-DD>.md`. When you write more than one the same day, add `-<slug>` after the date, for example `work/10-copywriting/10-swipe-file-2026-11-13-<slug>.md`:

```markdown
# Swipe file: <what it is for>
Skill: 10-swipe-file · Date: <YYYY-MM-DD> · Awareness level: <level> · Framework: <name>
Built from: <context sections used, with their status (draft or confirmed)>
## Copy
<the copy>
## Claims and proof
| Claim in the copy | Proof or source |
| --- | --- |
Models for the current piece: <example — what to borrow — what not to copy>
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

- [ ] Every example is real and supplied, with its source. None is reproduced from memory or invented.
- [ ] Performance is stated only where the source shows it, and otherwise marked unknown.
- [ ] Each example is filed by type, section, awareness level, structure and angle, with why it works.
- [ ] Models are borrowed for structure and angle, never copied word for word.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.
- [ ] The reply (not just the file) ends with the **Principle / Framework / Source** block, after the still-missing list.

## Principle and source

Model the structure of what works, never copy the words, and never call an example proven without evidence: a swipe file is a library of real examples filed by why they work. Swipe files in direct-response practice (Gary Halbert, The Boron Letters; Eugene Schwartz); The Complete Marketing System, section 10 Copywriting (Servidad, 2026).
