---
title: "Stratosyn Ambient — live desktop wallpaper, both displays"
date: 2026-06-20
allDay: false
startTime: "18:10"
endTime: "21:37"
area: "Build"
worth: 13
tvm: 3
by: claude
created: 2026-06-20 21:37
cssclasses:
  - nl-doc
---
Built **Stratosyn Ambient** — a bespoke *live* desktop wallpaper for Colton's Mac, animating on **both** displays (the 2560×1080 ultrawide + the 1080×1920 portrait). The brief: "a corporate office but I made it so it's perfect," with the art living in the screen edges that stay exposed around a Stage-Manager-centred window.

The load-bearing engineering was the renderer. macOS won't animate a custom wallpaper natively, so the motion needs a live host. First reach was **Plash** (Mac App Store) — but its own in-app help text admits it renders on **one display only**, which is why it kept landing on the ultrawide *or* the portrait, never both. Pivoted to **Übersicht**, whose scripting dictionary exposes a per-widget `showOnAllScreens` property — set it true (via AppleScript; note its `count of widgets` verb errors, so address `widget 1` by index) and one responsive vanilla-`<canvas>` widget renders on every screen, each sizing itself to its own viewport. No build step, GPU-friendly (baked static frame + ~300 particle draws + a 9-cell hero).

The design arc was a tight back-and-forth with Colton, and the **taste signal is the real artifact**: he steered hard toward **dim · shadow-based · squared**, and away from **bright · glowing · radial/"space-looking."** Path: squared rounded-rect border (outer + inner hairline frames) with a multicolor particle band that **hugs the rectangle** (box-distance exposure, killed the radial cosmic falloff) and two light "runners" orbiting the perimeter → the band **narrowed by half** to cling to the very edge. A centred **square-mosaic wordmark** (real letterforms rasterised to an offscreen canvas, sampled on a grid, one rounded brand-square per covered cell — so "more squares = more detail" is just a finer pitch) was built, refined to a fine multicolor mosaic… then **scrapped at his call**. It became a dead-centre **3×3 brand-square group cycling three colored animations** — **cyan pulse · gold jiggle · green wave** — rendered with **black drop-shadows** (the elevation grows the shadow blur/offset, so motion reads as *lift*, not light), tuned progressively dimmer.

Every iteration was verified headlessly through **Playwright** at both aspect ratios (no JS errors, crops of the hero at each animation phase) before pushing live and reloading the widget. Also installed and configured **Rectangle** (`gapSize` = 28px) so more of the border band shows around tiled windows — macOS's native *"Tiled windows have margins"* was already on but is a fixed ~8px with no size control, hence the third-party manager.

**Files:** `web/wallpaper/stratosyn-ambient.html` (source-of-truth / browser preview); the deployed **Übersicht widget** `~/Library/Application Support/Übersicht/widgets/stratosyn-ambient.jsx`; mirror at `~/.config/debelloai-wallpaper/`. Memory: `stratosyn-ambient-wallpaper`.
**Why:** a daily-driver desktop that's unmistakably *his* system — the Stratosyn squares-only language, the deep-navy void, the brand mark breathing in the centre — and that's engineered to occupy exactly the pixels Stage Manager + the auto-hide Dock leave exposed. The captured taste rule (dim/shadow/squared) should shorten every future "tweak my visuals" loop.
**Note:** live on both screens via Übersicht `showOnAllScreens`; Plash rejected (single-display). Rectangle needs an **Accessibility** grant on first use before the 28px gap takes effect. To tweak: edit the `.jsx`, `reload widget 1`, re-assert `showOnAllScreens`. Keep the `.jsx` and the repo `.html` in sync.
**TVM:** base 13 × 3 (evening build) ≈ **ƒ39 effective**. See [[Value Engine]] · [[Deb-Coin]].
