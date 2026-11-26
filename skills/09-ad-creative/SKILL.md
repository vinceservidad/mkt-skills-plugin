---
name: 09-ad-creative
description: Produce ad concepts, variations and iterations for paid social and display with Hook-Story-Offer. Use for ad concepts, new creatives, iterating winners. Not for ad words alone (10-ad-copy).
metadata:
  section: "09 Creative Strategy"
  covers: "Hook–Story–Offer; Meta Andromeda / creative diversity; Meta Reels creative essentials; Native advertising; Visual hierarchy"
---
# Ad creative

An ad has three parts: the hook that stops the scroll, the story that makes the viewer care, and the offer that tells them what to do. A concept is one way into the message, built from those three parts; a variation changes one element of a concept; an iteration is the next round, built from what the last round taught. Native ads borrow the look and feel of the feed they sit in, so they get watched before they get judged.

Save the concepts as a Markdown file in `work/09-creative-strategy/` when the required inputs are present. Creating this deliverable is part of the task. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/message.md` → **Promise**, from `08-message-doc`.
- `context/awareness.md` → **Awareness map**, from `03-awareness-map`.
- `context/offer.md` → **Core offer**, from `07-offer-design`.
- If present, also read `context/message.md` → Big idea, Mechanism, Enemy, Proof stack, Objection map, Story and Message house; `context/customer.md` → Voice of customer and Segments; `context/awareness.md` → Traffic temperature; `context/offer.md` → Price and model, Guarantee, Bonuses, Urgency and scarcity, Value ladder; `context/brand.md` → Distinctive assets and Voice; `work/09-creative-strategy/09-angle-matrix-*.md`, `work/09-creative-strategy/09-hooks-*.md`, `work/09-creative-strategy/09-creative-brief-*.md`; past ad results and ad logs in `inputs/`.
- If a required section is missing:
  - **The upstream evidence exists:** run the skill that fills it first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Promise → `08-message-doc`; Awareness map → `03-awareness-map`; Core offer → `07-offer-design`), and ask for evidence (interviews, reviews, call notes, past ad results), not a description of the buyer. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- Price, discounts, guarantees and deadlines are the owner's commitments. Use only what `offer.md` holds; if a concept needs one that isn't there, stop and ask.
- If `03-awareness-map` is not loaded, stop and say: enable mkt-q1-audience.
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/concepts-and-iteration.md](references/concepts-and-iteration.md) for the concept card, native formats, and how to read results; [references/creative-mechanics-and-diversification.md](references/creative-mechanics-and-diversification.md) for the 9 creative mechanic families, creative diversification matrix, AI-invariant rules and post-win single-variable iteration; [references/meta-andromeda-reels-diversity.md](references/meta-andromeda-reels-diversity.md) for Meta Andromeda creative diversity across Persona x Desire x Awareness x Mechanic x Format, similarity vs. fatigue triage, Reels creative essentials and Advantage+ Creative enhancement guardrails; [references/static-dtc-and-mobile-review.md](references/static-dtc-and-mobile-review.md) for static DTC visual direction, centered 4:5 to 1:1 cross-crop framing and the nine-criterion mobile-first review; and [references/demand-gen-and-youtube-creative.md](references/demand-gen-and-youtube-creative.md) for Google Demand Gen and YouTube creative variety (16:9, 1:1, 9:16 Shorts-first), ABCD 5-second structure, creator Partnership Ads and fatigue refresh rules.

1. **Read past results first, if any are in `inputs/`.** Count with [scripts/tally.py](scripts/tally.py) and compute every rate with its formula shown. Per concept, report spend, the platform-reported metrics (impressions, frequency, clicks, leads) and the business outcome from the CRM or orders (qualified calls, trials, purchases) separately. Judge concepts by cost per qualified outcome, not CTR or clicks. Say when samples are too small to call a winner, when concepts differ in more than one thing (destination, format, audience) so the comparison is confounded, and when a falling CTR with rising frequency is a *fatigue pattern* (a hypothesis, not a proven cause). Platform-reported and CRM numbers are different sources; never merge them into one figure.
2. **Decide per existing concept:** keep, iterate (new variation of what worked), refresh (same angle, new execution), or retire, each with the evidence. Budget changes, scaling and bid or audience changes are not this skill's call: hand them to `19-scale-paid`, which needs readiness, economics and authorization gates. Never recommend putting more money behind an ad.
3. **Write new concepts:** three to six, each one angle at one awareness level (from the angle matrix if it exists, or from the message house and awareness map). For each, the concept card: angle and evidence; format and why it suits the angle; **Hook** (seen, said, on-screen, all three written: for a sound-off or no-voiceover cut, *said* is the opening line as spoken in the sound-on cut or read in the first caption, never left blank); **Story** (the beats, in order, each tied to a message or proof item); **Offer** (one CTA to an offer that exists, and a destination that suits the concept's traffic temperature; if no existing destination suits it, leave the concept out and name the missing page under Open questions rather than shipping a concept you call a mismatch); native fit (what makes it look like the feed's content); proof used and its permission status.
4. **Variations:** for each concept, two or three variants that change exactly one element (hook, visual, proof, CTA), each naming the element. Placement crops and colour swaps are adaptations, not variations.
5. **Iteration plan:** what the next round will test, the one variable, the business outcome that decides, a minimum sample or time before judging, and a stop rule. Hand detailed test design to `18-creative-testing`.
6. **Platform currency:** formats, specs, placements, AI creative features and ad policies change. Cite the platform's own documentation with URL and date checked, or the user's ad account, or write *to confirm*. Never state what an algorithm rewards.
7. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features or delivery terms that aren't in `context/` or `inputs/`. No generalisations about buyers in your own lines, including in payoffs and frequency words (*most owners*, *many people*, *everyone*, *so often*, *usually*, *always*), unless a source counts them; say it about the evidence instead (*10 of 12 closed deals*) or mark it `(assumption)`. Never invent exclusivity claims (*only work with*), competitor labels (*generalists*), extra problem items, or *every [role]* phrasing inside hooks, story beats, or slide outlines unless a source states them verbatim. Never state how a platform format renders or behaves unless verified in first-party docs during this run; mark format behavior *to confirm*. Mark inferences `(assumption)` and list what is needed under Open questions. Reviews and testimonials in ads need permission: every review ID a concept draws on (quoted, paraphrased, used as a hook line, a variation or a proof beat) gets its own permission status on that concept's Proof and permission line. Competitor claims need a dated source or an `(assumption)` label. A concept that wins is evidence for that angle, audience, channel and period only.

## Output

Write `work/09-creative-strategy/09-ad-creative-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Ad creative: <campaign or channel>
Skill: 09-ad-creative · Date: <YYYY-MM-DD> · Framework: Hook–Story–Offer; concept → variation → iteration
Built from: <context sections and inputs used, with their status>
Status: draft concepts; nothing launched or changed in any ad account
## What past results show (if any)
| Concept | Spend | Platform-reported (impr., freq., clicks, leads) | Business outcome (source) | Cost per outcome (formula) | Read |
| --- | --- | --- | --- | --- | --- |
Decisions: <concept — keep / iterate / refresh / retire — evidence>
Confounds and sample limits: <…>
## New concepts
### Concept <n>: <name>
Angle and level: <angle — awareness level — evidence>
Format and native fit: <…>
Hook: seen <…> · said <…> · on-screen <…>
Story: <beat — message or proof item>
Offer: <CTA — offer in offer.md — destination>
Proof and permission: <item — permission status>
Variations: <a — changes: element> · <b — changes: element>
## Iteration plan
<next test — variable — deciding outcome — minimum sample or time — stop rule>
## Claims and sources
| Claim in a concept | Source |
| --- | --- |
## Hand-offs
<budget or scaling → 19-scale-paid; words → 10-ad-copy; visuals → 09-image-video; test design → 18-creative-testing>
## Open questions
## Principle, framework, source
```

Change nothing in `context/` and nothing in any ad account. Concepts are a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a review, an interview, a line from the ad log), with the source named. Hooks, scripts and lines you write go in plain text or italics, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/09-creative-strategy/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the key decisions (what to keep, retire and make next) and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Past results, if any, are judged by business outcome per cost, with formulas, sample limits and confounds stated; platform-reported and CRM figures kept apart.
- [ ] Fatigue is called a pattern or hypothesis, not a proven cause; no budget, bid or scaling recommendation (handed to `19-scale-paid`).
- [ ] Every concept has a hook with seen, said and on-screen all written, story beats, and one CTA to an offer that exists at a destination that suits its traffic temperature.
- [ ] Variations change exactly one named element.
- [ ] No invented results, testimonials, prices or terms, and no unsourced generalisation about buyers (*most owners*); every review ID used in a concept, quoted or paraphrased, carries its permission status.
- [ ] Platform formats, specs and policies are cited with a dated first-party source or marked *to confirm*.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Every ad is a hook, a story and an offer; test distinct concepts, then vary one element of what works, judged by the business outcome, not the click. Hook–Story–Offer, DotCom Secrets (Russell Brunson); concept → variation → iteration and the native ad principle, The Complete Marketing System, section 9 Creative Strategy (Servidad, 2026); Scientific Advertising (Claude Hopkins).
