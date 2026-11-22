# Canonical Marketing Glossary

This glossary defines Marketing OS terminology. Platform interface labels may change; preserve the strategic concept and map the current product label explicitly. When a client's source system uses a different definition, record that definition before comparing metrics.

## Commercial outcomes

- **Gross sales:** Sales before discounts, refunds, and other revenue deductions.
- **Net revenue:** Gross sales minus discounts, refunds, and explicitly defined revenue deductions. State whether tax and shipping revenue are included.
- **Gross profit:** Net revenue minus cost of goods sold (COGS).
- **Contribution profit before media:** Gross profit minus variable fulfillment, payment, marketplace, and servicing costs included in scope.
- **Contribution profit after media:** Contribution profit before media minus media spend.
- **Contribution margin:** The defined contribution profit divided by net revenue. Always state whether it is before or after media.
- **Operating profit:** Revenue minus the defined variable and fixed operating expenses. Do not use this term when fixed costs are unavailable.
- **Return on ad spend (ROAS):** Attributed revenue divided by media spend. ROAS is not profit.
- **Customer acquisition cost (CAC):** Acquisition costs divided by newly acquired customers under a stated cost and customer definition.
- **Realized revenue:** Revenue actually recorded under the business's defined recognition rule, not merely attributed or forecast.
- **Qualified pipeline:** Opportunity value meeting the business's explicit qualification and stage rules.
- **Average order value (AOV):** Revenue divided by orders for the same scope and period. State the revenue basis (gross sales or net revenue, and tax and shipping treatment) and the order definition. AOV is not profit per order.

Use one of these formulas, according to the available source definition:

`Contribution profit after media = gross sales - discounts - refunds - COGS - variable fulfillment - payment fees - media spend`

`Contribution profit after media = net revenue - COGS - variable fulfillment - payment fees - media spend`

Never subtract discounts or refunds again when they are already reflected in net revenue.

## Measurement and causality

- **Business source of truth:** The authoritative system for the outcome in question, such as paid orders, fulfilled revenue, qualified opportunities, or closed-won revenue.
- **Event:** A recorded occurrence with a defined trigger and parameters.
- **Conversion:** A context-dependent desired action. Name the exact action rather than relying on this word alone.
- **Primary business outcome:** The main commercial or qualified result for an analysis. This is not the Google Ads setting “Primary conversion action.”
- **Google Ads conversion action:** A specific measured action in Google Ads.
- **Google Ads conversion goal:** A grouping of related conversion actions used in campaign optimization settings.
- **Primary conversion action:** Google Ads action-optimization status eligible for bidding and the Conversions columns when the campaign uses its containing goal.
- **Secondary conversion action:** Google Ads observation-oriented status reported outside the primary Conversions columns, subject to custom-goal behavior.
- **Meta performance goal / optimization event:** State the campaign objective, conversion location, dataset or pixel, selected event, and performance goal separately; do not collapse them into one setting.
- **Bidding signal:** A measured input that can influence automated bidding. A tracked event is not necessarily a bidding signal.
- **Collection:** Capture and transmission of data.
- **Receipt:** Confirmation that the destination received the event; receipt does not prove correctness.
- **Deduplication:** Identification and suppression of duplicate representations of the same event.
- **Attribution:** A rule or model that assigns credit for an outcome.
- **Reconciliation:** Explanation of differences between systems after scope and definitions are aligned.
- **Incrementality:** Additional outcomes caused by an intervention compared with what would otherwise have happened.
- **Causality:** A supported claim that changing one factor produced a change in another; timing or correlation alone is insufficient.

## Audience, journey, and research

- **Market:** The broader demand environment in which customers and competitors participate.
- **Segment:** A distinguishable group sharing decision-relevant needs, situations, economics, or reachability.
- **Ideal Customer Profile (ICP):** The economically and operationally attractive customer or account profile. For consumer contexts, “priority customer segment” may be clearer.
- **Persona:** A research-backed representation of a customer type; never a substitute for evidence or economics.
- **Buying situation:** The context and trigger in which progress becomes important.
- **Jobs-to-be-Done (JTBD):** The progress a customer seeks in a situation, not the act of using a product.
- **Funnel or journey stage:** Relationship to the buying process.
- **Awareness level:** What the audience understands about the problem, solutions, product, and offer.
- **Audience temperature:** Degree of prior exposure or engagement.
- **Lifecycle stage:** CRM or customer-state classification, such as lead, opportunity, customer, or lapsed customer.
- **Voice of Customer (VoC):** Traceable customer language from supplied research. Model-generated language is a synthesis or hypothesis, not VoC.
- **Research provenance:** The source, date, segment, method, context, and limitations attached to evidence.

## Paid media and creative

- **New-customer acquisition / prospecting:** Strategic category for reaching eligible potential customers without a qualifying prior relationship. “Prospecting” may not be a platform interface label.
- **Retargeting / remarketing:** Strategic category for reaching eligible people based on prior engagement, visit, customer, or behavioral signals. Name the exact audience source, window, and exclusions.
- **Creative strategy:** System of insights, angles, messages, concepts, formats, and tests.
- **Angle:** Strategic reason the audience should care.
- **Hook:** Opening expression used to earn attention.
- **Creative concept:** Central advertising idea or execution.
- **Creative asset:** The produced image, video, copy, audio, or component.
- **Ad:** The configured platform entity combining identity, creative assets, copy, CTA, destination, and delivery settings.
- **Format:** Delivery form such as video, static image, carousel, or collection.
- **Adaptation:** Placement- or aspect-ratio-specific version; not automatically a distinct strategic test.
- **Message scent:** Continuity between the promise in an ad, query, or link and the destination's immediate message.
- **Full-funnel:** Demand/awareness through consideration, conversion, qualified or purchased outcome, and retention or realized customer value—not merely a set of campaign objectives.
- **Click-through rate (CTR):** Clicks divided by impressions. Name the exact click and impression metric used; click definitions can differ between platforms and between metrics on one platform, so verify the current definition before comparing. CTR is an engagement signal, not a business outcome.
- **Cost per mille (CPM):** Media spend per 1,000 impressions: `media spend / impressions × 1,000`.
- **Cost per click (CPC):** Media spend divided by clicks under the stated click definition.

Compare these delivery metrics only against the business's own matched history or a named, dated source; do not attach unsourced benchmark ranges to them.

## Lead lifecycle

Use the client's actual CRM stages, then map them where applicable:

`inquiry -> lead -> contacted lead -> qualified lead -> sales-qualified opportunity -> appointment or proposal -> closed-won customer -> realized revenue`

Define qualification, stage-entry rules, date basis, and value basis before comparing CPL, cost per qualified lead, pipeline, close rate, or CAC.

## Activation, retention, and customer economics

`$activation` owns first-value definitions, `$retention-strategy` owns loss reasons and interventions, and `$retention-economics` owns lifetime value, payback, and cohort curves. These short definitions do not replace those skills.

- **Activation / first meaningful value:** The first behavior or outcome that credibly indicates the customer has received meaningful value from the product, service, or relationship. Onboarding, tutorial, profile, or email completion is a supporting event, not activation, unless evidence shows it represents or predicts that value in scope. A business whose conversion itself substantially delivers the value may have no distinct activation stage.
- **Activation rate:** Customers meeting the defined activation criterion within the defined window divided by eligible customers entering the activation journey. Fix the denominator, exclusions, event, and window before reading results.
- **Time-to-value:** Elapsed time from entering the activation journey to first meaningful value. Report a distribution, including the not-yet-activated share, rather than only an average. Shorter is not better when it removes necessary qualification, safety, setup, education, compliance, or service work.
- **Churn:** Loss of customers (logo churn) or of recurring revenue (revenue churn) over a stated window. Name which one, the continuation behavior it measures, and whether voluntary and involuntary loss are separated.
- **Voluntary churn:** Loss through the customer's own decision to cancel, not renew, or stop. A cancellation reason is the customer's stated reason, not a verified cause.
- **Involuntary churn (payment failure):** Loss without a decision to leave, caused by a failed or expired payment method, billing error, insufficient funds, or a technical payment issue. It calls for payment-recovery mechanics, not persuasion or discounting by default.
- **Lapse:** A customer who stopped the expected repurchase, use, or return behavior without an explicit cancellation, judged against a stated inactivity window. A lapsed customer may be dormant between natural purchase cycles rather than lost.
- **Customer lifetime value (LTV):** Cumulative value per customer from a defined cohort. Always state the horizon, the variant, and whether it is historical or predictive:
  - *Historical (realized):* actual cumulative value from the cohort to date. *Predictive (modeled):* a projection from partial cohort data or a fitted curve, reported with its uncertainty. Never blend the two silently.
  - *Revenue LTV:* cumulative net revenue with no costs deducted; top-line scale only, never for acquisition-spend decisions.
  - *Gross-profit LTV:* cumulative net revenue minus COGS; label it and do not call it contribution.
  - *Contribution LTV:* cumulative contribution profit before media; the variant compared against acquisition cost.
  - *Contribution-after-media LTV:* contribution LTV minus acquisition cost; never compared against acquisition cost again.
- **Payback period:** The time until cumulative contribution profit before media per customer first exceeds acquisition cost (CAC from the business source of truth). Gross profit may stand in, labeled, when variable costs are unavailable. Never put a figure that already deducts media or acquisition cost on the profit side. Revenue payback ignores COGS and variable costs; label it as such, because it is not the decision figure for scaling.

## Optimization and scaling

- **Scaling:** Increasing a verified primary business outcome while keeping named economics, quality, capacity, measurement, and risk guardrails acceptable.
- **Spend growth:** An increase in advertising spend; not automatically scaling.
- **Profitable scaling:** Increasing contribution profit after media under explicitly defined revenue and cost inputs.
- **Qualified scaling:** Increasing qualified pipeline or realized customer value while preserving defined quality and capacity thresholds.
- **Vertical scaling:** Increasing budget or bidding pressure within existing eligible coverage.
- **Horizontal scaling:** Expanding products, queries, audiences, placements, markets, creatives, or other eligible coverage. Routine creative testing and refresh — new creatives or ads inside existing ad sets, ad groups, or campaigns with no budget increase — is not horizontal scaling: the channel skill owns the ads and `$creative-strategy` the concepts. Increasing spend or exposure behind a winning creative goes to `$optimization-scaling`.
- **Creative scaling:** Increasing evidence-backed creative diversity, learning, and production capacity.
- **Funnel scaling:** Increasing qualified post-click conversion capacity or reliability.
- **Operational scaling:** Increasing inventory, fulfillment, sales, service, support, onboarding, or cash capacity.
- **Blended efficiency:** Average performance across the scoped total spend and outcome.
- **Marginal efficiency:** Performance associated with the change in spend/outcome between comparable states.
- **Saturation:** Declining marginal opportunity as high-value eligible demand or capacity is increasingly exhausted.
- **Scale ceiling:** Highest currently supportable activity before a named economic, quality, capacity, measurement, or risk guardrail becomes unacceptable.
- **Scaling step:** One bounded, interpretable increase in spend, bidding pressure, exposure, or coverage with a decision and rollback contract.
- **De-scaling:** Controlled reduction in inefficient or unsustainable activity while protecting valuable coverage and evidence.
- **Recovery verification:** Source-of-truth confirmation that a breached condition has restored through the relevant lag/window.

## Evidence and experimentation

- **Observed:** Directly present in a named source and scope.
- **Calculated:** Derived with visible formula and inputs.
- **Experimentally observed:** Supported by a defined test or controlled comparison whose design and limitations are stated. It supports the observed effect under the tested conditions, not the proposed mechanism, and it is not itself a causal grade: grade causal strength on the causal evidence ladder.
- **Inferred:** Supported explanation that has not been isolated.
- **Assumed:** Explicitly unverified input used to proceed.
- **Unknown:** Missing information that may change the decision.
- **Verified defect:** Reproducible failure with direct evidence.
- **Hypothesis:** Falsifiable explanation or proposed mechanism.
- **Primary metric:** Metric used for the experiment's main decision; not necessarily a platform Primary conversion action.
- **Guardrail metric:** Metric that protects against unacceptable downstream harm.
- **Stop condition:** Predefined condition for ending or containing a test.
- **Decision rule:** Predefined interpretation leading to ship, iterate, reject, or inconclusive.

## Evidence and proof scales

Several scales grade different questions about the same work. Some share words, but a shared word never carries its meaning from one scale to another. Grade a claim on every scale that applies and record each grade under its own scale name, for example `intake: reconciled; causal: C1; scaling: S3`.

| Scale | What it grades | Defined in | Levels |
|---|---|---|---|
| Analysis claim labels | How a statement in an analysis was produced | [Evidence and experimentation](#evidence-and-experimentation) | observed, calculated, experimentally observed, inferred, assumed, unknown |
| Platform currency states | Support for a current platform or vendor product, control, reporting, or behavior claim, within the scope that contract sets | [`PLATFORM-CURRENCY.md`](PLATFORM-CURRENCY.md#evidence-states) | officially documented, account-visible, experimentally observed, inferred, unknown |
| Artifact evidence status | The evidence behind a governed artifact, recorded as metadata | [`KNOWLEDGE-TAXONOMY.md`](KNOWLEDGE-TAXONOMY.md#artifact-metadata-contract) (`evidence_status`) | observed, calculated, officially-documented, account-visible, experimentally-observed, inferred, assumed, unknown |
| Intake evidence register | How a decision-relevant claim was received and whether it agrees with the business source of truth | [Evidence register](../../skills/marketing-intake/references/evidence-register.md#evidence-states) | asserted, document-supplied, observed, reconciled, verified; blocking states unknown and contradicted |
| Causal evidence ladder | How strongly evidence supports that marketing activity caused a business result | [Causal evidence ladder](../../skills/tracking-measurement/references/causal-evidence-ladder.md#levels) | C0 platform-attributed, C1 correlation or uncontrolled before-and-after, C2 modeled attribution or Marketing Mix Modeling, C3 quasi-experiment, C4 randomized experiment, C5 replicated randomized evidence |
| Scaling proof standard | What may be called proven and scalable | [Scaling proof standard](../../skills/optimization-scaling/references/proof-standard.md) | S0 unverified, S1 officially documented, S2 account-visible, S3 analytically supported, S4 experimentally validated, S5 business-verified, S6 replicated, S7 currently scalable |
| Integration states | Whether an external adapter is usable for an exact read or write | [`integrations/README.md`](../integrations/README.md#integration-states) | documented → configured → authenticated → connected → authorized → verified |

Rules:

- **Labels are never translated across scales by name.** Intake `verified` is not C4, S5, or an integration `verified`. S1 and S2 reuse the platform-currency names, but each level carries only its own scale's definition. Where one scale gates another, the owning file states the gate explicitly (for example, S4 requires C3 or above); that is a stated requirement, not a name match.
- **The same word can mean different strengths.** "Documented" has three meanings. Intake `document-supplied` (formerly `documented`) means the claim appears in a supplied document or screenshot; it is weaker than `observed` because neither the named source system nor an unedited export from it has been seen. An unedited platform export with its source recorded is `observed` for platform behavior however it arrives, not `document-supplied`. Platform-currency "officially documented" means a current first-party source from the platform or vendor that owns the behavior supports it, with the source and verification date `library/contracts/PLATFORM-CURRENCY.md` requires; availability in an account and business impact remain unverified. Integration `documented` means only that an adapter contract exists; nothing is installed, authenticated, or connected. "Verified" also differs: intake `verified` is a reconciled and independently confirmed claim, an integration `verified` is a checked read or action, and a verified defect is a reproducible failure. None of them is a causal grade.
- **Causal claims use only the causal evidence ladder.** Intake `verified`, experimentally observed, statistical significance, and S-levels do not grade causality. State the C-level and its scope with every causal claim; an unlabeled causal claim is treated as C0.
- **Scaling proof uses only S0–S7.** "Proven," "validated," and "scalable" in a scaling decision carry an S-level and its scope, and `$optimization-scaling` owns the gates.
- **Integration states describe access, never evidence about a claim.** Data returned by a connected, verified read enters the evidence register at its own state, for example `observed` for platform behavior, and is graded on the other scales separately.
- **Domain grades keep their own names.** The activation candidate evidence ladder (`$activation`), experiment transfer status (`$tracking-measurement`), and growth-constraint evidence states (`$growth-strategy`) follow these rules. Record them as they are and do not convert them into another scale's level.

## Marketing operating knowledge

Use [`KNOWLEDGE-TAXONOMY.md`](KNOWLEDGE-TAXONOMY.md) for the full contract and artifact metadata. The short definitions below prevent common category errors:

- **Principle:** Durable rule or constraint governing decisions.
- **Strategy:** Directional choice about where to compete, for whom, why, and how resources are allocated.
- **Framework:** Structured lens or decision map; it organizes reasoning but does not prove an outcome.
- **Model:** Simplified representation, relationship, or formula; expose variables and assumptions.
- **Methodology:** Named way of solving a class of problems with an evidence standard and decision rule.
- **Process:** Ordered repeatable workflow with inputs, outputs, owners, and handoffs.
- **Playbook / SOP:** A process adapted to a recurring business or scenario context.
- **Pattern:** Recurring shape in observed evidence; it is not automatically causal.
- **Hypothesis:** Falsifiable explanation or proposed mechanism.
- **Tactic:** Specific action selected to advance a strategy.
- **Technique:** Method for executing a tactic or process step.
- **Template:** Reusable structure for producing an artifact.
- **Checklist / QA:** Completeness and validation control.
- **Best practice:** Evidence-backed default within a defined scope; not a guarantee.
- **Heuristic:** Practical shortcut under uncertainty; label its confidence, scope, and override condition.
- **Guardrail / policy:** Limit that protects against unacceptable downside.
