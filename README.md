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

⚠️ **Nothing here claims the app is on sale.** It is not, yet. The landing page
says "coming to the App Store" and there is no store link — when the app ships,
that line and the link change together.
