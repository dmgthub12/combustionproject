# Chamberproject.cc — Cloudflare Pages (No-Build) Repo

This repo is set up for **Cloudflare Pages** using a static site in `/public`.

## Files
- `wrangler.toml` — tells Pages to publish the `public/` directory
- `.cfignore` — keeps non-site files out of uploads
- `package.json` — provides a no-op `build` script for Pages
- `public/index.html`, `public/styles.css` — your site

## Cloudflare Pages Settings (Git deploy)
In the Pages project settings, set:
- **Build command:** `npm run build`  *(runs a safe no-op)*
- **Build output directory:** `public`
- **Root directory:** `/`

> Do **not** use `wrangler deploy` in Pages. If you ever want to deploy locally, run:
>
> ```bash
> npx wrangler pages deploy ./public
> ```

After first deploy, add **chamberproject.cc** under **Custom domains**.
