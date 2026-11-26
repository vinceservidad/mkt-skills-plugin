---
name: 12-landing-page
description: Plan a landing page for one traffic source and one offer, with message match, one call to action, proof and form. Use for opt-in or campaign pages. Not for page copy (use 10-page-copy).
metadata:
  section: "12 Funnel"
  covers: "Landing page"
---
# Landing page

A landing page serves one visitor from one source with one offer and one call to action. The page must match the ad or link the visitor came from, speak to their temperature and awareness, and remove the doubts that stop this visitor, nothing more.

Save the requested plan or asset as a Markdown file in `work/12-funnel/` (file name under Output) when the required inputs are present. Creating this deliverable is part of the task, including requests worded as planning or design. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Core offer**, from `07-offer-design` (plugin mkt-q2-offer).
- `context/message.md` → **Promise**, from `08-message-doc` (plugin mkt-q3-message).
- `context/awareness.md` → **Traffic temperature**, from `03-traffic-temperature` (plugin mkt-q1-audience).
- `context/awareness.md` → **Awareness map**, from `03-awareness-map` (plugin mkt-q1-audience).
  (Traffic temperature or Awareness map: at least one)
- If present, also read `context/message.md` → Proof stack and Objection map; `context/offer.md` (lead magnet, guarantee, price); `context/customer.md` → Voice of customer; the ad or source copy the user gives.
- If a required section is missing:
  - **The upstream evidence exists:** run the skill that fills it first, then continue. If that skill is not loaded, stop and say: enable mkt-q2-offer (Core offer), mkt-q3-message (Promise) or mkt-q1-audience (Traffic temperature, Awareness map). Price and guarantee are the owner's commitments: never generate them yourself; stop and ask, or offer the owning skill's proposal for approval.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Core offer → `07-offer-design`, in mkt-q2-offer; Promise → `08-message-doc`, in mkt-q3-message; Traffic temperature → `03-traffic-temperature`, or Awareness map → `03-awareness-map`, both in mkt-q1-audience), the plugin to enable if that skill is not loaded,, and what the user should bring. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Fix the source, the visitor and the offer:** one traffic source, its temperature, the offer shown (a free asset for cold, a call or purchase for hot), and the one call to action. Do not add other ladder items, freebies or bonuses as add-ons or sweeteners: anything offered besides the source's offer is a second offer. List it under Open questions instead.
2. **Match the message:** the headline continues the promise of the ad or link they clicked. If you don't have the ad, ask for it or mark it *to match*.
3. **Lay out the sections for this temperature,** using [references/landing-page.md](references/landing-page.md): headline, subhead, what they get, proof, top objections for this visitor, the form or button, and reassurance (privacy, what happens next).
4. **Keep the form minimal:** only the fields the next step needs.
5. **Write the copy at wireframe level,** with every claim in the claims table. Name a copy framework on the Method line only if the page follows its structure in order (for PAS: a problem section, then an agitate section, then the solution, before what they get); otherwise leave it off.
6. **Name the metric and the test:** conversion rate from this source, with its baseline or "unknown", and the first element to test.
7. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features, platform capabilities or delivery terms that aren't in `context/` or `inputs/`. Mark inferences `(assumption)`, and list what is needed under Open questions. Describe each source only as it reads: no outcome, motive or behaviour the source doesn't state. In the founder's or brand's voice, add no habits, promises or operational details (who reads replies, what a call covers) that context doesn't contain.

## Output

Write `work/12-funnel/12-landing-page-<YYYY-MM-DD>.md`, adding `-<slug>` after the date when more than one is written the same day:

```markdown
# Landing page: <what it is for>
Skill: 12-landing-page · Date: <YYYY-MM-DD> · Framework: <name>
Built from: <context sections used, with their status>
Source: <one traffic source> · Temperature: <cold/warm/hot> · Offer: <one offer> · Call to action: <one>
## Page (sections and copy)
## Form fields
## Metric and first test
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

- [ ] One traffic source, one offer and one call to action, and the offer suits the source's temperature.
- [ ] The page offers nothing besides that one offer: no other ladder item, freebie or bonus added as a sweetener (any such idea sits under Open questions).
- [ ] The headline matches the ad or link, or the gap is marked *to match*.
- [ ] The form asks only for what the next step needs.
- [ ] Proof, offers and terms come from context and are listed in the claims table. Nothing is invented.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

One visitor, one source, one offer, one action: match the message they clicked and remove only the doubts that stop this visitor. Landing page practice (Oli Gardner, Unbounce); Don't Make Me Think (Steve Krug); The Complete Marketing System, section 12 Funnel (Servidad, 2026).
