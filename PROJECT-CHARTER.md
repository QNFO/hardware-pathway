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

**Phase:** PROTOTYPE — Critically incomplete

**What exists:** A single `index.html` (6.5 KB, **72 lines JS**) with 2D Canvas and manual projection math. Atoms are drawn as circles. Rotation and zoom via mouse drag.

**CRITICAL ISSUE:** The spec requires "3D (or 2.5D isometric)" visualization. What was built is a flat 2D projection with 72 lines of manual trigonometry. There is no:
- Three.js or any 3D library
- Actual 3D rendering
- Rydberg blockade gate visualization
- Atom state coloring
- Depth cues or perspective

**72 lines of JS cannot produce a convincing 3D visualization of 40 atoms with Rydberg gates.** This is the most technically inadequate artifact in the portfolio.

---

*Updated: 2026-05-23 | QWAV Strategy: Build Gravity v3.0 | Artifact: Tier 1 — A5*
