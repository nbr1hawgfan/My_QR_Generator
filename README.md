# QR Forge

A tiny, installable QR code generator. Type anything — a link, a note, a wifi
password — and it renders a live QR code you can save as a PNG. Everything
happens in the browser; nothing you type is sent anywhere.

## Files

- `index.html` — the whole app (markup, styles, logic)
- `manifest.json` — makes it installable as a PWA
- `sw.js` — minimal offline caching
- `icon.svg`, `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` — app icons

## Run it locally

Just open `index.html` in a browser. No build step, no dependencies to install.

## Deploy to GitHub Pages

1. Create a new repo (e.g. `qr-forge`) and push these files to it, or drop
   them into an existing GitHub Pages repo.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`,
   pick your default branch (usually `main`) and the `/ (root)` folder.
4. Save. GitHub gives you a URL like `https://yourusername.github.io/qr-forge/`
   within a minute or two.

## Install as an app

Once it's live on GitHub Pages (PWAs need HTTPS, so this won't work from a
local file), open the URL on your phone or desktop and use your browser's
"Install app" or "Add to Home Screen" option. After that it opens in its own
window and works offline.

## Notes

- QR rendering uses the `qrcodejs` library from cdnjs — swap the `<script>`
  tag in `index.html` if you'd rather vendor it locally.
- The download button reads the canvas `qrcodejs` renders internally, so no
  server round-trip is needed to produce the PNG.
- Error correction levels: Low fits the most data per code; High survives
  the most damage/obstruction but stores less data. Medium is a good default.
