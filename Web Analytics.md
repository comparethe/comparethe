# Web Analytics

Tools that count visitors and pageviews on your website.

## What we were looking for

One analytics tool for a portfolio of about 25 small sites, launched fast with AI. One site gets around 120k visitors a month; most get a few hundred. Roughly 150-400k pageviews a month in total.

Criteria:

- **Cost at that scale**, and what the free tier really allows
- **API usable by AI agents**: create a site and pull numbers without a human logging in
- **Multi-site and multi-org**: many sites, several teams
- **Cookie-consent burden**: does it need a banner?
- **[Flowershow](https://flowershow.app) support**: native, or just a script tag
- **Open source and self-hostable**
- **Effort to add a site**
- **Data ownership**

## Our pick

**Self-hosted [Umami](https://umami.is) on [Railway](https://railway.com), one instance for all sites, about $10 a month (our estimate, range $8-15).** Keep Google Analytics 4 where it is already installed, add it nowhere new.

- Flowershow supports Umami natively (site ID plus a custom script URL for self-hosted).
- Open source (MIT), sets no cookies, so no consent banner.
- The self-hosted API takes API keys that don't expire. One key lets an agent create a site at launch and read every site's stats, with no per-site access grants.
- No cap on sites. Umami Cloud's free plan allows 1 site with no API, and Pro ($20/mo) has the API but caps at 20 sites. At 25 sites, self-hosting is cheaper and uncapped.
- The cost is running it ourselves: uptime and backups are ours.
- **Fallback:** Umami Cloud Pro. Same tracker and API, so moving means changing the script URL and key.
- **GA4 stays** on existing sites because it is free and holds history. Umami has nothing before its tag goes on.
- **Cloudflare Web Analytics** is a handy zero-install extra on Cloudflare-proxied sites, but it samples and keeps detailed data for only 7 days, so we don't use it as the standard.

## If you're different

- **One or two sites:** Umami Cloud Hobby (free, 1 site, no API) or GoatCounter (free).
- **No ops wanted, up to 50 sites:** Fathom, $25/mo for 200k pageviews.
- **Need product analytics** (funnels, events, session replay): PostHog. Umami and the others here are for traffic stats.
- **Already on Cloudflare and want zero setup:** Cloudflare Web Analytics.
- **Want the hosted original of an open source tool:** Plausible Cloud, but the API is Business plan only and 25 sites needs an Enterprise quote.

## Prices

Monthly cost for about 25 sites and 150-400k pageviews a month.

| Tool | Cost / month at this scale | Free tier |
|---|---|---|
| **Umami self-hosted on Railway** | ~$10 estimate (Railway Hobby $5 includes $5 usage; RAM $10/GB, vCPU $20, volume $0.15/GB per month; Umami plus Postgres is about 1 GB) | n/a |
| Umami Cloud | $20 Pro (1M events, 20 sites, API); more than 20 sites not priced | Hobby: 100k events, 1 site, no API, 6-month retention |
| GA4 | $0 | Free |
| Plausible Cloud | Enterprise quote (Business $19 covers up to 10 sites) | Trial only |
| Plausible CE (self-hosted) | ~$10-20 (needs at least 2 GB RAM: Postgres + ClickHouse) | n/a |
| GoatCounter | $0 hosted (asks for "reasonable public usage", donations welcome) | Free, no stated cap |
| PostHog | $0 (1M events free; whether pageviews count as events is unverified) | 1M events, 1 project, 1-year retention without a card |
| Cloudflare Web Analytics | $0 | All plans |
| Matomo | Cloud from $29 (lowest tier; the tier for 300k hits is not priced); On-Premise free | Free trial |
| Pirsch | From $6 for 10k pageviews, 50 sites; 200k price not shown | Trial |
| Fathom | $25 (200k pageviews, 50 sites; $15 for 100k) | Trial |

## Features

| Tool | API for agents | Multi-site | Cookies / banner | Flowershow | Open source | Add a site | Data ownership |
|---|---|---|---|---|---|---|---|
| **Umami self-hosted** | REST; non-expiring API keys, or login token | Unlimited sites, teams | None (per their FAQ) | Native (ID + script URL) | MIT | One API call, one config line | Yours |
| Umami Cloud | REST, API key (Pro only) | Pro: 20 sites, 10 members | None | Native | Same code as self-hosted | Same | Theirs; export available |
| GA4 | Data API, OAuth per Google account; 200k tokens per property per day | One Google account per org | Sets cookies; EU/UK likely needs consent (unverified) | Native | No | Create property and stream by hand, or Admin API | Google |
| Plausible Cloud | Stats API v2, Business plan only, 600 req/h | Up to 10 sites below Enterprise | None (unverified) | Script tag | AGPL | Dashboard | Theirs |
| Plausible CE | Stats API (unverified in CE); no sites API | Yes | None | Script tag | AGPL | Dashboard only | Yours |
| GoatCounter | REST, Bearer key, 4 req/s; CSV export | One site per code; sites API | None (unverified) | Script tag | Yes (licence unverified, likely EUPL) | API or dashboard | Theirs, or yours if self-hosted (single binary, SQLite) |
| PostHog | HogQL query API, personal key (unverified) | More projects need a card on file | Cookies by default; cookieless option (unverified) | Script tag | MIT core | New project per site | Theirs (EU or US cloud) |
| Cloudflare Web Analytics | GraphQL, token with Analytics Read; sampled | 10 sites per account by default | Cookieless (unverified) | Beacon tag, or automatic on proxied sites | No | Dashboard toggle | Cloudflare; 6 months, detailed data 7 days |
| Matomo | Reporting API, `token_auth` (unverified) | Yes; 30 sites on Cloud | Cookieless config possible | Script tag | GPL | Dashboard or API | Yours if self-hosted (PHP + MySQL) |
| Pirsch | REST API and SDKs | 50 sites (Standard) | None | Script tag | No | Dashboard | Theirs |
| Fathom | API on all plans | 50+ sites | None | Script tag | No | Dashboard or API | Theirs |

"Unverified" means the vendor's page did not say. Check before relying on it.

## Prices checked 17 Oct 2026

Sources: umami.is/pricing, docs.umami.is (install, FAQ, API authentication), railway.com/pricing, railway.com/deploy/umami, docs.fly.io/about/pricing (alternative host to Railway: Fly with self-run Postgres, roughly $8-15 a month; managed Postgres from $38), plausible.io (pricing, Stats API docs, CE README), goatcounter.com (home, API help), posthog.com/pricing, developers.cloudflare.com/web-analytics (overview, FAQ), matomo.org/pricing, pirsch.io/pricing, usefathom.com/pricing, Google Analytics Data API quotas page, and the Flowershow analytics docs.

The Umami self-hosting figure is our estimate from Railway's published rates, not a measured bill.
