---
name: copywriting
description: Write, rewrite, or evaluate email, lifecycle, website, landing-page, product-page, sales-page, long-form, or brand copy, including headlines, body, offer wording, CTAs, and microcopy, using evidence-backed customer language and a structure matched to funnel stage; not for paid-ad hooks, angles, or concepts, or for diagnosing why a page does not convert and designing its test, which are owned elsewhere.
---

# Copywriting

Classify each framework, structure, or heuristic with [`KNOWLEDGE-TAXONOMY.md`](../../library/contracts/KNOWLEDGE-TAXONOMY.md). A copywriting structure (AIDA, PAS, FAB, BAB) is a pattern that organizes an argument — it is not evidence that the argument is true, and applying it correctly does not make an unsupported claim supportable.

Per [`CAPABILITY-REGISTRY.md`](../../library/contracts/CAPABILITY-REGISTRY.md), this skill writes all page copy — landing-page, product-page, sales-page, and website copy, including headlines, body, offer wording, CTAs, and microcopy — plus email and lifecycle sequences, long-form content, and brand voice, from supplied customer evidence. Paid-ad hooks, angles, concepts, and static paid-creative text hierarchy stay owned by `$creative-strategy`. `$cro` owns conversion diagnosis of pages, forms, checkout, and pre-conversion friction: it evaluates copy as a conversion variable, writes the test hypothesis and design, and hands rewrites here. This skill writes the words; it does not diagnose why a page does not convert, design the test, or declare a winning variant.

## Required inputs

Primary business outcome, reader decision, intended next action and funnel stage the copy serves; audience — priority segment, buying situation, or Jobs-to-be-Done per `$icp-jtbd` where available; evidence-backed customer language available from `$customer-research`, with its provenance; brand voice guidelines if they exist; the specific claim or offer being communicated and what supports it; and the channel and format constraints (subject line length, email client rendering, page length). For page copy, also the page's conversion boundary, the upstream ad, query, or email promise the page must continue, the page section being written, and any `$cro` finding, rewrite brief, or test hypothesis it must address.

## Method

1. Name the primary reader decision, promise and next action per piece. Multiple roles may share that job; supporting audience modules must not create conflicting primary promises. Apply the Rule of One to the piece, not an absolute one-profession restriction.
2. Verify every factual or quantitative claim against a source before writing it in; do not write a number, result, or comparison the source evidence does not support.
3. Use customer language only when it is traceable to a supplied source — an interview, review, survey response — via `$customer-research`. Do not invent or paraphrase a quotation from memory and present it as customer language.
4. Select the smallest useful arrangement from reader intent, available proof, objection, format and destination; awareness is an evidence-backed input or an explicit unknown, not an automatic formula. See [Intent-led structure selection](references/structure-selection.md).
5. Produce the requested artifact, then apply [Drafting and editing](references/drafting-and-editing.md): verify facts and exact terms, use concrete language, cut stock rhetoric, preserve qualifications, and check headline/body/CTA continuity. Do not replace a short rewrite with a strategy lecture.
6. For a sequence (email, lifecycle), sequence the individual pieces against the funnel stage and lifecycle definitions `$marketing-intake` recorded, and against the segmentation, trigger, and cadence design `$lifecycle-marketing` owns; a single piece is evaluated on its own persuasive logic, a sequence on its cumulative arc. This skill writes the words for a sequence; it does not design the sequence, platform, or triggers — route that to `$lifecycle-marketing`.
7. For landing-page, product-page, sales-page, or website copy, write each element — headline, body, offer wording, CTA, microcopy — to the page's promise and conversion boundary and to any `$cro` brief. When `$cro` has named a copy problem (message scent, clarity, objection handling), address that problem explicitly. When the copy is a test variant, return it to `$cro` for the test design and to `$tracking-measurement` for validity rather than predicting the result.
8. State what would need to be true for the copy to work, and flag any claim in it that is unverified or aspirational rather than evidenced.

## Rules

For an ecommerce page, policy, voice or localized destination rewrite, use [Ecommerce decision copy](references/ecommerce-decision-copy.md) to deliver the actual wording with product, obligation and local-meaning checks. Read its source review only when provenance matters; article examples are not this client's customer evidence.

- Never fabricate a benchmark, result, testimonial, or customer quotation. A number or claim with no traceable source is not written into the copy; it is flagged as missing.
- Do not present a copywriting structure as a guarantee of performance; a structure organizes an argument, and whether the argument converts is an empirical question for `$cro` or `$creative-strategy` to test, not something this skill can assert.
- Do not write paid-ad hooks, angles, or static-ad type-overlay hierarchy; route those to `$creative-strategy`, including its static DTC creative-direction method.
- Write landing-page, product-page, sales-page, and website copy here. Do not diagnose why a page does not convert, design the test, or call a variant the winner; route conversion diagnosis and test design to `$cro` and causal validity to `$tracking-measurement`. Offer wording expresses approved commercial terms; it does not change the offer, price, or policy — route those to `$offer-strategy` or `$pricing-monetization`.
- Do not claim brand voice consistency without the brand guidelines actually supplied; write a best-effort draft and label the voice as unverified against guidelines if none exist.
- A claim of scarcity, urgency, authority, or social proof must be true and evidenced; do not manufacture false urgency or an unsupported authority claim.
- For regulated or compliance-sensitive claims (health, financial, legal outcome claims), do not write a claim beyond what the supplied evidence supports, and flag the claim for review rather than softening it silently.

## Output

Draft: requested copy first in placement order, with no framework skeleton in consumer-facing prose. Follow with concise notes on the primary reader decision, promise and next action; arrangement and reason only when useful; factual-claim sources, customer-language provenance, assumptions and verification gaps; and exact draft/approval/publication status. Keep qualifications needed for a decision beside the claim in the copy, not hidden in notes. Address the supplied CRO rewrite brief; return any conversion diagnosis or test design to `$cro` and validity to `$tracking-measurement`, without a winner or lift claim.

Evaluation: inspect the actual copy against its brief, reader decision, proof, format, destination and primary action; distinguish source-backed claims from assumptions and unsupported additions; allow audience modules serving the shared job; return specific revisions.

## QA

Confirm the piece has a clear primary decision, promise and next action, with explicit supporting audience differences where relevant; inspect the actual artifact, not just a framework explanation; every factual claim traces to a source; every customer-language use traces to a supplied source via `$customer-research`; the structure fits the communication goal rather than being applied by default; no paid-ad hook, angle, or concept was written here instead of routed to `$creative-strategy`; page copy was written here without a conversion diagnosis, test design, or winning-variant claim made on `$cro`'s behalf; and no claim exceeds what the evidence supports.
