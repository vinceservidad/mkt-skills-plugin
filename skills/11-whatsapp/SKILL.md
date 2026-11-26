---
name: 11-whatsapp
description: Plan WhatsApp and conversational messaging with opt-in, templates and flows. Use for WhatsApp marketing, WhatsApp Business API, Click-to-WhatsApp ads, chat cart recovery, or Messenger automation.
metadata:
  section: "11 Distribution"
  covers: "WhatsApp & conversational messaging"
---
# WhatsApp and conversational messaging

In much of the world — the UK, Europe, Latin America, Asia and the Middle East — WhatsApp is where customers already read messages and talk to brands, often outperforming SMS and email for reply speed and order recovery. Unlike plain SMS, WhatsApp is a rich two-way thread governed by Meta's strict opt-in rules, pre-approved message templates (Utility, Marketing, Authentication), a 24-hour customer-service window and per-message quality ratings that throttle or pause accounts when users block or report spam. WhatsApp works when opt-in is explicit and channel-specific (a phone number collected for delivery is not WhatsApp marketing consent), utility/service threads that solve real friction come before promotional broadcasts, conversations feel human with quick-reply buttons and a clear human hand-off, and broadcasts are tightly capped. It fails when brands import checkout phone lists without opt-in, blast unrequested promos that tank quality rating, or trap customers in dead-end bots.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present and the request does not depend on unconfirmed commercial terms (see Owner commitments). Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/awareness.md` → **Journey** (from `03-journey-map`) or **Awareness map** (from `03-awareness-map`): the moments where a WhatsApp or chat message helps.
- If present, also read `context/offer.md` → Core offer, Price and model, Bonuses, Urgency and scarcity; `context/customer.md` → ICP and personas, Voice of customer; `context/brand.md` → Voice; phone-number, consent, ticket, region and tool notes in `inputs/`; any work in `work/11-distribution/11-sms-*.md`, `work/11-distribution/11-email-channel-*.md`, `work/13-conversion/13-cart-recovery-*.md` or `work/15-retention/15-lifecycle-*.md`.
- If the required section is missing:
  - **The upstream evidence exists** (tickets, reviews or interviews in `inputs/`): run `03-journey-map` first, then continue.
  - **It doesn't:** stop. Name the missing section with the skill that fills it (Journey → `03-journey-map`; Awareness map → `03-awareness-map`) and ask for evidence. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Any offer, price, discount or deadline inside a WhatsApp broadcast or flow is the owner's commitment. If the request asks to write or send a promotional WhatsApp blast built around an unconfirmed offer, discount or deadline that `offer.md` and `inputs/` do not hold (such as a flash sale or coupon), stop, ask the owner to confirm the exact terms, and write no deliverable file in `work/11-distribution/` (a stop reply still ends with the **Principle, framework, source** block). If the request asks for a full WhatsApp channel plan that also mentions an unconfirmed promo idea alongside confirmed service needs (such as shipping updates and opt-in design), write the plan without writing that proposed offer as a live broadcast, mark it *owner to set*, and ask for confirmation.
- If `03-journey-map` and `03-awareness-map` are both not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/whatsapp-guide.md](references/whatsapp-guide.md) for WhatsApp Business App vs. Platform (API), explicit opt-in consent, Meta template categories, the 24-hour customer-service window, quality-rating protection, Click-to-WhatsApp ads and Messenger/ManyChat conversational flows.

1. **Outcome and channel fit.** Name what WhatsApp or conversational messaging is for (fewer "where is my order" tickets, higher-speed replies, abandoned-cart recovery, replenishment reminders or qualified lead triage) and verify regional audience fit (do buyers actually use WhatsApp vs. SMS in `11-sms`?). Raw open/read rates are never the outcome.
2. **Who can be messaged, and for what.** Count contacts by how their phone numbers were collected with [scripts/tally.py](scripts/tally.py) or the notes. A phone number entered at checkout for the carrier is **not** WhatsApp opt-in consent. Separate customer-initiated conversations (24-hour service window), opted-in **Utility** templates (order/shipment confirmations, delivery heads-up — zero promotional upsell tucked inside, or Meta reclassifies and rejects them), and explicitly opted-in **Marketing** templates (restocks, cart recovery, promos). Verify local privacy law (GDPR, UK PECR, TCPA, LGPD, etc.) and mark *to confirm*.
3. **Collect explicit channel opt-in.** Design clean opt-in entry points (unchecked checkout/thank-you box naming WhatsApp explicitly, QR/wa.me links on packaging or site, Click-to-WhatsApp ad entry, or chat widget), log timestamp + source + exact consent text, and include an immediate one-tap opt-out button or STOP reply on every marketing template. Route final consent copy to legal review.
4. **Templates and conversational flows by journey moment.** Map each message or two-way flow to an evidenced journey moment (a ticket group, a checkout drop-off, a reorder window). Utility/service messages that fix real customer friction come first. Keep automated flows short (2 to 3 quick-reply steps) with a clear human escalation path so no customer is trapped in a bot loop. Never stuff an unconfirmed promo or upsell inside a Utility template.
5. **Cadence, quiet hours and quality-rating guardrails.** Cap Marketing templates tightly, respect local quiet hours, segment inactive or non-engaging recipients out early, and monitor Meta's Phone Number Quality Rating (Green / Yellow / Red) and block/report rates before increasing volume.
6. **Platform setup and cost.** Distinguish WhatsApp Business App (free, manual, single/small-team inbox, not for scalable automated marketing) from WhatsApp Business Platform / Cloud API (Business verification, BSP or direct Cloud API, per-template pricing by category and country). Cite current Meta WhatsApp Business pricing and template category rules with a verified official URL and access date, or mark them *to confirm* cleanly — never cite this skill's own guide as official documentation. Buying a BSP/automation tool needs owner approval.
7. **Tracking.** Track per flow/template: delivered, read, replies, human escalations, blocks/opt-outs, tickets deflected, and orders/revenue attributed cleanly (`17-tracking-plan`). Watch block/opt-out rate per template.
8. **Approval.** The plan is a draft. Sending templates, adding WhatsApp opt-ins to checkout, connecting the Cloud API/BSP or launching Click-to-WhatsApp ads requires the owner's explicit approval.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, opt-in counts, offers, prices, response rates or per-message fee figures that are not in `context/` or `inputs/` or cited with a date from official docs. Mark inferences `(assumption)` and list missing facts under Open questions. No third-party benchmark read or conversion rate is evidence.

## Output

Write `work/11-distribution/11-whatsapp-<YYYY-MM-DD>-<slug>.md`:

```markdown
# WhatsApp and conversational messaging plan: <business, period>
Skill: 11-whatsapp · Date: <YYYY-MM-DD> · Framework: WhatsApp & conversational messaging (explicit channel opt-in, Utility before Marketing, 24-hour service window, quality-rating guardrails)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing sent, no opt-in changed, no BSP/tool bought
## Outcome and channel fit
## Who can be messaged
| Group | Count | How the number was collected | Utility templates? | Marketing templates? |
| --- | --- | --- | --- | --- |
## Explicit opt-in and opt-out design
## Templates and flows by journey moment
| Journey moment (evidence) | Trigger / entry | Meta category (Service 24h / Utility / Marketing) | Draft message & buttons | Cap & human hand-off |
| --- | --- | --- | --- | --- |
## Cadence, quiet hours and quality-rating guardrails
## Platform setup (App vs. Cloud API / BSP) and cost
## Tracking
## Platform and legal facts
| Fact the plan relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write draft WhatsApp messages and button labels in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`) and fix every line it prints until it reports every quotation matches.

Reply with the file path, who can be messaged now (and why checkout numbers cannot receive marketing blasts), the first Utility/service vs. Marketing flows, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Phone numbers are grouped by collection method; carrier/delivery checkout numbers are never treated as WhatsApp marketing opt-in.
- [ ] Meta template categories (Utility vs. Marketing vs. 24-hour Service window) are kept strictly separate, with no promotional upsell smuggled into Utility templates.
- [ ] Every flow maps to an evidenced journey moment, puts service/utility friction fixes first, caps marketing cadence with quiet hours, includes an opt-out and specifies human hand-off.
- [ ] Only offers in `offer.md` are used; any unconfirmed offer or discount is marked *owner to set* or triggers a stop on promo blasts.
- [ ] WhatsApp Business App vs. Cloud API/BSP costs, template rules and local privacy laws are cited with dated official docs or marked *to confirm*, with legal review and owner approval flagged.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

WhatsApp is an invited two-way conversation, not a broadcast megaphone: earn explicit WhatsApp opt-in first, separate clean Utility updates from Marketing templates, protect your quality rating with strict caps and human hand-off, and never blast unopted checkout numbers. WhatsApp & conversational messaging, The Complete Marketing System, section 11 Distribution (Servidad, 2026); Meta WhatsApp Business Platform Messaging Policy.
