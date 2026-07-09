# GEOMETRY.md — Canonical Spatial Model (Main Shelf System)

**What this file is.** The single source of truth for **where things are in space**:
member positions, orientations, clearance envelopes, and docking zones. The other
documents store facts *by type* (materials, joints, loads); this one stores facts *by
position*, so any geometry question ("does X fit?", "what does the cart roll over?",
"which face takes the bolt?") is answered by lookup, not reconstruction.

**Division of authority (sync discipline).**
- `DESIGN_SPECIFICATIONS.md` owns **what** things are (dimensions, materials, joints).
- This file owns **where** they are (coordinates, orientation, envelopes).
- Coordinate spans necessarily encode dimensions; if a span here disagrees with the
  spec, **the spec wins** and the span here is the bug — re-derive it.
- When a decision moves something, update the spec first, then this file, then the
  register card (same order as always).
- Anything spatially undecided goes in **§U Unresolved geometry** below — an explicit
  unknown beats a silent assumption. Never answer a geometry question using a §U item
  without stating it is unresolved.

---

## 0. Coordinate system

Origin at the **front-left floor corner** of the shelf. Units: **cm**.

```
X = width, 0 → 256, left → right (viewed from the front)
Y = depth, 0 → 50,  front face → back (wall side)
Z = height, 0 → 200, floor → top of beam
```

- The **wall** is at Y = 50. The **aisle** (pull-out space) is at Y < 0.
- "Front face" of a member = its −Y face. "4 cm face faces front" (spec §3) means the
  column's 4 cm dimension runs along X and its −Y face is visible.

## 1. Column lines (X positions — fixed by the width equation)

`TOTAL_WIDTH 256 = 3 × 80 clear + 4 × 4 column` (spec §1) → four column lines:

| Line | X span | Adjacent clear bay |
|---|---|---|
| A (left outer) | 0 – 4 | Bay 1: X 4 – 84 |
| B (inner) | 84 – 88 | Bay 2: X 88 – 168 |
| C (inner) | 168 – 172 | Bay 3: X 172 – 252 |
| D (right outer) | 252 – 256 | — |

Column cross-section: **4 cm along X, 6 cm along Y** (spec §3). Bolt holes pass through
the **6 cm (side, ±X-facing) faces** → **bolt axis runs along X**, into the bay. Never
drill the 4 cm (front/back, ±Y-facing) faces — `REFERENCE_DATA.md` §4 Error 1.

**All four lines carry a front + back pair — 8 columns total** (resolved 2026-07-09):
front columns at **Y 0 – 6**, back columns at **Y 44 – 50**. Every level is an 80 cm
platform bolted at its 4 corners, so each bay needs support front and back on both
flanking lines; at inner lines B and C one pair is shared by the adjacent bays (the
X-axis bolt serves both sides).

## 2. Beams (Y and Z positions)

| Member | Length (X) | Section | Position | Status |
|---|---|---|---|---|
| Top beam | 0 – 256 | 4 × 6 | Z top band (≈194–200), at the **back** (wall-anchored, spec §9) | orientation of 4 vs 6 in Y/Z: **§U2** |
| Back bottom beam | 0 – 256 | 4 × 6 | On the floor at the **back line** (Y 44–50 band, Z from 0); nailed full length; captures back column feet; its front face carries the D3 rear bumper | orientation of 4 vs 6: **§U2** |
| Front rail (raised) | 0 – 256 | 4 × 6 **laid flat** (4 in Z, 6 in Y) | **Z 36 – 40** (top flush with the 40 cm bolt row), against the bay side of the front columns (≈ Y 4 – 10), lap-notched 2 cm over each column. **No floor beam at the front line** — ground stays clear for D3 | decided 2026-07-09 (spec §4); Z assumes grid datum **§U7** |
| Side beams | Y 0 – 50 at X lines A and D | 4 × 6 | "Slightly above bottom main beam" (spec §4) — exact Z: **§U4** | **§U4** |

**No front top beam / no top depth ties — by design** (decided 2026-07-09, spec §4 Top
bracing): in a bay with no high platform the front column tips are free above the front
rail (Z 40 → 194); each installed platform ties front → back at its bolt row. Accepted
tip flex ≈ 2.4 cm per 5 kg bump, SF 12× (spec §11) — deliberate, doubles as platform
install tolerance. Retrofit path (notched front top beam + mid-bay lap ties) is in spec
§4; it depends on **§U2** (top-beam orientation).

## 3. Ground zone & rolling sprocket unit envelope (D3)

The bottom of every bay is reserved for the rolling unit (spec §12 "Ground level").

| Envelope | X | Y | Z | Basis |
|---|---|---|---|---|
| Ground zone (keep clear — nothing below the front rail) | full bay clear width | 0 – 50 | 0 – **36** | `FRONT_RAIL_UNDERSIDE` |
| Rolling unit body | bay clear − 2 (= **78**) | 0 – ~42 (rear bumper ~2 on the back beam face) | 0 – **33** | `SPROCKET_UNIT_MAX_H` = caster ≤7 + bottom 1.5 + sprocket **22** (`SPROCKET_MAX_DIA`, confirmed) + clearance 1 + cover 1.5 |
| Parked clearance under front rail | — | — | 36 − 33 = **3** | rail underside must stay ≥ 35 |
| Pull-out travel | (rolls along Y) | needs ~50 of clear aisle at Y < 0 | — | full extension + handle |
| First usable shelf level | — | — | bolt row at **Z = 40** | first 10 cm grid row above the ground zone; front edge rests on the rail top |

**Decided 2026-07-09 (spec §4):** no floor beam at the front line — the front brace is
the raised rail at Z 36–40; the back bottom beam stays floor-nailed as the system's
floor anchor; front column feet bear directly on the floor with 1 L-bracket each. The
unit rolls on the bare floor; its casters are **fixed (non-swivel)** and guided
sideways by the columns (1 cm clearance per side) — no guide rail exists or is needed.

## 4. Panels

| Panel | Position | Status |
|---|---|---|
| Back panel (ply 9–12 mm) | at Y ≈ 50 — inside (Y 48.8–50) or behind columns (Y 50+): **§U6** | **§U6** |
| Side partitions (200 × 50) | at inner column lines B, C — which X side of the column: **§U6** | **§U6** |

## 5. Hole grid (Z datum)

Holes every **10 cm** along the columns (spec §3). **Z of the first hole: unresolved —
§U7.** Until pinned, "bolt row at Z = n×10" assumes the grid starts at Z = 10 from the
floor.

---

## §U — Unresolved geometry (answer these; each blocks a class of questions)

- **U2 — Top beam & back bottom beam orientation** (4 or 6 cm vertical?) and the top
  beam's exact Y span.
- **U4 — Side beam Z offset** above the back bottom beam.
- **U6 — Panel placement** (back panel inside vs behind; partition side at B/C).
- **U7 — Z of the first bolt hole** (grid datum). The front rail's "top flush with the
  40 cm row" assumes the grid starts at Z = 10; if the datum differs, the rail follows
  the actual row nearest 40 — underside must stay ≥ 35.

*(U1 column arrangement, U3 bottom-beam position, U5 max sprocket Ø: resolved
2026-07-09 and moved up into §1–§3.)*

When one is resolved: move the fact up into §1–§5, update the spec if it's a decision,
delete the §U entry.

---

*Maintenance: standalone designs (D7 desk organizer, D8 tool cart) are spatially
self-contained and stay out of this file; anything that mounts into or docks under the
shelf gets an envelope here. Diagrams in `02-designs/` are **derived views** of this
model — if an SVG and this file disagree, this file wins.*
