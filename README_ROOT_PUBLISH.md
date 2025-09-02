# Cloudflare Pages — Root Publish Variant

This variant publishes the **repository root** (".") instead of `/public`.
Use it if your repo doesn't contain a `public/` directory.

## Use these settings
- Build command: `npm run build` (no-op)
- Build output directory: `.` (a single dot)
- Root directory: `/`

Or leave build command blank (no build step) and still use output directory: `.`

## Files to include in repo root
- `wrangler.toml` (use this root-publish version)
- `index.html` (your site's entry point)
- `styles.css` (optional)
- `package.json` (provided, for the no-op build)
- `.cfignore`

**Do not** run `wrangler deploy` in Pages. If deploying locally, use:
```bash
npx wrangler pages deploy .
```
