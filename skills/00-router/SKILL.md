---
name: 00-router
description: Diagnose marketing symptoms and route to the owning skill, upstream first. Use for leads but no sales, stalled growth, where do I start, or explaining a framework. Not for task requests.
---
# Marketing router

Every marketing request belongs to one of eight questions and one of twenty sections. The section that decides a thing owns it; the others only use it. Route to the owner, make sure its upstream context exists, then hand off. Routing to the visible symptom (the ad, the page) instead of the deciding section is the most expensive mistake in marketing, because it polishes something that was decided wrong earlier.

## Needs (read before routing)

- `context/` in the working directory: the frontmatter and every `Status:` line of `market.md`, `customer.md`, `awareness.md`, `positioning.md`, `offer.md`, `message.md` and `brand.md`. A missing file or folder is information, not an error: it means nothing upstream has been decided yet.
- [references/skills.md](references/skills.md): every skill, its section, whether it is built or planned, what it writes and what it requires.
- [references/diagnosis.md](references/diagnosis.md) whenever the user describes a result or symptom rather than a task.
- [references/term-index.md](references/term-index.md) whenever the user names a framework, tactic or metric (PAS, Value Ladder, RFM, retargeting, MER…).
- [references/sections.md](references/sections.md) for a section's job, principles, frameworks and sources: read only the section you need.
- Nothing is required to route. The router decides what has to happen first; it never refuses for lack of context, and it never fills a gap with invented business facts.

## Process

1. **Classify the request.** Build (wants one artifact), diagnose (reports a result or symptom), plan (where to start, what next, in what order), or learn (wants to understand a topic or framework).
2. **Diagnose symptoms.** Match the symptom to a row in diagnosis.md. Inspect the "check first" sections before the "then" sections: read their context status and any numbers the user gave. The route is the first owning section whose context is empty, draft-only on the point in question, or contradicted by the user's numbers. Name the evidence for each section you clear or flag. State only facts directly present in context/ or inputs/ and mark every inference (assumption); never assert unstated pricing limits, missing tiers, or buyer behavior without checking the files.
3. **Find the owner.** Use term-index.md for a named framework, tactic or metric, otherwise the purposes in skills.md. If a request spans sections, the section that decides goes first.
4. **Walk the upstream chain.** List the target skill's required context sections (skill-index "Requires"). For each one that is absent, put the skill that writes it earlier in the sequence, and repeat for that skill's own requirements. Phase-1 sections (Customer, Awareness, Offer) come before everything that reads them. Stop at skills whose requirements are all present.
   - **Paid-media pre-launch sequence rule:** When a user asks to set up or launch paid ads (Meta/Facebook, Instagram, TikTok, LinkedIn, Google Ads, Shopping), keep upstream strategy first (Customer research and ICP, `02-segmentation` if targeting is undecided, `03-awareness-map`, `07-offer-design`, `08-message-doc`, and `17-unit-economics` for allowable CPA if absent), then place destination landing page QA (`12-landing-page`) and conversion tracking setup (`17-tracking-plan`: Pixel and CAPI deduplication, Google conversion actions or offline CRM imports, and UTMs) BEFORE going live with paid spend (`11-paid-social` or `11-paid-search`). Ongoing reporting, attribution, and incrementality (`17-analytics`, `17-attribution`, `17-incrementality`) run after traffic starts.
5. **Plan from nothing.** If `context/` is empty or missing, follow the learning order: Customer → Awareness → Offer → Message → Copywriting → Funnel → Distribution → Measurement, starting from the first section whose context is missing. Start with `02-customer-research` even though `market.md` is empty too: 01 Market is not in the learning order, so any market work goes after customer research, never as step 1. When the end goal is paid ads, insert conversion tracking setup (`17-tracking-plan`) and destination landing page QA (`12-landing-page`) as pre-launch gates before live spend, keeping reporting and attribution after traffic starts. Write what each step must find out as open questions; do not fill in likely buyers, objections, competitors or prices, even as examples, in the route file or the reply.
6. **Teach.** For a learn request, explain the principle and framework from sections.md in the user's terms, show where it sits in the system (question, section, what it depends on), and recommend, in the reply as well as the route file, the skill whose output builds the artifact, by its full name (for example `07-value-ladder`), saying that running it builds the artifact for this business (and whether it is built or planned), because building the artifact is how the skill is learned.
7. **Write the route file** (below), then hand off:
   - Build request: invoke the first skill in the sequence now if it is `built`. If it is `built` but not loaded, name its plugin from skills.md and say enable <plugin>. If it is `planned`, say so plainly; you may do the work with that section's frameworks from sections.md, writing the result to `work/<NN-section>/<skill-name>-<YYYY-MM-DD>.md` (never into a context section another skill owns).
   - Diagnose, plan or learn request: stop after the route. Give the first step and what the user must supply, and offer to start it.

## Output

Write `work/00-router/00-router-<YYYY-MM-DD>.md`, adding `-<slug>` after the date when more than one route is written the same day:

```markdown
# Route: <one-line request>
Type: build | diagnose | plan | learn
Question: Q<n>. <question>   Section: <NN Section>
## Diagnosis            (diagnose only: symptom, sections checked in order, evidence for each, verdict)
## Context status       (each file: missing / template / draft / confirmed; required sections that are absent)
## Sequence             (ordered: skill path, why it is here, built or planned, what it needs)
## Next step            (the first skill and what the user must supply, if anything)
## Principle, framework, source
```

Change nothing in `context/`: the router reads context, it does not decide it. End your reply to the user with the same three-line **Principle, framework, source** block, so the routing decision teaches the system as well as answering the request.

## Checks

- [ ] Every skill in the sequence exists in skills.md; none is invented, and planned skills are labelled planned.
- [ ] Every required context section for the target skill is present or preceded in the sequence by the skill that writes it.
- [ ] For a symptom, the "check first" sections were inspected, with evidence, before any downstream fix was suggested.
- [ ] Ownership is respected: an item is routed to the section that decides it, not a section that uses it.
- [ ] For any paid-ad setup or launch route, destination landing page QA (`12-landing-page`) and conversion tracking (`17-tracking-plan`) are explicitly sequenced before live ad spend.
- [ ] No business facts were assumed to fill a gap; gaps are routed, not guessed, and `context/` is unchanged.
- [ ] The route file is written and the reply ends with the principle, framework and source.

## Principle and source

Fix the section that decides the result before the sections that express it: results fail at one of eight questions, and the owning section is checked first. Diagnosis table and ownership rule, The Complete Marketing System (Servidad, 2026); find the constraint before you optimize, Theory of Constraints (Goldratt, The Goal).
