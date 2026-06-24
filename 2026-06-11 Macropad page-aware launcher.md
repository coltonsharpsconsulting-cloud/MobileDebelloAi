---
title: "Macropad page-aware launcher"
date: 2026-06-11
allDay: false
startTime: "13:27"
endTime: "19:38"
area: "Build"
worth: 7
tvm: 3
by: claude
created: 2026-06-11 19:38
cssclasses:
  - nl-doc
---
Rebuilt the macropad daemon into a **page-aware launcher** so Colton can drive the whole DebelloAI system with one hand — the new **12-key + 3-knob** pad plus a mouse. Added a **page cursor** (`PageState`) over the bindings: a reserved page-dial knob cycles `GO ▸ THIS_APP ▸ CAPTURE`, and resolution becomes `(page, frontmost_app, slot) → binding` — GO and CAPTURE are global, THIS_APP is context-aware by the Mac's frontmost app. Extended the **FireRouter event range from 1..18 to 1..21** to pick up the third knob (events 19/20/21 = left/right/click), with matching boundary fixes in `http_server.py` and 3-knob parsing in the profile/state loop. Captured the new hardware's vendor/product IDs and per-key/knob emit map (the gate task — a mismatched pad fires *nothing*, silently), and wrote the hardware map + Karabiner filter.

**Files:** `macropad_controller/macropad_controller/{daemon,fire_router,http_server,hud,page_state}.py`, `config/config.yaml.example`, `docs/macropad-hardware-map.md`, `~/.config/karabiner/assets/complex_modifications/macropad-controller.json`, specs `docs/superpowers/specs/2026-06-11-macropad-launcher-design.md` + plan.
**Why:** The newest 3-knob hardware emitted an unknown event set that the old `vendor 1452 / product 591` filter ignored. Page state turns a flat 12+3 pad into a layered launcher — global actions, app-specific actions, and a capture inbox — without a keyboard. Remember: editing `config.yaml` needs `launchctl kickstart -k` to take effect.
**TVM:** base 7 × 3 (afternoon 1× +2 built-for-you) ≈ **ƒ21 effective**. See [[Value Engine]].
