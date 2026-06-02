---
tags:
  - vex
  - field
  - game-elements
  - reference
created: 2026-06-02
---

<style>
.hero-banner{background:linear-gradient(135deg,rgba(255,34,68,.1),rgba(0,128,255,.1));border:1.5px solid rgba(0,245,255,.2);border-radius:14px;padding:18px 22px;margin-bottom:20px}
.hero-banner h1{margin:0 0 4px;font-size:1.6em}
.hero-banner p{margin:0;color:rgba(255,255,255,.5);font-size:.85em;letter-spacing:1px}
.launch-btn{display:inline-block;margin:16px 0;padding:12px 28px;background:linear-gradient(135deg,rgba(0,245,255,.15),rgba(139,0,255,.15));border:1.5px solid rgba(0,245,255,.5);border-radius:10px;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;font-size:.85em;text-decoration:none;color:inherit}
.zone-grid{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin:16px 0}
.zone-card{border-radius:10px;padding:14px;border:1px solid}
.z-red{border-color:rgba(255,34,68,.4);background:rgba(255,34,68,.06)}
.z-blue{border-color:rgba(0,128,255,.4);background:rgba(0,128,255,.06)}
.z-yellow{border-color:rgba(255,238,0,.4);background:rgba(255,238,0,.06)}
.z-green{border-color:rgba(0,255,136,.4);background:rgba(0,255,136,.06)}
.z-purple{border-color:rgba(139,0,255,.4);background:rgba(139,0,255,.06)}
.zone-card h3{margin:0 0 6px;font-size:.9em;letter-spacing:1px;text-transform:uppercase}
.zone-card p{margin:0;font-size:.82em;color:rgba(255,255,255,.6);line-height:1.5}
.score-table{width:100%;border-collapse:collapse;margin:12px 0;font-size:.88em}
.score-table th{text-align:left;padding:8px 12px;background:rgba(255,255,255,.05);border-bottom:1px solid rgba(255,255,255,.1);letter-spacing:.8px;text-transform:uppercase;font-size:.8em}
.score-table td{padding:8px 12px;border-bottom:1px solid rgba(255,255,255,.04)}
.score-table tr:last-child td{border-bottom:none}
.tip-box{background:rgba(0,245,255,.05);border-left:3px solid rgba(0,245,255,.5);border-radius:0 8px 8px 0;padding:12px 16px;margin:14px 0;font-size:.88em;line-height:1.6}
.divider{border:none;border-top:1px solid rgba(255,255,255,.07);margin:20px 0}
</style>

<div class="hero-banner">
<h1>📍 VEX VRC Field Map</h1>
<p>Interactive field · Zone reference · Scoring guide · 2025–26 Season</p>
</div>

← [[⚡ VEX Robotics MOC]] | [[🏆 Competition Log]] →

---

## 🚀 Open Interactive Field Map

> Click the link below to open the fully interactive field in Obsidian. You can **drag and drop** robots, rings, and mobile goals onto the field, toggle zones on/off, and track scores.

**[[vex-field-map.html|🤖 Open Interactive VEX Field Map →]]**

<div class="tip-box">
<strong>How to use it:</strong> The field opens in its own Obsidian tab. Drag elements from the palette onto the field to plan autonomous routes or match strategies. Use the Print button to generate a clean physical copy for students.
</div>

<hr class="divider">

## 🗺️ Field Zones Reference

The VRC field is **12 × 12 feet** (144" × 144"), divided into 6×6 foam tiles (each tile = 24"×24").

<div class="zone-grid">
<div class="zone-card z-red">
<h3>🔴 Red Alliance Zone</h3>
<p>Bottom-left 3×3 tile area. Red robots must end Autonomous here to earn the Autonomous Win Point bonus.</p>
</div>
<div class="zone-card z-blue">
<h3>🔵 Blue Alliance Zone</h3>
<p>Top-right 3×3 tile area. Blue robots must end Autonomous here to earn the Autonomous Win Point bonus.</p>
</div>
<div class="zone-card z-yellow">
<h3>🟡 Neutral Zone</h3>
<p>Center 2×2 tile area. Contested space — neither alliance owns it. Mobile goals here are unscored at end of match unless claimed.</p>
</div>
<div class="zone-card z-green">
<h3>🟢 Positive Corner</h3>
<p>Top-left and bottom-right corners. Mobile goals placed here earn a <strong>+</strong> bonus. High-value real estate.</p>
</div>
<div class="zone-card z-purple">
<h3>🟣 Negative Corner</h3>
<p>Top-right and bottom-left corners (overlap with starting tiles). Mobile goals placed here score <strong>−</strong> against the owner. Avoid or trap opponents here.</p>
</div>
<div class="zone-card" style="border-color:rgba(255,255,255,.15);background:rgba(255,255,255,.02)">
<h3>⬜ Starting Tiles</h3>
<p>R1, R2 (bottom-left edge) and B1, B2 (top-right edge). Robots must start fully within these tiles at match start.</p>
</div>
</div>

<hr class="divider">

## 📐 Field Elements

| Element | Count | Description |
|---------|-------|-------------|
| Mobile Goals (MG) | 5 | Yellow goals — score rings placed on them |
| Wall Stakes | 8 | Fixed to walls, 2 per side — rings stack on these |
| Rings (Red) | 24 | Scored on stakes and mobile goals |
| Rings (Blue) | 24 | Scored on stakes and mobile goals |
| Climb Bar | 1 | Center high goal — robots hang here at end |

<hr class="divider">

## 🏅 Scoring Quick Reference

<table class="score-table">
<tr><th>Action</th><th>Points</th><th>Notes</th></tr>
<tr><td>Ring on mobile goal (top ring)</td><td>3 pts</td><td>Only top ring scores per stake</td></tr>
<tr><td>Ring on wall stake (top ring)</td><td>3 pts</td><td>Only top ring scores per stake</td></tr>
<tr><td>Mobile goal in positive corner</td><td>+3 pts</td><td>Bonus per goal in positive corner</td></tr>
<tr><td>Mobile goal in negative corner</td><td>−3 pts</td><td>Penalty per goal in negative corner</td></tr>
<tr><td>Autonomous Win Point</td><td>1 WP</td><td>Win autonomous period to earn</td></tr>
<tr><td>Autonomous Bonus</td><td>8 pts</td><td>Awarded to autonomous winner</td></tr>
<tr><td>Robot Climb — Low</td><td>3 pts</td><td>Hanging on low bar at end</td></tr>
<tr><td>Robot Climb — High</td><td>6 pts</td><td>Hanging on high bar at end</td></tr>
</table>

<hr class="divider">

## ⏱️ Match Structure

```
Autonomous Period    →    15 seconds    →    No driver input
Driver Control       →    1 min 45 sec  →    Full driver control
End Game             →    Last 30 sec   →    Climb bar eligible
```

<hr class="divider">

## 🧠 Strategy Notes

> Add your team's strategy notes here as the season progresses. Link to specific match notes below.

- *No strategy notes yet — add after first practice matches*
- [[Templates/VEX Match Notes|Create a match notes note →]]

<hr class="divider">

## 🔗 Connected Notes

- [[⚡ VEX Robotics MOC]] — Back to hub
- [[🏆 Competition Log]] — Track results
- [[📋 Rules & Scoring Quick Ref]] — Full rules reference
- [[🎓 Course Curriculum]] — Teaching this material
