# Faces of Cuyahoga County

An employee-profile section for the Cuyahoga County HR website, plus an
animated graphic explaining the county hiring process. Built as a static
prototype (HTML, CSS, JavaScript) for review and for hand-off to the web
team.

## What's in here

```
index.html          Landing page — links to all three design options
full.html           Option 1 "Full": big header, intro text, department filters, card quotes
simple.html         Option 2 "Simple": slim header, photos + names only, careers call-to-action
roster.html         Option 3 "Roster": big cinematic photos, one at a time, swipe/step through
photos/             The employee headshots (referenced by all versions)
hiring/index.html   The animated hiring-process flow chart
README.md           This file
DEPLOY.md           How to publish it on GitHub Pages
CONTENT.md          How to edit people, photos, and text
```

## Three options to compare

This prototype includes **three design directions** so reviewers can pick:

- **Full** (`full.html`) — the complete concept. A large "Faces of Cuyahoga"
  header with intro text, filter chips to browse employees by department, and
  a short quote on each card.
- **Simple** (`simple.html`) — a streamlined version built to sit lower on a
  page. A thin banner, photos and names only, and a "Your face could be here"
  careers prompt at the end.
- **Roster** (`roster.html`) — a big spotlight photo beside a browsable list
  of everyone, grouped by department. Pick a name and their photo and quote
  take over the stage. Ends with a careers call-to-action.

`index.html` is a landing page that links to all three, plus the hiring
graphic — share that one URL and reviewers can open each option themselves.

## Quick look

To view it without any setup: download the repo, then open `index.html`
in a browser and pick an option. Keep the `photos` folder next to the HTML
files.

## Live version (GitHub Pages)

See **DEPLOY.md** for step-by-step publishing. Short version: in the repo's
**Settings → Pages**, deploy from the `main` branch, root folder. The
landing page appears at `https://YOURNAME.github.io/REPO-NAME/`, the three
options at `.../full.html`, `.../simple.html`, and `.../roster.html`, and the
hiring graphic at `.../hiring/`.

## Design notes

- Colours and typography come from the Cuyahoga County style guide. The four
  seal colours (Orient blue, Fun Green, Flush Orange, Persian Red) appear as
  the banner bar and as per-department accents.
- Bright brand colours are used as graphic elements only. Where a colour has
  to carry text, a darker sibling is substituted so contrast meets
  WCAG 2.1 AA.
- Type is Open Sans (loaded from Google Fonts), the web-available typeface
  from the county's approved list.
- All motion is disabled automatically for anyone who has "reduce motion"
  turned on in their operating system.

## Status

This is a **prototype for review**, not the final CMS build. The county
site runs on Sitefinity; turning this into a live widget is a separate step
that the web team will handle once a direction is approved. The Sitefinity
version is still to be confirmed, which determines whether the widget is a
Razor template or a .NET Core renderer component.

## Still open

- Confirm the exact name of the civil-service body used in the hiring graphic
  ("Personnel Review Commission" is used as a placeholder).
- Mary Thomas is departing; her card stays until a replacement is provided.
- Replace placeholder text in the hiring graphic with final HR copy.
