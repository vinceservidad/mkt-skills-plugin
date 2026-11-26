---
name: 08-story-epiphany-bridge
description: Write the founder or brand discovery story as an Epiphany Bridge from real events. Use for origin story, about us story, webinar or VSL story, Brunson. Not for the core message (use 08-message-doc).
metadata:
  section: "08 Message"
  covers: "Epiphany Bridge; Hero's Journey"
---
# Story (Epiphany Bridge)

People don't change their beliefs because they were told to. They change them when they relive the moment someone else changed theirs. The Epiphany Bridge tells the true story of how the founder or brand discovered the thing they now sell, so the buyer has the same epiphany. It only works if it is true, so this skill builds it from the real events and never invents them.

## Needs (read before writing)

- `context/customer.md` → **Beliefs, objections and drivers**, from `02-buyer-psychology`. It must be present: it holds the beliefs the story must rebuild.
- `context/offer.md` → **Core offer**, from `07-offer-design`. It must be present: it is what the story leads to.
- **The real story material:** founder notes, an interview transcript, an "about" page, or what the user tells you in the conversation. Read `inputs/` for it.
- If present, also read `context/message.md` (Big idea, Enemy, Mechanism) and Voice of customer.
- If a required section is missing:
  - **The evidence exists:** run the missing skill first (`02-buyer-psychology` or `07-offer-design`), then continue. If `02-buyer-psychology` is not loaded, stop and say: enable mkt-q1-audience. If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.
  - **It doesn't:** stop. Name the missing sections and the skills that fill them.
- If the context is present but there is **no story material**, don't write the Story section and never invent events, people, numbers or feelings. Save the questions that would draw the story out to `work/08-message/08-story-epiphany-bridge-<YYYY-MM-DD>-story-questions.md` and ask the user to answer them.
- Every reply, including a stop, ends with the **Principle, framework, source** block.

## Process

1. **Pick the belief to rebuild,** usually the top vehicle belief ("this kind of solution can't work for me"). Then the internal and external ones, if the story can carry them. See [references/epiphany-bridge.md](references/epiphany-bridge.md).
2. **Find the true events in the story material:**
   - the backstory;
   - the desire;
   - the wall the founder hit;
   - the epiphany (the moment they saw it differently);
   - the plan;
   - the conflict;
   - the achievement;
   - the transformation.

   These beats follow the Hero's Journey shape, with the founder as hero of this true story; customer-as-hero framing (StoryBrand) is owned in Brand. Use only events, numbers and feelings the material states. Mark anything else as a question for the founder.
3. **Write the story,** short enough to tell in two to three minutes, in the founder's voice, using the material's own words where it has them. Proposed lines are not quotations; keep quotation marks for exact words from the material. Do not add a motive or causal link the material does not state ("that is why I…", "because of that weekend"): a list of refusals, values or habits stays a list, and if the material does not tie it to an event, ask the founder instead of tying it.
4. **Map the story to beliefs:** for each beat, note which belief it rebuilds, so later copy can cut it to fit.
5. **Write the one-line version,** for ads and bios.
6. **Check before saving.** Re-read the draft against the Checks and fix any failure.

## Output

With story material, write `context/message.md` → `## Story`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Story
Status: draft (<YYYY-MM-DD>, 08-story-epiphany-bridge)
Written by: 08-story-epiphany-bridge, <YYYY-MM-DD>
Belief to rebuild: <vehicle / internal / external belief — evidence>
Story (2–3 minutes): <backstory → desire → wall → epiphany → plan → conflict → achievement → transformation>
Beats → beliefs: <beat — belief it rebuilds>
One-line version: <proposal>
Open questions for the founder: <anything the material doesn't say>
Evidence: <story material and context used>
Method: Epiphany Bridge (Brunson, Expert Secrets)
```

Without story material, write only `work/08-message/08-story-epiphany-bridge-<YYYY-MM-DD>-story-questions.md` and leave `context/` unchanged.

Never set `confirmed` unless the user approves.

When you write the section, update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/message.md` does not exist, first copy [assets/message.md](assets/message.md) to `context/message.md`, then write this section.

Reply with:
- the epiphany in one line, or the questions to answer;
- the next skill: `10-vsl-script` or `12-webinar-challenge` for long-form use.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

**Quotation marks are evidence.** Put words in quotation marks only when they appear exactly in a source (a review, an interview, the story material), with its ID. Everything you write yourself (a promise, a belief to shift, an answer, a softened claim, a line of copy, a story line) goes in italics: *like this*. Before saving, find every quotation mark in your draft and check the words against the source.
Then run [scripts/check_quotes.py](scripts/check_quotes.py) on the file you wrote (`python3 <this skill's folder>/scripts/check_quotes.py context/message.md`). For every line it prints, copy the exact words from the source or drop the quotation marks and use italics, then run it again until it reports every quotation matches.

## Checks

- [ ] Every event, number, person and feeling in the story is in the story material. Nothing is invented or embellished, and gaps are listed as questions for the founder. No line gives the founder a reason, motive or cause the material does not state.
- [ ] The story rebuilds a named, evidenced buyer belief, and each beat is mapped to the belief it shifts.
- [ ] It follows the Epiphany Bridge arc, and the epiphany is a change of belief, not just an event.
- [ ] Without story material, no Story section was written and the questions file was saved.
- [ ] Quotation marks hold only words copied exactly from the material.
- [ ] Only `## Story` changed. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

People change beliefs by reliving someone else's epiphany, not by being told, so tell the true story of how you came to believe what you now sell, and never invent it. Epiphany Bridge, Expert Secrets (Russell Brunson); story structure, StoryBrand (Donald Miller); The Complete Marketing System, section 8 Message (Servidad, 2026).
