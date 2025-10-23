# Light — AI Patent Platform (Landing Page)

This repository contains a static, GitHub Pages–ready landing page for **Light** with:
- Luxury **Platinum Silver–Glass** theme + gold accents
- Left glass **sidebar** with collapse/expand toggle
- **CTA** wired to mailto fallback + easy backend hook
- Custom **SVG logo** and **PNG favicons**

## Files
- `index.html` — main landing page
- `light_logo_gold_silver.svg` — logo
- `light_favicon_32.png`, `light_favicon_180.png`, `light_favicon_512.png` — favicons

## Quick Start (Local)
Just open `index.html` in your browser.

## Connect the CTA to a Backend (optional)
In `index.html`, search for:
```js
const FORM_ENDPOINT = "";
const MAILTO_FALLBACK = "hello@light.ai";
```
Set `FORM_ENDPOINT` to your service (e.g., Formspree/Make/Zapier/Cloud Function) that accepts JSON:
```json
{ "name": "Jane Doe", "email": "jane@company.com", "source": "homepage-cta" }
```
If the POST fails or `FORM_ENDPOINT` is empty, the form falls back to `mailto:` with the same info.

## Deploy to GitHub Pages
1. Create a new public repo, e.g. `light-landing`.
2. Upload/commit all files in this folder (including `index.html`).
3. In the repo: **Settings → Pages** → *Build and deployment*:
   - Source: **Deploy from a branch**
   - Branch: **main** / folder: **/** (root)
4. Open the listed URL (e.g., `https://<your-username>.github.io/light-landing/`).

### Custom Domain (optional)
- In **Settings → Pages**, add your domain (e.g. `light.example.com`), and set DNS `CNAME` to `<your-username>.github.io`.
- Add a `CNAME` file at the repo root containing your domain name to keep it persistent across deployments.

## Notes
- Tailwind is loaded via CDN in `index.html` (no build step required).
- To change theme accents (gold/silver), tweak CSS variables in the `<style>` block.
- For SEO, edit `<title>` and `<meta name="description">`.