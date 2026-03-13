# hs-math-3-13-2026

Single-file counting exercise for young kids (iPad-optimized).

## Architecture
- Everything lives in `index.html` — HTML, CSS, JS, no build step
- Sound effects use Web Audio API (no external files)
- Hosted on GitHub Pages: https://dmiller1006.github.io/hs-math-3-13-2026/

## iPad / PWA notes
- `apple-mobile-web-app-capable` meta tag alone does NOT work on modern iPadOS
- Must include `manifest.json` with `"display": "standalone"` for fullscreen home-screen launch
- After any manifest changes, user must delete and re-add the home screen icon
- `touch-action: manipulation` on interactive elements to prevent double-tap zoom
- `user-scalable=no` in viewport meta (Safari may still ignore this)

## Deploy
Push to `main` — GitHub Pages auto-deploys from root.
