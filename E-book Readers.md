---
created: 2026-08-17
---

# E-book Readers (iOS)

Looking for something with **Apple Books-level reading UX**, that can **highlight and annotate**, and that gets those highlights **out as Markdown** — ideally straight into Obsidian. Free is great; paid is fine if it's worth it. This is not "best e-reader app" in general — it's specifically the price/quality trade-off for people who want their reading notes to become durable, portable notes, not stuck inside one app.

Readwise Reader (what prompted this — "Weedwise" 😄) does the export side better than anything else, but it's ~$120/year. Is there something nearly as good for free, or much cheaper?

## TL;DR

- **Probably the best all-round free pick:** [Readest](https://github.com/readest/readest) — free, open source (AGPLv3, 23.7k★ on GitHub), real iOS App Store app (no sideloading). Native Markdown export plus a free community Obsidian plugin that syncs straight from its local library files. Being open source is a real advantage over everything else on this page except KOReader: there's no company to shut down and no solo developer to walk away, which is exactly what killed Marvin and is quietly threatening KyBook 3.
- **Free and the nicest to actually read:** Apple Books. If pure reading feel is what matters most to you, this still wins — see the honesty note below on why it drops off the "efficient frontier" once Readest is in the mix. If you have a Mac, highlights sync via iCloud and a free open-source script/Obsidian plugin can pull them into Markdown periodically; no native path if you're iPhone/iPad-only.
- **The interesting cheap find:** [BookShelves](https://getbookshelves.app) — $6.99 one-time to unlock (free tier caps at 10 books). Built-in Markdown/JSON/CSV highlight export, iCloud sync across iPhone/iPad/Mac. Very new (10 App Store ratings) so treat as promising, not proven.
- **Best value if you want a subscription with real polish:** [justRead.app](https://justread.app) — $29.99/yr (or $79.99 once, lifetime). One-tap Markdown export, one-tap Readwise sync, actively developed, reads like a proper successor to the now-discontinued Marvin. Now only a marginal quality gain over free Readest — see the frontier below.
- **Best export power, cross-platform, worth it if you read a lot of articles too:** Readwise Reader, ~$120/yr. Only app here with fully automatic, *native* (first-party) two-way Obsidian sync — Readest's is a great community plugin, everything else is a manual export button or a workaround.
- **Free, most powerful, DIY, but sideloaded:** KOReader — not in the App Store, so real friction to install (AltStore or Xcode) that Readest doesn't have.
- **Power-user tool, use with caution:** KyBook 3 — $4.99 one-time, native Markdown export, CSS-level customization — but hasn't been meaningfully updated since 2019. Same abandonment risk that killed Marvin.

## The efficient frontier: price vs. quality

<div style="margin: 20px 0;">
  <iframe src="ebook-readers-price-vs-quality.html" style="width:100%; height:660px; border:1px solid #dde1e4; border-radius:10px;" loading="lazy" title="Efficient frontier: price vs. quality, 9 iOS e-book readers"></iframe>
</div>

[Open the interactive chart →](ebook-readers-price-vs-quality.html)

Three apps sit on the frontier: **Readest** (free, 8.2), **justRead.app** ($30/yr, 8.4), and **Readwise Reader** ($120/yr, 8.8). Apple Books, BookFusion, Kindle, Google Play Books, Neat Reader, and KOReader are all dominated in this scoring — something cheaper (or free) here scores as high or higher.

**An honesty note on Apple Books dropping off the frontier:** it's dominated here on paper only because Readest matches its price ($0) and scores higher on the *composite*. Apple Books almost certainly still has the nicer reading feel — the composite gives export weight 30%, and Readest's export is simply much stronger (native Markdown + Obsidian plugin vs. Apple Books needing a Mac and a script). Weight export lower — say 10% — and Apple Books likely retakes the top free spot. The chart is only as right as the weighting choice in [methodology](#methodology); read the per-app notes, not just the star, before picking.

Two apps aren't on the chart at all: **BookShelves** ($6.99 one-time) and **KyBook 3** ($4.99 one-time). A one-time purchase isn't directly comparable to a $/year subscription axis, so they're broken out separately below.

## Comparison table

| App | Price | Reading UX | Markdown / Obsidian export | Quality score |
|---|---|---|---|---|
| **Apple Books** | Free | ★★★★★ Best-in-class native polish, page-turn, huge format support | Manual — no iOS export; needs a Mac + free script/plugin reading the local highlights database | **7.6** |
| **Readest** | Free, open source (optional $4.99–9.99/mo for Readest's own hosted cloud sync — bring-your-own iCloud/WebDAV/etc. is free) | ★★★★☆ Modern, accessible (VoiceOver/TalkBack/NVDA), CarPlay, up to 4 books split-view on iPad; 4.5★/163 ratings | ★★★★★ Native Markdown export (filterable by color/style) + free community Obsidian plugin reading its local JSON library | **8.2** |
| **Readwise Reader** | $9.99/mo billed annually (~$120/yr), $12.99/mo month-to-month | ★★★★☆ Clean, cross-platform; built for articles/newsletters first, EPUBs second | ★★★★★ Native, automatic, two-way Obsidian sync + Markdown/CSV export | **8.8** |
| **justRead.app** | $29.99/yr, or $79.99 one-time (lifetime) | ★★★★☆ Modern, 200+ fonts, per-book layout memory, actively developed | ★★★★☆ One-tap Markdown export + one-tap Readwise sync (no native Obsidian plugin yet) | **8.4** |
| **BookFusion** | Free (10 books), ~$25/yr for full sync/storage | ★★★☆☆ Functional, cross-platform sync, less polished | ★★★★☆ Built-in CSV / Markdown / HTML / PDF export | **7.1** |
| **KOReader** | Free, open source | ★★★☆☆ Extremely powerful and customizable, utilitarian look, sideload-only on iOS | ★★★★★ Native Markdown sidecar files per book + free community Obsidian plugins for automatic sync | **7.5** |
| **Kindle app** | Free (books cost extra) | ★★★★☆ Solid, huge store, but Amazon-locked and DRM'd | ★★★☆☆ No native export; free third-party tools (Bookcision, ClipVault, Obsidian Kindle plugin) work but are unofficial workarounds | **6.7** |
| **Neat Reader** | $19.99/yr (lifetime option also sold) | ★★★☆☆ Decent, cross-platform (Android/iOS/Windows/Mac/web), unremarkable polish | ★★★☆☆ In-app note export, but no explicit Markdown/Obsidian format confirmed in docs | **6.5** |
| **Google Play Books** | Free | ★★★☆☆ Functional but dated on iOS, clearly an Android-first app | ★★☆☆☆ Backs up notes as one Google Doc per book — only triggers when you add a new note, so it's manual and indirect | **6.0** |
| ~~Marvin 3~~ | — | Loved by readers for years | CSV/HTML via email | *(discontinued — removed from the App Store, unmaintained; justRead.app is its closest spiritual successor)* |

**One-time purchases** (not on the $/yr chart — see [methodology](#methodology)):

| App | Price | Reading UX | Markdown / Obsidian export | Quality score |
|---|---|---|---|---|
| **BookShelves** | Free (10-book cap), $6.99 one-time to unlock (subscription also offered in some regions) | ★★★★☆ Clean, modern, 10 themes incl. accessible fonts, iCloud sync iPhone/iPad/Mac | ★★★★☆ Built-in Markdown/JSON/CSV export, plus full library export/restore | **8.2** *(4.3★, only 10 App Store ratings — promising but unproven)* |
| **KyBook 3** | $4.99 one-time | ★★★☆☆ Deep power-user customization — custom CSS, OPDS, WebDAV, Calibre sync, regex search | ★★★★☆ Clean native Markdown/plain-text export | **7.6** *(no meaningful update since Feb 2019 — real risk it breaks on a future iOS release)* |

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

### Readest

Free and open source under the AGPLv3 license — 23.7k★ on [GitHub](https://github.com/readest/readest), described by its own maintainers as "a modern rewrite of Foliate" (the well-regarded Linux EPUB reader), built on Next.js and Tauri. Real iOS/iPadOS App Store app plus macOS, Windows, Linux, Android, and web versions — one codebase, no sideloading. Reads EPUB, PDF, MOBI, KF8, FB2, CBZ, TXT, and Markdown; supports highlights, bookmarks, and structured notes; has genuinely deep accessibility support (VoiceOver, TalkBack, NVDA, Orca) plus a reading ruler and paragraph-by-paragraph mode. It can also sync reading progress, notes, and bookmarks directly with **KOReader devices**, which is a rare bridge between the two ecosystems.

Export is the standout: highlights/notes export **natively to Markdown**, filterable by color or style, and there's a free, independent [Obsidian plugin](https://community.obsidian.md/plugins/readest-highlights) that reads Readest's local JSON library and renders highlights straight into your vault — one note per book or appended to an open note, with re-syncing that preserves your own edits. That's the same "automated, not manual" tier as KOReader's plugin ecosystem, without KOReader's sideloading friction.

The core app and local Markdown export are entirely free; Readest also sells optional cloud-sync tiers ($4.99–9.99/mo, or storage add-ons) if you want its hosted sync instead of pointing it at your own iCloud/Google Drive/OneDrive/WebDAV/S3, which works for free. Being open source under a real copyleft license is the biggest differentiator versus everything else on this page except KOReader — nobody can quietly discontinue it the way Marvin's solo developer did, and even if the current maintainers stopped, the code stays forkable. Caveat: it's a cross-platform (Tauri/webview) app rather than hand-tuned native Swift, so it likely won't feel quite as buttery as Apple Books or justRead's SwiftUI animations — reflected in its slightly lower reading-UX sub-score here.

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

### BookShelves

Free with a 10-book cap; $6.99 one-time in-app purchase unlocks unlimited books, iCloud sync, Kindle/Kobo/reMarkable email delivery, and highlight export (a subscription option also exists in some regions). Genuinely interesting: EPUB/PDF/MOBI/AZW/KEPUB/CBZ support, 10 themes including OpenDyslexic and other accessible fonts, and — unusually for a $7 app — **built-in Markdown, JSON, and CSV export** for highlights, plus a full library export/restore. iCloud sync keeps books, highlights, and reading position in step across iPhone, iPad, and Mac. The catch is simply that it's new: 4.3★ but only 10 App Store ratings at the time of this research, so there's not much of a track record yet, and no confirmed native Obsidian plugin (you'd drop the Markdown export into a vault manually, same as justRead). Worth trying given the price is trivial either way.

### KyBook 3

$4.99 one-time. For years this was the other name (alongside Marvin) people reached for when they wanted real power-user control on iOS: custom CSS injection, font-level typography control, OPDS catalog and WebDAV/Dropbox/Google Drive/iCloud connections, Calibre library sync, regex search, and clean native export of highlights/notes to Markdown or plain text. The real problem: **its last meaningful update was version 0.7.8 in February 2019.** It's still purchasable and reportedly still works, but it carries the same abandonment risk that eventually killed Marvin outright — a future iOS release could break it with nobody left to fix it. Treat it as "great if it still works for you," not a safe long-term bet.

### Neat Reader

$19.99/yr (a lifetime option is also sold). Cross-platform — Android, iOS, Windows, Mac, and web — with WiFi import, 10GB cloud sync, and in-app note/highlight export. Reviews and documentation describe export in general terms ("export notes") without confirming a Markdown or Obsidian-specific path, so treat it as a competent, unremarkable middle option rather than an export specialist. Reasonable if you specifically need the same library synced across Android and iOS/Windows/Mac, which none of the frontier apps above do as completely.

### Google Play Books (iOS)

Free. Google's own reader app has an iOS version, and if your library is already there (e.g., you buy books from the Play Store or came from Android), it's a no-cost option. Export is the weak point: it backs highlights up as **one Google Doc per book**, dropped into a Google Drive folder — but only when you open that specific book and add a new note/highlight/bookmark, so it's a manual, per-book trigger rather than an automatic sync, and you're exporting to Google Docs, not Markdown, directly (a manual copy/paste or conversion step is still required for Obsidian). Fine if you're already all-in on Google; not worth switching to for export quality alone.

### Marvin 3 — discontinued, not scored

The app that inspired this whole category for a lot of readers, including the "Lithium on Android" comparison this research started from: excellent EPUB/CBR/CBZ support, deep customization, CSV/HTML highlight export via email. Removed from the App Store and no longer updated. Included here only as context — justRead.app is the closest thing to a modern replacement.

### Why not Lithium?

Lithium (Android-only EPUB reader, also praised for its export-your-data option) is what set the "Android had something great" bar in this research — but it isn't available on iOS at all, so it's out of scope for this list rather than scored.

### A dead end worth flagging: "Readwise Lite"

Readwise sells a cheaper tier called **Readwise Lite** ($5.59/mo billed annually, ~$67/yr) that syncs highlights from Kindle, Apple Books, and other sources without the Reader app — which looks, at first glance, like a way to get Readwise's sync quality at a lower price while reading in Apple Books for free. Checked directly against Readwise's pricing page: **it doesn't work that way.** Lite includes highlight review, search, tagging, and sync-from-all-sources, but Notion/Obsidian export is reserved for the full $9.99/mo plan — the same plan that includes Reader. So there's no cheaper path to automatic Obsidian sync via Readwise; the $120/yr price in the table is the real floor for that specific capability, whether or not you ever open the Reader app itself.

### Not scored: Voice Dream Reader

Worth a mention if accessibility/text-to-speech is the priority rather than Markdown export: [Voice Dream Reader](https://www.voicedream.com/reader/) (2021 Apple Design Award winner) reads EPUBs, PDFs, and web articles aloud with word-by-word highlighting, and does support exporting highlights/notes via clipboard or email. It's priced very differently from everything else here (up to $119.99 for the education/iPad edition) and optimized for a different job — listening, not annotating for a Markdown vault — so it's excluded from the scored table rather than force-fit into this comparison.

## What's not resolved

- None of this is hands-on, day-to-day testing — it's built from docs, App Store listings, and reviews. A real usage pass (a week each with Apple Books, Readest, justRead, and Readwise Reader) would sharpen the UX scores a lot — Readest's reading-UX sub-score in particular is more of an estimate than the SwiftUI-native apps, since cross-platform frameworks are harder to judge from docs alone.
- The export-quality weighting (30%) is a judgment call — someone who barely annotates might want it at 10%, someone building a serious Obsidian-based reading system might want it at 50%.
- Kobo's app and hardware have a whole separate highlight-export ecosystem ([kobo-highlights-exporter](https://github.com/unripeapple/kobo-highlights-exporter), Obsidian's Kobo importer plugin) that wasn't scored here since Kobo's iOS app is thinner than its e-ink devices — worth a follow-up if Kobo hardware is in play, not just the iOS app.
- PDF-heavy academic workflows (GoodReader, LiquidText, Zotero-adjacent tools) are a different comparison — this page is about ebook reading (EPUB-first), not PDF annotation specifically.

## Links

- [Readest (GitHub)](https://github.com/readest/readest) · [App Store](https://apps.apple.com/us/app/readest-ebook-reader/id6738622779) · [Obsidian plugin](https://community.obsidian.md/plugins/readest-highlights) · [KOReader sync wiki](https://github.com/readest/readest/wiki)
- [Readwise Reader](https://readwise.io/read) · [Reader export docs](https://docs.readwise.io/reader/docs/faqs/exporting) · [Obsidian export](https://readwise.io/changelog/obsidian-export)
- [justRead.app](https://justread.app) · [justRead vs. Apple Books](https://medium.com/macoclock/justread-app-vs-apple-books-ff9937f14011)
- [BookFusion](https://www.bookfusion.com) · [pricing](https://www.bookfusion.com/reading/pricing)
- [KOReader](https://koreader.rocks) · [koreader-ios (sideload)](https://github.com/hezi/koreader-ios) · [Obsidian KOReader plugins](https://community.obsidian.md/plugins/koreader-highlights-importer)
- [Bookcision](https://readwise.io/bookcision) · [ClipVault](https://www.clipvault.xyz/) · [Obsidian Kindle plugin](https://github.com/hadynz/obsidian-kindle-plugin)
- [Apple Books Highlights (Obsidian plugin)](https://community.obsidian.md/plugins/apple-books-highlights) · [ibook (Obsidian plugin)](https://www.obsidianstats.com/plugins/ibook)
- [BookShelves](https://getbookshelves.app) · [features](https://getbookshelves.app/features/)
- [KyBook 3](https://kybook-3-ebook-reader.en.softonic.com/iphone)
- [Neat Reader](https://www.neat-reader.com) · [pricing](https://www.neat-reader.com/price)
- [Google Play Books export guide](https://support.google.com/googleplay/answer/3165868)
- [Readwise pricing (Lite vs. Full)](https://readwise.io/pricing) · [Voice Dream Reader](https://www.voicedream.com/reader/)
