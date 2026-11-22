# MKT Skills for Claude

MKT Skills packages 31 evidence-led marketing specialists for Claude, Cowork and Claude Code. Use them to plan campaigns, review creative and copy, diagnose conversion problems, and prepare measurement or reporting plans. The skills distinguish supplied evidence from assumptions and do not treat recommendations as completed changes.

## Install in Claude Code

No GitHub access is needed. On Claude Code 2.1.275 or later, install in one step:

```text
/plugin install mkt-skills --marketplace https://mktskills.com/marketplace.json
```

On 2.1.224 or later, add the marketplace, then install:

```text
/plugin marketplace add https://mktskills.com/marketplace.json
/plugin install mkt-skills@mkt-skills
```

The marketplace pins the plugin ZIP's SHA-256, so Claude Code refuses a download that has been changed.

## Marketing system plugins

The marketplace (`https://mktskills.com/marketplace.json`, as well as the repository's `.claude-plugin/marketplace.json`) additionally lists the nine plugins from the Complete Marketing System: `mkt-core` (the `00-router` diagnosis router) and `mkt-q1-audience` to `mkt-q8-run`, one per question, served publicly as `/plugin/<name>.zip`:

```text
/plugin marketplace add https://mktskills.com/marketplace.json
/plugin install mkt-core@mkt-skills
/plugin install mkt-q2-offer@mkt-skills
```

Or with repository access: `claude plugin marketplace add vinceservidad/marketing-skills`. Enable `mkt-core` plus the one or two question plugins the task needs, and keep 40 skills or fewer enabled. Installed as plugins, skills are invoked as `/mkt-q2-offer:07-offer-design`. `00-router` plus all 128 of 128 catalog skills exist and pass live Claude Code `--plugin-dir` behavioural evals and trigger checks (`marketing-system/tests/validate.py` exits `0` with `0` failures). See [`marketing-system/README.md`](https://mktskills.com/support).

## Install the ZIP in Claude, Desktop or Cowork

Download <https://mktskills.com/plugin/mkt-skills.zip>. In Claude, open **Customize > Plugins > Add > Upload plugin** and select it. Open a new conversation and ask which MKT Skills are available. Plugins are available on paid Claude plans, and organization settings can limit them. This direct upload is not an Anthropic directory approval.

For a local Claude Code test, extract the ZIP and run:

```sh
claude plugin validate --strict ./mkt-skills
claude --plugin-dir ./mkt-skills
```

Try `/mkt-skills:marketing-router` or ask: “Review this campaign brief and identify the evidence we need before making a recommendation.”

## Optional account connection

The skills work with context you supply without a connected marketing account. The bundled remote connector points to `https://mktskills.com/mcp`. In Claude or Cowork, open the plugin's Connectors tab to connect it. In Claude Code, use `/mcp` to inspect its state and authorize it. Sign in to MKT Skills with your own account; configure available account connections at <https://mktskills.com/settings>.

The connector is read-only. Access is limited to authorized retained report files and connected, selected Google Ads accounts. Installing this package does not grant account access, select an advertising account, or transfer files attached to a Claude conversation into MKT Skills. Missing authorization or data must be reported, not invented. Do not paste credentials into chats or package files.

## Scope and limitations

No website chat or business dashboard is included. There are no hooks, agents, executable installers, bundled credentials or local MCP processes. This package does not change campaigns, budgets, products, orders or live pages. It is not the Shopify VA development preview.

The source skills and this package are MIT-licensed. A distributable source ZIP and a public directory listing are separate from the visibility of the development repository. Do not assume a private repository URL is anonymously installable.

## Build and verify

From the development repository, run `python3 scripts/build-claude-plugin.py --output /absolute/path/mkt-skills-claude.zip`. The site build runs the same builder and publishes `/plugin/mkt-skills.zip` alongside the nine system plugins (`/plugin/mkt-core.zip` through `/plugin/mkt-q8-run.zip`), with `/marketplace.json` pinning each archive's digest. The builder first checks that generated skills match their canonical source, then packages only the portable skills, this guide, the MIT license, logo and Claude configuration. The existing Git marketplace remains available to users with repository access.

Product and setup: <https://mktskills.com/>. Support: hi@mktskills.com.
