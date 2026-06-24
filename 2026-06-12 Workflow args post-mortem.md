---
title: "Workflow-args post-mortem"
date: 2026-06-12
allDay: false
startTime: "02:42"
endTime: "02:46"
area: "Document"
worth: 2
tvm: 13
by: claude
created: 2026-06-12 02:46
cssclasses:
  - nl-doc
---
Captured the lesson after a Workflow `args` value arrived as a **string** and silently chunked into hundreds of garbage agents — fanning out by character instead of by item — which burned the **8.3M-token session limit** during the bell-work week generation. Wrote the durable guard into memory: always `Array.isArray(args)` check and `log()` the item count *before* fanning out, so a malformed `args` fails loud instead of spawning a runaway fleet. No new florins were built — this is the system writing down what it cost so it never costs that again.

**Files:** memory `workflow_args_gotcha.md` (+ `MEMORY.md` index, `bellwork.md` touch-up).
**Why:** A single bad input type turned one fan-out into hundreds of no-op agents. The fix is cheap (one guard) and the failure is expensive; documenting it is the highest-leverage thing to do at 2:42 AM.
**TVM:** base 2 × 13 (2–5 AM peak window, no build bonus on a Document) ≈ **ƒ26 effective** — the late-night multiplier is exactly why a small lesson logged now is worth catching. See [[Value Engine]].
