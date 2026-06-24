---
title: "Deb-Coin density page"
date: 2026-06-13
allDay: false
startTime: "02:25"
endTime: "04:21"
area: "Build"
worth: 9
tvm: 15
by: claude
created: 2026-06-13 04:21
cssclasses:
  - nl-doc
---
Built **Deb-Coin** — Colton's rebrand of the in-vault currency (1 **Đ** = 1 effective florin, `worth × TVM`) as its own page that reads the *same* Build Log data, no duplication. The point is **macro density**: scan a month or week and see which day blazed and which was quiet at a glance. Full pipeline in one sitting — brainstorm → spec → plan → build → verify. Three toggleable lenses over per-day Đ (Wk/Mo/Qtr): a **Heat** calendar (square tiles, `color-mix` fill by value, hue = the day's dominant work-type), **Coins** (an SVG coin that fills by value), and **Bars** (stacked by work-type, best day flagged gold). **Tap a day → its coin cards** slide in — medallion + Fraunces-italic title + `ƒworth × ×TVM = Đeff` + the entry's excerpt (lazy `cachedRead`) + open ↗.

Engineered to the vault's grain: one ES module `Scripts/deb-coin.js` with a **pure, testable core** (TVM math copied verbatim from `ledger.js` so the two can never disagree), SVG via `createSvg` (no `innerHTML`), Stratosyn tokens (squares = identity, circles = state, no `backdrop-filter`). **Verified before it touched the live vault:** a node math harness (`web/debcoin/math.test.mjs`, 4/4, asserts per-day totals match the ledger) and a Playwright screenshot harness (`web/debcoin/shoot.mjs`, all three lenses, zero console errors). The harness also **caught two bugs** (wikilink aliases; the Đ mark blurring into digits — now a muted unit span) and surfaced a **double-counted campus entry** in the currency, which Colton had me dedupe (all-time corrected to Đ1587).

**Files:** `Deb-Coin.md`, `Scripts/deb-coin.js`, `stratosyn.css` (+Deb-Coin block), `web/debcoin/{math.test.mjs,shoot.mjs,preview.html}`; spec + plan `docs/superpowers/{specs,plans}/2026-06-13-deb-coin*`. Linked from the Build Log hub. See [[Value Engine]].
**Why:** The Build Log's table + bar-chart couldn't answer "was today good or bad" at a glance — Deb-Coin makes the day's density the headline and the per-entry coins the drill-down. Colton's idea, his rebrand, his "all three lenses" call.
**TVM:** base 9 × 15 (built 02:25–04:21 — the 2–5 AM peak ×13 + 2 built-for-you, ceiling 15) ≈ **ƒ135 effective**. Note: the late-night peak pushes this past the campus map's ƒ84 on *effective* value, but its base worth (9) stays below the campus's (12) — the campus is still the rarer build; the multiplier just rewards the ungodly hour, exactly as the engine intends. See [[Value Engine]].
