---
name: 11-aso
description: Optimize an app store listing for search, conversion and ratings. Use for ASO, App Store or Google Play listings, downloads, keywords, screenshots, or refusing/replacing fake/staff app reviews.
metadata:
  section: "11 Distribution"
  covers: "App Store Optimization (ASO)"
---
# ASO

An app store listing has two jobs: be found for the searches the buyer makes, and turn a page view into a download. App Store Optimization works when the name, subtitle and keywords match real search terms, the screenshots show the job the app does in the first two frames, ratings are earned and answered, and the work is judged on downloads that become active users or customers. It fails when the listing chases a broad term the app can't win, claims rankings it doesn't have, shows a login screen first, or asks for ratings at the wrong moment.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/positioning.md` → **Positioning statement** (from `06-positioning-statement`) or `context/customer.md` → **ICP and personas** (from `02-icp-persona`): who the listing speaks to and why the app is the choice.
- If present, also read `context/customer.md` → Jobs to be done, Voice of customer, Pains, desires and fears; `context/message.md` → Promise, Proof stack; `context/offer.md` → Core offer, Price and model; `context/brand.md` → Voice, Distinctive assets; the current listing, store analytics, reviews and release notes in `inputs/`.
- If the required section is missing:
  - **The upstream evidence exists** (reviews, tickets or interviews in `inputs/`): run `02-icp-persona` first, then continue.
  - **It doesn't:** stop. Name the missing section with the skill that fills it (Positioning statement → `06-positioning-statement`; ICP and personas → `02-icp-persona`) and ask for evidence. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- If neither section has content and `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.
- If neither section has content and `06-positioning-statement` is not loaded, stop and say: enable mkt-q2-offer.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/aso-guide.md](references/aso-guide.md) for the listing fields, keyword choice, screenshots, ratings and store facts.

1. **Outcome and funnel.** Name the outcome (downloads that log in, subscribe or stay active) and lay out the store funnel from analytics: impressions → product page views → downloads, with conversion at each step computed with [scripts/tally.py](scripts/tally.py) or shown arithmetic, labelled *observed* or *calculated*. Say which step loses most and whether search, browse or web referrals bring the downloads.
2. **Who searches, and for what.** From the ICP, jobs and Voice of customer, list the jobs people would search for (the problem words, not the brand's words). Store analytics may not show search terms; say so, and mark every candidate keyword *(assumption)* until a keyword tool or store data confirms volume and difficulty. A broad, crowded term (a category word) is a poor first target for a small app; prefer specific terms the app answers fully.
3. **Listing fields.** Write the name, subtitle (or short description) and keyword field within the store's limits, without repeating words across fields where the store indexes them once, and without competitor brand names. Field limits and indexing rules are store facts: cite the current developer documentation with URL and date or mark *to confirm*.
4. **Screenshots and preview.** Order screenshots by the job: the first two show the main outcome in the user's words, never a login or settings screen. Each frame gets a caption. A preview video is optional and only from real footage.
5. **Description and claims.** First lines carry the job and the reason to download. Rankings, awards, "#1" and download counts appear only with a dated source; otherwise they are removed and the owner is told why. Store review guidelines forbid misleading claims.
6. **Ratings and reviews.** Read the reviews in `inputs/`: what users praise, what fails, which complaints are fixed. Reply to existing reviews, especially fixed bugs (with their fix date if known), and plan fixes for what low ratings complain about. Never write or plan fake or staff-posted reviews (they mislead buyers and break store rules): if asked to add them, refuse and still write the ASO plan file in `work/11-distribution/` with zero fabricated reviews or ratings, marking any unverified store or legal rules *to confirm* unless verified in official docs with URL and date. Ask for ratings with the platform's own prompt at a moment of success (after a task works), not at launch or after an error; the platform's limits on prompts are store facts to cite or mark *to confirm*.
7. **Test and measure.** Change one thing at a time or use the store's product-page tests where available (a store fact to cite). Judge on conversion from page view to download and on downloads that become active users, with counts and dates.
8. **Approval.** The plan is a draft. Submitting listing changes, replying to reviews or changing in-app prompts needs the owner's explicit approval.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no rankings, download counts, ratings, awards, features or search volumes that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. A feature appears in the listing only if `inputs/` says the app has it.

## Output

Write `work/11-distribution/11-aso-<YYYY-MM-DD>-<slug>.md`:

```markdown
# App store listing plan: <app, store, date>
Skill: 11-aso · Date: <YYYY-MM-DD> · Framework: App Store Optimization (search, page conversion, ratings)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nothing submitted
## Outcome and store funnel
| Step | Count | Conversion | Label |
| --- | --- | --- | --- |
## Who searches and for what
| Candidate keyword | Job it matches (evidence) | Volume and difficulty | Status |
| --- | --- | --- | --- |
## Listing fields
## Screenshots and preview
## Description
## Ratings and reviews
## Tests and measurement
## Store facts
| Fact the plan relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a review, the current listing), with the source named. Titles of books, essays or talks, including in the Principle, framework, source block, go in italics, never in quotation marks. Write proposed listing text in italics or a plain block. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`) and fix every line it prints until it reports every quotation matches.

Reply with the file path, the weakest funnel step, the proposed name, subtitle and first two screenshots, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The store funnel is computed from analytics with labels, and the weakest step is named.
- [ ] Keywords come from the buyer's jobs and words; unconfirmed volumes are *(assumption)*; broad crowded terms are not the first target.
- [ ] Field limits, indexing, review rules and rating-prompt limits are dated or *to confirm*.
- [ ] The first two screenshots show the main outcome; no login or settings screen first.
- [ ] No "#1", ranking, award or count without a dated source; only features the app has.
- [ ] Reviews are read, fixed bugs are answered, and ratings are asked for at a moment of success.
- [ ] Success is judged on page-to-download conversion and active users with counts; nothing is submitted without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Be found for the job your buyer searches, show that job in the first two screenshots, earn ratings at the moment the app works, and judge the listing on downloads that stay. App Store Optimization (ASO), The Complete Marketing System, section 11 Distribution (Servidad, 2026); Apple App Store and Google Play developer documentation (to be cited with dates).
