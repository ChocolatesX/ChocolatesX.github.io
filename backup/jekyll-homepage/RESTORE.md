# Jekyll homepage backup

Snapshot of the GitHub Pages homepage that https://chocolatesx.github.io/ was serving from `main` commit `0e4bcdf3fff17c1541995b87461793903f9e3e0c` on 2026-11-25. That page was Jekyll 3.10 rendering the repository root `README.md` with the default GitHub Pages theme. It is unused. Lumen Dock replaces it at `/`.

## What is in this folder

| Path | What it is |
| --- | --- |
| `README.md` | Byte copy of the repository root `README.md` at that commit. The original file is still at the repository root. |
| `rendered-index.html` | The HTML GitHub Pages actually returned for `/`. |
| `assets/css/style.css` | The theme stylesheet that page loaded from `/assets/css/style.css?v=0e4bcdf3fff17c1541995b87461793903f9e3e0c`. It has no further `url()` assets. GitHub Pages generates this file; it was not stored in the repository. |
| `cdn/anchor-js-4.1.0.min.js` | Copy of the script the rendered page loaded from `https://cdnjs.cloudflare.com/ajax/libs/anchor-js/4.1.0/anchor.min.js` (integrity `sha256-lZaRhKri35AyJSypXXs4o6OPFTbTmUoltBbDCbdzegg=`). It was not part of the repository. |

`/favicon.ico` was referenced only inside an HTML comment and returned HTTP 404. It is not included.

`src/` and `wrangler.jsonc` are not part of this homepage. They stay in their original paths.

## Restore the old homepage

From a checkout of this repository:

1. Remove the Lumen Dock root files: `index.html`, `favicon.svg`, `ASSETS.md`, the cabinet `assets/` directory, and `.nojekyll`.
2. Leave `README.md` at the repository root. If it is missing, copy `backup/jekyll-homepage/README.md` to `README.md`.
3. Commit that change and push it to `main` with a normal push. Do not force-push.
4. Wait until the `pages-build-deployment` workflow succeeds. With `.nojekyll` gone, GitHub Pages runs Jekyll again and republishes `README.md` at `https://chocolatesx.github.io/`, regenerating `/assets/css/style.css`.

The saved `rendered-index.html` and `assets/css/style.css` are the reference copy of the old page. Opening `rendered-index.html` by itself will not load the stylesheet, because that file points at `/assets/css/style.css` on the live host. To view the snapshot locally, serve this backup folder’s parent so `/assets/css/style.css` maps to `backup/jekyll-homepage/assets/css/style.css`, or open the files directly.
