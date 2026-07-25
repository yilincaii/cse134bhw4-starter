# HW4 Starter Kit — The CSE Cheese Society

Read the assignment spec first. This folder is everything you need:

- `layouts/` — the nine layout demos from class. Your pages are **built from
  these**: copy the assigned demo, extend it, improve it. View source; the
  explanation is a comment in each file's `<head>`.
- `content/` — all the words for every page. Use this text as given.
  - `cheese.txt` — the HW3 guide (becomes `guide/index.html`)
  - `families.txt` — one section per family page
  - `about.txt` — history + board bios for `about.html`
  - `join.txt` — form copy and dialog copy for `join.html`
- `images/` — SVG illustrations: one per cheese family, a logo, and a sad
  cheese for your 404 page.

## Getting started

1. Make a new git repo. Build the directory structure from the spec.
2. Start with the shared skeleton (header / nav / main / footer) and
   `styles/tokens.css` + `styles/global.css` — steal from `layouts/vars.css`,
   `layouts/global.css`, and your HW3 tokens.
3. Build one page at a time from its assigned demo. Commit as you go.
4. Serve locally — view transitions do not fire from `file://`:

   ```sh
   python3 -m http.server 8000
   ```

5. Deploy early to Netlify or Cloudflare Pages; don't leave it for the last night.

Cheese responsibly.
