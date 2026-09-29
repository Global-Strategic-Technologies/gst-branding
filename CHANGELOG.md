# Changelog

Versions are date-based (`vYYYY.MM[.N]`) and tagged in git. Each entry records the
gst-website commit the design system was snapshotted from (see `design-system/SOURCE.json`).

## Unreleased

Brand assets and guidelines synced to gst-website `df882402`
(Global-Strategic-Technologies/gst-website#544). The design system (`design-system/`) is
unchanged and still snapshots `ce8d58f5`.

- **Install icons re-rendered** from `icon.svg`: `web-app-manifest-{192,512}.png` (`any`)
  now carry the GST Mono outline wordmark instead of a fallback sans.
- **New maskable icons** `web-app-maskable-{192,512}.png`: unframed, all ink inside the
  40% safe zone. The website previously reused the `any` icons, which Android's mask clipped.
- **`apple-touch-icon.png`** now uses the maskable composition (white, unframed) so iOS's
  rounded corners don't cut the frame.
- **New per-palette tab icons** in `assets/favicon/palettes/` (`palette-1…6.svg`):
  `favicon.svg` with only the stroke recoloured to each palette's light-theme primary.
- `assets/logo/gst-icon.svg` picks up the note that the PWA icons are rendered from it.
- `guidelines/` re-mirrored from `src/docs/styles/`, including STYLES_GUIDE § Browser
  chrome (tab icon and install icons).
- Asset page shows the maskable and per-palette tab icons; the sync script and drift check
  cover them, plus `favicon.ico`, `apple-touch-icon` and the manifest PNGs.
- `sync-from-website.sh` rewrote guideline links to `blob/main`; now `blob/master`,
  matching the drift check.

## v2026.09 — 2026-09-19

Rebuilt from the gst-website design system (website commit `ce8d58f5`).

- **Brand teal corrected to `#05cd99`** in every delta-icon SVG, favicon/ICO, app icons,
  OG image, LinkedIn assets and the CSS mask data-URIs. The previous assets used the
  stale `#00D9B5`. (Website fix: Global-Strategic-Technologies/gst-website#502.)
- New `index.html` brand-asset page (GitHub Pages) showing every asset in light and dark
  with when/how-to-use guidance.
- New `guidelines/LOGO_USAGE.md`: wordmark spec, minimum size, clear space, backgrounds.
- New vector wordmark (`assets/wordmark/`) generated from the site's `HeaderLogo.astro`
  spec, plus @2x PNGs.
- OG image regenerated in GST Mono from the OG template (the old one was a fallback sans-serif); editable SVG source kept alongside.
- New social templates (`assets/social/templates/`): 1080×1080, 1200×675, 1200×630.
- `guidelines/` now mirrors `src/docs/styles/` from the website; `design-system/` is the
  website's exported bundle (styles, fonts, rendered component cards, screenshots).
- `scripts/sync-from-website.sh` and a CI drift check against `gst-website@master`.
- Removed the 2026-02 logo package (full/stacked/"GS Tech" lockups, legacy brand board).
