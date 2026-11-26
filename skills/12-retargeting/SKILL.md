---
name: 12-retargeting
description: Build the retargeting ladder with audience rule, message, offer, frequency and exclusions per rung, from visitors to buyers. Use for retargeting, remarketing, abandoned-cart ads or custom audiences.
metadata:
  section: "12 Funnel"
  covers: "Retargeting"
---
# Retargeting

Most visitors leave without acting. Retargeting follows up with each group differently, according to how far they got: a visitor needs proof, a cart abandoner needs the last objection answered, a buyer needs the next offer, or nothing. One message for everyone wastes money and annoys people.

Save the requested plan or asset as a Markdown file in `work/12-funnel/` (file name under Output) when the required inputs are present. Creating this deliverable is part of the task, including requests worded as planning or design. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/awareness.md` → **Traffic temperature**, from `03-traffic-temperature` (plugin mkt-q1-audience).
- `context/offer.md` → **Core offer**, from `07-offer-design` (plugin mkt-q2-offer).
- If present, also read `context/awareness.md` → Awareness map; `context/offer.md` → Value ladder, Guarantee, and Urgency and scarcity; `context/message.md` → Objection map and Proof stack; any audience sizes or performance data in `inputs/`.
- If a required section is missing:
  - **The upstream evidence exists:** run the skill that fills it first, then continue. If that skill is not loaded, stop and say: enable mkt-q1-audience (Traffic temperature) or mkt-q2-offer (Core offer). Price and guarantee are the owner's commitments: never generate them yourself; stop and ask, or offer the owning skill's proposal for approval.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Traffic temperature → `03-traffic-temperature`, in mkt-q1-audience; Core offer → `07-offer-design`, in mkt-q2-offer), the plugin to enable if that skill is not loaded,, and what the user should bring. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Define the rungs:** all visitors, engaged (viewed key pages or video), leads (opted in), cart or checkout abandoners, buyers. Use only the events the business can actually track. If tracking is unknown, list it as a prerequisite for `17-tracking-plan`.
2. **Give each rung:** the audience rule (event and window), the message (the awareness map's entry message for cold rungs; the objection it answers, from the objection map, for warmer rungs), the offer (from the value ladder, or the Core offer if no ladder exists), the frequency cap, and exclusions (buyers out of acquisition ads).
3. **Platform capabilities.** Audience types, windows, minimum sizes, consent requirements and policy limits change. Verify them in the platform's current documentation or the ad account, and mark anything unverified *to confirm*. See [references/ladder.md](references/ladder.md).
4. **Privacy and consent:** retargeting depends on consent where the law requires it. Note the consent and policy checks; never suggest workarounds.
5. **Name the metric per rung,** with the baseline if known.
6. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features, platform capabilities or delivery terms that aren't in `context/` or `inputs/`. Mark inferences `(assumption)`, and list what is needed under Open questions. Describe each source only as it reads: no outcome, motive or behaviour the source doesn't state. In the founder's or brand's voice, add no habits, promises or operational details (who reads replies, what a call covers) that context doesn't contain.

For current platform capabilities specifically, the official documentation verified in step 3 is also a source: cite the URL and access date, preserve the documented scope, and distinguish documentation from availability in this account. This exception does not authorize external sources to supply the business's prices, offers, customer evidence or performance.

## Output

Write `work/12-funnel/12-retargeting-<YYYY-MM-DD>.md`, adding `-<slug>` after the date when more than one is written the same day:

```markdown
# Retargeting ladder: <what it is for>
Skill: 12-retargeting · Date: <YYYY-MM-DD> · Framework: <name>
Built from: <context sections used, with their status>
## Rungs
| Rung | Audience rule (to confirm) | Message (awareness entry or evidenced objection) | Offer | Frequency | Exclusions | Metric |
| --- | --- | --- | --- | --- | --- | --- |
## Prerequisites (tracking, consent)
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

- [ ] Each rung has its own audience rule, message, offer, frequency and exclusions. Buyers are excluded from acquisition ads.
- [ ] Cold-rung messages match the awareness entry; warmer-rung messages answer evidenced objections. Offers come from context.
- [ ] Platform capabilities, windows and limits are verified or marked *to confirm*. None is stated from memory.
- [ ] Consent and tracking prerequisites are named, with no workarounds.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Follow up by how far each person got: a different message and offer for visitors, leads, abandoners and buyers, within consent and the platform's current rules. Retargeting ladder; traffic temperature, Traffic Secrets (Russell Brunson); The Complete Marketing System, section 12 Funnel (Servidad, 2026).
