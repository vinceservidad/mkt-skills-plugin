# Evidence Register

One row per decision-relevant claim. The register records what is known and how — never what is assumed to be true.

## Evidence states

Ordered weakest to strongest. A state is never upgraded without the named artifact that justifies it. These states grade how a claim was received and whether it agrees with the source of truth; they are not causal, scaling-proof, or integration states. See [Evidence and proof scales](../../../library/contracts/GLOSSARY.md#evidence-and-proof-scales).

| State | Meaning | May support |
|---|---|---|
| `asserted` | A person stated it; no artifact seen | Hypotheses and questions only |
| `document-supplied` | Appears in a supplied document or screenshot; neither the named source system nor an unedited export from it has been seen | Provisional analysis, labeled |
| `observed` | Seen directly in a named source system | Analysis and recommendations, labeled by source |
| `reconciled` | Agrees with the business source of truth | Profitability and commercial conclusions |
| `verified` | Reconciled and independently confirmed by a second source or check | Confirmed commercial conclusions within the confirmed scope. Not a causal grade: a causal claim needs its own level on the [causal evidence ladder](../../tracking-measurement/references/causal-evidence-ladder.md) — at least C3, which supports only a provisional causal estimate within the observed scope; C4 supports a causal estimate within the tested scope and C5 an established scope of generalization |
| `unknown` | Required but not supplied | Nothing — blocks dependent decisions |
| `contradicted` | Two sources disagree and the conflict is unresolved | Nothing — must be resolved or declared |

## Row fields

Claim; value; source system or person; artifact or export name; collection method; date range covered; evidence state; decisions it supports; what would change the state; date recorded.

## Rules

- A platform export is `observed` for platform behavior and no stronger for business outcome. Reaching `reconciled` requires agreement with the source of truth.
- A stakeholder restating a platform number is `asserted`, not `observed`. The artifact, not the confidence of the speaker, sets the state.
- A platform export keeps that `observed` state however it arrives (emailed, uploaded, or shared) when it is the file as the named source system generated it and its source system, account, date range, and export name are recorded. A screenshot, a deck, a PDF or report prepared by a person, an edited export, or a figure excerpted, re-keyed, or restated in another document is `document-supplied` until the figure is seen in the named source system or in such an export. `document-supplied` is not the platform-currency "officially documented" state or the integration `documented` state.
- No evidence state licenses a causal claim. Reconciliation and independent confirmation establish that a figure is right, not what caused it; `$tracking-measurement` grades causality on the causal evidence ladder, and the claim carries that level and its scope.
- `contradicted` outranks convenience. Do not silently pick the more favorable source; record both and the resolution method.
- A claim used in two decisions at different confidence levels is one row, not two.
- Absence of evidence is `unknown`, never a default, benchmark, or industry figure.
- Record the collection method where it changes interpretation: modeled versus observed conversions, sampled versus complete data, survey self-report versus behavior.

## Decision blocking

For each pending decision, list the rows it depends on and the weakest state among them. The weakest dependency governs the decision's confidence. If that state is `unknown` or `contradicted`, the decision is blocked and must be reported as blocked rather than answered with a caveat.
