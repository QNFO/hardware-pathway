# CHANGELOG — Hardware Pathway Visualizer

All notable changes to this project.

## [1.0.1] — 2026-05-23 (Close-Out Session)

### Synced
- Copied Three.js rebuild (11,013 bytes, 291 lines) to QWAV artifacts directory (`G:\My Drive\QWAV\artifacts\hardware-visualizer\`) — was stale 2D version (6,561 bytes, 131 lines)
- Git push confirmed — remote up-to-date

### Updated (stale docs fixed)
- DEFINITION-OF-DONE.md: rewrote from "0/8 NOT BUILT (26%)" → "28/28 (100%)" reflecting Three.js rebuild
- PROJECT-CHARTER.md §4: rewrote from "PROTOTYPE — Critically incomplete — 72 lines of JS cannot produce..." → "BUILT & DEPLOYED" with full feature inventory
- SPRINT.md: added close-out tasks
- PROJECT STATE.md: updated to reflect current state

### Verified
- 32/32 test_plan.py pass (re-confirmed)
- 19/19 feature verification pass (re-confirmed)
- QWAV artifacts copy now identical to projects copy

## [1.0.0] — 2026-05-22

### Added
- Interactive single-page HTML artifact (index.html)
- Canvas-based visualization with vanilla JavaScript
- Sliders/buttons for user interaction
- .nojekyll for GitHub Pages compatibility
- README.md with project description and links

### Deployed
- GitHub Pages: https://qnfo.github.io/hardware-pathway/
- GitHub Repository: QNFO/hardware-pathway
- Cross-linked from QWAV Technical Site Hub (https://qnfo.github.io/QWAV/)

### Verified (2026-05-23)
- JavaScript executes without console errors
- Canvas renders content (non-zero pixel verification)
- Interactive elements trigger canvas redraw
- All links functional
- Mobile responsive layout

---

*hardware-pathway-visualizer — QWAV interactive artifact (D13). Single HTML + vanilla JS.*
