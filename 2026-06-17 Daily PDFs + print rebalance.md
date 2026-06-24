---
title: "Daily PDFs + print rebalance"
date: 2026-06-17
allDay: false
startTime: "10:00"
endTime: "11:25"
area: "Build"
worth: 5
tvm: 3
by: claude
created: 2026-06-17 17:20
cssclasses:
  - nl-doc
---
Made the Madewell Dailies **print** properly. Built `scripts/gen-daily-pdf.mjs` — each Daily `.md` → its **own** print-ready PDF via **Playwright driving the system Chrome** (`page.pdf()`; the Chrome `--print-to-pdf` CLI hung unreliably and was abandoned). First pass exposed two truths: my "single printed page" assumption was wrong (**Colton: "most are two pages"**), and the print was **cutting blocks off** at the page boundary. Fixed both in stratosyn's `@media print`: dropped the cram-to-one-page 3-column density to a **balanced 2 wide columns**, let the lead story flow like newspaper copy, and put `break-inside:avoid` on every bordered block so nothing clips. Then consolidated to **one canonical folder** — `The Madewell Daily/PDF Version/` (Colton's; the duplicate `Daily PDFs/` was removed) — and repointed the script's default output there.

**Files:** `scripts/gen-daily-pdf.mjs`; stratosyn `@media print` block retune; vault `The Madewell Daily/PDF Version/*.pdf` (first 10 issues). Memory corrected ([[madewell-daily]]).
**Why:** the Dailies are real handouts she prints on a school copier — they have to come out even, legible, and uncut. The "single page" goal was the wrong assumption that sent me compressing; the fix matches how they're actually built (2-page double-sided sheets).
**TVM:** base 5 × 3 (morning build) ≈ **ƒ15 effective**. See [[Value Engine]].
