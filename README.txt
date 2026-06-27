MONEE — Salary Budget (Progressive Web App)
===========================================

A single-page budgeting app: plan each pay cycle across categories, log
spending, and watch your free cash flow. Everything is stored on your own
device (no servers, no accounts, works offline). First launch walks you
through a one-time setup (currency + payday); after that it's ready to use.

-------------------------------------------------------------------
FILES IN THIS FOLDER
-------------------------------------------------------------------
  index.html             Page markup (links the stylesheet + script below)
  styles.css             All styling (base type, animations, scrollbars)
  app.js                 The application, bundled (compiled from source)
  manifest.webmanifest   PWA metadata (name, colors, icons)
  sw.js                  Service worker — offline caching
  icon-192.png           App icon (Android / general)
  icon-512.png           App icon (install splash, hi-res)
  icon-180.png           App icon (iOS home screen)
  README.txt             This file

Upload ALL of these together, keeping them in the same folder. They are
referenced by relative paths, so they must stay side by side.

-------------------------------------------------------------------
DEPLOY TO GITHUB PAGES
-------------------------------------------------------------------
  1. Create (or open) a repository, e.g.  monee
  2. Add the files above to the repo root (or a /docs folder).
  3. Repo  ->  Settings  ->  Pages.
  4. Source: "Deploy from a branch". Branch: main, folder: /(root)
     (or /docs if you put the files there). Save.
  5. Wait ~1 minute. Your app is live at:
        https://<your-username>.github.io/<repo>/

  Updating later: replace the files and push again. Because the service
  worker caches aggressively, after deploying a new version just reload
  the page once or twice (or reopen the installed app) to pick it up.
  The cache name is bumped on each release so old assets are cleared.

-------------------------------------------------------------------
INSTALL ON YOUR PHONE
-------------------------------------------------------------------
  iPhone / iPad (Safari):
    1. Open the Pages URL in Safari.
    2. Tap Share  ->  "Add to Home Screen"  ->  Add.
    3. Launch it from the home-screen icon (runs full screen, offline).

  Android (Chrome):
    1. Open the Pages URL in Chrome.
    2. Tap the  ⋮  menu  ->  "Install app" / "Add to Home screen".
    3. Launch it from the home-screen icon.

-------------------------------------------------------------------
YOUR DATA
-------------------------------------------------------------------
  Stored locally in the browser (localStorage) on each device — it is not
  synced or uploaded anywhere. Use Settings -> Backup -> Export to save a
  JSON copy, and Import to restore it (handy when moving to a new phone).
  Settings -> Reset all data wipes everything and returns to first-run setup.
