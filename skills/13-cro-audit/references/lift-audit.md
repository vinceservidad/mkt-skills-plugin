# LIFT audit: questions, the five-second test and ranking

The LIFT model (Chris Goward, WiderFunnel) is a **framework** for organising a page review. It names six conversion factors: the value proposition drives conversion, relevance and clarity amplify it, urgency adds pull, and anxiety and distraction subtract. It is a checklist for finding hypotheses, not proof that a change will work. A finding from it is a heuristic observation until a test or real user evidence supports it.

## The six factors

| Factor | Ask | Evidence that settles it |
| --- | --- | --- |
| Value proposition | Does the page say what the offer is and why it beats the visitor's alternative, in line with `offer.md` → Core offer and `message.md` → Promise? | The page's words against context |
| Relevance | Does the page continue what the visitor clicked (ad, post, search, referral) and fit their awareness and temperature? | Source copy; analytics by source; Awareness map; Traffic temperature |
| Clarity | Can the visitor tell what it is, who it is for and what to do next? Is the next step clear and does it match what happens after? | Five-second test; copy; the confirmation message |
| Anxiety | Which evidenced fears and objections are unanswered where the decision is made? Which claims are unsupported or contradict context? | Beliefs, objections and drivers; Objection map; Proof stack; polls and sales questions |
| Distraction | What competes with the one action: navigation, extra links, extra form fields, several calls to action? | Page structure; form fields and who uses each |
| Urgency | Is there a true reason to act now? | Only what `offer.md` → Urgency and scarcity says is true. Never invent a deadline, stock count or demand. |

## Five-second test

Read only what is visible before scrolling. Answer three questions using the page's own words: what is it, who is it for, what do I do next. If you cannot answer from the words, clarity fails. Say plainly that this is your heuristic read; a real five-second test asks strangers and records their answers.

## Defect or hypothesis?

| It is a defect when | It is a hypothesis when |
| --- | --- |
| Something is broken, slow by measurement, or fails on a device | The page might persuade better another way |
| A claim is unsupported, or contradicts context (a service not offered, a badge without a policy) | An objection might be answered better |
| The page promises a next step different from what the business does | A layout or order might be clearer |
| A field is required but nobody uses it | A headline might match the source better |

Fix defects first, with the owner's approval. Test hypotheses.

## Form fields

For each field: who uses it, for what decision, and when. Keep fields the next step needs (for example a revenue band that sets the price band). Make optional or remove what nobody uses. Do not remove qualification the business relies on just to raise the submit rate; say what it costs and test.

## Ranking

Rank by three things, stated in words, not a made-up score:
1. **Evidence strength:** observed numbers or customer words beat a heuristic read.
2. **Reach:** how many of the right visitors pass through that element (above the fold and the form touch everyone who converts).
3. **Effort and risk:** a wording change is cheap; a redesign is not. Prefer a focused change that tests the mechanism over a redesign.

Bigger levers before small ones: offer and value proposition, headline and relevance, form and next step, layout, then cosmetic details.

## Reading the numbers

- Rates need numerators, denominators and periods. Device and source splits often hide the leak a blended rate shows as average.
- Single-digit counts cannot separate one rate from another; say so and avoid ranking on them alone.
- Check how page conversions map to downstream records (CRM, orders). A form submit may already be counted under the person's first lead source; do not add it twice.
- Do not compare a rate with an industry average or a "typical" rate. Compare with the page's own baseline and the business's economics.

## Owners of the fixes

| Fix | Owner |
| --- | --- |
| Copy rewrite (headline, body, call to action) | `10-page-copy` |
| Trust elements, reviews, guarantees on the page | `13-trust-signals` |
| Prices and plans on the page | `13-pricing-page` |
| Checkout steps and fields | `13-checkout` |
| Account or product sign-up flows | `13-signup` |
| Popups and slide-ins | `13-popups` |
| A new campaign landing page | `12-landing-page` |
| Traffic quality and sources | `11-channel-selection` |
| Test design and reading | `18-ab-testing` |
| The offer itself, price, guarantee | `07-offer-design`, `07-pricing`, `07-guarantee-risk-reversal` |
