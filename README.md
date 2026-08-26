# OM Photography — Omer Mahmoud

A single-file, self-contained landing page. Open `index.html` in a browser, or
host the whole folder on GitHub Pages / any static host.

## Folder contents
- `index.html` — the entire site (HTML + CSS + JS inline)
- `photos/` — images used by the page
  - `omer.jpg` — Omer's real photo (used in the hero + About portrait)
  - `party1/2`, `event1/2`, `candid1/2`, `portrait1` — **placeholder** gallery
    tiles (coloured gradients labelled "replace with your photo")

## Replacing the placeholder gallery photos later
Each gallery tile in `index.html` looks like this:

```html
<div class="tile" data-cat="parties" data-img="photos/party1.jpg">
  <img src="photos/party1.jpg" alt="Party photography" loading="lazy" />
  <span class="cat">parties</span>
</div>
```

To use a real photo, just drop your image into `photos/` and update BOTH the
`src` and the `data-img` to point at it (keep `data-cat` so the filter and the
click-to-enlarge lightbox keep working). You can add more tiles by copying the
block. Categories: parties, events, portraits, candid.

The hero and About portrait both use `photos/omer.jpg` — swap that file (or the
`src`) any time.

## What works
- Sticky nav with active-section highlight + mobile hamburger
- Gallery filter (All / Parties / Events / Portraits / Candid) + lightbox
- Services cards with per-category accent colours
- Call + WhatsApp buttons wired to +44 7586 024878
- Scroll-reveal animation (respects reduced-motion), responsive to mobile

## Hosting on GitHub Pages
Push the whole folder (index.html + photos/) to a repo, then Settings → Pages →
deploy from branch. Placeholder social links (Instagram, email) in the footer
need real URLs; WhatsApp is already live.
