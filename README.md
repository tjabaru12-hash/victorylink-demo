# VictoryLink — Field Ops Demo

A privacy-safe demo build of the VictoryLink field operations app: six core
screens (Login, Dashboard, Voter Engagement, GOTV Tracker, Team, Reports) for
a supervisor + 10 canvassers per polling unit — now installable on iOS and
Android as a home-screen app.

## What's in here

- **`index.html`** — the clickable, wired-up interactive prototype. Real
  state, real interactions, sample data. This is a **PWA (Progressive Web
  App)**: it has a manifest, icons, and a service worker, so once it's hosted
  over HTTPS (e.g. GitHub Pages), phones can install it to the home screen
  and open it like an app — including with no connection.
- **`poster.html`** — a one-page visual overview / spec sheet of the app.
- **`manifest.json`**, **`service-worker.js`**, **`icons/`** — the pieces
  that make `index.html` installable. Leave these alongside `index.html`.

## What this deliberately does NOT do

- No photo capture of voters, at registration or on election day.
- No per-voter GPS / geolocation.
- No payment or compensation tied to an individual voter's turnout.
- The central dashboard only ever sees aggregate, polling-unit-level rollups —
  never a per-voter record.

Election-day "voted" status is self-reported by the voter to the canvasser,
not captured as evidence.

## Viewing it locally

Opening `index.html` straight from disk (double-click) works for browsing
the app, but the "Install to home screen" and offline-caching features only
activate once it's served over HTTPS — see GitHub Pages below.

## GitHub Pages (required for install-to-home-screen)

Push this repo to GitHub, then enable **Settings → Pages → Source: Deploy
from a branch → main → / (root)**. After ~1 minute it's live at:

`https://<your-github-username>.github.io/<repo-name>/`

- **On Android (Chrome):** visiting the link shows an "Install app" prompt,
  or use the strip at the top of the page → **Install App**.
- **On iPhone/iPad (Safari):** tap the Share icon → **Add to Home Screen**
  (iOS doesn't allow apps to trigger this automatically — the app shows a
  banner with these instructions).

Only people you send the link to will ever see it — it isn't listed or
searchable anywhere. Note: GitHub Pages for a **private** repo requires a
paid GitHub plan; on the free plan, Pages only works for public repos (the
repo can still be public while the link itself stays effectively
share-only, since nothing indexes or promotes it).

The poster is reachable at `.../poster.html` off the same link.
