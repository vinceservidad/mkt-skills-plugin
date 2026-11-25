# Paid search: decision rules

## The outcome chain

1. **Primary business outcome:** what the business is paid for or what reliably leads to it (a qualified call, a client, a subscriber who stays past the second box).
2. **Conversion action to optimise for:** the nearest tracked event that stands for the outcome. A contact form that anyone can fill (job seekers, other industries, tiny businesses) counts noise as success. Import CRM-qualified outcomes where the platform supports it (to confirm), or at least use a stricter event.
3. **Signals:** impressions, clicks, CTR, CPC, quality score, ad strength, platform conversions. Diagnostic only.
4. **Economics:** allowable cost per outcome = value of a customer (price × margin × expected lifetime, from context) × the share the owner will spend. Unknown margin → write the formula and ask.

## Intent and awareness

| Search looks like | Intent | Awareness level | Usual decision |
| --- | --- | --- | --- |
| The business's name | Navigational | Product / most aware | Protect; cheap, defends against competitors bidding on the name (verify whether they do) |
| [service] for [the ICP], specialist, [category] pricing | Commercial / transactional | Solution aware | Core of the plan |
| [competitor] alternative, X vs Y | Commercial | Solution aware | Only with sourced, dated competitor facts and a page that compares honestly |
| How to fix [problem], template, checklist | Informational | Problem aware | Only to an existing free asset, with a cap; usually SEO's job |
| Generic service, cheap, near me (for a remote specialist), free | Mismatched | n/a | Exclude or negative |
| Jobs, careers, software, courses, other industries | Irrelevant | n/a | Negative |

Volume never overrides fit. A term with large volume that the ICP does not use, or whose searchers want a price the offer does not have, is excluded.

## Match types (concepts; verify current behaviour)

- **Exact:** narrowest; best when budget is small and intent is specific.
- **Phrase:** searches that include the meaning of the phrase.
- **Broad:** widest; relies on the platform's understanding and the conversion signal; risky with a weak or noisy conversion action.
- Close variants and how each match type behaves are set by the platform and change; cite the current documentation or mark *to confirm*.

## Negatives

- Add a negative for clearly irrelevant intent (jobs, free, other industries, different products) even with few clicks: the intent is the evidence.
- Do not add a negative for a relevant term just because it has not converted in a small sample; check intent, spend against the allowable cost and any assisted value first.
- Choose the negative's match type so it blocks the bad intent without blocking good searches (for example, *jobs* as a broad negative, not *agency*).

## Structure

- One intent theme per ad group, with its own ad message and landing page.
- Separate brand from non-brand; separate solution-aware from problem-aware.
- Geography, schedule, devices and networks (search partners, display expansion) are hypotheses; start narrow and state why.

## Reading a search terms report

- Total by term and by theme with `scripts/sum_by.py`; show clicks, cost, platform conversions and business outcomes side by side.
- Compute share of spend on irrelevant intent (calculated) and cost per qualified outcome on relevant intent.
- Small counts (one or two outcomes) are directional; say what spend or count would make a call.
- Maximise-clicks style bidding with broad match and a form-fill conversion tends to buy cheap, broad clicks (pattern to confirm, not proof).

## Bidding and budget

- Bidding strategies that optimise for conversions need enough reliable conversion data; how much is a platform rule to confirm.
- While the signal is thin, cap cost per click or use manual control, and read search terms weekly (heuristic).
- The owner sets the budget. The plan proposes a test size from the allowable cost and the minimum outcomes needed to read (labelled heuristic).
- Keep and stop rules in cost per business outcome. Budget increases or coverage expansion: `19-scale-paid`. Capacity in `offer.md` caps scale.

## Platform claims

Match types, close variants, bidding strategies and their data needs, conversion imports and enhanced conversions, quality score, ad formats and asset rules, and policies change. For each one the plan relies on, cite the platform's own documentation `(first-party: <URL>, checked YYYY-MM-DD)`, note what the account shows, or mark *to confirm*. No third-party benchmarks.

## Authorisation

Creating campaigns, changing keywords, negatives, bids, budgets, conversion actions or goals, and pausing or enabling entities are live changes. Each needs the owner's explicit approval, exact scope, rollback, and a check of the account state afterwards (draft, saved, live, verified).
