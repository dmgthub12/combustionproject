# Chamberproject.cc — Cloudflare Pages Setup

This repo is configured for **Cloudflare Pages** using a simple static site in `/public`.

## Files in this commit
- `wrangler.toml` — tells Wrangler/Pages to publish the `public/` directory
- `.cfignore` — excludes non-site files from upload
- `public/index.html` — your site entry
- `public/styles.css` — your styles

## Deploy one of two ways

### Option A: Deploy via Git (recommended for Pages)
1. Push this repo to GitHub with this exact structure.
2. Cloudflare Dashboard → **Pages** → **Create project** → Connect your GitHub repo.
3. Set:
   - **Build command**: _leave blank_ (no build step)
   - **Build output directory**: `public`
4. Save and deploy.
5. After first deploy, add the custom domain **chamberproject.cc** under your Pages project → **Custom domains**.

### Option B: Deploy from your machine (Wrangler CLI)
```bash
npx wrangler pages deploy ./public
```

## Common gotcha
- Do **not** run `wrangler deploy` (that is for **Workers**, not **Pages**). Use `wrangler pages deploy`.
