---
name: blahatasks.app
description: Blaha's site, drawn as the app icon's planning board.
colors:
  ground: "#1f1630"
  strip: "#36275a"
  strip-ink: "#efe9f7"
  board: "#dcd6e4"
  card: "#f8f6fb"
  offer: "#fdfcfe"
  ink: "#1d1528"
  ink-2: "#4b4159"
  on: "#efeaf5"
  on-2: "#bdb3cd"
  check-red: "#cc3c35"
  ring-red: "#e0443a"
  ring-blue: "#2b7de3"
  ring-yellow: "#d9a514"
  ring-grey: "#8a8396"
  pill-purple: "#66499a"
  pill-orange: "#dd8c42"
  pill-green: "#36a078"
  pill-blue: "#5b92dc"
  done-green: "#186848"
  unlock-yellow: "#f2c94c"
typography:
  display:
    fontFamily: "Figtree, system-ui, sans-serif"
    fontSize: "clamp(2.3rem, 1.2rem + 2.6vw, 3.6rem)"
    fontWeight: 750
    lineHeight: 1.02
    letterSpacing: "-0.03em"
  headline:
    fontFamily: "Figtree, system-ui, sans-serif"
    fontSize: "clamp(1.9rem, 1rem + 1.8vw, 2.8rem)"
    fontWeight: 720
    lineHeight: 1.05
    letterSpacing: "-0.025em"
  title:
    fontFamily: "Figtree, system-ui, sans-serif"
    fontSize: "16px"
    fontWeight: 600
    lineHeight: 1
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.55
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "13px"
    fontWeight: 400
    lineHeight: 1.3
rounded:
  row: "16px"
  offer: "22px"
  board: "28px"
  pill: "999px"
spacing:
  row-gap: "8px"
  col-gap: "18px"
  section: "88px"
  gutter: "32px"
  gutter-phone: "16px"
components:
  button-primary:
    backgroundColor: "{colors.strip}"
    textColor: "#ffffff"
    rounded: "{rounded.pill}"
    padding: "0 22px"
    height: "48px"
  button-primary-hover:
    backgroundColor: "{colors.pill-purple}"
  button-line:
    backgroundColor: "transparent"
    textColor: "{colors.strip}"
    rounded: "{rounded.pill}"
    padding: "0 22px"
    height: "48px"
  task-row:
    backgroundColor: "{colors.card}"
    textColor: "{colors.ink}"
    rounded: "{rounded.row}"
    padding: "13px 14px"
  column-strip:
    backgroundColor: "{colors.strip}"
    textColor: "{colors.strip-ink}"
    typography: "{typography.title}"
    padding: "14px 16px"
  offer-card:
    backgroundColor: "{colors.offer}"
    textColor: "{colors.ink}"
    rounded: "{rounded.offer}"
    padding: "34px"
---

# Design System: blahatasks.app

## Overview

**Creative North Star: "The icon's board, life-size"**

The app icon is a board: a dark plum header strip over a lavender panel of coloured pills, with one red check. The site is that board at full scale. Lavender board panels sit on a plum ground; dark strips hang from each panel's top edge and name what is below; tasks sit on the board as rows that start with the app's own hollow priority rings. The real app screenshots are the main pictures, each set on its own board panel.

The page is dense where the board is (rows, counts, columns) and quiet on the plum between panels. It must never read as a generic SaaS page (gradient hero, device mockups beside a headline, a row of equal feature cards) or as Vikunja's own site.

**Key Characteristics:**
- Plum ground, lavender boards, strips hanging from the top edge.
- Hollow rings in priority colours lead every task row; the red check is the one mark of done.
- One project colour per pill, flat, never tinted.
- One calm card (the offer) on an occupied board.
- Real screenshots, never mock devices.

## Colors

A dark plum world taken from the icon, with the app's ring colours and the icon's pill colours as the only saturated notes.

### Primary
- **Header Plum** (#36275a): the icon's header band. Column strips, the top bar, the solid button.
- **Board Lavender** (#dcd6e4): the icon's panel. Every board and reading-page panel.

### Secondary
- **Check Red** (#cc3c35): the icon's check. A ticked ring fills with it; nothing else is red except the red ring and the Timesheet pill.
- **Ring colours** (#e0443a red, #2b7de3 blue, #d9a514 yellow, #8a8396 grey): the app's priority rings, used only as rings.
- **Pill colours** (#66499a purple, #dd8c42 orange, #36a078 green, #5b92dc blue): one per feature or project, as 34×16 pills or rings.

### Neutral
- **Night Plum** (#1f1630): page ground.
- **Row White** (#f8f6fb) and **Offer White** (#fdfcfe): task rows and the one offer card.
- **Ink** (#1d1528) and **Ink Soft** (#4b4159): text on lavender and white.
- **On Plum** (#efeaf5) and **On Plum Soft** (#bdb3cd): text on the ground.

### Named Rules
**The One Calm Card Rule.** Each board has at most one white offer card; everything else on it is a task row.
**The Flat Pill Rule.** Pill and ring colours are flat and unmixed: no tints, gradients or opacity washes of them.

## Typography

**Display Font:** Figtree, self-hosted (assets/fonts), with system-ui fallback
**Body Font:** the platform system sans (the app's own face)

**Character:** Figtree's round, open shapes echo the icon's pills; the system sans keeps rows and reading text looking like the app.

### Hierarchy
- **Display** (750, clamp 2.3–3.6rem, 1.02): the H1 on the offer card only.
- **Headline** (720, clamp 1.9–2.8rem, 1.05): section and feature headings.
- **Title** (600, 16px, Figtree): column strips and button labels.
- **Body** (400, 17px, 1.55): copy; reading pages hold 68ch.
- **Label** (400, 13px): row metadata, dates, counts, captions. Figures tabular.

## Layout

A 1360px container with 32px gutters (16px on phones). The hero board is a four-column grid (1fr 1.6fr 1fr 1fr) with 18px gaps: Deferred, Now (wider, holds the offer), Blocked, Review due with Done below. Under 1100px the board becomes two columns with Now first across the top; under 640px one column, side columns trimmed to two rows each. Feature panels are a 0.8fr/1.6fr text-and-screenshot grid, alternating sides, stacking under 1100px. Sections are 88–104px apart on the plum.

## Elevation & Depth

Boards and rows are lifted with soft, offset shadows, never halos or hard block shadows. Strips are flat.

### Shadow Vocabulary
- **Row** (`0 2px 6px rgba(29,21,40,.10), 0 8px 18px -10px rgba(29,21,40,.25)`): task rows and notes.
- **Offer** (`0 4px 10px rgba(29,21,40,.10), 0 22px 40px -22px rgba(29,21,40,.45)`): the offer card.
- **Board** (`0 30px 60px -30px rgba(0,0,0,.6)`): a board panel on the plum ground.
- **Screenshot** (`0 6px 14px rgba(29,21,40,.15), 0 30px 50px -30px rgba(29,21,40,.55)`).

## Shapes

Rounded like the icon: boards 28px, the offer card 22px, rows 16px, buttons, tags and pills fully round. Strips hang from the board's top edge with only their bottom corners rounded (16px), like the icon's header band. Rings are 22px circles with a 2.5px stroke.

## Components

### Buttons
- **Shape:** full pill (999px), 48px tall.
- **Primary:** Header Plum fill, white Figtree 600 label; hover shifts to the purple pill colour.
- **Line:** transparent with a 2px Header Plum inset ring; hover tints to #ece7f3.
- **Focus:** 3px #5b92dc outline, 3px offset, everywhere.

### Task row (signature)
A white row on the board: ring, optional coloured date label (red overdue, brown-orange today, ochre soon, grey otherwise), title, then a 13px path line ("Work › Client onboarding") and optional grey tag pill. Rings in Now are real buttons: ticking fills the ring red with a white check, strikes the title, and moves the row to Done. "Put them back" restores them.

### Column strip
Header Plum band, Figtree 600 16px label on the left, a count on the right in 13px. Done uses Done Green (#186848); the paid column in pricing uses the purple pill colour.

### Feature panel
A lavender board with a strip naming the feature, led by its pill colour, and a yellow "Unlock" pill for paid features; inside, the headline and copy beside a real screenshot.

### Navigation
The top bar is a Header Plum band: icon and "Blaha" left, Support, Forum, Privacy, Licence as pill-hover links right.

## Do's and Don'ts

### Do:
- **Do** start every task row with a hollow ring in a priority or pill colour.
- **Do** put real app screenshots on board panels, at their real aspect.
- **Do** label sample tasks as sample data near the board.
- **Do** keep store links as text buttons (no badge images) and every asset self-hosted.

### Don't:
- **Don't** add device mockups, gradient heroes or rows of equal feature cards.
- **Don't** put a label or eyebrow above a heading; the strip names the panel instead.
- **Don't** use any colour for decoration that is not from the icon or the app's rings.
- **Don't** show a Review screen or name a competing app.
