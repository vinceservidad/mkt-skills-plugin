---
name: 05-naming
description: Name a brand, product or feature and check the name is clear, ownable and available. Use for naming, name ideas, rename, is this name taken. Needs a brand foundation or positioning first.
metadata:
  section: "05 Brand"
  covers: "Naming (product and brand)"
---
# Naming

A name is the one brand asset that appears everywhere and is hardest to change, so it should be chosen deliberately, not brainstormed and voted on. A good name is clear about what kind of thing it is, distinctive against the alternatives, easy to say and spell, fits the brand, and can be owned. The first decision is not the name but the name *type*: a feature inside a product rarely needs an invented brand; a new company might. Availability is never assumed: until a clearance search is done, every name is a candidate.

## Needs (read before writing)

- Required, either one (drafted or confirmed, with content):
  - `context/brand.md` → **Brand foundation**, written by `05-brand-foundation` (promise, personality, essence); or
  - `context/positioning.md` → **Positioning statement**, written by `06-positioning-statement` (category, differentiation).
- If present, also read: `context/brand.md` → Distinctive assets, Voice, Naming (names already in use); `context/customer.md` → Voice of customer and ICP and personas; `context/offer.md` → Core offer, Name and one-liner, Value ladder (what is being named, and names already proposed); `context/market.md` → Competitors and alternatives; `inputs/` (competitor observations, existing names, any trademark or domain search results).
- What is being named must exist in `offer.md` or be described by the user as planned. Naming does not decide its scope, price or terms.
- If both required sections are missing:
  - **Customer evidence exists** (`customer.md` → ICP and personas is present): run `05-brand-foundation` first, then continue.
  - **It doesn't:** stop. Name both missing sections with their owners (Brand foundation → `05-brand-foundation`; Positioning statement → `06-positioning-statement`), and `customer.md` → ICP and personas with `02-icp-persona` behind them. Ask for customer evidence. A stop reply writes nothing and still ends with the **Principle, framework, source** block.

## Process

Use [references/naming-method.md](references/naming-method.md).

1. **Brief.** What is being named (company, product, plan, feature), who it is for, what it must signal, where the name will appear, and what it sits under (the brand architecture). Pull these from context; mark gaps.
2. **Choose the name type and architecture.** Branded house (Brand + descriptor), endorsed (Product by Brand), or a standalone brand. Features and plans usually get descriptive names under the master brand; a standalone brand needs a reason (a different audience, a risk to keep apart, a planned sale). Say why.
3. **Generate candidates** across types (descriptive, evocative, invented, founder or place, compound), drawing on the brand foundation's essence and personality and on the customer's own words, with sources. Aim for a long list, then cut.
4. **Screen each shortlisted name on Neumeier's seven criteria:** distinctiveness, brevity, appropriateness, easy spelling and pronunciation, likability, extendibility, protectability. Score each criterion (strong, fair, weak) with a reason. Distinctiveness is judged against the alternatives' names only from dated evidence; a generic category phrase fails it.
5. **Check fit with existing assets and claims.** Does the name work with the master brand, its taglines and its distinctive assets? Does it clash with or duplicate a name already proposed in `offer.md` or used in `brand.md`? If the name carries a claim (a day, a number, a speed, a result), compare it word for word with the brand foundation's Promise and the proof it cites, and quote any caveat the foundation records about that wording (for example a promise kept to what the proof says). Name the mismatch in the Notes column and the reply; a name cannot promise more than the foundation does.
6. **Availability, unknown until checked.** For each finalist list the checks still needed: a trademark clearance search in the relevant classes and countries by a qualified attorney; the domain; social handles; company registry if it is a company name. Never say a name is available, unregistered or trademarkable unless the user supplied a result, and then cite it with its date.
7. **Test with buyers.** Propose a short test: show the finalists to a handful of target buyers and ask what they think it is and who it's for; check spelling after hearing it said aloud.
8. **Recommend, don't decide.** Recommend one name and a runner-up, conditional on the checks. The owner decides. If the chosen name replaces the offer's working name, hand that change to `07-offer-design`; never edit `offer.md` yourself.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure. Run the quote check below.

**Nothing the context doesn't support.** No claims about trademark status, domain availability, competitor names, meanings in other languages or buyer reactions that no source gives. Mark inferences `(assumption)`.

## Output

Write `context/brand.md` → `## Naming`, replacing that section's body and leaving every other section exactly as it was. Keep earlier naming decisions (other names already recorded) unless the user replaces them:

```markdown
## Naming
Status: draft (<YYYY-MM-DD>, 05-naming)
Written by: 05-naming, <YYYY-MM-DD>
Brief: <what is named — for whom — what it must signal — where it appears>
Architecture: <branded house / endorsed / standalone — why>
| Name | Type | Distinct | Brief | Appropriate | Spell and say | Likable | Extendible | Protectable | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
Recommended: *<name>*, runner-up *<name>* — why; conditional on the checks below and the owner's decision
Checks still needed: trademark clearance (attorney, classes, countries) · domain · handles · registry — status: not done, unless a dated result is supplied
Buyer test: <who, how many, what to ask>
Handoffs: <e.g. 07-offer-design to update the offer's name>
Evidence: <files and IDs>
Method: Name type and brand architecture (Aaker); Neumeier's seven criteria for a good name (The Brand Gap)
```

Write candidate names in italics, not quotation marks. Never set `confirmed` unless the user approves.

Then update the file:
- In the frontmatter, set `status: draft` and `updated: <date>`.
- Append one line to `## Change log`.
- If `context/brand.md` does not exist, create it with frontmatter, the five brand sections (others `Status: empty`) and a change log.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source (customer language, existing copy), with the source named. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on the file (`python3 <this skill's folder>/scripts/check_quotes.py context/brand.md`). For every line it prints, copy the exact words or drop the quotation marks and use italics, then run it again until it reports every quotation matches.

Reply with:
- the recommended name and runner-up, and why;
- the checks that must pass before it is used;
- the next skill: `07-offer-design` if the offer's name changes, or `05-distinctive-assets` for a new logo or mark.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] The name type and brand architecture are chosen, with a reason, before candidates.
- [ ] Candidates draw on the brand foundation or positioning and on customer language, with sources.
- [ ] Each shortlisted name is scored on all seven criteria with reasons; distinctiveness uses only dated evidence about other names.
- [ ] No name is called available, unregistered or trademarkable without a supplied, dated result; clearance, domain and handle checks are listed as still needed.
- [ ] A name that carries a claim is compared with the brand foundation's Promise and proof, and any caveat recorded there is cited.
- [ ] The recommendation is conditional on the checks and the owner's decision; `offer.md` is not edited, and any name change there is handed to `07-offer-design`.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean. No unmarked inference.
- [ ] Only `## Naming` changed. It has Status, Evidence and Method lines, and the change log has a line for this write.

## Principle and source

Choose the name type before the name, judge candidates on clear criteria against the real alternatives, and treat every name as a candidate until it clears legal checks and the owner decides. Seven criteria for a good name (Marty Neumeier, The Brand Gap); brand architecture (David Aaker, Brand Portfolio Strategy); The Complete Marketing System, section 5 Brand (Servidad, 2026).
