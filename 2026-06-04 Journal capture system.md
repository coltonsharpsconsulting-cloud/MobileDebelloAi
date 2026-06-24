---
title: "Journal capture system"
date: 2026-06-04
allDay: false
startTime: "20:00"
endTime: "21:30"
area: "Fix"
worth: 6
by: claude
created: 2026-06-04 21:30
cssclasses:
  - nl-doc
---
Fixed Journal auto-dating end to end. Root-caused the Templater folder-template not firing (settings written to disk while Obsidian was running → the create-event listener was never registered), then made entries **timed** Full Calendar events and added the missing `title` field — Full Calendar 0.10.7 silently drops any note without one, which is why nothing showed.

**Files:** `Templater/Dated note.md`, `Journal/Journal.md`.
**Why:** every note needs a date so it lands on the calendar; this is the capture surface everything else reads.
