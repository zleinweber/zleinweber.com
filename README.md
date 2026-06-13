# zleinweber.com

Source for a personal static website built with [Astro](https://astro.build/)
and deployed to Cloudflare Workers static assets.

## Development

Install dependencies:

```sh
npm install
```

Start the local development server:

```sh
npm run dev
```

Build the static site:

```sh
npm run build
```

Run type, formatting, and build checks:

```sh
npm test
```

Format supported project files:

```sh
npm run format
```

Deploy to Cloudflare:

```sh
npm run deploy
```

Cloudflare should serve the contents of `dist/`, configured by
`wrangler.jsonc`.

## Design

The site uses a warm, natural palette built around cream neutrals and muted
forest greens. Blue is reserved for interactive accents so it remains visible
without competing with the primary green theme.

| CSS token             | Hex       | Use                                        |
| --------------------- | --------- | ------------------------------------------ |
| `--color-bg`          | `#FAF8F2` | Page background and light-on-dark text     |
| `--color-surface`     | `#F2F1E9` | Subtle surfaces, including inline code     |
| `--color-text`        | `#39423C` | Primary text and strong dark elements      |
| `--color-muted`       | `#687169` | Secondary text and metadata                |
| `--color-line`        | `#DDDCD2` | Borders and dividers                       |
| `--color-accent`      | `#738F7C` | Decorative forest-green accents            |
| `--color-accent-dark` | `#4B6254` | Green links and small accent text          |
| `--color-blue`        | `#52758B` | Hover, focus, and active navigation states |
| `--color-blue-light`  | `#C9D9DF` | Selected-text background                   |

The canonical tokens are defined in `src/styles/global.css`. The favicon uses
`--color-bg` and `--color-text` as literal SVG colors because CSS variables
from the page are not available inside an externally loaded SVG.
