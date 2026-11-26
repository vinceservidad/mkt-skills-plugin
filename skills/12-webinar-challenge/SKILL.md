---
name: 12-webinar-challenge
description: Design a webinar or challenge funnel from registration to show-up, event, offer and follow-up. Use for a webinar, masterclass or 5-day challenge that sells. Not for a full launch (use 12-launch).
metadata:
  section: "12 Funnel"
  covers: "Challenge funnel; Webinar funnel"
---
# Webinar and challenge funnel

A live event concentrates attention: people register, show up, learn something real, and decide while the energy is there. The funnel's job is to fill the event with the right people, get them to show up, deliver value that builds belief, and make the offer with a real reason to decide.

Save the requested plan or asset as a Markdown file in `work/12-funnel/` (file name under Output) when the required inputs are present. Creating this deliverable is part of the task, including requests worded as planning or design. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Core offer**, from `07-offer-design` (plugin mkt-q2-offer).
- `context/message.md` → **Story**, from `08-story-epiphany-bridge` (plugin mkt-q3-message).
- `context/message.md` → **Big idea**, from `08-message-doc` (plugin mkt-q3-message).
  (Story or Big idea: at least one)
- If present, also read `context/offer.md` → Price and model, Guarantee, Bonuses, and Urgency and scarcity; `context/message.md` → Proof stack and Objection map; `context/awareness.md` → Awareness map and Traffic temperature.
- If a required section is missing:
  - **The upstream evidence exists:** run the skill that fills it first, then continue. If that skill is not loaded, stop and say: enable mkt-q2-offer (Core offer) or mkt-q3-message (Story, Big idea). Price and guarantee are the owner's commitments: never generate them yourself; stop and ask, or offer the owning skill's proposal for approval.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Core offer → `07-offer-design`, in mkt-q2-offer; Story → `08-story-epiphany-bridge`, or Big idea → `08-message-doc`, both in mkt-q3-message), the plugin to enable if that skill is not loaded,, and what the user should bring. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Choose the format:** a webinar funnel (one session) for a mid- to high-ticket offer and a warm audience; a challenge (3–5 days, a small win each day) for a community-style offer or a less aware audience. See [references/event-funnels.md](references/event-funnels.md).
2. **Map the funnel:** traffic → registration page → confirmation → show-up reminders (email or SMS, with consent) → event → offer → replay window → follow-up sequence → close.
3. **Plan the event:** the webinar flow (hand off the script to `10-vsl-script`), or the challenge days (a daily task, quick win and belief shifted, with the offer on the last day).
4. **Make the offer and the reason to decide** real: terms from `offer.md`, and the replay or bonus deadline only if true.
5. **Set the metrics per step:** registration rate, show rate, offer conversion, replay conversion, each with a baseline or "unknown".
6. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features, platform capabilities or delivery terms that aren't in `context/` or `inputs/`. Mark inferences `(assumption)`, and list what is needed under Open questions. Describe each source only as it reads: no outcome, motive or behaviour the source doesn't state. In the founder's or brand's voice, add no habits, promises or operational details (who reads replies, what a call covers) that context doesn't contain.

## Output

Write `work/12-funnel/12-webinar-challenge-<YYYY-MM-DD>.md`, adding `-<slug>` after the date when more than one is written the same day:

```markdown
# Event funnel: <what it is for>
Skill: 12-webinar-challenge · Date: <YYYY-MM-DD> · Framework: <name>
Built from: <context sections used, with their status>
Format: <webinar / challenge> · Offer: <…> · Reason to decide: <true, from offer.md>
## Funnel steps
## Event plan (flow or days)
## Assets and hand-offs
| Asset | Owning skill | Inputs, gaps and approvals |
| --- | --- | --- |
| Webinar speaking script (for webinar format) | 10-vsl-script | Run-of-show, verified offer terms, proof limits and unresolved owner decisions |
## Metrics
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

- [ ] The format fits the offer and audience, and every funnel step from registration to close is planned.
- [ ] The event delivers real value, and its stories and proof come from context. No invented case studies.
- [ ] A webinar's speaking script is explicitly handed to `10-vsl-script` with its source inputs and gaps; the run-of-show alone does not complete that hand-off.
- [ ] Offer terms and any deadline are true and come from `offer.md`.
- [ ] Metrics have baselines or say unknown. Reminders respect consent.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

A live event sells when the right people show up, get real value that shifts their beliefs, and meet an offer with a true reason to decide. Webinar and challenge funnels, Expert Secrets and DotCom Secrets (Russell Brunson); The Complete Marketing System, section 12 Funnel (Servidad, 2026).
