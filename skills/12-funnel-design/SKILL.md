---
name: 12-funnel-design
description: Design the funnel from first touch to back end, one job per step, by funnel type and traffic temperature (TOFU/MOFU/BOFU, AARRR). Use for a sales, quiz or application funnel, or a leaky funnel.
metadata:
  section: "12 Funnel"
  covers: "AARRR / Pirate metrics; Application funnel; Bowtie funnel; Customer Value Optimization; Funnel hacking; Funnel types (Brunson); Quiz funnel; TOFU / MOFU / BOFU"
---
# Funnel design

A funnel is the offer sequence laid out in time: the value ladder on a timeline. Every step has one job and one call to action, and earns the next step. Cold traffic needs fewer, gentler steps; high-ticket offers need more. The money is in the follow-up, because most buyers don't buy on first contact.

Save the requested plan or asset as a Markdown file in `work/12-funnel/` (file name under Output) when the required inputs are present. Creating this deliverable is part of the task, including requests worded as planning or design. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/offer.md` → **Value ladder**, from `07-value-ladder` (plugin mkt-q2-offer).
- `context/offer.md` → **Core offer**, from `07-offer-design` (plugin mkt-q2-offer).
- `context/awareness.md` → **Traffic temperature**, from `03-traffic-temperature` (plugin mkt-q1-audience).
- `context/awareness.md` → **Awareness map**, from `03-awareness-map` (plugin mkt-q1-audience).
  (Value ladder or Core offer: at least one; Traffic temperature or Awareness map: at least one)
- If present, also read `context/awareness.md` → Journey (`03-journey-map`); `context/customer.md` → Buying triggers and process; `context/offer.md` → Price and model, Guarantee, and Urgency and scarcity; any conversion data in `inputs/`.
- If a required section is missing:
  - **The upstream evidence exists:** run the skill that fills it first, then continue. If that skill is not loaded, stop and say: enable mkt-q2-offer (Value ladder, Core offer) or mkt-q1-audience (Traffic temperature, Awareness map). Price and guarantee are the owner's commitments: never generate them yourself; stop and ask, or offer the owning skill's proposal for approval.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (Value ladder → `07-value-ladder`, or Core offer → `07-offer-design`, both in mkt-q2-offer; Traffic temperature → `03-traffic-temperature`, or Awareness map → `03-awareness-map`, both in mkt-q1-audience), the plugin to enable if that skill is not loaded,, and what the user should bring. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **Choose the funnel type** (Funnel types, Brunson) for each traffic temperature and offer, using [references/funnel-types.md](references/funnel-types.md):
   - **Lead:** squeeze or quiz funnel.
   - **Unboxing:** tripwire.
   - **Presentation:** VSL or webinar.
   - **Phone:** application funnel (qualify high-ticket buyers before a call), then the call.

   Match high price and complex offers to more steps; cold traffic to a free first step. If the user supplies competitors' funnels (funnel hacking), treat them as evidence about those competitors, with date and source, not as proof the type works for this offer.
2. **Lay out the steps:** traffic source → entry page → capture → nurture → sales step → checkout or call → thank-you → onboarding hand-off → back end. Give each step:
   - one job;
   - one call to action;
   - the supported offer from the value ladder, or the Core offer when no ladder exists;
   - the asset that exists, or the gap.

   Check the layout against Customer Value Optimization (lead magnet → tripwire → core offer → profit maximizer → return path). A stage with no real offer is a gap, not an invented rung. Where post-purchase matters, also check the Bowtie funnel: acquisition on the left, expansion and advocacy on the right. Right-side steps need real offers and assets or are gaps; retention tactics belong to the retention skills.

   Give each traffic temperature or source that needs a different entry page or call to action its own path: a separate numbered row, or sub-rows such as 2a and 2b, each with exactly one call to action. Never merge several sources' calls to action into one row. If a step needs two jobs or two calls to action, split it into two steps; a job joined with *then* or *and* is two jobs. A delivery, thank-you or service step can support the same offer; write *no new offer* where no sale is proposed. Do not invent a ladder rung or turn a bonus, guarantee or booking action into a separate offer.
3. **Use only real offers and assets.** A step that needs an offer or asset that doesn't exist is marked *gap → skill that builds it*: `12-lead-magnet`, `12-landing-page`, `12-email-sequences` and so on. If the sources do not establish whether an asset exists, mark its availability *unverified* and name the owner to check with; absent evidence does not prove an asset is missing.
   Account for the ladder's relevant back-end and side-entry offers. Include each as a conditional branch, or explicitly defer it with the source-supported reason (audience priority, missing terms or delivery readiness). A missing price or proposed feature is a hold, not permission to invent an offer or silently drop the branch.
4. **Set the metric per step** (opt-in rate, show rate, close rate, take rate), with the baseline if `inputs/` has one. Otherwise write "baseline: unknown". Never invent benchmarks.
5. **Separate a measured leak from an untested priority.** Name a measured leak only when comparable stage counts or conversion data establish it. Interviews and complaints can reveal friction but cannot establish the largest or weakest measured hand-off. Without stage data, state that no measured leak is established, label a proposed priority as a hypothesis, and name the counts needed to test and rank it.
6. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features, platform capabilities or delivery terms that aren't in `context/` or `inputs/`. Mark inferences `(assumption)`, and list what is needed under Open questions. Describe each source only as it reads: no outcome, motive or behaviour the source doesn't state. In the founder's or brand's voice, add no habits, promises or operational details (who reads replies, what a call covers) that context doesn't contain.

## Output

Write `work/12-funnel/12-funnel-design-<YYYY-MM-DD>.md`, adding `-<slug>` after the date when more than one is written the same day:

```markdown
# Funnel map: <what it is for>
Skill: 12-funnel-design · Date: <YYYY-MM-DD> · Framework: <name>
Built from: <context sections used, with their status>
## Steps
| # | Step | Job | Call to action | Offer | Asset (exists or gap → skill) | Metric (baseline or unknown) |
| --- | --- | --- | --- | --- | --- | --- |
## Measured leak or untested priority
Evidence status: <measured, with stage data; or hypothesis, with limits and the data needed>
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

- [ ] Every step has one job, one call to action, a supported ladder or Core offer (or *no new offer* for a delivery/service step), and an asset or a named gap with the skill that builds it. No offer is invented to fill a row.
- [ ] No Call to action cell lists more than one call to action (one path per traffic temperature or source, as separate rows or sub-rows), and no Job cell joins two jobs with *then* or *and*.
- [ ] The funnel type fits the traffic temperature and the offer's price and complexity.
- [ ] Metrics have a baseline from the inputs or say unknown. No invented benchmarks or conversion rates.
- [ ] A measured leak has supporting stage data. Qualitative friction and proposed priorities are labelled as hypotheses, with no unsupported ranking.
- [ ] Back end and follow-up are included, not only the first purchase. Relevant ladder branches are included or explicitly deferred with a reason; unresolved terms remain holds.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

The funnel is the value ladder on a timeline: every step has one job and earns the next, the front end acquires, the back end profits, and the money is in the follow-up. DotCom Secrets (Russell Brunson); Customer Value Optimization (DigitalMarketer); AARRR (Dave McClure); The Complete Marketing System, section 12 Funnel (Servidad, 2026).
