---
version: 1
slug: "index-html"
primary_target: "index.html"
related_targets: ["support.html","privacy.html","eula.html"]
---

# Surface: blahatasks.app home (index.html)

Mode: Persuade (home); support, privacy and eula are Read pages in the same world. Visitor: a Vikunja user (often self-hosted) deciding whether to install Blaha. Job: believe Blaha turns their own Vikunja into a planning system, and that the free client is real. Action: App Store / Google Play text links (no badge images). Proof: real screenshots in `screens/`, the 1.3 film in `video/`. Avoid (Jiri): generic SaaS look, looking like Vikunja's own site, losing the screenshots. Constraints: no external assets, no competitor names, no Review screen, `style.css?v=N` bump.

## Direction contract

THESIS: The page is the app icon's planning board, life-size: a plum header strip over a lavender board where tasks sit as rows, each starting with the app's hollow priority ring. It refuses the device-mockup split hero and the feature-card grid.
OWN-WORLD: Icon plum ground (#241a36 to #2e2244), board panel in icon lavender (#dcd6e4), column header strip in icon header plum; task rows carry the app's hollow rings (red, blue, yellow, grey) and coloured edge bars; icon pill colours (purple, orange, green, blue) as one-colour-per-project, flat, never tinted; the red check is the one mark of done. System sans throughout (the app's own face), tabular figures for dates and counts.
STORY: Visitor sees their kind of task list sorted into Deferred / Now / Blocked / Review due, reads the promise on the one clean card, ticks a ring and watches the row leave Now; then sees each job proved by a real screenshot, the film, free versus unlock, requirements, and downloads.
FIRST VIEWPORT: Full-width board under a slim plum bar: four columns with counts (Deferred 12 hidden, Now, Blocked, Review due); the Now column is wider and holds the offer card (kicker, H1 "A planner for Vikunja, not just a list.", one-line promise, App Store + Google Play links, "Free to use. No subscription.") above two real-looking rows with live rings; other columns dimmed until pointed at.
FORM: Planning board (T-card board) translated through the app icon and its priority rings, grounded candidate 3 of 7; seed:806880e7c3230c3c. Raises: one calm card on an occupied board (festival hoarding); flat unmixed project colours (toy catalogue); point at a column to isolate it (event display); numbered margin for the sections (origami sequence).
FINISH: unreviewed and undocumented is unfinished; this build ends with the finish review, the verdict, DESIGN.md, and every shipping raster carrying its provenance
