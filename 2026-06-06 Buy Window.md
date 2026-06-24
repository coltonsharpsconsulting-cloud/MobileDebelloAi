---
title: "Buy Window — purchase-timing flags"
date: 2026-06-06
allDay: false
startTime: "03:00"
endTime: "03:30"
area: "Build"
worth: 3
tvm: 15
by: claude
created: 2026-06-06 03:30
cssclasses:
  - nl-doc
---
Built the **Buy Window** — the Value Engine's purchase half. A live widget on `Value Engine.md` that, given the current day + hour, flags each category as **BUY** (cheap window), **WAIT** (expensive), or neutral, with each one's best-buy time. Pairs with the Value Window: one prices your time, the other prices the market. Single module (`Scripts/buy-window.js`), one embed.

**Files:** `Scripts/buy-window.js`, `.obsidian/snippets/stratosyn.css`, `Value Engine.md`.
**Why:** the Engine knew your TVM but didn't surface the purchase alpha; now it does, and I flag buys in chat too.
**TVM:** base 3 × 15× (2–5 AM ceiling) ≈ **ƒ45 effective**.
