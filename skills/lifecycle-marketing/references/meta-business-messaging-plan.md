# Meta business messaging: service response and lifecycle handoff

```yaml
artifact_type: playbook
decision: design a useful Messenger/WhatsApp response system with clear eligibility, ownership and business-outcome measurement
scope: service and lifecycle communication planning; paid acquisition, copy and live platform configuration retain their owners
owner: lifecycle-marketing
inputs: customer journey, verified service facts, entry points, events, permission basis, staffing and current messaging surface
evidence_status: inferred
confidence: not-assessed
freshness: live-check
dependencies: copywriting, organic-social, meta-ads, current messaging requirements and operations
authorization: draft
rollback_or_stop: stop unsolicited contact, suppression bypass, false response promises or unapproved sends
```

## Source basis

ASSOC-2026-01 pages 31-36 describe Messenger entry points, labels/activity/notes and instant/away/FAQ responses. Pages 38-44 cover WhatsApp Business profiles, conversation entry, greeting/quick/away/marketing messages, labels and catalogs. Page 46 places inbox work within Business Suite. [Source record](../../meta-ads/references/meta-2026-guides-source-notes.md).

A public [Blueprint WhatsApp onboarding overview](https://fbp.exceedlms.com/student/path/253151-whatsapp_for_business_onboarding_course), checked 2026-09-30, describes goals, use cases, measurement, governance and implementation planning. Its detailed lessons were sign-in gated. This reference does not claim to reproduce them.

The following design is an original MKT application. It is not a claim that the WhatsApp Business app, Business Platform/API, Messenger and Business Suite have interchangeable automation, pricing, eligibility or message rules. Verify the exact surface and current requirements before implementation.

## Separate conversation purposes

A greeting acknowledges a new inquiry; an away response manages availability expectations; a quick/saved reply helps answer a recurring question; a service update communicates a verified transaction state; a marketing message promotes an offer. An inquiry or prior purchase does not automatically authorize every future promotional message.

Use the existing [segmentation and triggers](segmentation-and-triggers.md) contract to record:

`entry/event | customer need | eligible state | permission basis | delay/response expectation | suppression and collision checks | human owner | fallback | exit condition | outcome`.

For a capacity-limited team, state staffed hours and the real response expectation rather than promise immediate support. If a late order event conflicts with a newer fulfillment state, recheck state before composing a message. Do not send a payment reminder after payment or a promotional follow-up after suppression. Data quality and capacity can be the limiting condition, not insufficient messaging frequency.

## Return an operational handoff

Map entry points only where they actually exist: a Page action, a verified short link/QR destination, an organic inquiry or a paid click-to-message campaign. `$meta-ads` owns the paid campaign and its objective/performance goal. A click or conversation start is not a qualified lead or a paid order.

Define a compact status vocabulary grounded in the business, such as new inquiry, awaiting customer, awaiting team, resolved or an actual order state. Assign owners and escalation rules. Labels and notes assist organization; they do not prove payment, order fulfillment or CRM synchronization. Keep private customer information out of shared reports and repositories.

For catalogs, maintain verified names, descriptions, prices, availability and links for the intended market. Browsing a catalog or receiving a product link is not a completed transaction. Do not promise payment or checkout capabilities merely because the guide describes them.

Give `$copywriting` a complete brief for each needed response: purpose, factual content, tone, required clarification, prohibited claims and next step. Produce the requested drafts through that owner within the same task instead of making the user open another conversation. This lifecycle reference owns logic, not the words of the message. `$organic-social` owns public-community response strategy; `$marketing-operations` owns recurring execution, state and escalation where applicable.

## Measurement and verification

Track service measures such as response delay, unresolved workload and resolution alongside verified downstream qualification/orders when available. Define cohorts, lag, source and status. Do not equate labels, conversation volume or reply speed with sales lift. Use `$tracking-measurement` for attribution and incremental-effect questions; use the actual business owner for outcome definitions.

Before any configured flow goes live, test eligible/ineligible entry, duplicate events, late data, suppression, human handoff and destination accuracy on approved synthetic evidence. A written flow, drafted response or public course outline does not authorize sending or establish an active integration.

**Return:** conversation-purpose map, eligibility/trigger table, staffing/escalation plan, coordinated copy brief/drafts, measurement contract and current-platform/permission checks. Keep design, configured, sent, delivered and outcome-verified states separate.
