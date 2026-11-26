---
name: 08-proof-stack
description: Assemble real proof under every claim and flag claims with none. Use for social proof, reason to believe, which testimonials to use. Not for collecting them (use 16-testimonials-case-studies).
metadata:
  section: "08 Message"
  covers: "Persuasion Equation (Bencivenga); Preemptive claim (Hopkins); Proof stack; Reason to Believe; Social proof"
---
# Proof stack

The reason to buy and the reason to believe are two different jobs, and most weak messaging does the first without the second. In sophisticated markets, proof beats promise. This skill lines up real proof under each claim, and finds the claims that have none. A claim without proof is either weakened until it is provable, or the proof gets collected. It is never faked.

## Needs (read before writing)

- The claims to prove, from at least one of these (drafted or confirmed, with content):
  - `context/message.md` → **Promise**, written by `08-message-doc`;
  - `context/offer.md` → **Dream outcome**, written by `07-offer-design`.

  Also read the Message house pillars, if present.
- The proof material. Read whatever exists in `inputs/` and these sections, each filled by its own skill:
  - `context/customer.md` → Voice of customer, from `02-voc-mining` (if absent and not loaded, say: enable mkt-q1-audience);
  - `context/customer.md` → Research log, from `02-customer-research`;
  - `context/offer.md` → Guarantee, from `07-guarantee-risk-reversal`.

  Proof material can be:
  - reviews and testimonials;
  - case results and client data;
  - delivery logs and metrics;
  - credentials and press;
  - demos and samples.
- If both Promise and Dream outcome are missing:
  - **Offer or customer evidence exists:** run `07-offer-design` (or `08-message-doc`) first, then continue. If `07-offer-design` is not loaded, stop and say: enable mkt-q2-offer.
  - **It doesn't:** stop. Name the missing sections and those skills. If the reply also reports any proof-material section as missing or empty, name the skill that fills it too (listed above): every section the reply calls missing gets its skill. A stop reply still ends with the **Principle, framework, source** block.

## Process

1. **List the claims:** the promise, each pillar, and any number or superlative the business uses.
2. **Find proof for each claim** in the material, by type, using [references/proof-types.md](references/proof-types.md) and the persuasion/preemptive proof rules in [references/proof-classics.md](references/proof-classics.md):
   - results and data;
   - testimonials and reviews;
   - case studies;
   - demonstrations and samples;
   - credentials and authority;
   - guarantees, which are proof of confidence;
   - social proof: counts, logos, peers.

   Cite each item's source. Copy testimonials word for word.
3. **Rate the strength:** specific beats general (a number, a name or role, a date), and a third party beats self-report. Note where the proof comes from the business's own logs. That is fine, as long as it is said.
4. **Find the gaps.** For a claim with no proof, either soften it to what can be proven, or name the proof to collect and how: ask three clients for a quoted result, pull the close log, film a demo. Never write placeholder proof.
5. **Check permission.** Mark any testimonial, client name or result that needs the client's permission before it is published.
6. **Check before saving.** Re-read the draft against the Checks and fix any failure.

## Output

Write `context/message.md` → `## Proof stack`, replacing that section's body and leaving every other section exactly as it was:

```markdown
## Proof stack
Status: draft (<YYYY-MM-DD>, 08-proof-stack)
Written by: 08-proof-stack, <YYYY-MM-DD>
| Claim | Proof | Type | Source | Strength | Permission needed? |
| --- | --- | --- | --- | --- | --- |
Unproven claims: <claim → soften to … / collect … by …>
Strongest proof to lead with: <item — why>
Evidence: <files and IDs>
Method: Proof stack and reason to believe; social proof (Cialdini)
```

Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/message.md` does not exist, first copy [assets/message.md](assets/message.md) to `context/message.md`, then write this section.

Reply with:
- the strongest proof;
- the biggest unproven claim;
- the next skill: `08-objection-map`.

**Quotation marks are evidence.** Put words in quotation marks only when they appear exactly in a source (a review, an interview, the story material), with its ID. Everything you write yourself (a promise, a belief to shift, an answer, a softened claim, a line of copy, a story line) goes in italics: *like this*. Before saving, find every quotation mark in your draft and check the words against the source.
Then run [scripts/check_quotes.py](scripts/check_quotes.py) on the file you wrote (`python3 <this skill's folder>/scripts/check_quotes.py context/message.md`). For every line it prints, copy the exact words from the source or drop the quotation marks and use italics, then run it again until it reports every quotation matches.

The reply's last lines are always the **Principle, framework, source** block, after the next skill, on a build and on a stop:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every proof item names its source. Testimonials are copied word for word with an ID or date. No result, number, logo or credential is invented.
- [ ] Every claim has proof, or is listed as unproven with a softening or a plan to collect proof.
- [ ] Strength is rated: specific beats general, and third party beats self-report. Self-reported business data is labelled as such.
- [ ] Items that need the client's permission before publishing are marked.
- [ ] Quotation marks hold only words copied exactly from a source.
- [ ] Only `## Proof stack` changed. It has Status, Evidence and Method lines, and the change log has a line for this write.
- [ ] The reply ends with the **Principle / Framework / Source** block, nothing after it (also on a stop).

## Principle and source

The reason to buy and the reason to believe are different jobs: put specific, sourced proof under every claim, and weaken or withdraw any claim you cannot prove. Persuasion Equation (Gary Bencivenga); third-party authority (Edward Bernays); Reason to believe and social proof (Robert Cialdini, Influence); preemptive claim and proof, Scientific Advertising (Claude Hopkins); The Complete Marketing System, section 8 Message (Servidad, 2026).
