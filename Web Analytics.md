# Web Analytics

Tools that count visitors and pageviews on your website, compared for a small team that launches many small sites (dozens, growing) and wants AI agents to do the analytics work.

## Our pick

**[Umami](https://umami.is).** One API key lets an agent read stats and create sites. It has an official MCP server, sets no cookies (so no consent banner), and [Flowershow](https://flowershow.app) supports it natively.

- **Dozens of sites:** self-host it on [Railway](https://railway.com), for about $10 a month. Railway automates updates and backups (see the fine print).
- **Up to 20 sites, nothing to run:** Umami Cloud Pro, $20 a month. The next plan up is $200.
- **Free:** Google Analytics 4. It costs $0 at any scale, but it needs a cookie banner in the EU and UK and more set-up for agents. See the bake-off below.

## What we compared on

1. **Price** per month at our scale: dozens of sites, about 150k pageviews a month, most of them on one site.
2. **Hassle**: setup, upkeep (upgrades, backups, uptime), and the steps to add a site. If you have little time, an hour of upkeep a quarter costs more than a $10 a month saving.
3. **Agent ease** (the key criterion): how many steps to give an AI agent access, whether there is a long-lived key, whether the API can both read stats and create sites, and whether there is an official MCP server.
4. Secondary: is a **cookie banner** needed, and is there **native support** in your site builder (here, Flowershow supports GA4 and Umami)?

## Bake-off: Umami vs Google Analytics 4

| | Umami | Google Analytics 4 |
|---|---|---|
| **Price, up to 20 sites** | $20/mo (Cloud Pro), or ~$10 self-hosted | $0 |
| **Price, dozens of sites** | ~$10/mo self-hosted on Railway, or $200/mo Cloud Business | $0 |
| **Hassle** | Cloud: none. Self-hosted: mostly automated (updates, backups); major upgrades are yours | None to run. New site = new property and stream |
| **Agent access** | One API key, about 4 clicks, never expires | Google Cloud project, APIs enabled, OAuth login per Google account (6–8 steps each); tokens can expire |
| **Agent can add a site** | Yes, one API call with the same key | Yes via the Admin API, but it needs an edit scope |
| **MCP server** | Official; remote (Cloud) or built in (self-hosted); read-only | Official, local, labelled experimental, read-only, one Google account per server |
| **Cookie banner (EU/UK)** | Not needed (no cookies) | Needed |
| **Counts everyone?** | Yes | No: visitors who decline are undercounted, partly modelled |
| **Depth** | Traffic, referrers, UTMs, events, funnels, goals, retention | All that, plus Search Console and Ads links, demographics, modelling |
| **Data and lock-in** | Open source (MIT); export; move Cloud ↔ self-hosted by changing the script URL | Google's. Standard reports keep aggregates; explorations and user-level data last 2 or 14 months |

**Deciding factor: no banner and easier agent access, against $0.** If price comes first and you will add a banner, choose GA4. If you want every visitor counted, no banner and one-key agent access, choose Umami.

## All options

✅ good · 🟡 OK · ❌ poor · ❓ not confirmed

| Tool | Price / month | Hassle | Agent ease (key) | Cookie banner | Flowershow |
|---|---|---|---|---|---|
| **Umami self-hosted (Railway)** | ✅ ~$10 (estimate) | 🟡 Updates and backups automated; major upgrades yours | ✅ 1 key; read + create API; official MCP | ✅ None | ✅ Native |
| Umami Cloud Pro | 🟡 $20 to 20 sites; $200 unlimited | ✅ Nothing to run | ✅ Same, MCP remote | ✅ None | ✅ Native |
| Google Analytics 4 | ✅ $0 | 🟡 Property per site; account per org | 🟡 6–8 steps per account; MCP experimental | ❌ Needed in EU/UK | ✅ Native |
| PostHog | ✅ $0 to 1M events | 🟡 Heavier script; 1 free project | ✅ Scoped key; official remote MCP with SQL | ❓ Cookies by default | 🟡 Script tag |
| Fathom | ❌ $25 (200k pageviews) | ✅ Nothing to run | 🟡 Scoped key; community MCP | ✅ None | 🟡 Script tag |
| GoatCounter | ✅ $0 (fair use) | ✅ Nothing to run | 🟡 Key, REST, CSV export; community MCP | ❓ | 🟡 Script tag |
| Plausible Cloud | ❌ Quote for >10 sites | ✅ Nothing to run | 🟡 API on Business plan only; community MCP | ✅ None | 🟡 Script tag |
| Cloudflare Web Analytics | ✅ $0 | ❌ 6 months max; no events, no UTMs | ❌ 8–10 step token; sampled | ❓ | 🟡 Beacon tag |
| Matomo | ❌ Cloud from $29 | ❌ Self-host is PHP + MySQL | 🟡 Token API; official MCP in preview | 🟡 Cookieless setting | 🟡 Script tag |
| Pirsch | ❓ $6 for 10k; 200k not shown | ✅ Nothing to run | 🟡 REST API; community MCP | ✅ None | 🟡 Script tag |

### Fine print

- **Umami self-hosted on Railway:**
  - The ~$10 is our estimate from Railway's rates, not a measured bill. Railway Hobby is $5 a month including $5 of usage; RAM is about $10/GB, and Umami plus Postgres is about 1 GB.
  - Deploy: a one-click [template](https://railway.com/deploy/umami) (Umami + Postgres, 4,000+ deploys). There is also a GraphQL [public API](https://docs.railway.com/guides/public-api) with workspace- and project-scoped tokens, and a CLI, so an agent can run it.
  - Updates: [image auto-updates](https://docs.railway.com/deployments/image-auto-updates) per service, patch-only or minor too; forum threads report occasional misses.
  - Backups: [scheduled](https://docs.railway.com/reference/backups) daily, weekly or monthly, kept 6, 27 and 89 days.
  - Yours: major upgrades, an occasional restore test, an uptime check.
  - The MCP server is built in from Umami v3.4; turn it on with `MCP_ENABLED=1`.
- **Umami Cloud:** Hobby is free but allows 1 site and no API. Pro is $20 for 1M events and 20 sites, with $0.00003 per extra event. Business is $200 for 10M events and unlimited sites. Collection isn't cut off when you go over.
- **GA4:**
  - Agents need a Google Cloud project, the Admin and Data APIs enabled, and an OAuth or service-account login per Google account. Data API quota is 200k tokens per property per day.
  - The [official MCP](https://github.com/googleanalytics/google-analytics-mcp) runs locally, is labelled experimental, and serves one Google account per instance. It can run arbitrary reports but cannot create properties.
- **PostHog:** 1M events free, and pageviews count as events. The free plan has 1 project; more need a card. The [MCP](https://posthog.com/docs/model-context-protocol) is remote, can read and write, and has a read-only mode. It is built for product analytics (funnels, flags, replay).
- **Cloudflare Web Analytics:**
  - Free on all plans, but not analytics over time. The dashboard shows only the last 6 months. Unsampled data is kept 7 days, then aggregated to about 10%. Queries are sampled dynamically.
  - No custom events, and query strings are dropped, so no UTMs ([FAQ](https://developers.cloudflare.com/web-analytics/faq/)).
  - 10 sites per account by default (raise it via support). Its GraphQL and analytics MCP servers are deprecated in favour of a general Cloudflare API MCP.
  - Good as a zero-install traffic check on proxied sites.
- **Plausible:** cloud plans cover up to 10 sites below Enterprise, and the Stats API is Business plan only. The self-hosted Community Edition (AGPL) needs Postgres plus ClickHouse and at least 2 GB RAM, and has no sites API.
- **GoatCounter:** free hosted "for reasonable public usage", supported by donations. The API takes a Bearer key at 4 requests a second and offers CSV export. It can self-host as a single binary with SQLite.
- **Fathom:** $15 covers 100k pageviews and $25 covers 200k, with 50 sites included; extra sites are $10 per 50. The API is on all plans, and the key can be read-only or site-scoped.
- **Matomo:** the Cloud price for 300k hits isn't shown. On-premise is free (GPL) but needs PHP and MySQL. Its [MCP plugin](https://plugins.matomo.org/McpServer) is an early preview.
- **Pirsch:** $6 for 10k pageviews with 50 sites; the price at 200k isn't shown. The MCP is [community-maintained](https://docs.pirsch.io/integrations/mcp).

## Does GA4 still need a cookie banner?

Yes, for EU and UK visitors. GA4 sets `_ga` cookies. In the EU, Google's Consent Mode still sends pings with device data when consent is refused, and no regulator says that removes the need for a banner. The UK's Data (Use and Access) Act 2025 added an exemption for analytics cookies, but only where the provider acts purely for you and does not use the data for its own purposes; default GA4 is unlikely to qualify. France's CNIL exemption effectively excludes GA. Umami sets no cookies. Not legal advice.

Sources: [Google Analytics cookie usage](https://support.google.com/analytics/answer/11397207), [consent mode](https://support.google.com/analytics/answer/9976101), [ICO exceptions](https://ico.org.uk/for-organisations/direct-marketing-and-privacy-and-electronic-communications/guidance-on-the-use-of-storage-and-access-technologies/what-are-the-exceptions/), [CNIL sheet 16](https://www.cnil.fr/en/sheet-ndeg16-use-analytics-your-websites-and-applications).

## Checked 17 Oct 2026

Sources: [Umami pricing](https://umami.is/pricing), [Umami docs](https://docs.umami.is) (FAQ, API auth, MCP), [Railway pricing](https://railway.com/pricing), [PostHog pricing](https://posthog.com/pricing), [Fathom](https://usefathom.com/pricing), [GoatCounter](https://www.goatcounter.com/help/api), [Plausible](https://plausible.io/docs/stats-api), [Cloudflare Web Analytics](https://developers.cloudflare.com/web-analytics/) and [MCP servers](https://github.com/cloudflare/mcp-server-cloudflare), [Matomo](https://matomo.org/pricing/), [Pirsch](https://pirsch.io/pricing), plus the links in the fine print.
