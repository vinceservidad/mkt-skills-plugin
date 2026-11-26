---
name: 11-influencer
description: Plan and vet influencer programs (seeding, sponsorship, affiliate, whitelisting). Use for influencer marketing, creator partnerships, vetting influencer lists, finding influencers, gifting.
metadata:
  section: "11 Distribution"
  covers: "Influencer / creator marketing"
---
# Influencer

Creator marketing borrows an audience someone else built. It works when that audience is the business's buyer, the creator would genuinely use the product, the deal matches what the business needs (a test, reach, sales or content it can reuse), and the terms are settled before anything is made. It fails when creators are picked by follower count, the media kit is taken on trust, rights and disclosure are left vague, or the program is judged on views.

Save the plan as a Markdown file in `work/11-distribution/` when the required inputs are present and the commercial terms are confirmed. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

Required (drafted or confirmed, with content):
- `context/customer.md` → **ICP and personas**, from `02-icp-persona`: whose audience the creator must reach, and who is disqualified.
- `context/offer.md` → **Core offer**, from `07-offer-design`: what the creator's audience is offered.
- If present, also read `context/customer.md` → Voice of customer, Pains, desires and fears, Beliefs, objections and drivers; `context/awareness.md` → Awareness map and Traffic temperature; `context/offer.md` → Price and model, Guarantee, Bonuses, Urgency and scarcity, Value ladder; `context/message.md` → Promise, Proof stack; `context/brand.md` → Voice; creator shortlists, media kits, budget, product-cost and capacity notes in `inputs/`; any work in `work/09-creative-strategy/09-ugc-brief-*.md`, `work/11-distribution/11-paid-social-*.md` or `work/11-distribution/11-channel-selection-*.md`.
- If a required section is missing:
  - **The upstream evidence exists** (interviews, reviews or call notes in `inputs/` but no ICP): run `02-icp-persona` first, then continue.
  - **It doesn't:** stop. Name every missing section with the skill that fills it (ICP and personas → `02-icp-persona`; Core offer → `07-offer-design`), and ask for evidence (interviews, reviews, sales notes), not a description of the buyer. Write nothing. A stop reply still ends with the **Principle, framework, source** block.
- **Owner commitments.** Creator fees, budget, product allowances, discount codes, commission rates, free trials, guarantees, launch dates and stock are the owner's commitments. If the program must carry one that `offer.md` and `inputs/` don't hold (a follower discount, a commission percentage, a giveaway), stop before writing without proposing alternative workarounds, ask the owner to confirm the exact terms — for any discount or code: first-order-only vs ongoing, eligibility, end date, usage cap, margin impact and who covers the cost — along with approved creator fees and schedule, and write no plan or outreach on assumed terms. An unknown budget alone is not a stop: plan in units (boxes, posts) and ask for the figure.
- If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.
- If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.

## Process

Use [references/influencer-guide.md](references/influencer-guide.md) for the vetting tests, deal types, rights and disclosure, and platform claims.

1. **Goal and outcome.** Say what the program is for (a small test, reach to a new audience, sales, content to reuse as ads) and the business outcome that judges it (first orders, subscribers who stay, qualified calls). Views, likes, follower growth and engagement rate are signals, not the outcome.
2. **Vet each creator on fit before reach.** Score every candidate against the ICP and its disqualifiers: who the audience is (the comments, the niche, the location share), whether the creator would use the product as it is, and conflicts (a competitor sponsorship, contempt for the buyer's current alternative, a price point far from the buyer's). Compute ratios from the shortlist with [scripts/sum_by.py](scripts/sum_by.py) (`python3 <this skill's folder>/scripts/sum_by.py <file> creator avg_views_last_10 followers rate_usd --ratio rate_usd/avg_views_last_10 --ratio avg_views_last_10/followers`), never by eye. Label each figure as the creator's own claim, platform-verified or calculated. Flag what looks inauthentic (sudden follower jumps, views far below the follower count) and ask for platform screenshots or analytics before paying.
3. **Choose the deal per creator.** Gifted seeding (product, no obligation to post), paid sponsorship (fee for agreed deliverables), affiliate commission (pay on tracked sales; the program design itself goes to `11-affiliate-jv`), or whitelisting (running the creator's content or handle as ads, which needs explicit rights). Use only offers in `offer.md`; any code or discount is an owner commitment.
4. **Budget and capacity.** Fit fees and product cost inside the owner's stated budget and stock or shipping capacity, with the arithmetic shown. Start with a small test cohort before any long commitment.
5. **The brief.** What the creator is asked to show (the real product, its real terms, the buyer's actual question), what must be true (only claims and offers in context, required disclosure), and what is the creator's call (voice, format). Production briefs for content the business will own go to `09-ugc-brief`.
6. **Rights, disclosure and contract points.** List what the agreement must settle: deliverables and dates, approval, exclusivity, usage rights (which content, which channels, how long, whether paid use or whitelisting is included), payment terms, and disclosure. Disclosure rules and platform branded-content tools are legal and platform facts to verify in current official guidance for the jurisdiction, or mark *to confirm*. Flag the contract for qualified legal review; this plan is not legal advice.
7. **Tracking and the read.** Give each creator a unique link (or a code only if the owner approves one), record orders or sign-ups by creator, and judge on cost per business outcome with counts. Links and codes support attribution, not proof of incrementality (`17-incrementality`). Paid amplification of creator posts goes to `11-paid-social`.
8. **Platform facts.** Branded-content labels, partnership-ad and whitelisting mechanics, audience-insight availability and creator-marketplace features change. Cite the platform's current official documentation with URL and date, or mark *to confirm*. Never state one from memory as current.
9. **Approval.** The plan is a draft. Contacting, contracting, paying or shipping to creators, and running their content as ads, needs the owner's explicit approval.
10. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no results, numbers, testimonials, prices, discounts, offers, features, audience facts or creator performance that aren't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Describe each source only as it reads: a media-kit figure is the creator's claim, not a verified number. Never look up or add real people; treat handles in `inputs/` as given. No third-party benchmark (a "typical" engagement rate or cost per view) is evidence about these creators.

## Output

Write `work/11-distribution/11-influencer-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Creator program: <business, period>
Skill: 11-influencer · Date: <YYYY-MM-DD> · Framework: Influencer and creator marketing (seeding, sponsorship, affiliate, whitelisting)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; nobody contacted, contracted or paid
## Goal and the outcome that decides
## Creator vetting
| Creator | Audience fit to the ICP (evidence) | Numbers (claimed / verified / calculated) | Red flags | Decision |
| --- | --- | --- | --- | --- |
## Deals
| Creator | Deal type | What they get | What we get | Offer used (from offer.md) | Cost |
| --- | --- | --- | --- | --- | --- |
## Budget and capacity
## Brief
## Rights, disclosure and contract points
## Tracking and how we judge it
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

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (a review, a creator's note in the shortlist, the owner's notes), with the source named. Write your own brief lines and outreach ideas in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/11-distribution/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches. Count anything you report from files with [scripts/tally.py](scripts/tally.py) or `sum_by.py`, not by eye.

Reply with the file path, the creators chosen and rejected with the reason, the deal for each, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every creator is vetted on audience fit to the ICP and its disqualifiers before reach; misfits and conflicts are rejected with the reason.
- [ ] Every number is labelled claimed, verified or calculated; ratios come from `sum_by.py`; suspected inauthentic audiences are flagged with a verification request.
- [ ] Each creator has one deal type; fees and product cost fit the owner's budget and capacity with the arithmetic shown; no code, discount or commission the owner hasn't set.
- [ ] Usage rights, whitelisting, exclusivity and disclosure are listed as contract points, legal and platform facts are dated or *to confirm*, and legal review is flagged.
- [ ] The program is judged on a business outcome per creator with counts; views and engagement are signals; links and codes are not called incrementality.
- [ ] The plan says nobody is contacted, contracted, paid or run as ads without the owner's approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Rent an audience only when it is your buyer: vet creators on fit and verified numbers, pick the deal that matches what you need, settle rights and disclosure before anything is made, and judge every creator on the customers they bring, not the views. Influencer and creator marketing (seeding, sponsorship, affiliate, whitelisting), The Complete Marketing System, section 11 Distribution (Servidad, 2026); Traffic Secrets (Russell Brunson) for working your way into the audiences buyers already follow (Dream 100).
