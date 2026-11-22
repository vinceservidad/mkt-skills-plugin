# Reporting Analysis Workflow

## Knowledge metadata

- Primary type: process
- Secondary type: reporting workflow / communication artifact
- Decision: what a report can responsibly state about what changed, why, and what action is justified
- Owner: `$marketing-reporting`; causal diagnosis belongs to `$performance-diagnostics` or the channel skill that produced it
- Evidence status: inherits each source finding's evidence state; restating a finding never upgrades it
- Authorization: report draft until verified; the report authorizes no action on its own

## Purpose

Turn marketing performance data into a decision-ready summary of findings owned by other skills. Reporting summarizes and cites. It does not diagnose.

## Workflow

1. **Collect data.** Name the source, freshness, date range, comparison, timezone, and currency for each input.
2. **Validate.** Confirm metric definitions, attribution basis, and profit level. Disclose any definition change between periods instead of smoothing it. Route source disagreements to `$tracking-measurement`, and never sum platform-attributed results across channels.
3. **Review performance.** Build the scorecard at one named profit level and revenue basis, applied consistently.
4. **Cite the diagnosis.** The "why" comes from `$performance-diagnostics` or the owning channel skill, cited with its source skill and evidence state. If no diagnosis exists, report the change as not yet diagnosed and route it to `$performance-diagnostics`. Do not supply a cause of your own.
5. **Recommend.** State the single most decision-relevant action, with its owning skill, evidence, current authorization state, and exact execution state from `$marketing-intake`'s authorization register (`draft`, `proposed`, `approved`, `saved`, `published`, `live`, `processing`, `verified`). An approval record is not evidence that the action happened.
6. **Plan the action.** The owning skill defines the action. Live changes need explicit approval, and scaling goes through `$optimization-scaling`.
7. **Measure.** State the observation window and the source that will verify the result. Do not describe a recommendation as implemented, or an implemented change as verified before its window closes.

## Review areas

- Spend efficiency
- Revenue or lead quality
- Conversion rate
- Funnel performance
- Creative performance
- Audience performance
- Search intent
- Tracking accuracy

## Output

A clear report containing:

- What changed: observed values, definition, comparison, and source
- Why it changed: the cited diagnosis with its source skill and evidence state, or "not yet diagnosed", routed to `$performance-diagnostics`
- Evidence: each source finding keeps the grade its source skill recorded, under that grade's own scale name (for example `intake: document-supplied; causal: C1`), without translation or upgrade; a statement the report itself adds, such as a calculated period delta, is labelled `observed`, `calculated`, `experimentally observed`, `inferred`, `assumed`, or `unknown`
- Recommended action, with owner, authorization state, and exact execution state
- Expected impact, only as quantified by the source skill and labelled an estimate
- Next test, owned by the domain skill
- Unknowns carried forward from the source skills
- Exact status
