# Anas Farooq  AMP Blogger Theme

A lightweight AMP-compatible Blogger theme focused on reading clarity, fast load, and simple customization. Uses the Courier Prime font and a responsive header that preserves the desktop header/search layout for tablets and medium screens.

## About
This is a single-file Blogger/AMP template (`theme.xml`) designed for speed and ease of editing. Main highlights:
- Clickable header title (`h1.navbar-brand`) showing "Anas Farooq".
- Desktop navigation + compact mobile hamburger menu.
- Mobile search aligned to the post column.
- Google font: Courier Prime.
- JSON-LD structured data for `WebSite` and `Person`.
- Sidebar and dark-mode toggle removed for a clean reading layout.

## Features
- AMP-ready markup and AMP component usage only.
- Desktop header/search visible at widths >= 601px; mobile behavior (hamburger/search) active at <= 600px.
- Mobile menu anchored directly under the hamburger.
- Minimal CSS using Spectre.css plus targeted overrides.

## Installation (Blogger)
1. Backup current theme: Theme  three-dot menu  Backup  Download theme.
2. In Blogger: Theme  three-dot menu  Restore  Upload. Choose `theme.xml`.
3. After upload, open your site on desktop and mobile to verify layout and AMP validation.

Notes:
- This is an AMP template. NonAMP widgets or custom JavaScript may break validation.
- If upload fails, ensure `theme.xml` is UTF-8 with no BOM and that the XML is intact.

## Quick Customization
Open `theme.xml` in a text editor and search/edit:
- Site title: `<h1 class='navbar-brand'>`  change text or anchor `href`.
- Desktop nav: `<nav class='nav-menu'>`  update `<li class='nav-item'>` entries.
- Mobile menu: `<div class='mobile-menu' id='mobile-menu'>` inside header  update links.
- Font: Google Fonts link near the top (`Courier Prime`)  change or add weights.
- Breakpoint: header/search mobile rules use `max-width:600px` / `min-width:601px`  change these values to adjust when mobile header applies.

## Accessibility
- Mobile toggle includes `aria-controls` and `aria-expanded`. Add `aria-label` if desired.
- Ensure meaningful link text in navigation for screen readers.

## Troubleshooting
- Mobile menu not opening: Ensure the inline `toggleMobileMenu()` script exists and `#mobile-menu` is present.
- Styling not updating: clear browser cache or append `?m=1` when testing.
- AMP validation errors: check Chrome DevTools Console or use the AMP Test tool.
- Upload rejects theme: check file encoding (UTF-8) and remove stray characters before XML prolog.

## Tips
- Keep a local backup before editing the theme in Blogger.
- For spacing/padding tweaks edit the inline CSS block near the top of `theme.xml`.
- To rename the site title in multiple places search for `Anas Farooq` inside the file.

## License & Credits
- Uses Spectre.css v0.5.7 (MIT).
- Font: Courier Prime (Google Fonts).
- You may modify and redistribute this theme; attribution is appreciated.
