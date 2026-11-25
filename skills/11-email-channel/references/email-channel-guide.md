# Email channel guide

## Consent by source

| Source | Usually | Action |
| --- | --- | --- |
| Checkout opt-in box ticked | Consent to marketing | Mail |
| Lead-magnet form whose wording mentions ongoing email | Consent to what the form said | Mail what the form promised |
| Lead-magnet form that only promised the download | Unclear | Ask the owner; consider one re-permission email |
| Customers who did not opt in | Transactional email only in many places; some laws allow marketing to existing customers with an opt-out | Verify the law for the country; mark *to confirm* |
| Paper sheets, events, business cards, imported lists with no record | No record of consent | Hold out of broadcasts until consent is obtained |
| Bought, rented or scraped lists | Not consent | Never |

Laws differ: the US CAN-SPAM Act is opt-out based; the EU and UK (GDPR and PECR) and Canada (CASL) generally need consent or a narrow existing-customer exception. Verify in current official guidance for each country the list covers and date it, or mark *to confirm*. Not legal advice.

## Deliverability

- Authenticate the domain: SPF, DKIM and DMARC. Check DMARC with the domain host or a DNS lookup.
- One-click unsubscribe and an unsubscribe link in every marketing email.
- Remove hard bounces; suppress contacts inactive for a long period after a re-permission email.
- Watch spam complaints, bounces and unsubscribes per send. A rising unsubscribe rate means the content or frequency is wrong for some of the list.
- Raise frequency in steps (for example monthly, then every two weeks, then weekly) while complaints and unsubscribes stay flat.
- Google, Yahoo and Microsoft publish bulk-sender rules (authentication, unsubscribe, complaint thresholds). They change; cite the current page with URL and date (Google: support.google.com/a/answer/81126; Yahoo: senders.yahooinc.com) or mark *to confirm*.

## Measurement

- Click rate = clicks / delivered. Unsubscribe rate = unsubscribes / delivered. Orders per 1,000 delivered = orders / delivered × 1,000.
- Opens are inflated by privacy features (for example Apple Mail Privacy Protection) and bots. Do not judge on them.
- Tool attribution (orders within N days of a click) is a last-touch view; it can over- or under-credit email.

## Calendar

- Pick a cadence the owner can write every time. A smaller, steady rhythm beats a weekly plan that stops in week three.
- Mix help (guides, how-tos, answers to common tickets) and sell (the real offer). Each send has one job.
- Hand off: one email's copy to `10-email-copy`, automated flows to `12-email-sequences` or `15-lifecycle`, SMS to `11-sms`.
