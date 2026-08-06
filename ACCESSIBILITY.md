# Accessibility checklist (WCAG 2.1 AA)

For whoever builds the production version in Sitefinity. This prototype was
built and audited to **WCAG 2.1 Level AA** — the standard for U.S. government
sites under ADA Title II and Section 508. Use this list to keep that standard
through the real build, and again before launch.

The prototype already passes an automated axe-core audit with zero
violations. Automated tools catch only about 30–50% of issues, though, so the
manual checks below matter just as much.

---

## Carry these over from the prototype

The prototype already does all of this. Make sure the Sitefinity widget keeps
it:

- [ ] **Every employee photo has descriptive alt text** — name, title, and
      department (e.g. "Kelly M. Marton, Engineer 4, Cuyahoga County Public
      Works"). In Sitefinity, this usually comes from an "alt text" or
      "caption" field on the image or profile item — make sure that field is
      required so no photo ships without it.
- [ ] **Decorative images use empty alt** (`alt=""`) so screen readers skip
      them — e.g. the small thumbnails in the Roster, where the name is right
      next to them as text.
- [ ] **Text contrast is at least 4.5:1** (3:1 for large text). Do NOT put
      text in bright Flush Orange (`#FF8200`) — it fails at 2.48:1. Use the
      county's text-safe brown (`#9B5000`) for orange text, or navy text on
      an orange background. Bright brand colours are fine for bars, buttons,
      and graphics — just not for the words themselves.
- [ ] **Headings run in order** — one `<h1>` per page, then `<h2>`, then
      `<h3>`, with no skipped levels. Screen-reader users navigate by these.
- [ ] **Everything works by keyboard** — every link, button, filter, and
      roster name is reachable with Tab and operable with Enter/Space. A
      visible focus outline must show which element is selected. Never remove
      focus outlines in CSS without replacing them.
- [ ] **Motion respects the user's setting** — all animation is wrapped so it
      turns off for anyone with "reduce motion" enabled in their OS. Keep
      that wrapper (`@media (prefers-reduced-motion: reduce)`).
- [ ] **Page declares its language** — `<html lang="en">`.
- [ ] **Each page has a unique, descriptive `<title>`.**

---

## Check these in the Sitefinity build

Things that depend on the CMS and the full page, not just this component:

- [ ] **The whole page passes, not just the widget.** Run the live Sitefinity
      page (with the county header, nav, and footer) through an automated
      checker — the free [WAVE tool](https://wave.webaim.org/) or the axe
      DevTools browser extension. Accessibility is a property of the whole
      page.
- [ ] **Landmarks and structure** — the profile section sits inside a `<main>`
      or an appropriately labelled region, not just loose `<div>`s.
- [ ] **Any new interactive widget** (a modal, a carousel, a filter that
      updates results) announces changes to screen readers — usually via an
      `aria-live` region, which the prototype already uses for its result
      count. Confirm it survives the port.
- [ ] **Forms, if added** (e.g. a search box) have real `<label>`s tied to
      their inputs.
- [ ] **Link text makes sense out of context** — "Explore careers" is good;
      "click here" is not. Screen-reader users often pull up a list of just
      the links.
- [ ] **Colour is never the only signal.** If a department is shown by colour,
      it's also shown by its name in text (the prototype does this).

---

## Test before launch

Automated tools are the floor, not the finish line. Before go-live:

- [ ] **Keyboard-only pass** — unplug the mouse. Tab through the whole page.
      Can you reach and operate everything? Can you always see where you are?
- [ ] **Screen-reader pass** — test with a real screen reader:
      [NVDA](https://www.nvaccess.org/) (free, Windows) or VoiceOver (built
      into Mac, `Cmd+F5`). Listen to a few profiles and the hiring graphic.
      Does it make sense with your eyes closed?
- [ ] **Zoom to 200%** — text should reflow and stay readable, nothing cut off
      or overlapping.
- [ ] **Ideally, test with someone who actually uses assistive technology.**
      Nothing substitutes for it. The county's ADA coordinator or a local
      disability-services organisation may be able to help.

---

## Reference

- WCAG 2.1 quick reference: https://www.w3.org/WAI/WCAG21/quickref/
- WebAIM contrast checker: https://webaim.org/resources/contrastchecker/
- WAVE page checker: https://wave.webaim.org/
- Section 508 (federal standard): https://www.section508.gov/

The county likely has its own ADA coordinator and web-accessibility policy —
loop them in early, since they may have specific requirements or a preferred
testing process.
