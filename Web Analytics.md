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
4. **Features**, scored 1–5: how many of the features below it covers well. The reason for each score is in the fine print.
5. Secondary: is a **cookie banner** needed, and is there **native support** in your site builder (here, Flowershow supports GA4 and Umami)?

### Key analytics features

| Feature | What it tells you |
|---|---|
| Visitors and pageviews | How many people came, and to which pages |
| Sources and referrers | Where they came from: search, social, other sites |
| UTM campaigns | Which tagged link or post brought them |
| Custom events and goals | Sign-ups, clicks, downloads: the things that count as success |
| Funnels | Where people drop out of a multi-step path |
| Retention and cohorts | Whether people come back |
| Real-time | Who is on the site now, for example during a launch |
| Search Console link | Search queries and impressions next to visits |
| Session replay and heatmaps | Where people click and scroll, per visit |
| Product analytics | Feature flags, experiments, per-user paths inside an app |
| Export and SQL | Raw data out, so an agent can ask anything |

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

## Bake-off: Umami vs Plausible

Both are privacy-first, cookieless and open source, and they look alike.

| | Umami | Plausible |
|---|---|---|
| **Hosted price, many sites** | $20 to 20 sites; $200 unlimited | $19 for up to 10 sites at the lowest tier; above 10 sites needs an Enterprise quote |
| **API** | On every paid plan; reads stats and creates sites | Stats API on Business only; site creation needs a separate Sites API key |
| **MCP server** | Official | Community only |
| **Self-host** | Node + Postgres, ~1 GB RAM, ~$10/mo; MIT | Postgres + ClickHouse, 2 GB+ RAM; AGPL; releases twice a year; no sites API |
| **Flowershow** | Native | Script tag |

**Deciding factor: agent access and cost at many sites.** Plausible's dashboard is a little more polished. But its API sits behind the Business plan, more than 10 sites needs a quote, and self-hosting it is heavier.

## Bake-off: Umami vs PostHog

| | Umami | PostHog |
|---|---|---|
| **Price** | ~$10 self-hosted, $20 Cloud | $0 to 1M events (pageviews count as events) |
| **Built for** | Traffic: pageviews, referrers, UTMs, simple events and funnels | Product analytics: funnels, feature flags, session replay, experiments |
| **Script and cookies** | Tiny script, no cookies | Heavier SDK, cookies by default (cookieless option) |
| **Many sites** | Unlimited self-hosted; 20 on Cloud Pro | 1 project free; more need a card |
| **MCP server** | Official, read-only | Official, remote, SQL, read/write |
| **Flowershow** | Native | Script tag |

**Deciding factor: what you need to learn.** For "is anyone coming, and from where?" across many content sites, Umami is lighter and needs no banner. For how people use an app, PostHog is far deeper and free to start. Many teams run both: Umami on the marketing sites, PostHog in the app.

## All options

✅ good · 🟡 OK · ❌ poor · ❓ not confirmed

| Tool | Price / month | Hassle | Agent ease (key) | Features (1–5) | Cookie banner | Flowershow |
|---|---|---|---|---|---|---|
| **Umami self-hosted (Railway)** | ✅ ~$10 (estimate) | 🟡 Updates and backups automated; major upgrades yours | ✅ 1 key; read + create API; official MCP | 4 | ✅ None | ✅ Native |
| Umami Cloud Pro | 🟡 $20 to 20 sites; $200 unlimited | ✅ Nothing to run | ✅ Same, MCP remote | 4 | ✅ None | ✅ Native |
| Google Analytics 4 | ✅ $0 | 🟡 Property per site; account per org | 🟡 6–8 steps per account; MCP experimental | 5 | ❌ Needed in EU/UK | ✅ Native |
| PostHog | ✅ $0 to 1M events | 🟡 Heavier script; 1 free project | ✅ Scoped key; official remote MCP with SQL | 5 | ❓ Cookies by default | 🟡 Script tag |
| Fathom | ❌ $25 (200k pageviews) | ✅ Nothing to run | 🟡 Scoped key; community MCP | 3 | ✅ None | 🟡 Script tag |
| GoatCounter | ✅ $0 (fair use) | ✅ Nothing to run | 🟡 Key, REST, CSV export; community MCP | 2 | ❓ | 🟡 Script tag |
| Plausible Cloud | ❌ Quote for >10 sites | ✅ Nothing to run | 🟡 API on Business plan only; community MCP | 4 | ✅ None | 🟡 Script tag |
| Cloudflare Web Analytics | ✅ $0 | ✅ Auto on proxied sites; 10-site cap | ❌ 8–10 step token; sampled | 1 | ❓ | 🟡 Beacon tag |
| Matomo | ❌ Cloud from $29 | ❌ Self-host is PHP + MySQL | 🟡 Token API; official MCP in preview | 5 | 🟡 Cookieless setting | 🟡 Script tag |
| Pirsch | ❓ $6 for 10k; 200k not shown | ✅ Nothing to run | 🟡 REST API; community MCP | 3 | ✅ None | 🟡 Script tag |

### Fine print

**Feature scores, briefly:**
- **GA4 5:** covers everything above except replay, and links to Search Console and Ads. Explorations are clunky.
- **PostHog 5:** product analytics, replay, flags, experiments and SQL. Basic web stats are a secondary view.
- **Matomo 5:** close to GA4, with heatmaps and replay as paid plugins.
- **Umami 4:** traffic, UTMs, events, goals, funnels, retention, journeys, attribution, revenue and Web Vitals. No Search Console link or replay.
- **Plausible 4:** traffic, UTMs, goals, funnels and a Search Console link. Funnels and revenue need the Business plan.
- **Fathom 3:** traffic, UTMs and events. No funnels or retention.
- **Pirsch 3:** traffic, UTMs, events and funnels. A small product.
- **GoatCounter 2:** pageviews, referrers and campaigns. Events only as fake paths.
- **Cloudflare 1:** pageviews, referrers and Web Vitals. The dashboard shows only the last 6 months, with no custom events and no UTMs.


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

## Can GA4 run without a cookie banner?

Mostly no, for EU and UK visitors. GA4 sets `_ga` cookies. Ways people try, from safest to riskiest (not legal advice):

| Route | How | Safe without a banner? |
|---|---|---|
| Audience outside the EU and UK | Turn Google signals and ad features off; honour opt-outs under US state laws | ✅ No federal US banner rule |
| UK statistics exemption (Data (Use and Access) Act 2025) | Turn off Google signals, data sharing and Ads links; accept Google's data processing terms; tell visitors and give a free opt-out | 🟡 Plausible but untested; the ICO doesn't name GA, and some commentators say GA4 can't qualify |
| Server-side only (Measurement Protocol, nothing stored in the browser) | Your server sends hits to GA4 | 🟡 Arguably outside the cookie rule, but you lose sessions and attribution, and GDPR still applies |
| Consent Mode v2 "advanced", defaulting to denied | No cookies; cookieless pings that Google models | ❌ The pings still read device data; the EU regulators' 2023 guidance covers tracking pixels too |
| Cookie-blocking hacks (random ID per page) | Unsupported workaround | ❌ Data still goes to Google; breaks visitor counts |
| France | GA isn't on the CNIL's exempt audience-measurement list | ❌ Consent needed |

So if you want no banner and EU visitors, use a cookieless tool such as Umami, Plausible or Fathom.

Sources: [Google Analytics cookie usage](https://support.google.com/analytics/answer/11397207), [consent mode](https://support.google.com/analytics/answer/9976101), [ICO exceptions](https://ico.org.uk/for-organisations/direct-marketing-and-privacy-and-electronic-communications/guidance-on-the-use-of-storage-and-access-technologies/what-are-the-exceptions/), [CNIL sheet 16](https://www.cnil.fr/en/sheet-ndeg16-use-analytics-your-websites-and-applications).

## Appendix: why does Google Analytics still use cookies and need a banner?

GA4 could count visitors without cookies. Google chooses not to, because GA4 is built to serve its ads business.

**How Umami counts without cookies.** It stores nothing in the browser. It builds a visitor ID by hashing data the browser sends anyway: IP address, browser details and the site, plus a secret value that it replaces periodically. That's enough to count unique visitors and sessions within that window. Once the secret changes, the same person looks new.

**Why GA4 doesn't do the same.** GA4 is designed around a long-lived visitor ID in a cookie, kept for up to 2 years, plus Google signals, which links visitors across devices for signed-in Google users. That persistent ID is what feeds:

- Ads conversion tracking and remarketing audiences, the main reason Google offers GA free;
- returning-user and retention reports per person over months;
- cross-device journeys and demographics.

A rotating hash would break all of these. Google's answer for people who refuse cookies is Consent Mode: send limited pings and estimate the missing visitors with a model.

**What you lose with Umami's approach:**

- **For content sites: little.** Visitors, pageviews, referrers, UTMs, events and funnels all work fine.
- **Real losses:** accurate "same person came back 3 months later" counts, cross-device tracking, demographics, and Ads audiences and attribution. None of these matter unless you run Google Ads or need long-term retention per person.

One caveat: Umami's approach still processes IP addresses. Most EU and UK guidance treats it as not needing a banner, but EU regulators' 2023 guidance on what counts as accessing a device is broad, so "no banner" is the common reading rather than a ruling.

## Checked 17 Oct 2026

Sources: [Umami pricing](https://umami.is/pricing), [Umami docs](https://docs.umami.is) (FAQ, API auth, MCP), [Railway pricing](https://railway.com/pricing), [PostHog pricing](https://posthog.com/pricing), [Fathom](https://usefathom.com/pricing), [GoatCounter](https://www.goatcounter.com/help/api), [Plausible](https://plausible.io/docs/stats-api), [Cloudflare Web Analytics](https://developers.cloudflare.com/web-analytics/) and [MCP servers](https://github.com/cloudflare/mcp-server-cloudflare), [Matomo](https://matomo.org/pricing/), [Pirsch](https://pirsch.io/pricing), plus the links in the fine print.
