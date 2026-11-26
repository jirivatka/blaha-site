# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users
Primary: people who already keep their tasks in Vikunja, on a server they host or on Vikunja Cloud, and want more from it than a list. Their situation: the tasks are there, but nothing tells them what can be done now, what is waiting, or which project has quietly gone stale. Their job: run a personal planning system (next actions, defer dates, regular reviews) on their own data, on the devices they carry.
Secondary: freelancers who track hours against projects and invoice from them (Timesheet); App Review and store visitors who arrive at the Support and Privacy URLs.

## Product Purpose
Blaha is a native Vikunja client for iPhone, iPad, Mac, Apple Watch and Android that turns a Vikunja task list into a planning system: Forecast puts the day's calendar events beside the tasks due, defer dates hide work until it can be done, Blocked keeps waiting work aside, projects get review cycles, Perspectives are saved filters in the sidebar, Timesheet tracks hours with CSV/PDF export. Success: a Vikunja user tries the free client, then buys the unlock because the system layer is worth it.

## Positioning
A planner for Vikunja, not just a list. The tasks stay on the user's own server: no account at Blaha, no backend of ours in the middle. No subscription: a client for someone else's server has nothing honest to charge rent for.

## Operating Context
A visitor usually arrives already running Vikunja (often self-hosted), from the Vikunja community, an app store listing or a search. They want to know whether it works with their server, what is free, what the unlock adds, and whether they can try it without a server (the in-app demo on sample data).

## Capabilities and Constraints
- Platforms: iOS/iPadOS 17+, macOS 14+, Android 8.0+, plus Apple Watch. All live: App Store (id 6815227673, one Universal Purchase) and Google Play (com.redpixl.blaha).
- Free: a full task client (Forecast, Tasks, Calendar, Done, Tags, capture, share extension, widgets). One-time unlock adds seven: Projects (with Folders), Blocked, Review, Perspectives, defer dates, multiple accounts, time tracking. 7-day trial of everything from first launch. The site does not state the price.
- Needs a Vikunja server reachable over HTTPS, or none for the demo.
- Static site on GitHub Pages: no build step, no external assets (no CDN, no web fonts from elsewhere, no store badge images; text links to the stores). `style.css?v=N` must be bumped when CSS changes. Push to main deploys.
- Pages: index (landing), support (App Store Support URL), privacy (Privacy Policy URL), eula, forum/ (redirect to GitHub Discussions; publish only blahatasks.app/forum/).

## Brand Commitments
- Name: Blaha. Maker: RedPixl s.r.o. "Blaha is an independent third-party client for Vikunja" disclaimer stays.
- The app icon (red check) and the real app screenshots in `screens/` and the launch film in `video/` stay as the imagery.
- Voice: plain, precise, no hype; says what Blaha does.
- Never name a competing app anywhere (copy, meta, commit messages). Never show a Review screen (its empty state names one).

## Evidence on Hand
- Real screenshots from the store sets (`screens/`), the 80 s silent 1.3 film (`video/blaha.mp4` + poster).
- Live on both stores. No testimonials, ratings, user counts or press exist; do not invent any.

## Product Principles
1. Your data stays on your server.
2. A system, not a list: show what can be done now.
3. Free is genuinely useful; the unlock is paid once.
4. Native on every platform it ships on.
