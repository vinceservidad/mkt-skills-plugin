---
name: 08-message-doc
description: Write the message document every ad, page and email draws from, with big idea, promise, mechanism, reason why, enemy and message house. Use for what to say, messaging framework, Rule of One.
metadata:
  section: "08 Message"
  covers: "4Ps of persuasion (taught by AWAI); Big Idea; Big Idea 5-question test (Ogilvy); Enemy / villain; Intensification and copy mechanics (Schwartz); Laddering (benefit ladder); Message house; Reason Why (Hopkins); Rule of One; SUCCESs (Heath)"
---
# Message document

Decide what you say before writing any ad or page. One message, one idea, one reader. A claim with a reason beats the bare claim, and the best message is usually found in customer research, not invented. The message document is the single source that copy, creative and funnel skills read, so they all say the same thing.

## Needs (read before writing)

- `context/offer.md`, with both sections present (drafted or confirmed, with content):
  - **Dream outcome**, from `07-offer-design`: what the promise is about;
  - **Core offer**, also from `07-offer-design`: what delivers it.
- `context/awareness.md` → **Awareness map**, from `03-awareness-map`. It must be present: the message enters at the level most buyers are at.
- If present, also read:
  - `context/customer.md`: Voice of customer (`02-voc-mining`), Beliefs, objections and drivers, Jobs to be done, Current alternatives;
  - `context/positioning.md` → Unique mechanism (`06-unique-mechanism`), the owned mechanism;
  - the rest of `context/offer.md` (guarantee, price).
- If a required section is missing:
  - **The upstream evidence exists:** run the missing skill first (`07-offer-design` or `03-awareness-map`), then continue. If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer. If `03-awareness-map` is not loaded, stop and say: enable mkt-q1-audience.
  - **It doesn't:** stop. Name every missing section and the skill that fills it, and what the user should bring. Do not write a message for an undefined offer or buyer. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Find the big idea in the evidence.** Any claim about competitors or "everyone else" (what they say, what they lack) needs a source: `context/market.md` → Competitors and alternatives, or the inputs. Without one, mark it `(assumption)` or leave it out. Look for one surprising, emotionally charged, relevant idea that the dream outcome, the buyer's language and the mechanism point to. Write two or three candidates and pick one, with the reason.
2. **Write the promise.** Ladder each candidate benefit (laddering): feature → functional benefit → emotional benefit → value, stopping at the rung the buyer's own words support and marking higher rungs `(assumption)`. This is the headline claim: the outcome, for this reader, with a time frame or specificity the offer can keep. Pitch it at the awareness level most buyers are at, from the awareness map.
3. **Name the mechanism.** This is how the offer produces the result. If `positioning.md` owns a unique mechanism, use it as written; otherwise describe the actual method and mark the name as a proposal.
4. **Write the reason why.** Why it works, and why the offer is shaped and priced as it is (Hopkins). Use only facts from the offer, the context or the inputs.
5. **Name the enemy.** A villain or false belief that the buyer and the brand oppose together, drawn from the beliefs and alternatives in evidence. Attack an idea or a way of doing things, never a named competitor's character.
6. **Build the message house:**
   - **Roof:** the core promise.
   - **Three pillars:** supporting messages, each tied to a top objection or job.
   - **Foundation:** the proof each pillar needs. Leave the proof detail to `08-proof-stack`.
7. **Run the 4Ps of persuasion (taught by AWAI) check:** Promise, Picture, Proof, Push, each present or flagged as a gap. Then run the Rule of One, SUCCESs, Ogilvy's Big Idea 5-question filter, and Schwartz's intensification checks using [references/message-tests.md](references/message-tests.md) and [references/message-classics.md](references/message-classics.md).
8. **Check before saving.** Re-read the draft against the Checks and fix any failure.

## Output

Write these sections of `context/message.md`, replacing each body and leaving every other section exactly as it was:

| Section | What goes in it |
| --- | --- |
| `## Big idea` | the idea and why it beat the alternatives |
| `## Promise` | the claim, the reader, and the awareness level it is pitched at |
| `## Mechanism` | the method, and whether its name is owned or proposed |
| `## Reason why` | why it works and why the offer is shaped as it is |
| `## Enemy` | the villain or false belief, with evidence |
| `## Message house` | roof, three pillars, and the proof needed per pillar |

Format each section the same way:
- It starts with `Status: draft (<YYYY-MM-DD>, 08-message-doc)`, then `Written by: 08-message-doc, <YYYY-MM-DD>`.
- It ends with `Evidence:` and `Method:`. Name the framework used, for example: *Big Idea (Ogilvy); Rule of One (Masterson & Forde); Reason Why (Hopkins); message house*.
- Proposed lines (the promise, the pillars, a mechanism name) are written in italics, not quotation marks. Quotation marks are only for buyers' exact words, with a source.
- Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/message.md` does not exist, first copy [assets/message.md](assets/message.md) to `context/message.md`, then write your sections.

Leave Proof stack, Objection map and Story to their own skills.

Reply with:
- the promise and the big idea;
- the next skill: `08-proof-stack`, then `08-objection-map`.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

**Quotation marks are evidence.** Put words in quotation marks only when they appear exactly in a source (a review, an interview, the story material), with its ID. Everything you write yourself (a promise, a belief to shift, an answer, a softened claim, a line of copy, a story line) goes in italics: *like this*. Before saving, find every quotation mark in your draft and check the words against the source.
Then run [scripts/check_quotes.py](scripts/check_quotes.py) on the file you wrote (`python3 <this skill's folder>/scripts/check_quotes.py context/message.md`). For every line it prints, copy the exact words from the source or drop the quotation marks and use italics, then run it again until it reports every quotation matches.

## Checks

- [ ] One big idea, chosen over named alternatives with a reason. The promise makes one claim, for one reader, that the offer can keep.
- [ ] The promise is pitched at the awareness level the map says most buyers are at.
- [ ] The mechanism is either the owned one from `positioning.md` or is labelled a proposal. The reason why uses only real facts.
- [ ] The enemy is an idea or a way of doing things, drawn from evidence, and attacks no named competitor.
- [ ] The message house has a roof, three pillars tied to evidenced objections or jobs, and the proof each pillar needs.
- [ ] Claims about competitors or the category cite a source or carry `(assumption)`.
- [ ] No invented results, numbers or credentials. Quotation marks hold only buyers' exact words, and proposed lines are in italics.
- [ ] Only the six owned sections changed. Each has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

One message, one idea, one reader, with a reason why: a claim with a reason outperforms the bare claim, and the best message is found in customer research, not invented. Big Idea (David Ogilvy, Ogilvy on Advertising); Breakthrough Advertising (Eugene Schwartz); Reason Why, Scientific Advertising (Claude Hopkins); Rule of One, Great Leads (Michael Masterson & John Forde); SUCCESs, Made to Stick (Chip & Dan Heath); The Complete Marketing System, section 8 Message (Servidad, 2026).
