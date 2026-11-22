# Platform Currency Contract

Marketing platforms change faster than stable marketing principles. This contract keeps the Marketing OS current without pretending to know undocumented auction, ranking, filtering, or recommendation-system internals. It applies to any platform or vendor a skill makes a current-state claim about, not only Google and Meta. That includes ad platforms, demand-side platforms, verification vendors, mailbox providers, search engines, organic social or video platforms, and commerce and analytics platforms; a platform missing from the scope table below is still covered and is checked against its own first-party source.

## Evidence states

- **Officially documented:** supported by a current first-party source from the platform or vendor that owns the behavior (see [Platform scope](#platform-scope-and-first-party-sources)), with its URL and a verification date.
- **Account-visible:** directly observed in the relevant account or interface, with account scope and observation date.
- **Experimentally observed:** supported by a defined test or controlled comparison; state design and limitations.
- **Inferred:** a plausible explanation supported by evidence but not isolated or officially documented.
- **Unknown:** not verified, unavailable, or undisclosed.

Never describe a rumor, community report, correlation, or platform recommendation as an algorithm change. Separate product availability, default behavior, eligibility, recommended practice, and measured business impact.

Third-party benchmarks, industry surveys, agency reports, and cross-platform cost comparisons (for example, one platform's cost per lead against another's) are not platform documentation. Do not present them as a platform fact or use them to judge an account; judge cost by the account's own cost per qualified outcome against its economics.

## Platform scope and first-party sources

A current-state claim is verified only against the first-party source of the platform or vendor that owns the behavior, or against account-visible behavior in that platform. A different platform's documentation, a partner's summary, or a vendor's marketing page is not a substitute.

| Platform family | First-party source to check | Owning skill |
|---|---|---|
| Google Ads, including YouTube video campaigns | Google's own Google Ads and YouTube help and developer documentation | `$google-ads`, `$youtube-ads` |
| Meta | Meta's own business help and developer documentation | `$meta-ads` |
| TikTok | TikTok's own ads and business help documentation | `$tiktok-ads` |
| LinkedIn | LinkedIn's own Marketing Solutions help and developer documentation | `$linkedin-ads` |
| Demand-side platforms and verification vendors | The DSP's or vendor's own documentation and published methodology; for an industry standard, the standards body's own publication | `$programmatic` |
| Mailbox providers | Each provider's own published sender requirements and privacy documentation | `$lifecycle-marketing` |
| Search engines | Each search engine's own search and webmaster documentation | `$seo` |
| Organic social and video platforms | The platform's own help, creator, and transparency documentation | `$organic-social` |
| Commerce and analytics platforms, such as Shopify, Google Analytics 4, and tag managers | The platform's own help center and developer documentation | `$cro` for storefront and checkout; `$tracking-measurement` for analytics events, tags, and attribution; `$marketing-analytics` for exports, connectors, and pipelines |

The owning skill applies this contract; this table does not certify that any listed source currently documents a given behavior. A claim's change class comes from what the claim is about, using the [freshness gates](#freshness-gates), not from its platform family.

## Registries

Repository registries exist only for Google Ads — the [Google Ads platform registry](../../skills/google-ads/references/platform-current.md) — and Meta — the [Meta platform registry](../../skills/meta-ads/references/platform-current.md). Each carries a `Last verified` date that `scripts/check-platform-freshness.py` checks against the 30-day high-change maximum. That registry check is the only freshness gate the script automates. No script reads inline citation dates (below), because an inline citation does not record its change class in a form a script can read. They are checked manually: at the time of use, the owning skill compares each check date with the gate for its claim's change class. Known gap: an inline citation can age past its gate with no automated warning, so a skill relying on one confirms its check date before a decision depends on it.

Every other platform deliberately has no registry, so no unowned recurring maintenance burden exists. For those platforms:

1. Verify against the platform's first-party source, or against account-visible behavior, at the time of use.
2. When a skill or reference keeps a platform fact in its text, cite it inline as `(first-party: <URL>, checked YYYY-MM-DD)` immediately next to the exact claim it supports; the page title is optional in an inline citation (see source rule 2). The inline check date ages under the same freshness gates as a registry: recheck a cited claim older than its change class allows before a decision depends on it.
3. Label anything not verified this way as unverified, and state it as a check to perform, not as a current fact.

Adding a registry for another platform is a governance change: it needs an owning skill, a freshness validator, and an update to this contract.

## Freshness gates

| Change class | Examples | Maximum age of the registry entry or inline check date | Required action when stale |
|---|---|---:|---|
| High-change | AI/automation features, campaign creation defaults, bidding or audience controls, ad formats and specifications, reporting availability, experiments, interface labels | 30 days | Recheck official documentation before making a current-state claim or configuration recommendation. Confirm account visibility before an account-specific plan. |
| Medium-change | Setup workflows, policy wording, sender requirements, attribution options, standard reports | 90 days | Recheck first-party documentation when the detail affects the decision. |
| Stable concept | Economics, evidence states, causal inference, experiment design | 180 days | Review for conceptual or regulatory changes; do not replace with platform slogans. |

Always perform a live first-party check regardless of age when the user asks for the latest/current behavior, a documented capability may determine spend, compliance, or measurement, the account contradicts the registry or the cited source, or a live mutation is being proposed.

## Source rules

1. Prefer first-party product help, developer documentation, release notes, and account-visible evidence.
2. Record the source URL, verification date, and the exact claim supported. A registry entry also records the page title. An inline citation may omit the title because it sits next to the claim it supports; include the title where several claims share one source line or where the URL alone would not identify the page.
3. Treat marketing claims and platform case studies as vendor evidence, not guaranteed outcomes.
4. Do not infer access from documentation: rollouts can depend on account, country, objective, inventory, permissions, or experiment enrollment.
5. Preserve the stable strategic concept in `library/contracts/GLOSSARY.md`; map the current interface label separately.
6. When a material label, control, eligibility rule, or reporting capability changes, update the platform registry (Google Ads or Meta) or, for any other platform, the inline citation in the affected skill or reference, together with the skill decision rules, evaluation case, and `docs/CHANGELOG.md`.
7. If a first-party source cannot be reached, do not state its specifics; record the claim as unverified and name the check still required.

## Response contract

For a platform-current answer, report:

1. **Verified as of:** date, source, and scope.
2. **Officially documented:** supported product behavior.
3. **Account-visible:** what was actually observed, or `not checked`.
4. **Business implication:** a recommendation, distinct from the platform claim.
5. **Unknowns:** undisclosed mechanics, rollout uncertainty, or missing account evidence.
6. **Status:** advice only, draft, saved, published, processing, or live-verified.

The OS can be current to its verification standard; it cannot guarantee knowledge of undisclosed algorithms or changes released after the latest verification.
