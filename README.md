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

`{product}-{type}-{variant}-{color}.{ext}`

- lowercase, kebab-case, no spaces, ASCII only
- `type`: `logo` | `icon`
- `variant`: `horizontal` | `stacked` (logos only)
- `color`: `color` | `white` | `black`
- **Never put versions or dates in file names.** Use git tags (`v1`, `v2`, …) for versioning.

Examples:

- `traxcope/logo/traxcope-logo-horizontal-color.svg`
- `traxcope/logo/traxcope-logo-horizontal-white.svg`
- `traxcope/logo/traxcope-icon-color.svg`
- `traxcope/favicon/favicon.ico`

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
