# ZENVORA — Vercel-ready static site

This is a static website package made from the supplied `index.html`.

## Included files

- `index.html` — the complete storefront and its CSS/JavaScript.
- `package.json` — basic npm scripts; no framework or dependencies are required.
- `vercel.json` — Vercel static-site configuration.
- `app.json` — basic app metadata.
- `.gitignore` — ignores local and deployment-only files.

## Run locally

You can simply open `index.html` in a browser.

Optional local server (requires Node.js and an internet connection the first time `npx` downloads `serve`):

```bash
npm run dev
```

## Deploy with GitHub + Vercel

1. Extract this ZIP on your computer.
2. Create a new, empty repository on GitHub.
3. Open the extracted `zenvora-vercel` folder.
4. Upload **the contents of the folder** to the repository root (so `index.html` is at the top level, not buried in another folder).
5. Commit the files to the `main` branch.
6. Sign in to Vercel and choose **Add New → Project**.
7. Import your GitHub repository and authorize access if asked.
8. In project settings, use these values:
   - Framework Preset: **Other**
   - Root Directory: `./`
   - Build Command: leave blank (or use `npm run build`)
   - Output Directory: `./`
   - Install Command: leave blank
9. Click **Deploy**. Vercel will provide a `*.vercel.app` URL.
10. For future changes, commit and push to GitHub; Vercel will redeploy automatically.

## Important: demo storefront, not a live shop backend

The source describes itself as a showcase/demo. Its checkout creates a sample order in the current browser; it does not take payment, send orders to a warehouse, or create real orders. The newsletter form does not send or store email addresses on a server. Account/order data is browser-local. Product prices, stock, shipping and imagery are illustrative.

Before accepting real customers or payments, connect a secure backend, real product/inventory data, an authentication provider, and a payment provider (for example Stripe), and add appropriate privacy, shipping, returns and legal information. Never put secret API keys in this static HTML or in a public GitHub repository.

## External assets

The page loads fonts from Google Fonts and fashion imagery from Unsplash. Those require an internet connection and are not bundled in this ZIP.
