# Account and Firmographic Targeting

LinkedIn's distinguishing targeting input is professional and firmographic data. Its documented targeting attributes include company name, industry, size, revenue, and growth rate, job function, seniority, and title, member skills, and years of experience, and it maps job titles to function and seniority with its own proprietary taxonomy; audiences are subject to members' preferences, and the documented minimum audience size to run an ad set is 300 member accounts (first-party: https://www.linkedin.com/help/lms/answer/a424655, checked 2026-09-26). Recheck attribute availability per [`PLATFORM-CURRENCY.md`](../../../library/contracts/PLATFORM-CURRENCY.md) before a plan depends on it. Where the business runs account-based marketing, a defined target account list is the other input. Building this well is largely an evidence problem: targeting should reflect who actually buys and how, not an assumed persona.

## Account-based targeting

Match a target account list (from `$icp-jtbd` or the business's own account-based marketing program) against the platform's account targeting. Confirm the actual match rate before assuming the campaign reaches the intended accounts. LinkedIn defines match rate as the percentage of entries in the uploaded source data that matched member accounts or, for company targeting, LinkedIn Pages within the past seven days, and states that Matched Audiences are created subject to members' ads-settings preferences (first-party: https://www.linkedin.com/help/lms/answer/a420595, checked 2026-09-26). A low match rate means the campaign is reaching a narrower or different set of accounts than the plan states, and budget or expectations should be adjusted accordingly rather than assumed to be working as planned. Why a particular list matches poorly is an account-specific question; do not assume a cause (such as company size or platform activity) without checking the unmatched entries.

Within a matched account, layer buyer-role targeting (seniority, function, title) to reach the actual buying-committee members rather than the entire company; targeting an entire matched account indiscriminately dilutes spend across roles with no purchasing influence.

## Attribute-based targeting

Where no defined account list exists, build targeting from `$icp-jtbd`'s buyer-role and buying-situation evidence: which functions and seniority levels are actually involved in this purchase decision, not a generic "decision-maker" assumption. Layer firmographic filters (company size, industry) to the segment `$marketing-intake` established as the primary business outcome's actual addressable market.

## Buying-committee coverage

State explicitly which buyer roles a given campaign targets and which it does not. A multi-stakeholder purchase (common in B2B) is rarely won by reaching one role; a plan should either cover the relevant roles with role-appropriate messaging, or state clearly that it targets only part of the committee and why.

## Rules

- Confirm match rate for any account-based campaign before reporting reach or budget efficiency; an unconfirmed match rate is an unverified claim about who the campaign actually reaches.
- Do not target an entire matched company indiscriminately when buyer-role evidence is available to narrow to the actual buying committee; broad within-account targeting wastes spend on non-influential roles.
- Do not assume a "decision-maker" title-based filter reflects the actual buying committee without `$icp-jtbd` evidence; job titles vary widely across companies and a title-only filter can both include irrelevant roles and exclude actual influencers with different titles.
- Firmographic targeting narrows reach; do not stack filters (industry, company size, seniority, function) so tightly that the addressable audience becomes too small to deliver meaningfully, without checking estimated audience size before launch.
