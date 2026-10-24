# blahatasks.app

The site for **Blaha**, a task manager for [Vikunja](https://vikunja.io) on
iPhone, iPad and Mac. Three static pages, one stylesheet, no build step and
**no external assets** — these must render if a CDN is blocked, and App Review
fetches them from who-knows-where.

| page | what it is for |
|---|---|
| `index.html` | the landing page |
| `support.html` | the App Store **Support URL** |
| `privacy.html` | the App Store **Privacy Policy URL** |

The support forum is published as **https://blahatasks.app/forum/** — the one forum address to use anywhere (site, app, store listings). `forum/index.html` forwards it to [jirivatka/Blaha-Support](https://github.com/jirivatka/Blaha-Support/discussions), so the forum can move without breaking a link.
⛔ If that repo is ever renamed or made private, both the support page and the
App Store link break.

`screens/` holds the three shots on the landing page, downscaled from the App
Store sets in the app repo (`AppStore/screenshots/`). ⛔ **Never put a Review
screen on this site**: that screen's own empty-state text names a competing
app, and a screenshot puts it on the web exactly as a sentence would.

`style.css` is tradelogbook.app's sheet with Blaha's palette — ink plum, with
the app icon's red check as the one warm colour. The icons are generated from
the app's own `AppIcon.appiconset/ios_1024.png`, so they cannot drift from the
shipped icon.

⛔ **Never name a competing app on these pages** — not in the copy, not in a
meta tag, not in a commit message, which is as public as the page itself. The
copy says what Blaha DOES: defer dates, review cycles, saved perspectives.
That is the stronger claim anyway, because it means something to a reader who
has never used the other app.

✅ **Store status, as the page states it:** every platform is live — **Android**
on Google Play since 2026-09-27, the **Mac** on the App Store since 2026-09-30,
and **iPhone/iPad** on the App Store since 2026-10-24 (same app id 6815227673,
one Universal Purchase). The status line says "On the App Store and Google
Play" and the hero carries one text link to each store. ⛔ Text links only — no store badge images (they
would be third-party brand assets with their own usage rules, and nothing here
loads from outside).

## The launch film

`video/blaha.mp4` (60 s, 1080p, crf 26 re-encode, no audio track, 3.7 MB) and
`video/blaha-poster.jpg` sit under the hero in `figure.film`. Since 2026-10-20
this is the **all-platform cut**, silent by Jiri's request: Android screens from
the Play listing, iPad, Mac and iPhone screens from the App Store sets. The
master and the HyperFrames project are in the app repo's untracked
`brag-output-all/`. It replaced the 45 s Apple cut (`brag-output-mac/`).
- ⛔ **Self-hosted, never a YouTube or Vimeo embed** — see the note at the top:
  no external assets, and an iframe would set cookies the privacy page does not
  mention.
- ⚠️ `preload="none"` stays — otherwise every visitor downloads the film.
- ⛔ It shows no Review screen (see `screens/` above) and makes no store or
  availability claim, so it does not go stale when the app ships.

## Structured data and title

`index.html` carries one JSON-LD block (Organization = RedPixl s.r.o.,
WebSite, SoftwareApplication). Added 2026-10-20 for SEO checkers; the title
was lengthened to 59 characters at the same time (aim 50–60).
- `operatingSystem` lists iOS, iPadOS, macOS and Android since 2026-10-24, when
  the iPhone/iPad app went live. `sameAs` needs no iOS entry: the one App Store
  URL serves iPhone, iPad and Mac.
- ⛔ Never add `aggregateRating` or `review` values that are not the stores'
  real ones — Google requires one for a software rich result, so without it the
  block describes the app but earns no star snippet. That is fine.
- Prices: `offers` says free (0) with the one-time unlock in words; the unlock's
  price is not on this site, so it is not in the markup either.
