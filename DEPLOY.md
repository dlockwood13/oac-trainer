# OAC Trainer PWA: deploy to GitHub Pages

Same pattern as the rest of the dlockwood13 PWA portfolio.

1. New public repo, e.g. `oac-trainer`.
2. Put every file in this folder at the repo root (index.html, sw.js, manifest.webmanifest, the four PNG icons).
3. Settings > Pages > Deploy from a branch > `main`, `/ (root)`. Save.
4. After a minute: `https://dlockwood13.github.io/oac-trainer/` (adjust username or repo name if different). All paths are relative, so any repo name works.

## Install
- Android Chrome: menu > Add to Home screen (or the Install app prompt).
- iPhone or iPad Safari: Share > Add to Home Screen.
- Desktop Chrome or Edge: install icon in the address bar.

## Behaviour
- Works offline after the first online load (app shell and fonts are cached).
- Updates: push to `main`; the app fetches the new version on the next online open, no cache-busting needed. To force a clean break, bump `CACHE` in sw.js.
- Data: answers, ratings and the example bank live in the browser's storage, per site and per device. They do not sync. Use "Copy data export" and "Import data" on the Today tab to move data from the claude.ai version, between devices, or as a backup.
