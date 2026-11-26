---
name: 03-traffic-temperature
description: Classify traffic as cold, warm or hot and match each source to a landing page, offer and call to action. Use for where traffic should land. Not for awareness levels (use 03-awareness-map).
metadata:
  section: "03 Awareness"
  covers: "Traffic temperature"
---
# Traffic temperature

Cold traffic doesn't know you, warm traffic knows you, and hot traffic is ready to buy. The same page cannot serve all three. Sending cold strangers to a "book a call" page wastes the click; sending hot referrals through a free guide wastes the sale. This skill gives each source a temperature and the page, offer and call to action that fit it.

## Needs (read before writing)

- `context/awareness.md` → **Awareness map**, from `03-awareness-map`. It must be present (drafted or confirmed, with content): temperature is awareness, expressed as traffic.
- If present, read:
  - `context/offer.md` → **Value ladder** (`07-value-ladder`), for which offer exists at each step;
  - `context/awareness.md` → **Journey** (`03-journey-map`), for today's assets.
- Read the list of traffic sources: the user's message, lead-source data in `inputs/`, or Buying triggers and process. Read conversion data by source, if supplied.
- If the Awareness map is missing:
  - **ICP and pains are present:** run `03-awareness-map` first, then continue.
  - **Not present:** stop. Name every missing section with the skill that fills it (Awareness map → `03-awareness-map`; ICP and personas → `02-icp-persona`; Pains, desires and fears → `02-customer-research`; Value ladder → `07-value-ladder`, which lives in mkt-q2-offer: if it is not loaded, say enable mkt-q2-offer). Ask for customer evidence (interviews, call notes, reviews), not a description of the buyer: the user's own summary is a hypothesis, not evidence. Do not assign temperatures, pages or offers for an unmapped buyer; one line on the general principle is the most you give.
  - A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **List every traffic source** the user has or plans to use: referrals, search terms, paid social, podcasts, email list, retargeting, partners, events. Keep any volume or conversion numbers given, with their source.
2. **Assign a temperature from the awareness evidence:**
   - **Cold:** unaware or problem aware; has never heard of you.
   - **Warm:** problem or solution aware; knows you a little, through content, a list or a podcast.
   - **Hot:** product or most aware; a referral, a returning visitor, a branded search, an existing customer.

   When conversion by source is known, let it confirm or correct the label. For example, referrals closing at several times other sources are hot.
3. **Match the landing page, offer and call to action** to the temperature, using the awareness map's entry message and offer:
   - **Cold:** a story, a lead magnet or free value; a low-commitment call to action.
   - **Warm:** proof and a mid-commitment step, such as a demo, sample or trial.
   - **Hot:** the offer, pricing and a direct call to action.

   Use only offers that exist in `offer.md` or the user's message. Mark a needed offer that does not exist yet as a gap. Do not invent it.
   Write each call to action as proposed copy in italics, never in quotation marks: *Book a call*, not a quoted button label.
4. **Flag mismatches:** a source landing on a page built for another temperature, for example cold ads sent to a booking page.
5. **Note the warming path:** how a cold visitor becomes warm. That means a list, retargeting or follow-up content. Pass it to `12-funnel-design` as a gap if none exists.
6. **Check before saving.** Re-read the draft against every item under Checks and fix any failure before you write the section. The usual ones are a call to action, search term or label you wrote in quotation marks, an offer that does not exist, and a statement about buyers without `(assumption)`.

See [references/temperature.md](references/temperature.md) for the matching table.

## Output

Write `context/awareness.md` → `## Traffic temperature`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Traffic temperature
Status: draft (<YYYY-MM-DD>, 03-traffic-temperature)
Written by: 03-traffic-temperature, <YYYY-MM-DD>
| Source | Temperature | Evidence | Page | Offer | Call to action | Mismatch today |
| --- | --- | --- | --- | --- | --- | --- |
Warming path: <how cold becomes warm, or "missing" → 12-funnel-design>
Offers needed but missing: <offer — temperature — hand off to 07-offer-design>
Evidence: <sections and inputs used>
Method: Traffic temperature (Brunson, Traffic Secrets); Schwartz's awareness levels
```

Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/awareness.md` does not exist, first copy [assets/awareness.md](assets/awareness.md) to `context/awareness.md`, then write your section into it.

Reply with:
- the biggest mismatch;
- the next skill: `12-funnel-design` or `12-landing-page` for the pages, or `07-value-ladder` if the offers are missing.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every source the user named has a temperature, with the evidence or reasoning behind it, and conversion data where given.
- [ ] Cold sources get a low-commitment entry. Hot sources get the offer and a direct call to action.
- [ ] Only offers and pages that exist are assigned. Missing ones are listed as gaps, not invented.
- [ ] Mismatches between source and landing page are named.
- [ ] A warming path for cold traffic is stated or flagged as missing.
- [ ] Quotation marks hold only words copied exactly from a source (no added or moved words, and not the note-taker's summary around a quote). Paraphrased buyer questions, labels, proposed messages and calls to action go without quotation marks (use italics for proposed copy).
- [ ] No unmarked inference: any statement about buyers that the evidence does not state (a motive, a frequency word such as "often" or "most", a share or rate the inputs don't give) carries `(assumption)` or is left out.
- [ ] Only `## Traffic temperature` changed in `context/awareness.md`. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

Match the ask to the temperature: cold traffic gets value before a request, warm traffic gets proof, and hot traffic gets the offer, because the same page cannot serve strangers and buyers. Traffic temperature, Traffic Secrets (Russell Brunson); levels of awareness, Breakthrough Advertising (Eugene Schwartz); The Complete Marketing System, section 3 Awareness (Servidad, 2026).
