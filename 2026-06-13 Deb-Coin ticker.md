---
title: "Deb-Coin ticker"
date: 2026-06-13
allDay: false
startTime: "04:25"
endTime: "04:50"
area: "Build"
worth: 6
tvm: 15
by: claude
created: 2026-06-13 04:50
cssclasses:
  - nl-doc
---
Built a **stock-market ticker** atop the Deb-Coin page — a **DCX index** headline (all-time Đ level in gold Fraunces + today's move + %) over a continuously scrolling tape of **work-types as "stocks"** (price = all-time balance, sorted by price). Own reusable module `Scripts/deb-coin-ticker.js` that reuses Deb-Coin's math via `engine.importJs` so the numbers can never diverge. **Today's-move basis** (Colton's call): the ▲ is Đ minted today; since coin only accrues, the tape is **green or flat, never red** — every day's a green day, the only question is how green. Seamless loop = a duplicated track + `@keyframes` translateX 0→−50% (the first keyframes in `stratosyn.css`), duration set from measured width, pause-on-hover, edge fade via `mask-image` (no `backdrop-filter`).

**Files:** `Scripts/deb-coin-ticker.js`, `stratosyn.css` (+ticker block & keyframes), `Deb-Coin.md` (ticker block above the lenses), `web/debcoin/{math.test.mjs,preview.html,shoot.mjs}`; spec + plan `docs/superpowers/{specs,plans}/2026-06-13-deb-coin-ticker*`.
**Why:** Colton wanted the currency to *move* like a market. The DCX makes the whole book a glanceable index; the tape gives each work-type a live "stock." Verified: 7/7 harness tests (added `tickerModel`/`fmtK`) + a zoomed element screenshot, zero console errors.
**TVM:** base 6 × 15 (built 04:25–04:50 — 2–5 AM peak ×13 + 2 built-for-you, ceiling 15) ≈ **ƒ90 effective**. See [[Value Engine]].
