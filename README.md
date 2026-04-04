# tharunipages

Minimal static website starter for Tharuni, configured for Cloudflare Workers
Static Assets.

## Project Layout

- `public/index.html`: editable landing page starter
- `wrangler.jsonc`: Cloudflare deployment config
- `package.json`: local preview and deploy scripts

## Local Development

1. Install dependencies:

   ```bash
   npm install
   ```

2. Run the local preview server:

   ```bash
   npm run dev
   ```

3. Open the local URL printed by `wrangler`.

## Cloudflare Setup

1. Push this repo to GitHub.
2. In Cloudflare, open `Workers & Pages`.
3. Import the GitHub repository.
4. Choose `main` as the production branch.
5. Confirm Cloudflare detects `wrangler.jsonc` and deploys the Worker with static assets from `public/`.
6. Use the generated `*.workers.dev` URL as the first live hostname.

This repo does not need a GitHub Actions deploy workflow. Cloudflare can build
and publish directly from GitHub on the free plan.

## Optional Manual Deploy

If you want to deploy from your machine instead of Cloudflare Git integration:

```bash
npm run deploy
```

That requires authenticating `wrangler` with your Cloudflare account first.
