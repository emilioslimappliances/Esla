# ESLA Appliances — Installable Web App (PWA)

This version of the site can be "installed" straight from the browser —
no App Store, no Google Play, no review process. On a phone it adds a
home-screen icon and opens full-screen like a normal app; on desktop
Chrome/Edge it installs as its own window.

## What's included

- `index.html` — the site, with PWA tags added (manifest link, theme
  color, iOS-specific meta tags, service worker registration, and an
  "Install App" button that appears automatically when the browser
  supports it)
- `manifest.json` — app name, colors, icons
- `service-worker.js` — caches the site so it still opens if the phone
  briefly loses signal
- `icons/` — every icon size needed for Android, iOS, and desktop,
  including "maskable" versions Android needs for adaptive icon shapes

## How to make it live

Unlike the single-file version, a PWA needs all these files hosted
**together at the same location** (manifest and service worker must sit
next to index.html).

**Fastest option — Netlify Drop:**
1. Go to app.netlify.com/drop
2. Drag the *entire folder* (not just index.html) onto the page
3. You'll get a live HTTPS URL — PWAs require HTTPS, which Netlify
   gives you automatically

**Also easy — GitHub Pages:**
1. Create a repo, upload all these files keeping the folder structure
2. Settings → Pages → enable, pick the branch
3. Live at `yourname.github.io/repo-name`

## How customers install it

- **Android (Chrome)**: visiting the site shows an "Install App" button
  (the one built into the page) or Chrome's own install banner/menu
  option
- **iPhone (Safari)**: Safari doesn't support the automatic install
  prompt — visitors tap the Share icon → "Add to Home Screen"
- **Desktop (Chrome/Edge)**: an install icon appears in the address bar

## Notes

- This is separate from the native App Store/Play Store project
  (`esla-app.zip`) — that one produces a real listing in both stores;
  this one skips stores entirely and installs directly from the browser.
- If you want both, that's normal — many businesses offer the PWA as the
  fast option and the store app later once it's justified.
