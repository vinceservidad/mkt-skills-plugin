---
name: 05-brand-foundation
description: Define the brand promise, story, values, personality and archetype on one page from customer evidence. Use for brand strategy, brand pyramid, brand story, who we are. Not for voice (05-brand-voice).
metadata:
  section: "05 Brand"
  covers: "Binet & Field (60/40); Brand archetypes; Brand equity model (Aaker); Brand key / brand pyramid; CBBE pyramid (Keller); Founder-led / personal brand; Golden Circle; Purple Cow and Smallest Viable Market (Godin); Share of voice; Sponsorships; StoryBrand; Thought leadership"
---
# Brand foundation

A brand is what buyers remember when the ad is over, and whether they think of you when the need arrives. A brand foundation decides, on one page, what the business stands for, what it promises, how it behaves and which buying situations it must come to mind in. Everything later (assets, voice, names, copy) is built on it. A foundation is only useful if it is true: the promise is one the offer keeps, the values show in what the business already does, and the story is the founder's real one.

## Needs (read before writing)

- Required (drafted or confirmed, with content): `context/customer.md` → **ICP and personas**, written by `02-icp-persona`.
- If present, also read:
  - `context/positioning.md` → Positioning statement (`06-positioning-statement`), and Differentiation;
  - `context/customer.md` → Jobs to be done, Pains desires and fears, Current alternatives, Buying triggers and process, Voice of customer;
  - `context/offer.md` → Dream outcome, Core offer, Guarantee (what the business can actually keep);
  - `context/message.md` → Big idea, Promise, Proof stack, Story;
  - `context/market.md` → Competitors and alternatives;
  - `inputs/`: founder notes, about pages, existing brand documents, reviews.
- If ICP and personas is missing:
  - **Customer evidence exists** (interviews, reviews, call notes in `inputs/`, or the other customer sections): run `02-icp-persona` first (it may run `02-customer-research` itself), then continue. If `02-icp-persona` is not loaded, stop and say: enable mkt-q1-audience.
  - **It doesn't:** stop. Name the missing section, `customer.md` → ICP and personas, and its owner `02-icp-persona` (with `02-customer-research` for the research behind it), and ask for customer evidence: interviews, reviews, sales-call notes, support tickets. A description of the buyer from the user is a hypothesis, not evidence. A stop reply writes nothing and still ends with the **Principle, framework, source** block.
- If Positioning statement is missing, continue, but say the differentiation in the foundation is provisional until `06-positioning-statement` sets it. Never write `positioning.md`.

## Process

Work through the brand key in [references/brand-key.md](references/brand-key.md) and the brand checks in [references/brand-classics.md](references/brand-classics.md) (Godin's Purple Cow and Smallest Viable Market, Ogilvy on Brand Image, Jobs's values-based rally, and Ries & Trout's Sacrifice and Line Extension filters). Fill each slot from evidence; where evidence is missing, write a gap, not a guess.

1. **Insight.** The buyer truth the brand is built on: a tension in the buyer's own situation, taken from the ICP, jobs and voice of customer, with source IDs.
2. **Purpose (why).** Why the business exists beyond selling, from the founder's own account if one is supplied (Golden Circle: why, how, what). With no founder material, leave *Why* as a question for the owner. Never compose an origin.
3. **Root strength.** What the business has that the alternatives don't, with evidence (offer, proof, positioning). If positioning is empty, mark it provisional.
4. **Benefits.** Functional (what it does) and emotional (how it feels), each traced to a job, pain or quote.
5. **Values.** Three to five, each proven by a behaviour the business already shows: something it refuses, a practice, a guarantee. A value without a behaviour is `(assumption)` for the owner to confirm, or dropped.
6. **Personality and archetype.** Choose one primary archetype (Mark & Pearson) and at most one secondary. Justify it from the buyer's need and the founder's real behaviour. Say what the archetype rules out. An archetype is a lens, not proof that it will work, and a competitor using an archetype is not a reason to copy it.
7. **Promise.** One sentence the business can keep every time, tied to deliverables that exist in `offer.md`. Do not promise beyond the offer, the guarantee or the proof. If message.md has a Promise, keep the brand promise consistent with it.
8. **Story.** StoryBrand roles: the customer is the hero, the brand is the guide (empathy plus authority). Use the founder's real story only. If `message.md` → Story exists, summarise and point to it rather than rewriting it. With no story material, leave the story as questions for the owner.
9. **Essence.** Two to four words that sum up the key. This is an internal summary, not a tagline.
10. **Mental and physical availability.** List the category entry points: the buying situations in which the brand must come to mind (from triggers, struggling moments and jobs, with evidence). List where buyers can find and buy today, and the gaps. Name the brand-building routes the evidence supports (founder-led content, thought leadership, sponsorships, referrals) as options, with their evidence, not as a plan.
11. **Brand and activation balance.** Do not prescribe a budget split. Binet & Field's long-horizon finding (roughly 60% brand, 40% activation, varying by category) is a framework default, not a rule for this business. Say what data would decide it (spend by type, horizon, category, share of voice against share of market) and hand the split to `20-budget`. Share of voice needs measured competitor spend or mentions; never estimate it.
12. **Founder-led brand.** If the founder is the brand's most visible asset, say so with evidence and name the key-person risk.
13. **Check before saving.** Re-read the draft against the Checks and fix any failure. Run the quote check below.

**Nothing the context doesn't support.** No invented origin stories, missions, customer quotes, awards, results, competitor facts or values. Mark inferences `(assumption)`. Describe each source only as it reads. The foundation is a draft for the owner: the promise and values are commitments only the owner can confirm.

## Output

Write `context/brand.md` → `## Brand foundation`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Brand foundation
Status: draft (<YYYY-MM-DD>, 05-brand-foundation)
Written by: 05-brand-foundation, <YYYY-MM-DD>
Built from: <sections read, with status; positioning provisional if empty>
| Brand key slot | Decision | Evidence |
| --- | --- | --- |
| Insight | … | <IDs> |
| Purpose (why · how · what) | … or *question for the owner* | founder notes / gap |
| Root strength | … | … |
| Functional benefits | … | … |
| Emotional benefits | … | … |
| Values (with the behaviour that proves each) | … | … |
| Personality and archetype | <primary (+ secondary)>; rules out … | … |
| Promise | *…* | offer.md → … |
| Story (customer hero, brand guide) | … or *questions for the owner* | … |
| Essence | *…* | internal, not a tagline |
Category entry points: <buying situation — evidence> …
Physical availability: <where they find and buy today — gaps>
Brand-building routes the evidence supports: <route — evidence> (options, not a plan)
Brand and activation balance: no split prescribed; decide in 20-budget with <data needed>
Founder-led: <yes/no, evidence, key-person risk>
Open questions for the owner: …
Evidence: <files and IDs>
Method: Brand key (one-page brand definition); brand archetypes (Mark & Pearson); Golden Circle (Sinek); StoryBrand (Miller); mental availability (Sharp)
```

Write your own words (insight statements, promise, essence, values) in italics or plain text, never in quotation marks. Label rows inside tables with plain text and source IDs. Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/brand.md` does not exist, create it with frontmatter, the five brand sections (others `Status: empty`), and a change log.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (an interview, a review, the founder's notes), with its ID. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py context/brand.md`). For every line it prints, copy the source's exact words or drop the quotation marks and use italics, then run it again until it reports every quotation matches.

Reply with:
- the promise and essence in one line each;
- the biggest open question for the owner;
- the next skills: `05-brand-voice`, `05-distinctive-assets`, and `06-positioning-statement` if positioning is empty.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every brand key slot is filled from evidence with source IDs, or names a gap or question for the owner. Nothing is filled with a plausible guess.
- [ ] The promise is tied to deliverables in `offer.md` and promises nothing beyond the offer, guarantee or proof.
- [ ] Every value is backed by a behaviour the business already shows, or is marked `(assumption)` for the owner.
- [ ] One primary archetype (at most one secondary) is justified from the buyer and the founder's behaviour, with what it rules out.
- [ ] The story uses the founder's real material only; with none, it is left as questions.
- [ ] Category entry points come from evidenced buying situations. No budget split, share of voice or competitor fact is invented.
- [ ] No unmarked inference. Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] Only `## Brand foundation` changed. It has Status, Evidence and Method lines, and the change log has a line for this write. `positioning.md` is untouched.

## Principle and source

A brand is what buyers remember and the situations they remember you in; define it on one page, from evidence, so every asset, word and name repeats the same true promise. Brand key (one-page brand definition); brand archetypes (Margaret Mark & Carol Pearson, The Hero and the Outlaw); Golden Circle (Simon Sinek, Start with Why); StoryBrand (Donald Miller, Building a StoryBrand); mental availability and category entry points (Byron Sharp, How Brands Grow; Jenni Romaniuk); Purple Cow (Seth Godin); Ogilvy on Advertising (David Ogilvy); The Complete Marketing System, section 5 Brand (Servidad, 2026).
