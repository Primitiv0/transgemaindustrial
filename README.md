# Transgema Industrial SRL

Corporate website for Transgema Industrial — a multi-division company spanning
managed IT, heavy transportation, environmental analysis, and project management,
with a commitment to circular-economy and sustainable practice.

The name **Transgema** is a wordplay on *Transportation* + *Gems*, reflected in
the logo: a faceted gem resolving into forward-motion chevrons.

## Structure
- `index.html` — single-page site (all CSS inline; no build step required)
- `images/logo.svg` — primary logo (gem + motion)
- `images/favicon.svg` — favicon
- `CNAME` — custom domain (transgema.com)

## Hosting
Served via GitHub Pages from the `gh-pages` branch. No build or dependencies —
fonts load from Google Fonts; all icons and graphics are inline SVG.

## Contact form
The contact form posts to Formspree (endpoint in `index.html`). Update the
`action` URL if the endpoint changes.

## Bilingual (EN / ES)
The site is fully bilingual with an in-page language toggle (the EN/ES button in
the nav). No separate pages or reload — all text swaps instantly via a small
dictionary in `index.html`. The visitor's choice is remembered between visits
(localStorage).

To edit or add translations: find the `i18n` object near the bottom of
`index.html`. Each English element is tagged with `data-i18n="key"` (plain text),
`data-i18n-html="key"` (text containing markup like line breaks), or
`data-i18n-ph="key"` (input placeholders). Add the matching key to the `es`
dictionary. To add a third language, duplicate the `es` block under a new code
(e.g. `pt`) and extend the toggle logic.
