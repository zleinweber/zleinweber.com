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

Deploy to Cloudflare:

```sh
npm run deploy
```

Cloudflare should serve the contents of `dist/`, configured by
`wrangler.jsonc`.

