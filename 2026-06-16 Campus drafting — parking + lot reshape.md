---
title: "Campus drafting — parking + lot reshape"
date: 2026-06-16
allDay: false
startTime: "10:05"
endTime: "18:11"
area: "Build"
worth: 4
tvm: 3
by: claude
created: 2026-06-16 22:18
cssclasses:
  - nl-doc
---
Continued the campus model across the day. Filleted and joined the **bottom three wires** into one, then — once he'd closed the driveways onto school property so the road area was fully enclosed — **inserted the roadways** into that boundary. Worked the **parking lots**: marked stalls as **circles** (debated circles-only vs. stripe-lines, landed on circles end-to-end after his feedback that mine were too small and not edge-to-edge), cleared his scratch markings so only the clean set remained, **reshaped the west-lot boundary** to enclose two added circles and re-filleted it, and built a **curb-matching array** to space a connecting line to the real curb spacing.

**Files:** `web/CAD/campus.FCStd` (parking + west lot); live socket client `/tmp/fc_sock.py`.
**Why:** parking and lot boundaries are the last big geometry gap before the map is complete enough to layer wayfinding on; getting stall markers and lot outlines right keeps the render honest.
**TVM:** base 4 × 3 (daytime build) ≈ **ƒ12 effective**. See [[Value Engine]] · [[ala_campus_mapping]].
