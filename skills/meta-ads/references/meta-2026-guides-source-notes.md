# Meta Blueprint 2026 guides: provenance, coverage and interpretation

```yaml
artifact_type: standard
decision: use the supplied guides and accessible catalog without promoting recommendations into proven account outcomes
scope: January Associate and February Buying/Planning guides; public Blueprint discovery
owner: meta-ads
inputs: supplied editions, page evidence, retrieved public pages, existing MKT governance
evidence_status: observed
confidence: high
freshness: live-check
dependencies: source identity, canonical terminology, platform currency and specialist ownership
authorization: read-only
rollback_or_stop: stop unsupported source attribution, invented account access or unverified configuration instructions
```

## Source identity

Reviewed 2026-09-30. Page references are one-based PDF pages. These hashes identify the user-supplied files, not a separately downloaded or authenticated copy.

| ID | Supplied file and cover edition | Pages | SHA-256 |
|---|---|---:|---|
| ASSOC-2026-01 | `Meta Certified Digital Marketing Associate study guide 1_2026_v2_.pdf`, January 2026 | 124 | `2e371f699198c28123924b23ba694f5fd8fdbd7b89452a051d15384b02c53d28` |
| BUY-2026-02 | `Media Buying Study Guide.pdf`, February 2026 | 122 | `8f62386f941cb5d76a6b5fa37bf32cd71afb5a6695df3ec0cc6571a6ac624aa1` |
| PLAN-2026-02 | `Media Planning Study Guide (2_1_26).pdf`, February 2026 | 129 | `f6dd268ece33a36f2f9d12a3fcf851683da40175dcc605e180f828a87fd967cb` |

Public Meta Blueprint pages corroborate the guide titles and link to downloadable guides: [Associate](https://fbp.exceedlms.com/student/activity/205373-digital-marketing-associate-study-guide), [Buying](https://fbp.exceedlms.com/student/activity/206244-media-buying-professional-study-guide), [Planning](https://fbp.exceedlms.com/student/activity/206246-media-planning-professional-study-guide). Retrieved 2026-09-30. Byte equivalence between the uploads and linked downloads was not established. No Meta certification or endorsement of MKT Skills is implied.

The original PDFs, photographs, diagrams, sample exam questions and answer keys are not redistributed. References contain concise source summaries and explicitly original MKT applications. Relevant chapters and selected rendered tables were reviewed; this is not an exhaustive transcription or a complete portal ingestion. The previously released July creative-strategy references remain separate and unchanged.

## Task-oriented coverage

| Application | Source pages | Existing owner / new reference |
|---|---|---|
| Bid choice, budget structure, pacing and scenario math | BUY 29-38; PLAN 16-22, 37-50 | meta-ads / `meta-budget-bid-planning.md` |
| Catalog readiness, product sets and audience constraints | BUY 44-70 | meta-ads / `meta-catalog-audience-readiness.md` |
| Asset access, launch review and suitability | BUY 15-19; PLAN 92-98; ASSOC 109-110 | meta-ads / `meta-launch-access-preflight.md` |
| Results definitions and six-step account review | BUY 84-90; ASSOC 99-104 | meta-ads / `meta-results-review.md` |
| Event/data-source choice and lift readiness | BUY 24, 41-46, 88-96; PLAN 83; ASSOC 107-108 | tracking-measurement / `meta-signal-and-lift-readiness.md` |
| Organic presence, content and community operations | ASSOC 10-29, 46 | organic-social / `meta-presence-content-operations.md` |
| Messenger/WhatsApp service and lifecycle planning | ASSOC 31-44, 46 | lifecycle-marketing / `meta-business-messaging-plan.md` |

These are conditional extensions of existing owners, not new skills or competing master frameworks. Creative concepts, copy, causal analysis, cross-channel reporting and scaling retain their current specialist boundaries.

## Catalog access actually observed

The requested [catalog](https://fbp.exceedlms.com/student/catalog/list) and selected course overview pages were publicly readable. The following are discovery leads, not completed lessons:

| Course overview | Publicly supported scope | Attempted lesson and result |
|---|---|---|
| [Improve lead quality with Meta Conversions API for CRM](https://fbp.exceedlms.com/student/path/253141-conversions-api-crm-lead-quality) | Connect first-party CRM data to optimize for lead quality; integration planning and monitoring | `/student/path/253141/activity/612421`: sign-in required |
| [Proposing a campaign budget](https://fbp.exceedlms.com/student/path/246731-ads-budget-type-course) | Plan estimated budgets by buying type | `/student/path/246731/activity/661977`: sign-in required |
| [Understand the true value of your campaigns with Conversion Lift](https://fbp.exceedlms.com/student/path/253065-conversion-lift-marketing-measurement) | Measure impact and decide from lift results | `/student/path/253065/activity/393168`: introductory description plus sign-in required |
| [Facilitate client onboarding to WhatsApp for Business](https://fbp.exceedlms.com/student/path/253151-whatsapp_for_business_onboarding_course) | Goals, use cases, measures, governance and implementation planning | `/student/path/253151/activity/640160`: sign-in required |

Checked 2026-09-30 using unauthenticated public browsing. The user's logged-in browser session was not available to this retrieval tool. No credentials, cookies, session tokens, course progress, quiz submissions or certificates were accessed or changed. Do not infer gated lesson instructions from an overview. Full lesson ingestion requires an authorized accessible source or a user-provided export, not a credential-sharing workaround.

## Preserve source limitations

- ASSOC page 1 identifies the Associate exam; its page 3 overview instead names the Media Buying Professional exam. Preserve that discrepancy rather than silently relabel the file.
- BUY page 34's rendered cost-per-result-goal row says to enter an average CPM. PLAN page 18 uses a maximize-ROAS label while BUY page 34 uses maximize value of conversions; PLAN page 19 describes cost-per-result setup before bid cap. These instructions are not reconciled into a current UI recipe. Define the actual result unit and verify the account's current fields before implementation.
- PLAN pages 43-45 call the goal/average-order/CPA calculation an estimated minimum budget, but use a maximum cost per result. The displayed formula does not use the supplied CPM or conversion-rate inputs. Preserve its source framing when explaining the guide; MKT treats the calculation as a conditional planning scenario, not a demonstrated minimum or a sales guarantee.
- PLAN page 83's rendered table requires Pixel for websites and SDK for apps, while its surrounding text permits multiple sources; BUY page 95 likewise permits different combinations. Record the differing statements and check the actual study/event requirements instead of choosing one silently.
- ASSOC page 18's role table and page 19's full/partial/task-control descriptions use different permission vocabularies. PLAN pages 38-41 discuss scheduling restrictions and accelerated delivery. Cover dates do not certify these as current controls.
- Numeric recommendations and example outcomes stay edition-specific: learning-event targets, ad-set budget sharing, daily-budget flexibility, reservation eligibility, catalog product/match targets, source-audience sizes, video/caption limits and lift-test spend/sample/duration guidance are not universal launch rules, statistical guarantees or spending authority.
- BUY page 10 explicitly says opportunity score does not predict or guarantee actual performance. Its experimentally supported recommendation wording does not establish a result for this user. Fictional budget diagrams and examples are not experiments.
- Privacy/policy chapters provide source-specific summaries, not a legal determination, an exhaustive current policy or permission to bypass consent. Do not import sensitive-category examples or broad shorthand as operational instructions.

For any current control, eligibility, API field, policy or account-specific setup, apply `library/contracts/PLATFORM-CURRENCY.md`. A source can be useful while a particular instruction is dated, incomplete or inconsistent. A retrieved method is not a completed campaign, an authenticated integration or proof of business effectiveness.
