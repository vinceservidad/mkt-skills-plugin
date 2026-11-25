# WhatsApp and conversational messaging guide

## 1. WhatsApp Business App vs. WhatsApp Business Platform (API)

- **WhatsApp Business App:** Free mobile/desktop app for solo operators or tiny teams handling manual replies, quick replies and small catalog views. Not built for automated checkout triggers, CRM sync or scalable broadcasts.
- **WhatsApp Business Platform (Cloud API / BSP):** Required for automated order/shipment alerts, Shopify/Klaviyo/CRM sync, multi-agent inbox routing, Click-to-WhatsApp attribution and compliant template broadcasts. Requires Meta Business verification, a dedicated phone number and per-message template fees (verify current Meta pricing tables — cite URL + date).

## 2. Explicit opt-in rules (non-negotiable)

Under Meta's WhatsApp Business Policy and regional laws (GDPR, UK PECR, TCPA, etc. — verify per country):
- Users must **actively opt in** to receive messages from your business **specifically on WhatsApp**, knowing the business name and message types.
- A phone number typed at checkout "for delivery updates" is **NOT** consent for WhatsApp marketing messages (and even for Utility order updates, check whether the customer explicitly chose WhatsApp vs. email/SMS).
- Store an audit trail: timestamp, opt-in source (checkout checkbox, thank-you page widget, QR code, inbound Click-to-WhatsApp message), exact disclosure wording, and opt-out timestamp.

## 3. Meta template categories and the 24-hour service window

- **Customer Service Window (24 hours):** When a customer messages you first (or clicks a Click-to-WhatsApp ad / CTA button), a 24-hour free-form reply window opens. Use this for genuine two-way help, guided product selection, objection answering and human hand-off.
- **Utility templates:** Strictly tied to an existing order, shipment, subscription renewal or account action requested by the customer. **Do not include upsells, promo codes or cross-sell offers inside a Utility template** — Meta automatically reclassifies mixed templates as Marketing (higher cost + requires marketing opt-in) or rejects them.
- **Marketing templates:** Promotions, abandoned-cart nudges, back-in-stock alerts, win-back offers, replenishment reminders with offers. Require explicit Marketing opt-in, a visible opt-out button (`Stop promotions`) and tight frequency caps.
- **Authentication templates:** One-time passcodes / login verification only.

## 4. Quality rating and throttling guardrails

Meta scores each business phone number continuously (**Green / High**, **Yellow / Medium**, **Red / Low**) based on user blocks, spam reports and opt-outs:
- Never blast cold or unengaged lists. Start with high-intent opted-in segments and ramp slowly.
- If a template triggers elevated blocks or drops quality rating to Yellow, pause marketing broadcasts immediately, audit opt-in source and copy, and tighten targeting.
- Always include a fast, frictionless opt-out button on marketing templates — a clean opt-out hurts far less than a user hitting **Block & Report**.

## 5. Conversational flows (WhatsApp, Messenger, ManyChat)

- Keep automated branches short (max 2–3 quick-reply buttons per turn).
- Always offer a visible **Talk to a human** escape hatch.
- Use **Click-to-WhatsApp** ads (`11-paid-social` owns ad creative/bidding; this skill owns the post-click chat flow) only when response SLA is fast (instant qualifying question + human hand-off for high-ticket or consultative sales).
- Hand full abandoned-cart email/site strategy to `13-cart-recovery` and SMS texting to `11-sms`; coordinate so a buyer never gets hit by email + SMS + WhatsApp simultaneously for the same event.

## 6. Platform facts rule

Meta's WhatsApp per-message pricing, free entry-point windows (Click-to-WhatsApp / Page CTA), template reclassification rules, frequency capping ("per-user marketing template limits") and Messenger 24-hour rules change frequently. Cite verified official Meta documentation (URL + date) or mark *to confirm*.
