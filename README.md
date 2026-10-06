# 75 HARD — Reinvention Tracker

A single-file personal habit tracker. No build step, no backend, no login.
Open `index.html` and it works.

## On your phone

1. Open the Pages URL in Safari.
2. Share → **Add to Home Screen**.

It then launches fullscreen like a normal app and works without signal.

## How it stores data

Everything lives in `localStorage` on the device you use it on. Nothing is
uploaded anywhere, which also means the phone and the laptop keep separate logs.

Back up from **Settings → Export backup**: it opens the iOS share sheet so you
can save the file to Files or mail it to yourself. **Copy backup as text** is the
fallback that always works. Either one can be loaded again from the same screen.

## Habits are data, not schema

The habit list is editable in Settings — add, rename, reorder, delete. Scores are
always out of however many habits currently exist, so changing the list mid-challenge
doesn't break anything. Deleting a habit leaves past logs untouched; it just stops
counting toward scores.

## Editing the app

`index.html` holds the markup, styles and logic. After changing it, bump `CACHE`
in `sw.js` so phones already running the old version pull the new one down.
