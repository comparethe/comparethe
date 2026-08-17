---
created: 2026-08-17
---

# E-book Readers (iOS)

Looking for something with **Apple Books-level reading UX**, that can **highlight and annotate**, and that gets those highlights **out as Markdown** — ideally straight into Obsidian. Free is great; paid is fine if it's worth it. This is not "best e-reader app" in general — it's specifically the price/quality trade-off for people who want their reading notes to become durable, portable notes, not stuck inside one app.

Readwise Reader (what prompted this — "Weedwise" 😄) does the export side better than anything else, but it's ~$120/year. Is there something nearly as good for free, or much cheaper?

## TL;DR

- **Free and zero fuss:** Apple Books. Best reading experience of anything here, and if you have a Mac, highlights sync via iCloud and a free open-source script/Obsidian plugin can pull them into Markdown periodically. No native path if you're iPhone/iPad-only.
- **Best value if you're willing to pay something:** [justRead.app](https://justread.app) — $29.99/yr (or $79.99 once, lifetime). One-tap Markdown export, one-tap Readwise sync, actively developed, reads like a proper successor to the now-discontinued Marvin.
- **Best export power, cross-platform, worth it if you read a lot of articles too:** Readwise Reader, ~$120/yr. Only app here with fully automatic, native two-way Obsidian sync — everything else is an export button or a workaround.
- **Free, most powerful, DIY:** KOReader — but it's not in the App Store, so you're sideloading it (AltStore or Xcode), which is real friction on iOS specifically.

## The efficient frontier: price vs. quality

<div style="margin: 20px 0;">
  <iframe src="ebook-readers-price-vs-quality.html" style="width:100%; height:660px; border:1px solid #dde1e4; border-radius:10px;" loading="lazy" title="Efficient frontier: price vs. quality, 6 iOS e-book readers"></iframe>
</div>

[Open the interactive chart →](ebook-readers-price-vs-quality.html)

Three apps sit on the frontier: **Apple Books** (free, 7.6), **justRead.app** ($30/yr, 8.4), and **Readwise Reader** ($120/yr, 8.8). BookFusion, Kindle, and KOReader are all dominated in this scoring — something cheaper (or free) here scores as high or higher. That doesn't make them bad; see the notes below for why you might still pick KOReader (fully free, most hackable) or Kindle (if your library is already there) despite not being "efficient" on this particular chart.

## Comparison table

| App | Price | Reading UX | Markdown / Obsidian export | Quality score |
|---|---|---|---|---|
| **Apple Books** | Free | ★★★★★ Best-in-class native polish, page-turn, huge format support | Manual — no iOS export; needs a Mac + free script/plugin reading the local highlights database | **7.6** |
| **Readwise Reader** | $9.99/mo billed annually (~$120/yr), $12.99/mo month-to-month | ★★★★☆ Clean, cross-platform; built for articles/newsletters first, EPUBs second | ★★★★★ Native, automatic, two-way Obsidian sync + Markdown/CSV export | **8.8** |
| **justRead.app** | $29.99/yr, or $79.99 one-time (lifetime) | ★★★★☆ Modern, 200+ fonts, per-book layout memory, actively developed | ★★★★☆ One-tap Markdown export + one-tap Readwise sync (no native Obsidian plugin yet) | **8.4** |
| **BookFusion** | Free (10 books), ~$25/yr for full sync/storage | ★★★☆☆ Functional, cross-platform sync, less polished | ★★★★☆ Built-in CSV / Markdown / HTML / PDF export | **7.1** |
| **KOReader** | Free, open source | ★★★☆☆ Extremely powerful and customizable, utilitarian look, sideload-only on iOS | ★★★★★ Native Markdown sidecar files per book + free community Obsidian plugins for automatic sync | **7.5** |
| **Kindle app** | Free (books cost extra) | ★★★★☆ Solid, huge store, but Amazon-locked and DRM'd | ★★★☆☆ No native export; free third-party tools (Bookcision, ClipVault, Obsidian Kindle plugin) work but are unofficial workarounds | **6.7** |
| ~~Marvin 3~~ | — | Loved by readers for years | CSV/HTML via email | *(discontinued — removed from the App Store, unmaintained; justRead.app is its closest spiritual successor)* |

## Methodology

Quality score (0–10) is a weighted blend of three things, since the brief was both UX *and* export, not just one:

- **50% Reading UX** — typography, page-turning feel, library management, overall polish
- **20% Annotation UX** — how good highlighting/note-taking feels in the moment
- **30% Markdown/Obsidian export** — native automatic sync scores highest; a built-in one-tap export button scores well; a free but unofficial third-party workaround scores lowest, because it's extra friction and can break

This is a judgment call, not a lab measurement — built from App Store listings, developer docs, and reviews (linked below), not hands-on testing of every app. Treat the 0–10 scores as "roughly this much better/worse," not decimal-precise.

Price on the chart is annualized cost — one-time/lifetime options (justRead's $79.99, Marvin's old one-off price) are noted in the table but not directly comparable to a $/yr axis, so they're not on the chart.

## Notes on each app

### Apple Books

Free, built into iOS. Nothing beats it on raw reading feel — this is the bar everything else gets measured against. The catch is export: there's no built-in way to get highlights out as Markdown on iPhone/iPad alone. If you also have a Mac, Apple Books syncs highlights there via iCloud, and free tools exist to pull them into Obsidian: the [Apple Books Highlights](https://community.obsidian.md/plugins/apple-books-highlights) and [ibook](https://www.obsidianstats.com/plugins/ibook) Obsidian plugins, or a [standalone Python script](https://gist.github.com/eristoddle/5a8e7dd0597d09d00aa5de066788c303). No good answer for iOS-only users with no Mac.

### Readwise Reader

$9.99/mo billed annually, $12.99/mo month-to-month, 30-day free trial, 50% off for students/educators/nonprofits. Built on Readwise's highlight infrastructure, so EPUB, PDF, articles, newsletters, RSS, and even YouTube/X threads all live in one place and sync everywhere. The [Obsidian integration](https://readwise.io/changelog/obsidian-export) is the best of anything surveyed here — fully automatic, two-way, with a template system for how highlights land in your vault. The trade-off: it's a read-it-later app that grew EPUB support, not an EPUB reader that grew export — so the pure novel-reading experience is very good but not quite Apple Books or justRead-level polish, and the app is useless without an active subscription (no offline "own it forever" mode).

### justRead.app

$4.99/mo, $29.99/yr, or $79.99 once (lifetime) — 14-day free trial. Reads as the direct successor to Marvin (see below): 200+ fonts, true zero margins, full RGB text/background control, per-book layout memory, two-way Calibre sync, actively developed through 2026. Highlights in six colors, with one-tap Markdown export and one-tap Readwise sync built in. No dedicated Obsidian plugin yet, but Markdown files drop straight into a vault folder. Best pick if you own your EPUB library (DRM-free or de-DRM'd) and want something close to Marvin's old power without the abandonment risk.

### BookFusion

Free for up to 10 books; paid tiers (~$25/yr, roughly £20/yr) add more storage and sync headroom. Reviews are mixed on polish, but it's the only app here with a built-in **Markdown export button** alongside CSV/HTML/PDF, plus solid EPUB/PDF support and Calibre-style library sync across iOS/Android/web. A reasonable cheap option if justRead or Readwise feel like overkill.

### KOReader

Free and open source. The power-user's choice — deep customization, excellent PDF reflow, dictionary lookups, and highlight/note files that are already structured Markdown-adjacent sidecar files per book. Free community Obsidian plugins ([obsidian-koreader-highlights](https://github.com/t5k6/obsidian-koreader-highlights), [obsidian-koreader-sync](https://github.com/Edo78/obsidian-koreader-sync)) automate the sync fully. The catch, specifically on iOS: **it isn't in the App Store.** You sideload it via [AltStore](https://altstore.io) or build it yourself with Xcode ([koreader-ios](https://github.com/hezi/koreader-ios)), and a free Apple ID re-signs it every 7 days unless you're paying for a developer account or using a service like AltStore Classic. Worth it if you're comfortable with that; a real barrier if you're not.

### Kindle app

Free (you pay per book, or via Kindle Unlimited). Fine reading experience, enormous library, but you're locked into Amazon's ecosystem and DRM. No native export — but free third-party tools cover it: [Bookcision](https://readwise.io/bookcision) (bookmarklet on read.amazon.com), [ClipVault](https://www.clipvault.xyz/) (free unlimited export to Obsidian Markdown/CSV/Evernote), or the [Obsidian Kindle plugin](https://github.com/hadynz/obsidian-kindle-plugin) (syncs from Amazon's cloud or a `My Clippings.txt` file). All free, all a bit more manual than a built-in button, and dependent on Amazon not changing its site layout.

### Marvin 3 — discontinued, not scored

The app that inspired this whole category for a lot of readers, including the "Lithium on Android" comparison this research started from: excellent EPUB/CBR/CBZ support, deep customization, CSV/HTML highlight export via email. Removed from the App Store and no longer updated. Included here only as context — justRead.app is the closest thing to a modern replacement.

### Why not Lithium?

Lithium (Android-only EPUB reader, also praised for its export-your-data option) is what set the "Android had something great" bar in this research — but it isn't available on iOS at all, so it's out of scope for this list rather than scored.

## What's not resolved

- None of this is hands-on, day-to-day testing — it's built from docs, App Store listings, and reviews. A real usage pass (a week each with Apple Books, justRead, and Readwise Reader) would sharpen the UX scores a lot.
- The export-quality weighting (30%) is a judgment call — someone who barely annotates might want it at 10%, someone building a serious Obsidian-based reading system might want it at 50%.
- Kobo's app and hardware have a whole separate highlight-export ecosystem ([kobo-highlights-exporter](https://github.com/unripeapple/kobo-highlights-exporter), Obsidian's Kobo importer plugin) that wasn't scored here since Kobo's iOS app is thinner than its e-ink devices — worth a follow-up if Kobo hardware is in play, not just the iOS app.
- PDF-heavy academic workflows (GoodReader, LiquidText, Zotero-adjacent tools) are a different comparison — this page is about ebook reading (EPUB-first), not PDF annotation specifically.

## Links

- [Readwise Reader](https://readwise.io/read) · [Reader export docs](https://docs.readwise.io/reader/docs/faqs/exporting) · [Obsidian export](https://readwise.io/changelog/obsidian-export)
- [justRead.app](https://justread.app) · [justRead vs. Apple Books](https://medium.com/macoclock/justread-app-vs-apple-books-ff9937f14011)
- [BookFusion](https://www.bookfusion.com) · [pricing](https://www.bookfusion.com/reading/pricing)
- [KOReader](https://koreader.rocks) · [koreader-ios (sideload)](https://github.com/hezi/koreader-ios) · [Obsidian KOReader plugins](https://community.obsidian.md/plugins/koreader-highlights-importer)
- [Bookcision](https://readwise.io/bookcision) · [ClipVault](https://www.clipvault.xyz/) · [Obsidian Kindle plugin](https://github.com/hadynz/obsidian-kindle-plugin)
- [Apple Books Highlights (Obsidian plugin)](https://community.obsidian.md/plugins/apple-books-highlights) · [ibook (Obsidian plugin)](https://www.obsidianstats.com/plugins/ibook)
