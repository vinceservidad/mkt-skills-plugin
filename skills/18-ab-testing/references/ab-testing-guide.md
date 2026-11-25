# A/B testing guide

## Sample size (two proportions, about 95% confidence, 80% power)

n per arm ≈ 16 × p × (1 − p) ÷ d², where p = baseline rate and d = absolute difference to detect. Example: p = 2.6%, relative lift 20% → d = 0.52 points → n ≈ 16 × 0.026 × 0.974 ÷ 0.0052² ≈ 15,000 per arm. Use scripts/sample_size.py.

## Duration

Visitors per arm × 2 ÷ daily eligible visitors, rounded up to whole weeks.

## Peeking

Checking a fixed-horizon test daily and stopping when it looks good inflates false positives. A tool's "winning" label after a few days on a thousand visitors per arm is not a result.

## Sequential and Bayesian

Valid if the method is designed for continuous monitoring and its rules are followed. Write the rule before launch.

## Multivariate

Needs traffic for every combination; rarely right for small sites.

## Read

Effect with interval, guardrails, decision per the rule, learning scoped to season and audience, logged.
