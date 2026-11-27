# Marketing Skills (Claude Plugin)

Marketing Skills gives Claude, Cowork, and Claude Code 133 evidence-led marketing skills: a marketing router (`00-router`) plus 132 skills across 20 sections covering market research, customer research, positioning, offers, copywriting, creative strategy, paid ads, shopping feeds, local SEO, marketplaces, WhatsApp, funnels, CRO, sales, retention, referrals, measurement, experimentation, growth, and operations. The skills ask for your own data, label what is observed versus assumed, and do not invent benchmarks or results.

**Published by Vince Servidad ([mktskills.com](https://mktskills.com)). Independent of Anthropic: this is not Anthropic's own marketing plugin, and Anthropic does not endorse or certify it.** The plugin id `mkt-skills` is kept for compatibility.

## Install

```text
/plugin install mkt-skills --marketplace https://mktskills.com/marketplace.json
```

(Claude Code 2.1.275 or later.) In Claude and Cowork, install it from the plugin directory once listed.

## Example prompts

- "Leads are coming in but few buy. Which marketing area should I look at first?" (the router diagnoses and names the owning skill)
- "Review this Meta Ads export and tell me what I can and cannot conclude from it."
- "Draft three positioning statements for my product from the customer notes in this folder."

## What the plugin contains and runs

- `skills/`: 133 text-only skills (Markdown). They run no code, install nothing, and call no tools or connectors of their own.
- `.mcp.json`: one optional remote MCP server, described below.
- No hooks, agents, local processes, bundled credentials, or executables.

## Network use: the optional connector

The only network destination is `https://mktskills.com/mcp` (HTTPS, operated by the publisher, Marketing Skills). Installing the plugin does not send anything there; Claude contacts it only when the connector is enabled and a task uses one of its tools.

- **What it does:** serves the Marketing Skills methods and reference documents, and runs deterministic calculations and reviews on figures you supply.
- **Read-only:** it has no write tools and never changes campaigns, budgets, products, orders, or pages.
- **Data it can read:** (1) text you or Claude pass to its tools, for example campaign rows for a review (these are processed to return the result and are not saved); (2) report files you have already imported into your Marketing Skills workspace; (3) Google Ads accounts you connect and select at mktskills.com, read only after you approve the `ads.read` permission. Other reporting sources (Google Analytics 4, Search Console, Meta Ads, Shopify) are available only when enabled and selected by you. Files attached in a Claude conversation are not uploaded automatically.
- **Sign-in:** OAuth 2.0 with PKCE at mktskills.com; you can review and revoke access any time at <https://mktskills.com/settings>. A no-login link, `https://mktskills.com/mcp/marketing-skills`, offers the methods and review tools without an account.
- **Privacy policy:** <https://mktskills.com/privacy>. Terms: <https://mktskills.com/terms>.

The skills work without the connector.

## Support and contact

Email <hi@mktskills.com> (support and security reports) or see <https://mktskills.com/support>. Source and releases: <https://github.com/vinceservidad/mkt-skills-plugin>.

## No advertising

The plugin contains no ads, sponsored content, affiliate links, or paid placements.

## Full Skills Repository

For CLI install (`npx skills add vinceservidad/marketingskills`), Cursor, Codex, and Antigravity, see <https://github.com/vinceservidad/marketingskills>.

## License

MIT. See [LICENSE](./LICENSE).
