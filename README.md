# michaelpresecan.com

The personal website of **Mihael Presečan** — a one-page portfolio written as a
mathematical proof.

Instead of a CV, the page states a theorem — *"Mihael Presečan can be trusted with
the technical direction of an AI product"* — and discharges it from four lemmas
(**diagnosis, construction, depth, handover**), each backed by dated, named,
linkable evidence. Press **Check the proof** and the page verifies itself, walking
the lemmas one by one to a closing *Q.E.D.* A first-person postscript covers the
things the proof leaves out — books, faith, and Hanna.

🔗 **Live:** https://michaelpresecan.com

## Structure

The entire site is a single self-contained file. There is no build step, no
framework, and no dependencies beyond two web fonts.

```
.
├── index.html   # the whole site — markup, styles, and script inline
├── og-image.png # social-share / Open Graph preview image (1200×630)
└── README.md
```

- **Styles** — plain CSS in a `<style>` block, driven by custom properties
  (`--paper`, `--ink`, `--mark`, …) for the paper-and-ink, academic-preprint look.
  Fully responsive, with `prefers-reduced-motion` and print stylesheets.
- **Script** — a small vanilla-JS block (no libraries) that runs the "check the
  proof" animation, highlights cross-references on click, opens the portrait
  lightbox, and marks lemmas as you scroll past them.
- **Fonts** — [Crimson Pro](https://fonts.google.com/specimen/Crimson+Pro) and
  [DM Mono](https://fonts.google.com/specimen/DM+Mono), loaded from Google Fonts.

## Running locally

No tooling required — just open the file:

```bash
open index.html
```

Or serve it over HTTP (useful so relative asset paths behave like production):

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

Any static host will do (GitHub Pages, Netlify, Cloudflare Pages, S3, …) — deploy
the repository root as-is.

One thing to update if you change hosts: the Open Graph and Twitter Card tags in
`index.html` use **absolute** URLs (`og:url`, `og:image`, `twitter:image`), because
social scrapers require them. Point them at the new host so link previews keep
working.

## Contact

- Email — hello@michaelpresecan.com
- LinkedIn — [michaelpresecan](https://linkedin.com/in/michaelpresecan)
- GitHub — [mpresecan](https://github.com/mpresecan)

---

© 2026 M. Presečan · Set in Crimson Pro & DM Mono
