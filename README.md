# Beyond Brazil

A four-page responsive travel guide to Brazil, written for someone in Ireland planning
a first trip there.

Built for the Web Design Assignment, Module 1, UCD Professional Academy Professional
Diploma.

Live site: https://danielmurphy2022.github.io/brazil-travel-guide/

## Pages

| Page | File | What is on it |
|---|---|---|
| Home | `index.html` | Hero, three routes into the site, quick facts, three photographs |
| Destinations | `html/destinations.html` | Image gallery, six destinations with an "at a glance" list each, the World Heritage table, photo credits |
| Culture | `html/culture.html` | Music, football, Carnival with the video, food, a few Portuguese phrases |
| Plan your trip | `html/plan-your-trip.html` | Flights from Ireland, a seasons table, money, plugs, official advice |

There is also a `404.html` in the root. GitHub Pages serves it automatically when an
address does not exist, so a mistyped link still lands on a page with the menu on it.

## Tech stack

- HTML5, using the semantic elements: `header`, `nav`, `main`, `section`, `article`,
  `footer`, `address`
- CSS3 in one external stylesheet, `css/style.css`. No inline styles, no `<style>`
  blocks and no `<font>` tags anywhere. Custom properties for the colours, spacing and
  type sizes; CSS Grid for the gallery; CSS transitions for the hover states.
- Bootstrap 5.3.3 from a CDN, the stylesheet only, for the grid and the navbar layout.
  It uses an `integrity` hash so the browser can check it has not been altered.
- Two fonts from Google Fonts: Fraunces for headings, Libre Franklin for body text.
- No JavaScript at all, not mine and not anyone else's. The menu that opens on a phone
  is a checkbox and a few CSS rules, so there is no `<script>` tag on any page.

## Folder structure

```
brazil-travel-guide/
├── index.html      home page (has to stay in the root for GitHub Pages)
├── 404.html        error page (also served from the root)
├── html/           the three content pages
├── css/style.css   the stylesheet
├── images/         14 photographs and the SVG logo
├── docs/           site map, wireframe and the list of sources
└── README.md
```

## Responsive layout

Written mobile-first: the base CSS is the phone layout and the `min-width` media queries
add the wider layouts on top, at 576px, 768px and 992px.

- No horizontal scrolling at 375px on any page.
- Both tables sit in a wrapper that scrolls sideways on its own, so the page does not.
- Images use `max-width: 100%` with `aspect-ratio` and `object-fit`, so they keep their
  shape at any size.

## Accessibility

- Skip link to jump past the navigation
- Alt text on every image, checked against the actual photograph
- One `h1` per page, and no skipped heading levels
- `aria-current="page"` on the current menu item, `aria-label` on the nav
- Breadcrumbs on the three inner pages
- Visible focus outlines for keyboard users
- Every text colour checked against WCAG 2.1 AA
- Gallery captions always show on touch screens, where there is no hover
- The scrolling table wrappers can be focused, so they work without a mouse
- Portuguese words carry `lang="pt-BR"` so a screen reader says them properly
- `prefers-reduced-motion` is respected

## Assignment features

- [x] Meta tags on every page
- [x] A page using a table for real tabular information (there are two)
- [x] E-mail link in the footer contact section
- [x] External link to a working, relevant site
- [x] Consistent banner and logo area
- [x] Consistent main navigation
- [x] External stylesheet
- [x] Bootstrap for the responsive layout and the navigation, stylesheet only
- [x] HTML and CSS only, with no JavaScript on any page
- [x] Bonus features: CSS image gallery, CSS transitions and an embedded video
- [x] Works in Chrome, Edge and Firefox
- [x] Mobile-first

## Checks

The HTML on all five pages and the stylesheet both pass the W3C validators with no
errors. Internal links, images and in-page anchors were all checked, along with the
external links and the video.

Checked in Chrome, Microsoft Edge 150 and Firefox 153. All three render the pages the
same, including the fonts, the image gallery and the World Heritage table.

## Credits

Photographs come from Wikimedia Commons under Creative Commons licences. Facts come from
UNESCO and the Department of Foreign Affairs. The full list is in
[`docs/SOURCES.md`](docs/SOURCES.md).

## Author

Daniel Murphy — DanoMurphy@live.ie
