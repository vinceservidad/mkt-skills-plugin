---
name: 01-sophistication-stage
description: Place the market on Schwartz's five sophistication stages and pick the claim type that still works. Use for market sophistication, why claims stop working, what to lead with.
metadata:
  section: "01 Market"
  covers: "Market sophistication (Schwartz)"
---
# Sophistication stage

The more claims a market has heard, the less a plain claim works. The first provider can just say what it does. The second has to say it bigger. When bigger stops working, buyers need to hear how it works (a mechanism), then a better mechanism, and finally, when they distrust every claim, they respond to being recognised: identification. This skill reads the claims the market has already heard and says which kind of claim still has room.

## Needs (read before writing)

- `context/market.md` → **Competitors and alternatives**, written by `01-competitor-profiling`. It must be present (drafted or confirmed, with content). It supplies the claims the market has already heard.
- If present, also read:
  - `context/message.md` → Promise, Mechanism and Big idea (`08-message-doc`): the claim this business makes today;
  - `context/customer.md` → Beliefs, objections and drivers (`02-buyer-psychology`) and Voice of customer (`02-voc-mining`): evidence of buyer scepticism, such as *they all promised the same thing*;
  - `context/awareness.md` → Awareness map (`03-awareness-map`);
  - `context/offer.md` → Core offer and Guarantee: what the business can actually back;
  - competitor headlines, ads or pages in `inputs/`.
- If Competitors and alternatives is missing:
  - **Competitor evidence supplied** (headlines, pages, ads, notes in `inputs/` or the conversation): run `01-competitor-profiling` first, then continue.
  - **Nothing supplied:** stop. Name the missing section, Competitors and alternatives, and its skill, `01-competitor-profiling`. Ask for competitors' headlines, ads, pricing pages and the claims buyers repeat back, with dates. Never judge sophistication from your own sense of the category. A stop reply still ends with the **Principle, framework, source** block.

## Process

Use [references/stages.md](references/stages.md) for the five stages, their signs and the claim each needs.

1. **List the claims the market has heard.** From the competitor section and inputs, write each claim with who makes it and the date seen, and classify it:
   - **Direct:** says what it does (*bookkeeping for agencies*).
   - **Enlarged:** a bigger, faster or more specific version (*close in 10 business days*).
   - **Mechanism:** says how it works (*an agency-specific chart of accounts*, *a taste quiz*).
   - **Improved mechanism:** a newer, easier or surer version of a mechanism already claimed.
   - **Identification:** speaks to who the buyer is, with little product claim (*for people who'd rather be outside*).

   Count each type with `scripts/tally.py` or `python3`, not by eye.
2. **Add buyer evidence.** Scepticism (*they all promise the same thing*), comparisons of numbers, or questions about how it works show that claims are worn. Quote only exact words.
3. **Place the stage.** Name the stage (1–5) where most of the claims and buyer evidence sit, with the evidence that puts it there.
   - If segments, channels or regions differ, say so and place each.
   - If the evidence is thin (few competitors, one date, no buyer evidence), say the placement is tentative and what would confirm it.
4. **Place the current claim.** If `message.md` or the inputs show the business's own claim, say which type it is and whether it is behind the market (a stage-2 claim in a stage-3 market).
5. **Choose the claim type that still works.**
   - **Stage 1:** the direct claim.
   - **Stage 2:** an enlarged claim the business can prove.
   - **Stage 3:** a new mechanism.
   - **Stage 4:** a better, easier or more specific mechanism than the ones already claimed.
   - **Stage 5:** identification with the buyer, backed by the mechanism and proof.

   Give two or three directions, in italics, never as finished copy. Use only mechanisms, numbers and guarantees that exist in the offer, the proof or the inputs; anything else is *Gap: needs …* for its owner (`06-unique-mechanism` for the mechanism, `08-proof-stack` for proof).
6. **Note the awareness interplay.** If an awareness map exists, say how the stage changes the entry message at the main level. Leave the map itself to `03-awareness-map`.
7. **Check before saving.** Re-read the draft against every item under Checks, and run `scripts/check_quotes.py` on it. Fix any failure before you save.

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from a source: a competitor's headline as recorded, a review, an interview. Your claim types, directions, example lines and summaries go in italics or plain text, in the section and in the reply alike (*for the owner who signed the lease first*, never "for the owner who signed the lease first"). Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py context/market.md`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches. Counts come from [scripts/tally.py](scripts/tally.py) or `python3`.

**Competitor claims are claims.** A claim competitors make shows what buyers have heard, not that it is true or that it works. Never copy one because it is visible.

## Output

Write `context/market.md` → `## Market sophistication`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Market sophistication
Status: draft (<YYYY-MM-DD>, 01-sophistication-stage)
Written by: 01-sophistication-stage, <YYYY-MM-DD>
| Claim type | Who makes it (date seen) | Count |
| --- | --- | --- |
Buyer evidence: <scepticism or comparison, with sources>
Stage: <1–5, name> — <why, with evidence; tentative if thin; by segment or channel if they differ>
Our current claim: <type, and whether it is behind the market, or "not known">
Claim type that still works: <type> — directions: *…*; *…*
Gaps: <mechanism or proof needed, with owner skill>
Evidence: <sections and inputs used>
Method: Five stages of market sophistication, Breakthrough Advertising (Schwartz)
```

Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.

Reply with:
- the stage and the claim type that still works, in one line;
- whether the current claim is behind the market;
- the next skill: `06-unique-mechanism` (stage 3 or 4) or `08-message-doc`.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every claim listed has a competitor and a date from the evidence, and the type counts were tallied, not eyeballed.
- [ ] The stage is placed from the claims and buyer evidence, and marked tentative when the evidence is thin.
- [ ] The claim type that still works matches the stage, and the current claim is compared with it where known.
- [ ] Directions use only mechanisms, numbers and guarantees that exist; anything else is a named gap with its owner skill.
- [ ] Directions and example lines are in italics, not quotation marks or finished copy, in the file and in the reply, and no competitor claim is recommended because it is visible.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] With Competitors and alternatives missing and no competitor evidence, nothing was written and the stop names `01-competitor-profiling`.
- [ ] Only `## Market sophistication` changed (plus Competitors and alternatives if competitor-profiling ran first). It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

The more claims a market has heard, the less a plain claim works: read the claims buyers have already heard, then make the kind of claim that still has room, from a direct claim to a bigger one, a mechanism, a better mechanism, and finally identification. Five stages of market sophistication, Breakthrough Advertising (Eugene Schwartz); The Complete Marketing System, section 1 Market (Servidad, 2026).
