# hs-math

Interactive math exercises for young kids (iPad-optimized).

## Architecture
- `index.html` — launcher/menu linking to all exercises
- Each exercise is a self-contained single HTML file (HTML + CSS + JS, no build step)
- Sound effects use Web Audio API (no external files)
- Hosted on GitHub Pages: https://dmiller1006.github.io/hs-math/

## Exercises
- `counting-circles.html` — tap circles to match a number (10–30)
- `simple-math.html` — addition & subtraction with single digits (modes: addition, subtraction, all)

## iPad / PWA notes
- `apple-mobile-web-app-capable` meta tag alone does NOT work on modern iPadOS
- Must include `manifest.json` with `"display": "standalone"` for fullscreen home-screen launch
- After any manifest changes, user must delete and re-add the home screen icon
- `touch-action: manipulation` on interactive elements to prevent double-tap zoom
- `user-scalable=no` in viewport meta (Safari may still ignore this)

## Conventions
- Each exercise has: Check button, Clear button, confetti + sound on correct, auto-advance after 2s
- Back-to-menu link at top-left of each exercise
- Settings checkboxes for difficulty toggles

## Deploy
Push to `main` — GitHub Pages auto-deploys from root.
