# AI Search and Agent Access

Search engines, AI assistants and AI agents now reach a site through different crawlers, for different uses, under different controls. A single "block AI" decision can remove a site from ordinary search, and a single "allow everything" decision can hand over training use the business did not intend. Decide each use against the primary business outcome, verify every control in the vendor's own documentation, and treat each change as a live change.

Every vendor fact below is high-change under [`PLATFORM-CURRENCY.md`](../../../library/contracts/PLATFORM-CURRENCY.md): recheck a citation older than 30 days before a decision depends on it. Citations were checked on 2026-10-04.

## Three uses, five kinds of access

Separate the use before choosing a control. Content Signals name the three uses (first-party: https://contentsignals.org/, checked 2026-10-04):

- **search**: building a search index and returning links and short excerpts. It excludes AI-generated search summaries.
- **ai-input**: putting content into a model at answer time, such as retrieval or grounding for an AI answer.
- **ai-train**: training or fine-tuning a model.

Then identify which kind of access is involved:

| Access | Examples | What controls it |
|---|---|---|
| Search crawler | Googlebot, Bingbot, Applebot | Search-engine robots rules and page directives. Blocking it removes ordinary search visibility. |
| Mixed-use crawler | Googlebot, Bingbot and Applebot, which Cloudflare classifies as serving both search and training | A separate training token or setting where the vendor offers one. Never block the crawler itself to stop training. |
| AI search crawler | OAI-SearchBot, Claude-SearchBot, PerplexityBot | Its own robots.txt group. Blocking it can remove the site from that assistant's answers and citations. |
| Training crawler or token | GPTBot, ClaudeBot, CCBot, Google-Extended, Applebot-Extended | Its own robots.txt group. A token such as Google-Extended or Applebot-Extended only states a use preference; it is not a separate crawler. |
| User-triggered fetcher | ChatGPT-User, Claude-User, Perplexity-User | Vendor-specific. Some vendors say robots.txt may not apply to these. |

## Vendor controls (documented)

- **Google.** Google-Extended controls whether crawled content is used to train Gemini models and to ground Gemini Apps and Vertex AI. Google says it "does not impact a site's inclusion in Google Search nor is it used as a ranking signal" (first-party: https://developers.google.com/crawling/docs/crawlers-fetchers/google-common-crawlers, checked 2026-10-04). For AI features in Search, Google names `nosnippet`, `data-nosnippet`, `max-snippet` and `noindex`, with Googlebot robots rules as the crawl control (first-party: https://developers.google.com/search/docs/appearance/ai-features, checked 2026-10-04). A Search Console setting (Settings > Search generative AI) excludes a site from AI Overviews, AI Mode and Discover generative features. Google says it rolled out to all sites by 2026-08-31, is not a ranking or inclusion signal for the rest of Search, and does not affect training (first-party: https://support.google.com/webmasters/answer/16908024, checked 2026-10-04).
- **OpenAI.** OAI-SearchBot is for search. Disallowing GPTBot signals that content should not be used to train foundation models. For ChatGPT-User, OpenAI says "robots.txt rules may not apply" because a user starts the fetch (first-party: https://developers.openai.com/api/docs/bots, checked 2026-10-04).
- **Anthropic.** Blocking ClaudeBot signals exclusion from future training data. Blocking Claude-User stops retrieval in response to a user's query, and Anthropic says its bots honor robots.txt (first-party: https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler, checked 2026-10-04).
- **Apple.** Applebot-Extended does not crawl. Pages that disallow it can still appear in search results, and its rules are not used in Search ranking (first-party: https://support.apple.com/en-us/119829, checked 2026-10-04).
- **Perplexity.** PerplexityBot surfaces and links sites in Perplexity search and is not used for foundation-model training. Perplexity-User "generally ignores robots.txt rules" because a user requested the fetch (first-party: https://docs.perplexity.ai/docs/resources/perplexity-crawlers, checked 2026-10-04).
- **Common Crawl.** The robots.txt token is `CCBot` (first-party: https://commoncrawl.org/faq, checked 2026-10-04).
- **Microsoft Bing.** The last first-party statement found is from 2023 and names Bing Chat: content tagged `NOARCHIVE` is left out of Bing Chat answers and is not used to train Microsoft's foundation models, while `NOCACHE` and `NOARCHIVE` content still appears in search results (first-party: https://blogs.bing.com/webmaster/september-2023/Announcing-new-options-for-webmasters-to-control-usage-of-their-content-in-Bing-Chat, checked 2026-10-04). Whether this applies to Copilot today is unverified. Check Bing Webmaster documentation before relying on it.

## CDN and network controls

robots.txt and Content-Signal state preferences that compliant crawlers honor. They identify no one and stop nothing. Enforcement happens at the network edge, where the provider identifies the crawler. Check the site's CDN before recommending any change, because a CDN setting can override what the site's own robots.txt says.

For Cloudflare, the company's own announcement is ahead of its developer documentation as of 2026-10-04. The documentation still describes the earlier settings, so record both when advising (first-party: https://blog.cloudflare.com/accountable-mixed-use-ai-crawlers/, checked 2026-10-04):

- From 2026-09-15, Training can be set to Allow, Disallow AI Training, Block on pages with ads, or Block, on all plans. Disallow AI Training publishes a no-training rule in robots.txt, keeps Googlebot, Bingbot and Applebot crawling for search, and blocks other training crawlers.
- **Block and Block on pages with ads now apply to Googlebot, Bingbot and Applebot, so either setting affects search as well as training.** A site that chooses Block to stop training can lose ordinary search traffic.
- "Block AI Bots" and managed robots.txt are being deprecated in favor of the Search, Training and Agent controls and Bot Preference Sync. Domains added from 2026-09-15 are offered presets based on whether the site earns advertising revenue.
- Markdown for Agents returns Markdown to requests that send `Accept: text/markdown`. It is available on Pro, Business and Enterprise plans, and it adds `Content-Signal: ai-train=yes, search=yes, ai-input=yes` when the origin sends no `content-signal` header (first-party: https://developers.cloudflare.com/fundamentals/reference/markdown-for-agents/, checked 2026-10-04). That default grants all three uses unless the site states otherwise.
- Pay Per Crawl is in closed beta (first-party: https://developers.cloudflare.com/ai-crawl-control/features/pay-per-crawl/what-is-pay-per-crawl/, checked 2026-10-04). Pay Per Use is described as a beta in a 2026-09-30 announcement with no documentation page. Treat both as availability to confirm, not options to plan around.

For any other CDN or host, verify its bot controls in its own documentation. Do not assume Cloudflare's behavior applies elsewhere.

## Decide by business outcome

1. Name the primary business outcome and how the site earns from a visit: advertising seen by people, leads, purchases, subscriptions, or authority and citation.
2. For each use (search, ai-input, ai-train) and each access type above, state what the business gains and loses. An ad-funded publisher loses revenue when an answer replaces a visit. A lead-generation or software business may gain from being cited in answers.
3. Choose the narrowest control that expresses the decision: a training token or setting rather than blocking a search crawler, and a page directive rather than a site-wide rule where only some pages differ.
4. Check the live robots.txt, the CDN's bot settings and the page directives together. Any one of them can contradict the others.
5. Treat every change to robots.txt, a CDN setting, a page directive or a Search Console control as a live change: exact scope, expected effect, downside, stop condition and rollback, with the owner's approval.

## Diagnosing a visibility loss

Add CDN bot-control and managed robots.txt changes to the technical-regression check in [Ranking change diagnosis](ranking-change-diagnosis.md). The provider may change a default or a setting's meaning without any deploy by the site, as happened on Cloudflare on 2026-09-15. Compare the live robots.txt, the CDN's security events for search crawlers and search-console crawl statistics around the date. A matching date is a hypothesis to confirm, not a cause.

## Measuring AI-search visibility

- Citation rate, mention rate, share of voice and similar AI-visibility metrics come from sampled prompts run by a tool. They estimate visibility for those prompts. They are not traffic, conversions or revenue.
- Measure the business outcome from AI-assistant referrals in analytics and the business's own conversion records, with the referral definition stated. An answer read without a click produces no referral, so referrals can undercount influence. Do not fill that gap with an assumed multiplier.
- Do not invent a conversion rate or benchmark for AI-search traffic. A vendor's published figure is vendor evidence for that vendor's sample, not a target for this business.

## Agent readiness

Agent-readiness checks (robots.txt, sitemap, Markdown negotiation, `llms.txt`, Content Signals, API catalog, MCP server card, agent skills index and similar) test whether a site follows emerging standards. A readiness score is a standards checklist. It is not evidence of ranking, citation or revenue. Prioritize by what the business offers: a content site needs crawlable pages and readable Markdown, and a product with an API or MCP server benefits from machine-readable discovery. No search engine's first-party documentation reviewed for this reference describes `llms.txt` as a ranking or citation input; treat any such claim as unverified until the engine documents it.

## Rules

- Never block a mixed-use search crawler to stop training while the business wants search traffic. Use the vendor's training token or a no-training setting.
- Do not describe robots.txt or Content-Signal as enforcement, or promise that content will not be used.
- Do not assume a user-triggered fetcher obeys robots.txt. Vendors differ; cite the vendor.
- Do not present an AI-visibility metric or a readiness score as a business outcome or as proof that a change worked.
- Do not change robots.txt, CDN bot settings, page directives or Search Console controls without explicit approval, and verify the live result after any approved change.
- Label any current claim about these controls that was not checked against the vendor's own documentation as unverified, and name the check still needed.
