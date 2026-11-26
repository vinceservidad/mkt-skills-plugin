---
name: 07-value-ladder
description: Lay out the value ladder from free to low-ticket, core, high-ticket and continuity with the trigger to each step. Use for tripwire, memberships, premium tier. Not for core offer (use 07-offer-design).
metadata:
  section: "07 Offer"
  covers: "Continuity / subscription; Tripwire; Value Ladder"
---
# Value ladder

A value ladder gives buyers a path of increasing value and price. Free value earns attention, a low-ticket offer turns a stranger into a customer, the core offer delivers the result, a high-ticket offer serves those who want more, and continuity keeps the relationship. Each step needs a job and a trigger that moves people up. Steps nobody climbs are clutter.

## Needs (read before writing)

- `context/offer.md`, with both sections present (drafted or confirmed, with content):
  - **Core offer**, written by `07-offer-design`: the centre of the ladder;
  - **Price and model**, written by `07-pricing`: the core price the other steps are set around.
- If present, also read:
  - `context/customer.md` → Segments (`02-segmentation`), for which segment sits on which step;
  - `context/awareness.md` → Awareness map (`03-awareness-map`), for which step each awareness level enters at;
  - Beliefs, objections and drivers;
  - any data in `inputs/` on repeat purchase, upgrades or what customers asked for beyond the core.
- If Core offer or Price and model is missing:
  - **The upstream skill's inputs exist:** run `07-offer-design` or `07-pricing` first, then continue.
  - **They don't:** stop. Name the missing sections and those skills. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Place the core offer** and its price at the centre.
2. **For each step, decide whether it should exist,** with evidence:
   - **Free:** lead magnet, content, a tool.
   - **Low-ticket:** a tripwire or self-liquidating offer.
   - **High-ticket:** done for you, advisory, premium.
   - **Continuity:** a subscription, retainer or membership.

   A step exists when evidence shows demand or a clear job: customers asking for more, a segment that can't afford the core, churn that a lighter plan would save, a free asset that already draws people. Leave a step empty, and say why, rather than inventing one.
3. **Give each step** a job, a deliverable, a price (or "not set" for `07-pricing`), and the trigger that moves a buyer up. Write the Job and the trigger in your own words, without quotation marks. Quote only in the Evidence column, only words copied exactly from the source, with its ID. Mark proposed steps as proposed. See [references/ladder-guide.md](references/ladder-guide.md).
4. **Check the economics.** The front end should pay for acquisition, or the back end should profit. Say what is known and what is `(assumption)`.
5. **Map the segments and awareness levels to entry steps,** where the evidence allows.
6. **Check before saving.** Re-read the draft against the Checks and fix any failure.

## Output

Write `context/offer.md` → `## Value ladder`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Value ladder
Status: draft (<YYYY-MM-DD>, 07-value-ladder)
Written by: 07-value-ladder, <YYYY-MM-DD>
| Step | Offer | Job | Price | Exists or proposed | Moves up when (trigger) | Evidence |
| --- | --- | --- | --- | --- | --- | --- |
Entry points: <segment or awareness level → step>
Economics: <front end pays for acquisition? back end profit? known vs (assumption)>
Empty steps: <step — why it is left empty>
Evidence: <sources>
Method: Value Ladder (Brunson, DotCom Secrets); tripwire (DigitalMarketer); continuity
```

Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/offer.md` does not exist, first copy [assets/offer.md](assets/offer.md) to `context/offer.md`, then write your section.

Reply with:
- the ladder in one line;
- the step with the strongest evidence to add first;
- the next skill: `12-funnel-design`, or `12-upsell-path`.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every step has a job, a deliverable, a price (or "not set") and a trigger to the next step.
- [ ] Steps are marked as existing or proposed. A proposed step cites evidence of demand. Steps without evidence are left empty with a reason.
- [ ] The economics are stated: what the front end and back end do, with unknowns marked.
- [ ] No price, conversion rate or demand figure is invented. Inferences carry `(assumption)`.
- [ ] Quotation marks hold only words copied exactly from a source. Job and trigger cells have none.
- [ ] Only `## Value ladder` changed. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

Give every buyer a next step of greater value: free value earns attention, the front end acquires the customer, the core delivers the result, and the back end and continuity create the profit, but only steps with evidence of demand belong on the ladder. Value Ladder, DotCom Secrets (Russell Brunson); tripwire and self-liquidating offers (DigitalMarketer); The Complete Marketing System, section 7 Offer (Servidad, 2026).
