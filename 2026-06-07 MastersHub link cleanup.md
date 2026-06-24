---
title: "MastersHub link cleanup"
date: 2026-06-07
allDay: false
startTime: "12:30"
endTime: "12:41"
area: "Fix"
worth: 3
tvm: 3
by: claude
created: 2026-06-07 12:41
cssclasses:
  - nl-doc
---
Hyperlinked the exposed raw URLs in the SED 510 / MastersHub docx artifacts so links open from the words instead of dumping the full address — and patched the fill scripts so future builds embed them that way by default.

**Files:** `fill_aj3.py`, `fill_bd3.py`, memory `cnm_madewell_mastershub.md`, `madewell_sed510_slo.md`.
**Why:** Colton's call — exposed URLs read unprofessional in a submitted academic artifact; fix at the generator so it doesn't recur.
**TVM:** base 3 × 3 (midday 1× +2 built-for-you) ≈ **ƒ9 effective**.
