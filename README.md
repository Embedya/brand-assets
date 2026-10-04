# Embedya Brand Assets

Official logos, favicons and color definitions for Embedya and its products.
Files in this repository are served publicly and referenced by external services
(e.g. Cryptlex customer/reseller portals), so **paths must stay stable**.

## Structure

```
<product>/
├── logo/      # full logos and icon-only marks
├── favicon/   # favicon.ico, PNG favicons, apple-touch-icon
└── colors.json
```

Products: `embedya/`, `traxcope/`

## Naming convention

`{product}-{type}[-{layout}]-{style}.{ext}`

- lowercase, kebab-case, no spaces, ASCII only
- `type`: `icon` (symbol only) | `logo` (symbol + wordmark)
- `layout` (logos only): `horizontal` (tight crop) | `square` (centered on a square canvas)
- `style`:
  - `color` — transparent background, for **light** backgrounds
  - `white` — transparent background, for **dark** backgrounds
  - `light-bg` — includes a solid light background
  - `dark-bg` — includes a solid dark background
- **Never put versions or dates in file names.** Use git tags (`v1`, `v2`, …) for versioning.

Current Traxcope files (`traxcope/logo/`):

| File | Use |
|---|---|
| `traxcope-icon-color.svg` | Icon on light backgrounds |
| `traxcope-icon-white.svg` | Icon on dark backgrounds |
| `traxcope-icon-light-bg.svg` / `-dark-bg.svg` | Icon with solid background (avatars, app tiles) |
| `traxcope-logo-horizontal-color.svg` | Main logo on light backgrounds |
| `traxcope-logo-horizontal-white.svg` | Main logo on dark backgrounds |
| `traxcope-logo-horizontal-light-bg.svg` / `-dark-bg.svg` | Main logo with solid background |
| `traxcope-logo-square-*.svg` | Same styles, square canvas (social, previews) |

## File requirements

| Asset | Format | Notes |
|---|---|---|
| Logo | SVG (preferred) + PNG | Transparent background, trimmed, no padding |
| Icon | SVG + PNG (512×512) | Square |
| Favicon | ICO (16/32/48) + PNG 32×32 | |
| Apple touch icon | PNG 180×180 | Non-transparent background |

## Usage (public URLs)

Pinned to a release tag (recommended for external services):

```
https://cdn.jsdelivr.net/gh/Embedya/brand-assets@v1/traxcope/logo/traxcope-logo-horizontal-color.svg
```

Do not use `raw.githubusercontent.com` URLs — SVGs are served as `text/plain` and will not render.

## Updating an asset

1. Replace the file **in place** (same path, same name).
2. Commit and create a new tag (`v2`).
3. Update the tag in URLs used by external services when ready.

## License

See [LICENSE.md](LICENSE.md). All logos are trademarks of Embedya.
