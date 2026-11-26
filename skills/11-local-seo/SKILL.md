---
name: 11-local-seo
description: Plan Local SEO and Google Business Profile to win Map Pack visibility. Use for local SEO, Google Business Profile, Google Maps ranking, local citations, NAP consistency, or service-area pages.
metadata:
  section: "11 Distribution"
  covers: "Local SEO"
---
# Local SEO

Local search works on different rules than national or blog SEO. When a buyer searches with local intent (a city name, "near me", or a local service), Google ranks businesses in the Map Pack and local organic results on three pillars — relevance, distance and prominence — before the buyer ever sees ten blue links. Local SEO works when the Google Business Profile is accurate and complete, the primary and secondary categories match what the business actually sells, NAP (Name, Address, Phone) is consistent across core directories, real local reviews arrive steadily and get answered, and location or service-area pages carry genuine local proof rather than copy-pasted city names. It fails when businesses stuff keywords into their business name (risking suspension), build thin doorway pages for cities they do not serve, ignore Google Business Profile verification rules, or chase generic blog traffic while invisible on Maps.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present and the request does not depend on unconfirmed operational facts (see Owner commitments). Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`.
- If present, also read `context/offer.md` → Core offer; `context/brand.md` → Brand foundation, Reputation; `context/awareness.md` → Journey; site inventory, Search Console exports, location lists, Google Business Profile notes or review exports in `inputs/`; any work in `work/11-distribution/11-seo-*.md`, `work/11-distribution/11-schema-*.md` or `work/16-referral-community/16-reviews-*.md`.
- If the required section is missing:
  - **The upstream evidence exists** (interviews, reviews or customer notes in `inputs/`): run `02-icp-persona` first, then continue.
  - **It doesn't:** stop. Name the missing section with the skill that fills it (ICP and personas → `02-icp-persona`) and ask for evidence. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Physical street addresses, service-area boundaries, staffed office hours, phone numbers, multi-location eligibility and Google Business Profile verification methods are operational facts only the owner can confirm. Never invent a street address, phone number, opening hours, suite number or service radius that is not in `context/` or `inputs/`. If the request asks to create or publish listings for locations whose real physical eligibility (staffed storefront vs. service-area business vs. virtual office) is unconfirmed, stop and ask the owner to confirm before drafting live listings; if planning a local SEO audit for a known city/site, flag unconfirmed address, phone and GBP eligibility facts explicitly as *owner to confirm*.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/local-seo-guide.md](references/local-seo-guide.md) for the Relevance–Distance–Prominence framework, Google Business Profile audit, storefront vs. service-area eligibility rules, NAP citations, local landing pages and review velocity.

1. **Outcome and local eligibility.** Name the business outcome (qualified local calls, direction requests, consultation bookings or walk-ins) and check whether the business qualifies for Google Business Profile (in-person storefront or direct in-person service-area contact — online-only businesses and virtual/PO-box offices do not qualify under Google's guidelines; verify current rules and mark *to confirm*).
2. **Audit current local footprint.** Inspect `inputs/` (site inventory, footer address, Search Console queries, existing pages, reviews) and count pages or queries with [scripts/tally.py](scripts/tally.py), never by eye. Identify what exists today (for example only a city name in the footer and no local page or `LocalBusiness` schema) and what is missing.
3. **Google Business Profile (GBP) architecture.** Specify exact business name (real-world name only, zero keyword stuffing), primary category (strongest local ranking lever) and strictly relevant secondary categories, storefront vs. hidden-address service-area configuration, services/products list, photos, UTM-tagged website link and Q&A. Mark any unverified owner facts (street address, phone, hours, verification status) as *owner to confirm*.
4. **NAP consistency and core citations.** Define one canonical NAP (Name, Address, Phone) format across website footer, GBP, Apple Business Connect, Bing Places and high-trust local/industry directories (hand broad software/startup directory listings to `11-directories`). Flag duplicate or mismatched listings to clean up before building new citations.
5. **Local landing page and schema plan.** Plan one real page per physical location or core local service + city pair where genuine local proof exists (local clients, local regulatory/market nuances, embedded map/directions if storefront, local FAQs, clear call/booking CTA). Never generate thin doorway pages swapping only city names. Hand JSON-LD `LocalBusiness` / `AccountingService` / `MedicalBusiness` markup implementation to `11-schema` and general non-local blog/technical SEO to `11-seo`.
6. **Review velocity and local prominence.** Connect local prominence to steady, ethical review collection (never gated, never incentivized against platform policy — hand the review-ask workflow to `16-reviews`) plus local PR, partnerships and chambers/associations (`11-pr`, `11-co-marketing`).
7. **Tracking and measurement.** Tag GBP website links with UTMs so Maps traffic is separated from organic web traffic in GA4 (`17-tracking-plan`), track GBP calls, direction clicks and local pack visibility by realistic local grid/queries.
8. **Platform facts.** Google Business Profile eligibility rules, video verification requirements, category taxonomy and Apple Business Connect rules change. Cite verified official documentation (URL and date) or mark *to confirm*.
9. **Approval.** The plan is a draft. Creating or editing GBP listings, changing canonical NAP, publishing location pages or requesting verification requires the owner's explicit approval.
10. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no street addresses, phone numbers, opening hours, rankings, review counts or local search volumes that are not in `context/` or `inputs/`. Even inside draft GBP descriptions or page copy, use only product traits explicitly stated in `context/` or `inputs/` — never add unverified adjectives such as small-batch, handcrafted or award-winning. Mark inferences `(assumption)` and list missing facts under Open questions. No third-party benchmark rank or conversion rate is evidence.

## Output

Write `work/11-distribution/11-local-seo-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Local SEO plan: <business, location(s), period>
Skill: 11-local-seo · Date: <YYYY-MM-DD> · Framework: Local SEO (Relevance, Distance, Prominence; Google Business Profile, NAP citations, local landing pages)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; no GBP listing, citation or page changed
## Outcome and GBP eligibility check
## Current local footprint audit
## Google Business Profile setup
| Field | Recommendation | Status / owner fact needed |
| --- | --- | --- |
## Canonical NAP and citation plan
## Local landing pages and schema hand-off
| Page / URL | Target local intent | Genuine local proof required | Hand-off skill |
| --- | --- | --- | --- |
## Reviews and local prominence
## Tracking (UTMs and GBP actions)
## Platform facts
| Fact the plan relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The plan is a deliverable, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write proposed page titles, GBP descriptions and headlines in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`) and fix every line it prints until it reports every quotation matches.

Reply with the file path, the GBP eligibility check, the top local SEO priorities, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] GBP eligibility (in-person storefront or service-area contact vs. online-only/virtual office) is checked explicitly before recommending a profile.
- [ ] Unconfirmed operational facts (street address, phone, hours, verification status) are marked *owner to confirm* and never invented.
- [ ] GBP categories, real-world business name (no keyword stuffing), canonical NAP and core local citations are specified.
- [ ] Local landing pages require genuine local proof (no thin city-swap doorway pages); `LocalBusiness` markup hands off to `11-schema`, broad SEO to `11-seo`, and review collection to `16-reviews`.
- [ ] GBP website links use UTMs for measurement, and platform rules are cited with a dated official URL or marked *to confirm*.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Local search rewards verified real-world relevance, proximity and prominence, so an accurate Google Business Profile, consistent canonical NAP, genuine local proof pages and steady real reviews outperform keyword stuffing or doorway pages. Local SEO (Relevance, Distance, Prominence), The Complete Marketing System, section 11 Distribution (Servidad, 2026); Google Business Profile Help guidelines.
