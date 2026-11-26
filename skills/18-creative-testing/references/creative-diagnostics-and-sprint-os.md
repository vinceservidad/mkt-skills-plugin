# Creative Diagnostics Matrix, Testing Sprint OS and Meta Learning Agenda

Use when designing ongoing creative test plans, diagnosing where specific ads fail in the feed-to-checkout funnel, or building a formal Meta Blueprint creative learning agenda. Diagnostic ratios point to where to investigate next; **cost per verified business outcome** (never hook rate, hold rate, or CTR alone) decides winners and losers.

## 1. Funnel-drop creative diagnostic matrix

Compare each metric against the account's own historical baseline for that format and objective (never use borrowed industry benchmarks as pass/fail gates):

| Symptom in delivery | Formula | Likely root cause | Action and owning skill |
| --- | --- | --- | --- |
| Low 3-second Hook Rate | `3s video plays / impressions` | Weak opening frame, slow intro, unclear audience callout, or dull first text overlay | Keep core body if hold is unknown; rewrite 3 to 5 opening hooks (`09-hooks`) |
| High Hook, low Hold Rate | `ThruPlays` or `15s plays / 3s plays` | Hook feels clickbaity or disconnected from body; slow pacing; missing middle proof beat | Re-edit body sequence, cut filler, add visual proof earlier (`09-ad-creative`) |
| High Hold, low Outbound CTR | `outbound clicks / impressions` | Passive storytelling with weak urgency, unclear offer bridge, or hidden CTA | Sharpen problem-to-offer bridge, value framing, and explicit CTA (`10-ad-copy`) |
| High Outbound CTR, low LP CVR | `purchases or qualified leads / outbound clicks` | Ad overpromises or omits price/qualification filters; landing page lacks message match or proof | Align headline and offer on landing page, or add clarifying qualifier in ad (`12-landing-page`, `13-cro-audit`) |

## 2. Creative testing sprint operating system

Run creative testing as an explicit feedback loop rather than ad-hoc boosts:
1. **Fair-read test structure:** Isolate net-new concepts in dedicated test ad sets or via platform A/B test tools (`11-paid-social`; verify current tool rules) so early algorithmic spend skew does not starve new concepts before reaching the minimum spend or outcome threshold.
2. **Winner graduation rule:** Promote a concept only when it hits the target sample/spend floor and beats or matches the allowable cost per business outcome in `17-unit-economics` with stable post-click quality. Pass scaling budget changes to `19-scale-paid`.
3. **Portfolio cadence heuristic (owner sets capacity):** Aim roughly `70%` of testing output at single-variable iterations of proven winning angles (new hooks, new creators, static vs. video adaptations) and `30%` at net-new persona, desire, or mechanic swings (`09-angle-matrix`, `09-ad-creative`), labelled heuristic.
4. **Track Creative Hit Rate:** Divide validated winners by net-new concepts tested each month to spot research gaps vs. production bottlenecks.
5. **Structured naming taxonomy:** Enforce consistent tags such as `ConceptID_Angle_Hook_Format_Creator_YYYYMM` in ad names so `scripts/sum_by.py` aggregates performance cleanly by angle, hook, or creator across campaigns.

## 3. Meta Creative Learning Agenda

Distilled from the Meta Blueprint Creative Strategy Professional study guide (July 2026) and aligned with MKT experiment governance (`17-incrementality`, `18-experiment-log`):

Populate one decision-changing row before launching a structured study:
`decision | learning question | hypothesis | evidence gap | method | assigned arms | primary metric (source) | guardrails | lag/window | stopping rule | next brief`

- **Pre-campaign:** Verify objective and conversion-event integrity, design materially distinct creative alternatives, and confirm viewers can actually comprehend the tested message in mobile previews.
- **Mid-campaign:** Audit equal delivery/exposure and data quality; prohibit peeking or editing treatments mid-test.
- **Post-campaign:** Wait out conversion lag, evaluate outcome vs. uncertainty, record null and losing concepts honestly in `18-experiment-log`, and translate findings into the next `09-creative-brief`.

Match the study method strictly to the question:
- **A/B Testing:** Compares creative variant A vs. B under randomized delivery; measures relative difference between exposed arms, not causal lift over no ads.
- **Brand Lift:** Survey-based measure of ad recall, awareness, favorability, or purchase intent; never treat survey intent as observed sales.
- **Conversion Lift:** Randomized holdout measuring incremental conversions/revenue (`17-incrementality`); check current platform eligibility and power before planning. Keep social metrics, brand outcomes, and store/CRM business outcomes strictly separate.

## Sources

Meta Blueprint Creative Strategy Professional study guide (July 2026); Meta Performance 5 creative experimentation workflow; The Complete Marketing System, section 18 Experimentation (Servidad, 2026).
