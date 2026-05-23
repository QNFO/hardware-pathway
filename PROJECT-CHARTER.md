# PROJECT CHARTER — Hardware Pathway Visualizer

## 1. PROJECT IDENTITY

| Field | Value |
|:------|:------|
| **Project Name** | `hardware-pathway-visualizer` |
| **Title** | Hardware Pathway Visualizer |
| **Type** | QWAV Spinoff — Interactive Artifact (D13) |
| **QWAV Strategy Reference** | `strategy/3.0.md` — Build Gravity, Tier 1 Artifact A5 |
| **Created** | 2026-05-22 |
| **Repository** | `QNFO/hardware-pathway` |
| **Live Target** | `https://qnfo.github.io/hardware-pathway/` |
| **Parent Program** | QWAV — Ultrametric Quantum Computing & AI |

## 2. RAISON D'ÊTRE — QWAV STRATEGY NEXUS

**This project exists because the question every reviewer, funder, and collaborator asks is "can you actually build this?" — and the answer needs a visual.**

The Symmetric Extension paper (DOI: `10.5281/zenodo.20208437`) specifies a 40-atom neutral atom layout in a ternary Bruhat-Tits tree structure, using Rydberg blockade gates. This is physically realizable with current technology. But a text specification is not convincing. A 3D visualization of the atom layout — showing how Rydberg blockade gates map to tree vertices — answers the "can you build this?" question instantly.

**Strategic contribution:**
- Answers the primary objection: "this is just math, you can't build it"
- Shows the 40-atom layout is compact, regular, and compatible with existing neutral atom platforms
- Provides the hardware story for grant applications and lab outreach
- Rounds out the portfolio: A1=theory, A2=AI, A3=dynamics, A4=education, A5=hardware

**Without this project, QWAV has no answer to the hardware feasibility question.**

## 3. SCOPE

### In Scope
- 3D (or high-quality 2.5D isometric) visualization of the 40-atom neutral atom layout
- Ternary Bruhat-Tits tree structure with labeled vertices
- Rydberg blockade gate visualization — which atom pairs interact
- Rotation (drag) and zoom (scroll) controls
- Atom state coloring (ground/excited/Rydberg)
- Responsive design

### Out of Scope
- Real-time quantum dynamics simulation
- Actual Rydberg pulse sequence modeling
- Integration with experimental control software

## 4. CURRENT STATUS (2026-05-23)

**Phase:** BUILT & DEPLOYED — Rebuilt with Three.js (commit `5fb0833`)

**What exists:** A single `index.html` (11,013 bytes, **291 lines**) with full Three.js 3D rendering:
- Three.js v0.160.0 via import map CDN
- `WebGLRenderer` with antialiasing enabled
- `OrbitControls` with smooth damping, zoom limits (1x to 5x)
- `MeshStandardMaterial` (PBR) with `AmbientLight` + `DirectionalLight`
- `SphereGeometry` for 64 atoms in ternary Bruhat-Tits tree ($p=3$, depth 3, 85 total nodes)
- 378 Rydberg blockade gate connections within radius 1.5, rendered as `LineBasicMaterial` edges
- Atom state coloring: ground (blue), Rydberg (red), excited (orange)
- **Interactive error suppression simulation:** click any atom → red error pulse → geometrically suppressed by sibling majority vote → strong triangle inequality prevents cross-branch propagation → status panel tracks active errors and suppressed count
- Window resize handler with pixel ratio handling
- Cross-linked footer to all 5 QWAV artifacts + technical site hub

**The rebuild replaced the initial 72-line 2D Canvas projection** with a fully interactive 3D visualization. 19/19 feature checks pass. 32/32 `test_plan.py` tests pass. QWAV SPRINT.md tasks S7.10 (Decide A5 approach) and S7.11 (Execute A5 approach) completed.

**Live:** https://qnfo.github.io/hardware-pathway/

---

*Updated: 2026-05-23 — Post-rebuild status. QWAV Strategy: Build Gravity v3.0 | Artifact: Tier 1 — A5*
