---
name: 11-ai-seo-geo
description: Get the brand cited in AI search answers (generative engine optimization). Use for GEO, AI SEO, showing up in ChatGPT, Perplexity or AI Overviews, LLM visibility.
metadata:
  section: "11 Distribution"
  covers: "AI search / GEO (generative engine optimization)"
---
# AI search and GEO

When a buyer asks an AI assistant "who should I use for this?", the answer names a few options and cites a few sources. The job is to make the business easy to find, easy to describe correctly and easy to corroborate: crawlers that serve answers can reach the pages, the business is described the same way everywhere, its pages state specific facts it can stand behind, and the third-party sources the assistants already cite know it exists. Nobody controls an AI answer. A plan that promises placement, games answers with fake reviews or planted forum posts, or blocks the crawlers that serve search to stop training, does harm.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required, either one (drafted or confirmed, with content):
- `context/positioning.md` → **Positioning statement**, from `06-positioning-statement`: how the business should be described; or
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: whose questions matter.
- If present, also read `context/positioning.md` → Category, Differentiation, Competitive alternatives; `context/awareness.md` → Journey, Voice of customer, Buying triggers and process (the questions buyers ask); `context/message.md` → Proof stack; `context/offer.md` → Core offer; `context/market.md` → Competitors and alternatives; any AI-answer spot checks, analytics referrals, robots.txt, CDN settings, site inventory or third-party mention lists in `inputs/`; any work in `work/11-distribution/11-seo-*.md` or `work/06-positioning/06-competitor-pages-*.md`.
- If both required sections are missing:
  - **The upstream evidence exists** (for example interview notes in `inputs/`): run the skill that fills one first, then continue.
  - **It doesn't:** stop. Name both sections with their skills (Positioning statement → `06-positioning-statement`; ICP and personas → `02-icp-persona`), and ask for evidence (customer interviews, sales notes, competitor research), not a description. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- No AI-answer sample is not a stop: design the prompt set and the baseline as the first step, and state current visibility as *unknown*.
- If `06-positioning-statement` is not loaded, stop and say: enable mkt-q2-offer.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.

## Process

Use [references/geo-guide.md](references/geo-guide.md) for the access table, the baseline protocol and the platform-claims rule.

1. **The outcome.** Name what being recommended should produce for this business (a qualified call, a subscriber, a visit to a comparison page) and how it will be measured: referral sessions from assistant domains and their conversions in analytics and the CRM, with the referral definition stated. Mention or citation rates from sampled prompts are visibility estimates, not traffic or revenue. An answer read without a click leaves no referral; never fill that gap with an assumed multiplier.
2. **The prompt set.** Build 10 to 20 prompts from the buyer's real questions: sales-call questions, journey-stage questions, Voice of customer words, alternatives they compare. Cover category ("best … for …"), problem ("how do I …"), comparison ("X vs Y", "alternatives to …") and brand ("[name] reviews").
3. **Baseline.** If a spot check is in `inputs/`, tally it per prompt and assistant with [scripts/sum_by.py](scripts/sum_by.py) or line by line: who is named, which sources are cited, whether the business appears. Label it a dated snapshot (one run, one account, one place), not a measurement. If no check exists, write the protocol: assistants, dates, runs per prompt, logged-out or logged-in, location, and what to record.
4. **Access.** Read robots.txt, page directives and any CDN bot settings in the material. For each rule, name the use it affects (search index, AI answers at query time, model training) and whether it supports the business outcome. Never recommend blocking a search crawler to stop training; use the narrowest control that expresses the decision. Which user agent does what is vendor documentation: cite it with URL and date or mark *to confirm*. robots.txt states a preference; it is not enforcement.
5. **Entity clarity.** Write the one plain description the business should carry everywhere (from the Positioning statement or ICP and Core offer): what it is, for whom, where, and the facts that set it apart. List where it must match: the site's home and About pages, profiles (Google Business, LinkedIn), directories, podcast and partner pages. Inconsistent or missing descriptions are a gap.
6. **Citable pages.** For the prompts that matter, name the page that should answer each one directly and early, with specific facts the business can stand behind (from context and `inputs/`, with their source). Existing pages already cited are protected and strengthened first. Comparison pages go to `06-competitor-pages`; search fundamentals (indexing, intent) to `11-seo`; structured data to `11-schema`.
7. **Third-party corroboration.** From the baseline, list the sources the assistants cite (review sites, lists, forums, publications, podcasts). For each, the legitimate way to be present: a listing request (`11-directories`), earned coverage (`11-pr`), customer reviews asked for honestly (`16-reviews`), genuine participation disclosed as the company. No fake reviews, paid placements presented as editorial, sock-puppet forum posts or undisclosed incentives.
8. **Emerging standards.** `llms.txt`, Markdown versions, agent-readiness checklists and similar are standards checks, not evidence of citation or revenue; recommend them only as low-cost hygiene, labelled as such, unless an engine documents otherwise (cite it).
9. **Measurement rhythm.** Re-run the same prompt set on a stated cadence and compare like with like. This plan *designs* the check; it does not schedule or run it.
10. **Platform facts and approval.** AI products, crawler names and controls, CDN settings and answer features change often: cite the vendor's own current documentation with URL and date, or mark *to confirm*. Never state one from memory as current. Changes to robots.txt, CDN bot settings, page directives or site-wide content are live changes needing exact scope, rollback and the owner's approval.
11. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, deadlines, offers, features, benchmarks, platform capabilities or delivery terms that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Describe each source only as it reads. A vendor's or tool's published figure about AI traffic is not evidence about this business; leave it out. Competitor claims need a dated source or an `(assumption)` label.

## Output

Write `work/11-distribution/11-ai-seo-geo-<YYYY-MM-DD>-<slug>.md`:

```markdown
# AI search plan: <business, period>
Skill: 11-ai-seo-geo · Date: <YYYY-MM-DD> · Framework: Generative engine optimisation (entity, access, citable content, corroboration)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing on the site or in any setting changed
## Outcome and measurement
## Prompt set
| # | Prompt | Type (category / problem / comparison / brand) | Why it matters (evidence) |
| --- | --- | --- | --- |
## Baseline (dated snapshot)
| Prompt | Assistant | Named | Sources cited | Business appears? |
| --- | --- | --- | --- | --- |
## Access: crawlers and controls
| Rule or setting (as found) | Use it affects | Keeps or hurts the outcome | Proposal | Status of the vendor fact (documented URL and date / to confirm) |
| --- | --- | --- | --- | --- |
## Entity description and where it must match
## Pages to answer the prompts
| Prompt group | Page (exists / to build) | Facts it must state (source) | Owner skill |
| --- | --- | --- | --- |
## Third-party sources to earn
## Not now
## Measurement rhythm (designed, not scheduled)
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`, on the site, or in any setting. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a page, a spot-check log, a review), with the source named. Write your own descriptions, prompts and proposals in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the baseline in one line (or that there is none), the top three actions, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The business outcome is measured by assistant referrals and conversions; mention or citation rates are called sampled estimates; no placement is promised and no multiplier is assumed.
- [ ] The prompt set comes from the buyer's real questions with evidence; any baseline is tallied and labelled a dated snapshot with its method.
- [ ] Every crawler or control proposal names the use it affects, never blocks a search crawler to stop training, cites vendor documentation with URL and date or marks it *to confirm*, and needs the owner's approval.
- [ ] One entity description, consistent with the positioning or ICP, with the places it must match.
- [ ] Pages state only facts in context or `inputs/`; third-party presence is earned honestly, with no fake reviews, planted posts or undisclosed incentives.
- [ ] `llms.txt` and readiness checks are labelled hygiene, not citation levers, unless an engine's documentation is cited.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

AI assistants recommend what they can reach, describe and corroborate: make the business crawlable for answers, described the same way everywhere, specific on its own pages and present in the sources assistants already trust, then measure the visits and customers it brings, not the mentions. Generative engine optimisation (GEO), The Complete Marketing System, section 11 Distribution (Servidad, 2026); GEO: Generative Engine Optimization (Aggarwal et al., 2023); vendor crawler documentation (verify current).
