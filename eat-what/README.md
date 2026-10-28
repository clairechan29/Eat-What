# Eat What? 🍜

An office-lunch decision app (spin the wheel, swipe suggestions, map to the spot).

## Technology
Plain **static HTML + CSS + vanilla JavaScript** in a single `index.html`. No framework, no build step, no dependencies.
Images (logo, blobs, emoji) live in `assets/`. Fonts (Baloo 2, Nunito) load from Google Fonts, so the viewer needs internet.
Screens are switched with URL hashes (`#01`–`#12`), so no server routing is needed.

## Project structure
```
index.html     the whole app
assets/        logo, blobs, emoji PNGs
vercel.json    Vercel settings (static site, caching)
package.json   project metadata (no dependencies)
```

## Run locally
Double-click `index.html`, or run `npm run dev` and open http://localhost:3000

## Deploy on Vercel

### Option A: drag-free via GitHub (recommended)
1. Unzip this project. Create a new repository on github.com and upload the **contents** of this folder (so `index.html` is at the repository root).
2. Go to vercel.com, sign in, click **Add New → Project**, and import the repository.
3. Leave everything default: Framework Preset **Other**, Build Command empty, Output Directory empty (or `.`).
4. Click **Deploy**. Your link looks like `https://eat-what-xxxx.vercel.app`.

### Option B: Vercel CLI
```
npm i -g vercel
cd eat-what
vercel          # follow prompts, accept defaults
vercel --prod   # publish to production
```

### Troubleshooting
- **404 on the homepage:** `index.html` must be at the root of what you deploy, not inside an extra folder. In Vercel, set *Root Directory* to the folder that contains `index.html`.
- **Fonts look different:** Google Fonts failed to load; check your connection.
