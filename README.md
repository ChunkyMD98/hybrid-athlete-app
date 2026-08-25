# HYBRID — Hybrid Athlete Tracker

A single-page web app for hybrid athletes: track **running**, **strength**, and **nutrition** in one place, and level up as you go.

**Live app:** _(GitHub Pages URL goes here after deploy)_

## Features
- **Running & strength leveling** — every run and every movement levels on its own, rolled into a Hybrid Index.
- **Nutrition** — calorie and macro targets built from your logged training (not a flat number), with a sex-specific fat floor, protein target, and RED-S / energy-availability guardrails.
- **Recipes & meals** — build a recipe (paste ingredients or import from a URL), auto-price the macros from the free [USDA FoodData Central](https://fdc.nal.usda.gov/) database, then log it by the portion.
- **Breastfeeding support** — adds the calories of milk production to a nursing mother's daily target, with a per-day feed logger.
- **Custom movements** — create your own lift with a primary muscle group and sub-muscles.
- **Installable** — "Add to Home Screen" on your phone for an app-like, offline-capable experience.

## Install on your phone
1. Open the live URL in your phone's browser.
2. **iPhone (Safari):** Share → *Add to Home Screen*. **Android (Chrome):** menu → *Install app* / *Add to Home Screen*.
3. Launch it from the new icon — it runs full-screen like a native app.

## Your data
Everything is stored **locally in your own browser** (`localStorage`) — nothing is uploaded, and each person who opens the app has their own private data. Recipe lookups are the one exception: they call the USDA API using a key you paste into Settings.

## Tech
No build step, no framework, no backend. One `index.html` with inline CSS/JS, plus a web manifest, a service worker for offline use, and PNG icons.

## Recipe lookups (optional)
To auto-fill recipe macros, grab a free API key at [fdc.nal.usda.gov/api-key-signup.html](https://fdc.nal.usda.gov/api-key-signup.html) and paste it into **Settings → Recipe Lookups**. Without a key you can still enter macros by hand.
