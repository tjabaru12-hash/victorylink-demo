# VictoryLink — Field Ops Demo

A privacy-safe demo build of the VictoryLink field operations app: six core
screens (Login, Dashboard, Voter Engagement, GOTV Tracker, Team, Reports)
for a supervisor + 10 canvassers per polling unit.

## What's in here

- **`index.html`** — a clickable, wired-up interactive prototype. Real state,
  real interactions, sample data. Tuned for touch (iOS/Android tap-target
  sizing, no unwanted zoom on inputs). Open it directly in any browser, or
  serve it via GitHub Pages (see below).
- **`poster.html`** — a one-page visual overview / spec sheet of the app
  (screens, features, data model, staffing math, situation-room dashboard).

## What this deliberately does NOT do

This build excludes the features that raise voter-privacy and election-integrity
concerns:

- No photo capture of voters, at registration or on election day.
- No per-voter GPS / geolocation.
- No payment or compensation tied to an individual voter's turnout.
- The central dashboard only ever sees aggregate, polling-unit-level rollups —
  never a per-voter record.

Election-day "voted" status is self-reported by the voter to the canvasser
(the same way any door-knock or phone-bank GOTV program works), not captured
as evidence.

## Viewing it

Open `index.html` in any browser to try the prototype directly — no build
step, no dependencies, everything is client-side.

## GitHub Pages

Once this repo is pushed to GitHub, enable Pages under
**Settings → Pages → Source: Deploy from a branch → main → / (root)**.
The prototype will then be live at:

`https://<your-github-username>.github.io/<repo-name>/`

and the poster at:

`https://<your-github-username>.github.io/<repo-name>/poster.html`
