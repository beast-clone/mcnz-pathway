# AMC Pathway Blueprint — Landing Page

Bold-editorial landing page for the GooCampus AMC Pathway Blueprint ebook (₹999).

Built with **Astro 5** for **Netlify** deploy.

## Quick preview — no setup needed

Open **[`preview.html`](preview.html)** in any browser. It's a single self-contained file (~72 KB) with the entire landing page including the full chapter reader. You can:

- Download it from GitHub and double-click to open it
- Share it via WhatsApp, email, or any file-sharing app
- Open it offline — only fonts load from the network

This is the easiest way to show the page to the team without cloning or building anything.

## Local development

```bash
npm install
npm run dev
```

Opens at `http://localhost:4321`.

## Production build

```bash
npm run build
```

Output: `dist/`

## Deploy to Netlify

Push the folder to GitHub and connect via Netlify — `netlify.toml` already configures build (`npm run build`) and publish dir (`dist`). No further setup needed.

## File map

```
src/
  pages/index.astro      ← all sections, easy to edit
  layouts/Layout.astro   ← head, meta, fonts, FAQ toggle script
  styles/global.css      ← design tokens + every section's CSS
```

To edit copy or section order, edit `src/pages/index.astro`. The chapter list, stats, testimonials, and FAQ are all arrays at the top of that file.

## Notes

- Fonts: Fraunces (display) + Inter (body), loaded from Google Fonts.
- Palette: warm cream paper (`#F7F2EA`) with AMC red (`#B5251F`) and ochre accents.
- Chapter list shows 9 rows for visual weight — the page copy still says "16 chapters." Add the remaining 7 to the `chapters` array in `index.astro` when ready.
- Author/authority block currently positions GooCampus as the brand. Swap for an individual author when one is confirmed.
- Testimonials use placeholder doctor names. Replace with real, attributed quotes before launch.
