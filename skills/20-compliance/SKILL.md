---
name: 20-compliance
description: Check marketing for ad policy, privacy, consent, claim and dark pattern problems before it ships. Use for compliance checks, is this claim allowed, consent, fake urgency, ad rejected.
metadata:
  section: "20 Operations"
  covers: "Compliance checklist; Consent and privacy; Dark patterns (what not to do)"
---
# Compliance check

A compliance check finds claims, consent gaps and design tricks that could mislead buyers, break a platform's rules or the law, or damage trust, before they ship. It works when each claim is matched to the evidence that supports it, consent and privacy are checked against how data is actually collected and used, dark patterns are named plainly, and each finding cites the rule with its source and date or says it needs a lawyer to confirm. It fails when it is a generic checklist, legal rules are stated from memory, or the check approves a claim because competitors make it.

Save the compliance checklist as a Markdown file in `work/20-operations/` when the required inputs are present. Creating this deliverable is part of the task, including requests worded as a question. Complete the file and its checks before replying with its path.

## Needs (read before writing)

No context section is required: this skill works from the data in `inputs/`. The claims, pages, emails, forms and data practices in `inputs/` and context are the evidence.
- If present, also read `context/offer.md` → Guarantee, Price and model; `context/message.md` → Proof stack; pages, ads, emails, forms, cookie and data notes in `inputs/`; any work in `work/13-conversion/` or `work/20-operations/20-martech-*.md`.
- **No data:** Without pages, emails, forms, ad copy or data-collection notes in `inputs/` to check, ask for those materials and how data is collected, explicitly say how to provide them (drop files in `inputs/` or paste into chat), and give the checklist only. Write nothing until it arrives. A stop reply still ends with the **Principle, framework, source** block.

## Process

For the named methods this skill owns, see [references/methods.md](references/methods.md).

Use [references/compliance-guide.md](references/compliance-guide.md) for claim substantiation, consent and privacy checks, dark patterns, platform ad policies and citing rules.

1. **Inventory the material.** Every claim, price statement, urgency device, form and data practice from `inputs/`.
2. **Claims.** For each claim, the evidence that supports it (from `context/` or `inputs/`) or *unsupported*; superlatives and numbers need proof; testimonials must be real and typical or disclosed.
3. **Price and urgency.** Reference prices must be real prices; timers and scarcity must be true.
4. **Consent and privacy.** Opt-ins (email, SMS) freely given and not pre-ticked; cookies and pixels; who receives cancellations and suppression; where the business sells. Rules are cited with URL and date or marked *to confirm with a lawyer*.
5. **Dark patterns (what not to do).** Hard cancellation, pre-ticked boxes, fake timers, confirmshaming, hidden costs; name each and its fix.
6. **Ad platform policies.** For ads, the relevant policy with URL and date or *to confirm*.
7. **Findings.** Each with severity, the rule (source and date or *to confirm*), the fix and the owner; not legal advice.
8. **Approval.** The checklist is a draft and not legal advice. Changing live pages, forms, emails or ads needs the owner's explicit approval.
9. **Check before saving.** Re-read the draft against the Checks and fix any failure.

**Nothing the context doesn't support.** Write no laws, rules, penalties or policy text from memory as fact; cite with URL and date or mark *to confirm with a lawyer*. Write no evidence for claims that isn't in `context/` or `inputs/`. Mark inferences `(assumption)` and list what is needed under Open questions. Count from files with [scripts/tally.py](scripts/tally.py) or [scripts/sum_by.py](scripts/sum_by.py), never by eye. No third-party benchmark is evidence about this business.

## Output

Write `work/20-operations/20-compliance-<YYYY-MM-DD>-<slug>.md`:

```markdown
# Compliance checklist: <business, material, date>
Skill: 20-compliance · Date: <YYYY-MM-DD> · Framework: Compliance checklist; Consent and privacy; Dark patterns (what not to do)
Built from: <context sections and inputs used, with their status>
Status: draft for the owner's approval; not legal advice
## Material checked
## Findings
| Item | Issue | Severity | Rule (source and date, or to confirm) | Fix | Owner |
| --- | --- | --- | --- | --- | --- |
## Claims and their evidence
## Consent and privacy
## Dark patterns
## To confirm with a lawyer
## Claims and sources
| Claim or number | Source |
| --- | --- |
## Open questions
## Principle, framework, source
```

Change nothing in `context/`. The deliverable is a draft, not a decision.

**Quotation marks are evidence.** Quotation marks hold only words that appear exactly in a source, with the source named. Write your own lines, and the titles of books, essays or talks (including in the Principle, framework, source block), in italics or plain text, never in quotation marks. Before saving, run [scripts/check_quotes.py](scripts/check_quotes.py) on your file (`python3 <this skill's folder>/scripts/check_quotes.py work/20-operations/<file>.md`). For every line it prints, copy the source's exact words or drop the quotation marks, and run it again until it reports every quotation matches.

Reply with the file path, the highest-severity findings with fixes, which claims are unsupported, and what needs a lawyer, and what is still missing, then end with the same block.

End with the **Principle, framework, source** block:

```markdown
**Principle:** …
**Framework:** …
**Source:** …
```

## Checks

- [ ] Every claim is matched to evidence or marked *unsupported*.
- [ ] Reference prices, timers and scarcity are checked for truth.
- [ ] Consent, cookies, pixels and suppression are checked against actual practice.
- [ ] Dark patterns are named with fixes; rules are cited with source and date or *to confirm with a lawyer*.
- [ ] It is not legal advice; nothing changes without approval.
- [ ] Quotation marks hold only exact source words, and `check_quotes.py` reports clean.
- [ ] No file in `context/` changed.

## Principle and source

Every claim needs proof, every opt-in must be a real choice, every deadline must be true, and every rule you rely on needs a source. Compliance checklist, Consent and privacy, and Dark patterns (what not to do), The Complete Marketing System, section 20 Operations (Servidad, 2026).
