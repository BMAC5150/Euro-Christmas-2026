# Paris · Köln Advent 2026

Travel guide for BMAC and Judy, Nov 30 to Dec 6, 2026. All times are local (CET).

- **[GUIDE.md](GUIDE.md)** is the master itinerary. Change plans there first.
- **[app/](app/)** is the iPhone web app built from it: Today, Days, Bookings, To do, Info.

## Using the app on an iPhone

1. Open the GitHub Pages address in Safari: `https://bmac5150.github.io/euro-christmas-2026/`.
2. Share → **Add to Home Screen**.
3. Open it once from the home screen while online. After that it works offline.

When online, the app loads the newest version; offline it shows the last one it saw.

## Files

| Path | What it is |
|---|---|
| `app/index.html` | The whole app in one file (React is inlined, no network needed) |
| `app/manifest.webmanifest` | Home-screen name, colors and icons |
| `app/sw.js` | Service worker that caches the app for offline use |
| `app/icons/` | Home-screen and favicon icons |
| `.github/workflows/pages.yml` | Publishes `app/` to GitHub Pages on every push to `main` |

## Updating

The app's trip data is written into `app/index.html` (the `DAYS`, `BOOKINGS` and `TODO` arrays). When GUIDE.md changes, update those arrays to match and push to `main`. The workflow redeploys, and phones pick up the new version the next time the app is opened online.

## One-time setup

Settings → Pages → Build and deployment → Source: **GitHub Actions**.
