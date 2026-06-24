---
title: "Deb-Coin constellation"
date: 2026-06-13
allDay: false
startTime: "04:55"
endTime: "05:30"
area: "Build"
worth: 7
tvm: 15
by: claude
created: 2026-06-13 05:30
cssclasses:
  - nl-doc
---
Built a **force-directed constellation** as Deb-Coin's 4th lens (`Heat · Coins · Bars · Map`) — every Build Log entry is a **square** (Stratosyn identity) that drifts into a **work-type "star system,"** so you *see* where the weight lives: a huge BUILD cluster, with FIX / DESIGN / ORGANIZE / DOCUMENT as their own separated constellations. Each entry springs to its work-type hub; a hand-rolled physics sim (link + charge repulsion + centering on `requestAnimationFrame`) settles it, then freezes. **Drag** any star (it re-energizes and re-settles), **hover** for its label + lit edge, **click** for its coin card. Squares sized by √Đ, hue by work-type, hubs labeled.

Kept the physics in its own module `Scripts/deb-coin-constellation.js` (pure `buildGraph`/`sideFor` + `renderMap`), reusing Deb-Coin's math via `engine.importJs`. Wiring it as a lens turned `deb-coin.js`'s `render` **async** and added the Map chip (period chips + day-cards hide in Map mode, since the map is all-time). **Re-verified every existing lens still renders error-free after the async refactor.**

**Files:** `Scripts/deb-coin-constellation.js`, `Scripts/deb-coin.js` (async + Map lens), `stratosyn.css` (+constellation block), `Deb-Coin.md` (async embed), `web/debcoin/{math.test.mjs,preview.html,shoot.mjs}`; spec + plan `docs/superpowers/{specs,plans}/2026-06-13-deb-coin-constellation*`.
**Why:** Colton wanted the data shown "completely different, more visually" — density/gauge/bar/tape are all grids; the constellation is the body of work as a star map you can grab. Verified: 9/9 harness tests (`buildGraph`/`sideFor`) + a settled-layout screenshot, zero console errors across all five lenses.
**TVM:** base 7 × 15 (built 04:55 — 2–5 AM peak ×13 + 2 built-for-you, ceiling 15) ≈ **ƒ105 effective**. See [[Value Engine]].
