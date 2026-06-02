---
tags:
  - vex
  - robot
  - design
  - engineering
robot-name: "{{Robot Name}}"
team: "{{Team Number}}"
version: "v1.0"
created: {{date}}
---

<style>
.robot-header{background:linear-gradient(135deg,rgba(255,102,0,.1),rgba(255,34,68,.08));border:1.5px solid rgba(255,102,0,.3);border-radius:14px;padding:18px 22px;margin-bottom:20px}
.robot-header h1{margin:0 0 4px;font-size:1.5em}
.robot-header .meta{color:rgba(255,255,255,.4);font-size:.82em;letter-spacing:1.2px}
.spec-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin:14px 0}
.spec-box{background:rgba(255,255,255,.025);border:1px solid rgba(255,255,255,.07);border-radius:9px;padding:12px}
.spec-box .spec-label{font-size:.72em;letter-spacing:1.5px;text-transform:uppercase;color:rgba(255,255,255,.35);margin-bottom:4px}
.spec-box .spec-val{font-size:.95em;font-weight:600;color:rgba(255,255,255,.85)}
.edp-step{display:flex;gap:12px;margin:10px 0;align-items:flex-start}
.edp-num{width:28px;height:28px;border-radius:7px;background:rgba(255,102,0,.15);border:1px solid rgba(255,102,0,.3);display:flex;align-items:center;justify-content:center;font-weight:900;font-size:.8em;color:#ff6600;flex-shrink:0;margin-top:2px}
.edp-content{flex:1;background:rgba(255,255,255,.02);border:1px solid rgba(255,255,255,.05);border-radius:8px;padding:12px;font-size:.87em;line-height:1.6;color:rgba(255,255,255,.7)}
.edp-content strong{color:#fff;display:block;font-size:.85em;letter-spacing:.8px;text-transform:uppercase;margin-bottom:4px}
.change-log{font-size:.85em}
.change-log table{width:100%;border-collapse:collapse}
.change-log th{text-align:left;padding:7px 10px;background:rgba(255,255,255,.05);border-bottom:1px solid rgba(255,255,255,.1);letter-spacing:.8px;text-transform:uppercase;font-size:.78em}
.change-log td{padding:7px 10px;border-bottom:1px solid rgba(255,255,255,.04);color:rgba(255,255,255,.7)}
.change-log tr:last-child td{border-bottom:none}
.divider{border:none;border-top:1px solid rgba(255,255,255,.07);margin:16px 0}
</style>

<div class="robot-header">
<h1>🔩 {{Robot Name}}</h1>
<div class="meta">Team {{Team Number}} &nbsp;·&nbsp; 2025–26 VRC Season &nbsp;·&nbsp; Version {{version}}</div>
</div>

← [[⚡ VEX Robotics MOC]] | [[🎓 Course Curriculum]] →

---

## ⚙️ Robot Specifications

<div class="spec-grid">
<div class="spec-box">
<div class="spec-label">Drive Train</div>
<div class="spec-val">{{e.g. 6-motor tank drive}}</div>
</div>
<div class="spec-box">
<div class="spec-label">Drive Speed</div>
<div class="spec-val">{{e.g. 200 RPM / 11:1 ratio}}</div>
</div>
<div class="spec-box">
<div class="spec-label">Intake Mechanism</div>
<div class="spec-val">{{e.g. flex wheel intake}}</div>
</div>
<div class="spec-box">
<div class="spec-label">Lift / Scoring</div>
<div class="spec-val">{{e.g. 4-bar lift}}</div>
</div>
<div class="spec-box">
<div class="spec-label">Autonomous</div>
<div class="spec-val">{{e.g. right-side 3-mobile-goal}}</div>
</div>
<div class="spec-box">
<div class="spec-label">Climb</div>
<div class="spec-val">{{e.g. passive hang / none}}</div>
</div>
<div class="spec-box">
<div class="spec-label">Motor Count</div>
<div class="spec-val">{{e.g. 8 motors}}</div>
</div>
<div class="spec-box">
<div class="spec-label">Weight (est.)</div>
<div class="spec-val">{{e.g. 12 lbs}}</div>
</div>
</div>

<hr class="divider">

## 🔬 Engineering Design Process

<div class="edp-step">
<div class="edp-num">1</div>
<div class="edp-content">
<strong>Problem Definition</strong>
What does the robot need to do this season? What game elements must it handle?
</div>
</div>

<div class="edp-step">
<div class="edp-num">2</div>
<div class="edp-content">
<strong>Research & Brainstorm</strong>
Concepts we considered. Robots we looked at for inspiration. Pros/cons of different approaches.
</div>
</div>

<div class="edp-step">
<div class="edp-num">3</div>
<div class="edp-content">
<strong>Design Selection</strong>
What we chose and why. What we rejected and why.
</div>
</div>

<div class="edp-step">
<div class="edp-num">4</div>
<div class="edp-content">
<strong>Build & Test</strong>
Key build decisions made. Unexpected problems encountered. How we solved them.
</div>
</div>

<div class="edp-step">
<div class="edp-num">5</div>
<div class="edp-content">
<strong>Iteration</strong>
What we changed after testing. Results before vs. after each iteration.
</div>
</div>

<hr class="divider">

## 📋 Subsystem Notes

### Drive Train
- 

### Intake
- 

### Scoring Mechanism
- 

### Autonomous / Sensors
- 

### Climb (End Game)
- 

<hr class="divider">

## 📝 Build Log / Change History

<div class="change-log">

| Date | Version | Change Made | Reason | Result |
|------|---------|-------------|--------|--------|
| {{date}} | v1.0 | Initial build | — | — |

</div>

<hr class="divider">

## 🔗 Connected Notes

- [[⚡ VEX Robotics MOC]]
- [[📍 Field Map]] — Strategy planning
- [[🏆 Competition Log]] — Match results with this robot
- *Link to team members: [[Templates/VEX Student Profile]]*
