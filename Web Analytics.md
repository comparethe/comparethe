# Web Analytics

Tools that count visitors and pageviews on your website, compared for a small team that launches many small sites with AI agents.

## Our pick

**[Umami](https://umami.is) Cloud Pro, $20 a month.** It is hosted, so there is nothing to run. One API key lets an agent read stats and create sites, it has an official MCP server, it sets no cookies (so no consent banner), and [Flowershow](https://flowershow.app) supports it natively.

- **Free alternative:** Google Analytics 4 costs nothing, but it needs a cookie banner for EU and UK visitors, Google Cloud set-up for each account, and its MCP server is experimental. It wins on price only.
- **More than 20 sites:** self-host Umami (about $10 a month on Railway, plus your own upgrades and backups), since Pro caps at 20 sites.

## What we compared on

Scale assumed: about 15 sites, 150k pageviews a month, most of them on one site.

1. **Price** per month at that scale.
2. **Hassle**: setup, upkeep (upgrades, backups, uptime), and the steps to add a site. If you have little time, an hour of upkeep a quarter costs more than a $10 a month saving.
3. **Agent ease** (the key criterion): how many steps to give an AI agent access, whether there is a long-lived key, whether the API can both read stats and create sites, and whether there is an official MCP server.
4. Secondary: is a **cookie banner** needed, and is there **native support** in your site builder (here, Flowershow supports GA4 and Umami)?

## Comparison

✅ good · 🟡 OK · ❌ poor · ❓ not confirmed

| Tool | Price / month | Hassle | Agent ease (key) | Cookie banner | Flowershow |
|---|---|---|---|---|---|
| **Umami Cloud Pro** | 🟡 $20 (1M events, 20 sites) | ✅ Nothing to run; new site = 1 API call | ✅ 1 key; read + create API; official remote MCP | ✅ None | ✅ Native |
| Umami self-hosted (Railway) | ✅ ~$10 (estimate) | ❌ You run upgrades, backups, uptime | ✅ Same API and MCP (enable a flag) | ✅ None | ✅ Native |
| Google Analytics 4 | ✅ $0 | 🟡 New property per site; one Google account per org | 🟡 6–8 setup steps per account; MCP local, experimental | ❌ Needed in EU/UK | ✅ Native |
| PostHog | ✅ $0 to 1M events | 🟡 Heavier script; 1 free project | ✅ Scoped key; official remote MCP with SQL | ❓ Cookies by default; cookieless option | 🟡 Script tag |
| Fathom | ❌ $25 (200k pageviews) | ✅ Nothing to run | 🟡 Scoped key; community MCP only | ✅ None | 🟡 Script tag |
| GoatCounter | ✅ $0 (fair use) | ✅ Nothing to run | 🟡 Key, REST, CSV export; community MCP | ❓ | 🟡 Script tag |
| Plausible Cloud | ❌ Quote for >10 sites | ✅ Nothing to run | 🟡 API only on Business plan; community MCP | ✅ None | 🟡 Script tag |
| Cloudflare Web Analytics | ✅ $0 | ✅ Auto on proxied sites; 10-site default cap | ❌ 8–10 step token; sampled data; analytics MCP deprecated | ❓ | 🟡 Beacon tag |
| Matomo | ❌ Cloud from $29 | ❌ Self-host is PHP + MySQL | 🟡 Token API; official MCP in preview | 🟡 Cookieless setting | 🟡 Script tag |
| Pirsch | ❓ $6 for 10k pageviews; 200k not shown | ✅ Nothing to run | 🟡 REST API; community MCP | ✅ None | 🟡 Script tag |

## If you're different

- **One site:** Umami Cloud Hobby (free, 1 site, no API) or GoatCounter (free).
- **Price above all:** GA4 or GoatCounter, both $0.
- **Need product analytics** (funnels, feature flags, session replay): PostHog. The rest here are traffic stats.
- **No ops, up to 50 sites, no API needs:** Fathom, $25 a month.

## Does GA4 still need a cookie banner?

Yes, for EU and UK visitors. GA4 sets `_ga` cookies. In the EU, Google's Consent Mode still sends pings with device data when consent is refused, and no regulator says that removes the need for a banner. The UK's Data (Use and Access) Act 2025 added an exemption for analytics cookies, but only where the provider acts purely for you and does not use the data for its own purposes; default GA4 is unlikely to qualify. France's CNIL exemption effectively excludes GA. Umami sets no cookies. Not legal advice.

Sources: [Google Analytics cookie usage](https://support.google.com/analytics/answer/11397207), [consent mode](https://support.google.com/analytics/answer/9976101), [ICO exceptions](https://ico.org.uk/for-organisations/direct-marketing-and-privacy-and-electronic-communications/guidance-on-the-use-of-storage-and-access-technologies/what-are-the-exceptions/), [CNIL sheet 16](https://www.cnil.fr/en/sheet-ndeg16-use-analytics-your-websites-and-applications).

## Checked 17 Oct 2026

Sources: [Umami pricing](https://umami.is/pricing), [Umami docs](https://docs.umami.is) (FAQ, API auth, MCP), [Railway pricing](https://railway.com/pricing), [PostHog pricing](https://posthog.com/pricing) and [MCP](https://posthog.com/docs/model-context-protocol), [Google Analytics MCP](https://github.com/googleanalytics/google-analytics-mcp), [Fathom](https://usefathom.com/pricing), [GoatCounter](https://www.goatcounter.com/help/api), [Plausible](https://plausible.io/docs/stats-api), [Cloudflare Web Analytics](https://developers.cloudflare.com/web-analytics/) and [MCP servers](https://github.com/cloudflare/mcp-server-cloudflare), [Matomo](https://matomo.org/pricing/) and its [MCP plugin](https://plugins.matomo.org/McpServer), [Pirsch](https://pirsch.io/pricing) and its [MCP](https://docs.pirsch.io/integrations/mcp). The Railway figure is an estimate from published rates, not a measured bill.
