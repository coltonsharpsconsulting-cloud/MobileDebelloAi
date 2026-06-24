---
title: "Close the value loop — savings → Value Index"
date: 2026-06-06
allDay: false
startTime: "03:30"
endTime: "04:15"
area: "Build"
worth: 6
tvm: 15
by: claude
created: 2026-06-06 04:15
cssclasses:
  - nl-doc
---
Closed the Value Engine loop: buying smart now mints currency. Built a **Smart buy** capture (`Templater/Smart buy.md` + Savings folder-template) that prompts category + dollars saved and banks the spread ×1.5 as florins; a **Savings ledger** on the Value Engine page (florins saved by category); and the grand **Value Index** widget (`Scripts/value-index.js`) that sums all three books — You (Journal), System (Build Log), Savings — TVM-weighted, into the one number that backs the florin.

**Files:** `Scripts/value-index.js`, `Templater/Smart buy.md`, Templater `data.json`, `Value Engine.md`, `Savings/Savings.md`, `stratosyn.css`.
**Why:** Colton's Engine step 4 — translate the savings spread into currency value; cheap purchases literally grow the VI.
**TVM:** base 6 × 15× (2–5 AM ceiling) ≈ **ƒ90 effective**.
