# 02 — Designs

Blueprints, sketches, and diagrams for the shelf system.

- Prefer **SVG** for anything Claude generates — it is text, so it versions and diffs
  cleanly in git.
- Use descriptive names: `front-elevation.svg`, `side-elevation-holes.svg`,
  `dado-joint-detail.svg`, `t-bracket-detail.svg`, `rolling-sprocket-unit.svg`.
- Current files: `shelf-3d-isometric.svg` (whole system, generated from
  `../01-claude-project/GEOMETRY.md` — regenerate rather than hand-edit),
  `desk-drawer-organizer.svg`, `mechanic-tool-cart.svg`.
- `shelf-3d-viewer.html` — **offline interactive 3D viewer** (drag to rotate,
  scroll/pinch to zoom, toggle members). Fully self-contained: open it in any
  browser by double-clicking; no internet needed. Its box model is copied from
  `GEOMETRY.md` — when geometry changes, regenerate both this and the SVG.
- Hand-drawn sketches or CAD exports can live here too; if they are large raster images,
  see the image-handling notes in the root `README.md`.

The current design state these diagrams illustrate is in
`../01-claude-project/DESIGN_SPECIFICATIONS.md` (see §16 for the diagram list).
