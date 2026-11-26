---
name: 06-unique-mechanism
description: Name the mechanism that makes the result happen, as the strongest reason to believe. Use for unique mechanism, why it works, our secret sauce, what makes the method different.
metadata:
  section: "06 Positioning"
  covers: "Unique mechanism"
---
# Unique mechanism

When every competitor promises the same result, a bigger promise stops working. What still works is the *how*: a named, believable reason this product gets the result when the alternatives didn't. A unique mechanism has two halves. The **problem mechanism** explains why the buyer's earlier attempts failed (the real cause, not their fault). The **solution mechanism** is the specific method, process, ingredient or set-up that deals with that cause. It must be true: a mechanism is found in how the business already delivers, never invented for the copy.

## Needs (read before writing)

- Required (drafted or confirmed, with content): `context/positioning.md` → **Differentiation**, written by `06-positioning-statement`. The mechanism explains the differentiation; without it there is nothing to explain.
- If present, also read:
  - `context/positioning.md` → Competitive alternatives, Positioning statement, and any earlier Unique mechanism;
  - `context/market.md` → Market sophistication (`01-sophistication-stage`): whether a mechanism is what the market needs now; and Competitors and alternatives (`01-competitor-profiling`): which mechanisms competitors already claim;
  - `context/offer.md` → Core offer and Guarantee: how the product is actually delivered, and which parts are only proposed;
  - `context/customer.md` → Pains desires and fears, Beliefs objections and drivers, Voice of customer, Current alternatives: why earlier attempts failed, in the buyer's words;
  - `context/message.md` → Mechanism (`08-message-doc`): a downstream draft you may build on, but never edit;
  - `inputs/`: process notes, founder notes, onboarding or delivery documents, results data.
- If Differentiation is missing:
  - **Its upstream exists** (`context/customer.md` → ICP and personas, plus Current alternatives or `context/market.md` → Competitors and alternatives): run `06-positioning-statement` first, then continue.
  - **It doesn't:** stop. Name the missing section, Differentiation, and its skill, `06-positioning-statement`, with what that skill needs (ICP and personas from `02-icp-persona`; alternatives from `02-customer-research` or `01-competitor-profiling`). Ask for evidence of how the product is delivered and why customers' earlier attempts failed. Write nothing. A stop reply still ends with the **Principle, framework, source** block.

## Process

Use [references/mechanism-guide.md](references/mechanism-guide.md) for the tests and traps.

1. **Map the real process.** From offer.md and inputs, list the steps, components or ingredients the business actually delivers today, in the order they work. Mark each *exists*, *proposed* or *unknown* exactly as the context does. Only *exists* parts may carry the mechanism.
2. **Problem mechanism.** From customer evidence, state the cause that made the alternatives fail: what they did wrong, not what the buyer did wrong. Each cause needs a source (an interview, a review, a lost-deal reason). If the evidence shows a symptom but not the cause, say so and mark your reading `(assumption)`.
3. **Solution mechanism.** Connect the existing parts from step 1 to the causes from step 2: *because X causes the failure, Y does Z*. Keep each link to what the evidence shows. Where the link from the part to the result is plausible but unproven, write it as how the business believes it works `(assumption)`, and name the proof that would show it (rule: a mechanism is an explanation, not proof of causality).
4. **Uniqueness test.** Compare each part with the alternatives' dated claims. A part a competitor also claims is not unique; uniqueness may lie in the combination, the order, the cadence or the specific customer, and must be stated honestly as such (*the parts are not unique; the combination is, as far as the evidence of <date> shows*). Never claim *only* or *proprietary* beyond the evidence.
5. **Sophistication fit.** If Market sophistication is present, say whether the market needs a mechanism (stage 3), a better mechanism (stage 4) or identification more than a mechanism (stage 5), and whether this mechanism is new to the market or an improvement on one already claimed. If it is absent, say the fit is unchecked and name `01-sophistication-stage`.
6. **Name it.** Propose two or three names, descriptive enough to explain themselves, in italics. A name may not promise more than the proof (a day, a number, a speed must match the evidence). Names are untested and not cleared: no trademark, ownership or *proprietary* claim. Brand-level naming belongs to `05-naming`.
7. **Proof and demonstration.** For each link, name the proof that exists (a number, a review, a sample) or the gap, and one way to show the mechanism to a buyer (a sample report, a before-and-after, a walkthrough) using what exists.
8. **Hand-offs.** If `message.md` → Mechanism differs from this, hand the update to `08-message-doc`; never edit `message.md`. Proposed parts that would strengthen the mechanism go to `07-offer-design` or `04-product` as suggestions, not claims.
9. **Check before saving.** Re-read the draft against the Checks and run `scripts/check_quotes.py`. Fix every failure before you save.

**Nothing the context doesn't support.** No feature, ingredient, step, result, speed, percentage, study or customer count that isn't in `context/` or `inputs/`. If the business has no distinct way of working beyond what alternatives also do, say so plainly in the section: an honest *no unique mechanism evidenced yet; the strongest candidate is …, which needs …* is a valid result. A mechanism made up for the copy is not.

**Quotation marks are evidence.** Quotation marks hold only words copied exactly from a source, with the source named. Mechanism names, links and your summaries go in italics or plain text. Run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py context/positioning.md`); for every line it prints, copy the exact words or drop the quotation marks, until it reports every quotation matches.

## Output

Write `context/positioning.md` → `## Unique mechanism`, replacing that section's body and leaving every other section (and every other file) exactly as it was:

```markdown
## Unique mechanism
Status: draft (<YYYY-MM-DD>, 06-unique-mechanism)
Written by: 06-unique-mechanism, <YYYY-MM-DD>
Problem mechanism: <why the alternatives fail — cause, with sources>
Solution mechanism: <the existing parts and how they deal with that cause, step by step>
| Part (exists today) | What it does | Cause it answers | Unique? (vs whom, date) | Proof or gap |
| --- | --- | --- | --- | --- |
Uniqueness: <what is unique — a part, the combination, the cadence — and what is shared>
Sophistication fit: <stage and whether this is a new or better mechanism> or unchecked
Name candidates: *<name>*, *<name>* — untested, not cleared
Demonstration: <how to show it with what exists>
Not yet part of it: <proposed parts and their owners>
Hand-offs: <08-message-doc to update Mechanism; others>
Evidence: <sources>
Method: Unique mechanism (Schwartz, Breakthrough Advertising; Bencivenga; Kennedy)
```

- In table cells, paraphrase without quotation marks unless you copy a source exactly.
- Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.

Reply with:
- the mechanism in one sentence (problem cause, then solution), and its leading name candidate;
- the weakest link and the proof that would close it;
- the next skill: `08-message-doc` (to carry the mechanism into the message) or `08-proof-stack`.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every part of the mechanism exists today; proposed or unknown parts are listed only under *Not yet part of it*.
- [ ] The problem mechanism names a cause with a source, not the buyer's fault, and unproven causes are marked `(assumption)`.
- [ ] Each link from part to result states its proof or its gap; no causal or result claim goes beyond the evidence.
- [ ] Uniqueness is tested against dated competitor claims; shared parts are named as shared, and no *only* or *proprietary* claim exceeds the evidence.
- [ ] Name candidates promise no more than the proof, carry no trademark claim, and are in italics.
- [ ] `message.md` is not edited; any difference is handed to `08-message-doc`.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean. No unmarked inference.
- [ ] Only `## Unique mechanism` changed. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

In a market that has heard every promise, the strongest reason to believe is a true, named explanation of why the result happens here when it failed elsewhere: the cause of the old failure and the method that answers it, found in how the business already works. Unique mechanism, Breakthrough Advertising (Eugene Schwartz); Gary Bencivenga; Dan Kennedy; The Complete Marketing System, section 6 Positioning (Servidad, 2026).
