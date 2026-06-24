---
title: "Build Log reconciler"
date: 2026-06-07
allDay: false
startTime: "15:30"
endTime: "15:57"
area: "Build"
worth: 6
tvm: 3
by: claude
created: 2026-06-07 15:57
cssclasses:
  - nl-doc
---
Built the system's own catch-up machine: a reconciler that reads the Claude Code session transcripts (`~/.claude/projects/**.jsonl`), segments them into work-blocks by idle gap, converts UTC→Phoenix so the TVM hour is right, de-dups against entries already logged, and emits a **facts sheet** — the evidence Claude prices into Build Log entries. `--since` auto-detects the latest logged window, so every re-run surfaces only the new gap. The book now keeps *itself* current; pricing stays editorial so the florin keeps its backing. First run reconciled this very session.

**Files:** `scripts/reconcile-build-log.py`, `docs/superpowers/specs/2026-06-07-build-log-reconciler-design.md`.
**Why:** Colton — the in-vault currency was going stale because the scorekeeper fell behind; this is the structured way to update it "until right now," repeatably.
**TVM:** base 6 × 3 (afternoon 1× +2 built-for-you) ≈ **ƒ18 effective**.
