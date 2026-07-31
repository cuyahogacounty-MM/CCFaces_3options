# Editing content

There are three versions of the page — `full.html`, `simple.html`, and
`roster.html` — plus the `index.html` landing page. **The people list lives in
all three,** so if you add, remove, or change a person, make the same edit in
each file to keep them in sync. (They were built to share the same roster.)

Note: `full.html` and `simple.html` use a `pull` quote field; `roster.html`
uses it for the large on-screen quote. Keep the data consistent across all
three.

Everything is inside the HTML file — no build tool. Edit, save, and refresh
the browser (or commit to update the live site).

## The people

Near the bottom of each version file (`full.html` / `simple.html`), inside the `<script>`, there's a list called
`PEOPLE`. Each person is one block:

```js
{
  name: "Kelly M. Marton, P.E., P.S.",
  title: "Engineer 4 — Planning",
  department: "Public Works",
  family: "works",
  photo: "photos/kelly-marton.jpg"
}
```

- **name / title / department** — shown on the card.
- **family** — sets the card's accent colour. Valid values:
  `hhs`, `safety`, `works`, `fiscal`, `dev`. (See the `FAMILIES` list just
  above `PEOPLE` for the label and colour of each.)
- **photo** — path to the headshot. Leave it as `""` to show an initials
  placeholder instead (useful while waiting on a photo or HR approval).

### To add a person

Copy an existing block, paste it into the list, and change the values. Add
their photo to the `photos` folder first.

### To remove a person

Delete their block. If nobody else references their photo, you can delete the
image from `photos` too.

## The photos

Headshots are cropped to **900 × 1125** (a 4:5 portrait) with the face
centred and the eyes about a third of the way down. If you add someone, match
that framing so the grid stays even. Keep the original full-size photos
somewhere safe in case a different crop is ever needed.

## The headline and footer

- The banner title is in the `<h1>` near the top of the `<body>`.
- The footer call-to-action ("Your face could be here." etc.) is in `simple.html`, in the
  `<section class="cta-bar">` block. The **Explore Careers** button links to
  `#` — change that `href` to your county careers page URL.

## The hiring graphic

Text for the flow chart lives in `hiring/index.html`, in the `NODES` object
near the top of its `<script>`. Edit a label there and it updates in the
diagram. The comment above it explains the layout if you need to add a step.
