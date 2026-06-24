---
title: "Pokémon Donut Calculator"
date: 2026-06-10
allDay: false
startTime: "14:30"
endTime: "15:00"
area: "Build"
worth: 5
tvm: 3
by: claude
created: 2026-06-10 15:00
cssclasses:
  - nl-doc
---
Built a live, data-driven **Ansha donut calculator** (Pokémon Legends Z-A · Mega Dimension) as a new `Pokémon/` vault surface — js-engine widget with a BUTTER slot stepper (3 now → 8), berry dropdowns, a literal flavor **donut ring** (SVG), and live star tier / calories / Level Boost / Flavor-Power prediction. Reverse-engineered the real engine from the pokeos donut maker: pulled the full berry + power tables from `api.pokeos.com` and the exact thresholds out of its JS bundle, then baked them offline.

**Files:** `Scripts/donut.js`, `Scripts/donut-data.json` (66 berries / 51 powers), `Pokémon/Donut Calculator.md`, `+donut*` CSS in `stratosyn.css`.
**Why:** Colton's at 3 berries and wanted a planner that scales as butter unlocks — real numbers, no placeholders. Verified math against known thresholds (3 sweet Hyper berries → 2★, 220 sweet → Alpha/Sparkling Lv2).
**TVM:** base 5 × 3 (afternoon 1× +2 built-for-you) ≈ **ƒ15 effective**.
