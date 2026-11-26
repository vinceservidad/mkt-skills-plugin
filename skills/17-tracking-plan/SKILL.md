---
name: 17-tracking-plan
description: Design tracking plans with events, UTMs, pixels, CAPI and CRM fields, and fix collection defects. Use for tracking plans, UTMs, conversion tracking, Meta reporting more purchases than orders.
metadata:
  section: "17 Measurement"
  covers: "First-party data / CDP; Tracking plan / UTMs / server-side tracking"
---
# Tracking plan

A tracking plan says which events and fields the business records, where, with what names, and which system is the source of truth for each number. It works when every event maps to a business question, names and UTMs follow one convention, browser and server-side collection agree with the store or CRM, consent is respected, and defects are found by reconciling platform counts with the source system. It fails when tags are added because a tool suggests them, a pixel double-counts, UTMs are missing on owned links, or a platform's number is trusted over the order system. Platform setup steps change often and must be checked in current documentation.

Save the tracking plan as a Markdown file in `work/17-measurement/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. The current setup, platform counts and the source system's counts in `inputs/` are the evidence; journey and value ladder context say what matters.
- If present, also read `context/awareness.md` → Journey; `context/offer.md` → Value ladder, Price and model; tool lists, installation notes, platform-reported conversions, store or CRM exports, consent banner details and UTM examples in `inputs/`; any work in `work/17-measurement/` or `work/11-distribution/11-paid-search-*.md` and `11-paid-social-*.md`.
- **No data:** Without a description of the current setup or any counts, write no file in `work/17-measurement/`; in your reply, ask for the list of tools, how each is installed, and one month of platform versus source-system counts (tell the user how to provide them — paste in chat or drop files in `inputs/`), and outline the planned events and UTM rules with every status marked *unknown*. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/tracking-guide.md](references/tracking-guide.md) for event design, UTM conventions, browser and server-side collection, reconciliation, consent and first-party data, and [references/google-data-manager-and-tag-gateway.md](references/google-data-manager-and-tag-gateway.md) when planning Google Ads first-party signal infrastructure (Data Manager CRM/offline imports, Google Tag Gateway first-party tagging, Enhanced Conversions and Consent Mode v2 rollout checks).

1. **Business questions first.** List the questions measurement must answer (which channels bring subscribers who stay, where the checkout loses people), and map each to the events and fields needed.
2. **Source of truth.** For each number (orders, revenue, subscribers, leads), name the system of record (store, billing, CRM) and treat platform numbers as that platform's view.
3. **Reconcile and find defects.** Compare platform-reported conversions with the source system for the same period, with [scripts/sum_by.py](scripts/sum_by.py). Separate collection defects (an event firing on the wrong page, double counting, missing tags) from attribution differences (windows, view-through, models) and from real business change. Each defect gets a fix and an owner.
4. **Event spec.** Event names, when each fires, parameters, and where it is sent (analytics, ad platforms, CRM), in one naming convention. Fire purchase events once per new order, with an order ID for deduplication.
5. **UTMs.** One convention for source, medium, campaign, content; required on every owned link (email, podcast, social bio, partners); a short list of allowed values.
6. **Server-side and first-party data.** Where server-side collection (for example a platform's conversions API) would improve match and reliability, say so with the deduplication rule; what first-party data (email, order history, survey answers) is kept, where, and with what consent. A CDP only if the stack needs one.
7. **Consent and privacy.** Which tags need consent in which places; the banner and settings; data minimisation. Rules and platform requirements are facts to cite with URL and date or mark *to confirm*.
8. **QA.** How each event is tested before and after release, and a monthly reconciliation.
9. **Approval.** The plan is a draft. Installing, removing or changing tags, pixels, server-side connections or CRM fields needs the owner's explicit approval and a post-change check.
10. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no counts, match rates, defects or platform behaviour that aren't in `context/` or `inputs/` or a cited, dated source. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/17-measurement/17-tracking-plan-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Tracking plan: <business, date>
Skill: 17-tracking-plan · Date: <YYYY-MM-DD> · Framework: Tracking plan / UTMs / server-side tracking, first-party data
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; no tag, pixel or field changed
## Business questions
## Source of truth by number
| Number | System of record | Other views |
| --- | --- | --- |
## Reconciliation and defects
| Number | Platform says | Source says | Gap | Cause (defect / attribution / real) | Fix |
| --- | --- | --- | --- | --- | --- |
## Event spec
| Event | Fires when | Parameters | Sent to |
| --- | --- | --- | --- |
## UTM convention
## Server-side and first-party data
## Consent and privacy
## Platform facts
| Fact the plan relies on | Status (documented with URL and date / to confirm) |
| --- | --- |
## QA and monthly check
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/17-measurement/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the defects found with their fixes, the source of truth for each number, the UTM rule, and what is still missing, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every event maps to a business question; each number has a named system of record.
- [ ] Platform and source counts are reconciled with `sum_by.py`; collection defects, attribution differences and business change are separated.
- [ ] Purchase events fire once per new order with deduplication; UTMs are required on every owned link.
- [ ] Server-side, first-party data and consent are planned with dated or *to confirm* platform and legal facts.
- [ ] QA and a monthly reconciliation are set; nothing changes without approval and a post-change check.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Measure what answers a business question, trust the system of record over any platform's view, reconcile every month, and fix collection defects before arguing about attribution. Tracking plan / UTMs / server-side tracking and First-party data, The Complete Marketing System, section 17 Measurement (Servidad, 2026); platform documentation (Google Analytics, Meta Conversions API) to be cited with dates.
