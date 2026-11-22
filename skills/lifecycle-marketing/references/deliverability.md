# Deliverability

Inbox placement is a prerequisite for every other lifecycle-marketing decision — a perfectly designed sequence that lands in spam has zero effect regardless of its logic or copy. Damage can also outlast the send that caused it: Google states that it can take time for improvements in spam rate to reflect positively on spam classification (first-party: https://support.google.com/mail/answer/81126, checked 2026-09-26). Treat any specific recovery timeline as unknown until the sender's own postmaster data shows it.

## What governs deliverability

Sender reputation (domain and IP); authentication (SPF, DKIM, DMARC configured and aligned); list hygiene (bounces, spam complaints, invalid or unengaged recipients); consistency of sending volume and pattern; and recipient feedback such as spam reports and unsubscribes. The mailbox-provider documentation below names these inputs.

The Google and Yahoo pages cited below (checked 2026-09-26) publish some engagement guidance — Google suggests considering unsubscribing recipients who don't open or read messages, and Yahoo states that sending to users who are not reading the mail harms delivery metrics and reputation — but do not publish how their filtering weights these signals; for any other provider this is unknown until checked on its own documentation. Any claim about relative weighting — for example, that deleting without opening counts more than an open — is an inference, not documented behavior; label it that way per [`PLATFORM-CURRENCY.md`](../../../library/contracts/PLATFORM-CURRENCY.md) and do not base a decision on it alone.

## Documented mailbox-provider sender requirements

These are the providers' own published requirements, verified 2026-09-26. Sender requirements are medium-change platform facts: recheck the page per `library/contracts/PLATFORM-CURRENCY.md` before a compliance decision, a sending-infrastructure change, or a claim about current enforcement depends on it. Meeting them is a prerequisite, not a guarantee of inbox placement. There is deliberately no mailbox-provider registry; requirements for any provider not listed here are unverified until checked on that provider's own documentation.

### Gmail

Sources: "Email sender guidelines" (first-party: https://support.google.com/mail/answer/81126, checked 2026-09-26) and "Email sender guidelines FAQ" (first-party: https://support.google.com/mail/answer/14229414, checked 2026-09-26). They apply to mail sent to personal Gmail accounts (addresses ending in @gmail.com or @googlemail.com).

- **All senders:** SPF or DKIM authentication; valid forward and reverse DNS (PTR) records for sending domains or IPs; a TLS connection; spam rate reported in Postmaster Tools below 0.3%; messages formatted to RFC 5322; no impersonation of Gmail From: headers.
- **Bulk senders:** Google defines a bulk sender as one sending close to 5,000 messages or more to personal Gmail accounts within a 24-hour period, counting all messages from the same primary domain, and states that a sender meeting that criterion once is permanently considered a bulk sender. Bulk senders must also set up SPF and DKIM, set up DMARC for the sending domain (the enforcement policy can be `none`), align the From: domain with the SPF or DKIM domain for direct email, and make marketing and subscribed messages support one-click unsubscribe with a clearly visible unsubscribe link in the body.
- **Spam rate:** Google advises keeping the Postmaster Tools spam rate below 0.10% and never reaching 0.30% or higher.
- **Unsubscribes:** the FAQ recommends fulfilling unsubscribe requests within 48 hours.
- **Enforcement:** the FAQ states that from November 2025 Gmail is ramping up enforcement on non-compliant traffic, with temporary and permanent rejections for messages that fail the requirements.
- **Volume:** increase sending volume slowly, send at a consistent rate, avoid bursts, and start with a low volume to engaged users.
- **Lists:** do not purchase email addresses or send to people who did not sign up.
- **Open rates:** Google states that it doesn't track open rates, can't verify the accuracy of open rates reported by third parties, and that low open rates aren't necessarily an accurate indicator of deliverability or spam-classification issues.

### Yahoo

Sources: "Sender Best Practices" (first-party: https://senders.yahooinc.com/best-practices/, checked 2026-09-26) and "FAQs" (first-party: https://senders.yahooinc.com/faqs/, checked 2026-09-26).

- **All senders:** SPF or DKIM at minimum; spam rate below 0.3%; valid forward and reverse DNS records for sending IPs; compliance with RFCs 5321 and 5322.
- **Bulk senders:** both SPF and DKIM; a valid DMARC policy of at least `p=none`, and DMARC must pass; From: domain aligned with the SPF or DKIM domain; a functioning list-unsubscribe header supporting one-click unsubscribe for marketing and subscribed messages (the RFC 8058 POST method is highly recommended, mail-to is acceptable); a clearly visible unsubscribe link in the body; unsubscribes honored within 2 days; spam rate below 0.3%, which Yahoo calculates on mail delivered to the inbox.
- **Bulk definition:** Yahoo classifies a bulk sender as one sending a significant volume of mail and states it will not specify a volume threshold. Do not assume a sender falls below it.
- **Change:** Yahoo states the requirements are subject to change and asks senders to monitor the page.
- **Engagement:** Yahoo states that sending to users who are not reading the mail, or who report it as spam, harms delivery metrics and reputation.

### Apple Mail Privacy Protection

Source: "Mail Privacy Protection & Privacy" (first-party: https://www.apple.com/legal/privacy/data/en/mail-privacy-protection/, checked 2026-09-26).

- **Documented:** when Protect Mail Activity is on, the Mail app and Mail on iCloud.com download remote content in the background by default when an email is received, regardless of whether the recipient engages with it, and route that content through two separate relays so senders can't use the recipient's IP address as a unique identifier to connect their activity across websites or apps. Users can turn the setting off.
- **Documented effect on open tracking:** Apple states that email senders may learn when and how many times a recipient opened their email, and that Protect Mail Activity helps protect privacy by preventing email senders, including Apple, from learning information about the recipient's Mail activity. Open rate, open-based engagement segments, and open-triggered or send-time logic are therefore unreliable for recipients with the setting on.
- **Inference (mechanism not stated by Apple):** a pixel-based open recorded by the sending platform for such a recipient may reflect the background download rather than a person reading the email. Apple's page does not say what share of any list uses the setting; measure it from the sending platform's own data if it identifies these opens, otherwise record it as unknown.

## Rules

- Do not increase send volume or frequency sharply without a ramp; Google tells senders to increase volume slowly, send at a consistent rate, and avoid bursts (see Gmail above).
- Remove or suppress chronically unengaged contacts on a stated cadence rather than continuing to send indefinitely; Yahoo states that sending to recipients who are not reading the mail harms delivery metrics and reputation. Define "unengaged" from clicks, replies, conversions, or other signals the sender can verify, not from opens alone, given the Gmail and Apple documentation above.
- Do not purchase, rent, or otherwise acquire a list from outside the business's own consented capture; it is a consent violation, and Google's guidelines tell senders not to purchase addresses or send to people who did not sign up.
- A spike in spam complaints or bounce rate is a stop condition, not a metric to monitor passively; treat it with the same urgency as a tracking defect — pause the implicated send and diagnose before continuing. Compare against the documented provider thresholds above, and note that a provider's own rate (Yahoo's is calculated on inbox-delivered mail) can differ from the rate the sending platform reports.
- Warm a new sending domain or IP gradually with the most engaged segment first; Google advises starting with a low volume to engaged users. Do not launch a new domain directly into full-list volume.
- Authentication configuration (SPF/DKIM/DMARC) and the one-click unsubscribe requirement are prerequisite checks before diagnosing any other deliverability problem; verify them against each relevant provider's current requirements for the sender's volume class before attributing a placement issue to content or list quality.
- Do not diagnose a deliverability or spam-folder problem from a falling open rate alone; Google states low open rates aren't necessarily an accurate indicator, and Apple documents that Protect Mail Activity prevents senders from learning Mail activity, including when and how many times an email was opened (see Apple above). Confirm with provider postmaster data, bounce and rejection codes, or seed or placement evidence, and label the evidence used.
- Do not state a mailbox provider's requirement, threshold, or filtering behavior without its first-party source and check date; label anything else unverified per `library/contracts/PLATFORM-CURRENCY.md`.
