# AI search and GEO: decision rules

## Three uses, five kinds of access

Separate the use before choosing any control:

- **Search:** building a search index and returning links and short excerpts.
- **AI input (answer time):** fetching or retrieving content to ground an AI answer.
- **AI training:** using content to train or fine-tune a model.

| Access | What it is | What blocking it can cost |
| --- | --- | --- |
| Search crawler | The main crawler of a search engine | Ordinary search visibility, and AI features built on that index |
| Mixed-use crawler | A search crawler whose data the vendor also uses for AI | Search visibility; use the vendor's separate training token or setting instead |
| AI search crawler | A vendor's crawler for its assistant's search and citations | Appearing and being cited in that assistant's answers |
| Training crawler or token | A crawler or robots token that states a training preference | Usually nothing in answers, if the vendor keeps it separate (verify per vendor) |
| User-triggered fetcher | A fetch made because a user asked the assistant to open a page | Vendor-specific; some vendors say robots.txt may not apply |

## Vendor facts: always verify

Crawler names, what each one is used for, and whether robots.txt applies are vendor statements that change. This library last recorded the following from first-party pages on 2026-10-04. They are leads to check, not facts to state: in the plan, write each as *to confirm* with the URL to check, unless it was consulted during this run (then cite the URL and the date checked).

| Vendor | Recorded statement (2026-10-04) | Page to check |
| --- | --- | --- |
| OpenAI | OAI-SearchBot is for search; disallowing GPTBot signals content should not be used to train foundation models; for ChatGPT-User robots.txt rules may not apply | https://developers.openai.com/api/docs/bots |
| Google | Google-Extended controls use for Gemini training and grounding and does not affect inclusion in Google Search; AI features in Search follow Googlebot rules and snippet directives | https://developers.google.com/crawling/docs/crawlers-fetchers/google-common-crawlers and https://developers.google.com/search/docs/appearance/ai-features |
| Anthropic | ClaudeBot relates to training; Claude-User to retrieval for a user's query; Claude-SearchBot to search | https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler |
| Perplexity | PerplexityBot surfaces and links sites in Perplexity search; Perplexity-User may ignore robots.txt because a user requested the fetch | https://docs.perplexity.ai/docs/resources/perplexity-crawlers |
| Apple | Applebot-Extended states a training preference and does not crawl | https://support.apple.com/en-us/119829 |
| Common Crawl | The robots token is CCBot | https://commoncrawl.org/faq |

A CDN or website builder can add its own bot rules or override robots.txt. Check its settings (or mark them unknown) before recommending a change; never assume one provider's behaviour applies to another.

## Deciding access by business outcome

1. How does the business earn from a visit or a mention? A lead-generation or service business usually gains from being cited; an ad-funded publisher can lose when an answer replaces a visit.
2. For each use and access type, what is gained and lost?
3. Choose the narrowest control: a training token or setting rather than blocking a search crawler; a page directive rather than a site-wide rule.
4. Check robots.txt, CDN settings and page directives together; any one can contradict the others.
5. Every change is live: scope, expected effect, downside, stop condition, rollback, owner's approval, and a check of the live result afterwards.

## Baseline protocol

- 10 to 20 prompts from the buyer's own questions; keep wording fixed between runs.
- Record: date, assistant and mode (with or without web search), logged in or out, location, runs per prompt, the companies named, the sources cited, and whether the business appears and how it is described.
- A single run is a snapshot. Answers vary by user, time, place and wording; repeat runs before reading a change as real.
- Tally per prompt and per assistant; never summarise a share without the denominator.

## What makes a page citable (heuristics, not guarantees)

- It answers one question directly in the first lines, in the buyer's words, then gives detail.
- It states specific, checkable facts the business can stand behind (prices, timelines, who it is for, what it does not do), each traceable to context or `inputs/`.
- It is crawlable, indexable and consistent with how the business is described elsewhere.
- Original data, worked examples and clear comparisons are more useful to cite than generic advice.

Label all of these heuristics. No vendor has documented a recipe for being cited; do not present one as known.

## Third-party corroboration

Assistants often cite review sites, lists, forums, publications and podcasts. The legitimate routes: request listings on the lists buyers actually use, earn coverage, ask real customers for reviews without incentives that platforms prohibit, appear on partners' and podcasts' pages, and take part in communities openly as the company. Never write reviews, post as a fake customer, pay for placement presented as editorial, or offer undisclosed incentives.

## Measurement

- Outcome: sessions referred by assistant domains and what they convert to, from analytics and the CRM, with the referral definition stated.
- Visibility: the prompt-set tally on a fixed cadence. It estimates visibility for those prompts only.
- Never infer unseen influence with a multiplier, and never use a vendor's or tool's published AI-traffic conversion figure as a target for this business.

## Emerging standards

`llms.txt`, Markdown negotiation, content-signal headers and agent-readiness scores check whether a site follows emerging conventions. As recorded on 2026-10-04, no major engine's first-party documentation describes `llms.txt` as a ranking or citation input; treat any such claim as unverified until an engine documents it.
