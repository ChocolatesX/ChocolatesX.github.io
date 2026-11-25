# Assets

The court, ball, bar, bricks, pickups, shatter, attendant, sky, and stars are original Three.js geometry and materials in `src/arena.ts`. Nothing is a photograph, a generated still, an HDRI, or a downloaded model.

`public/favicon.svg` is an original mark: an ink rounded rectangle, a teal bar, and a hot circle. It has no letters and no third-party icon.

There are no image, video, or audio files. Hits are synthesized with the Web Audio API after the player starts a round.

## Fonts

Loaded locally from Fontsource (no font CDN). Vite bundles the woff2 files, plus the woff fallbacks those CSS files reference.

| Family | Weights | Package files |
| --- | --- | --- |
| Syne | 700, 800 | `@fontsource/syne/files/syne-latin-700-normal.woff2`, `syne-latin-800-normal.woff2`, `syne-latin-ext-700-normal.woff2`, `syne-latin-ext-800-normal.woff2`, `syne-greek-700-normal.woff2`, `syne-greek-800-normal.woff2` |
| Sora | 400, 500, 600 | `@fontsource/sora/files/sora-latin-400-normal.woff2`, `sora-latin-500-normal.woff2`, `sora-latin-600-normal.woff2`, `sora-latin-ext-400-normal.woff2`, `sora-latin-ext-500-normal.woff2`, `sora-latin-ext-600-normal.woff2` |
| Share Tech Mono | 400 | `@fontsource/share-tech-mono/files/share-tech-mono-latin-400-normal.woff2` |

## Packages

- [three](https://www.npmjs.com/package/three) — MIT. License text: `node_modules/three/LICENSE`.
- [@fontsource/syne](https://www.npmjs.com/package/@fontsource/syne) — SIL Open Font License 1.1. `node_modules/@fontsource/syne/LICENSE`.
- [@fontsource/sora](https://www.npmjs.com/package/@fontsource/sora) — SIL Open Font License 1.1. `node_modules/@fontsource/sora/LICENSE`.
- [@fontsource/share-tech-mono](https://www.npmjs.com/package/@fontsource/share-tech-mono) — SIL Open Font License 1.1. `node_modules/@fontsource/share-tech-mono/LICENSE`.
- [vite](https://www.npmjs.com/package/vite) and [typescript](https://www.npmjs.com/package/typescript) are dev dependencies.

The SIL Open Font License 1.1 is also published at <https://openfontlicense.org/> and <http://scripts.sil.org/OFL>.

No third-party icons are used.
