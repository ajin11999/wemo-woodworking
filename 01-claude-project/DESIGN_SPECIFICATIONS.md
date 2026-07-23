# Modular Parts Shelf — Design Specifications

**Project**: Motorcycle Parts Shop Storage System
**Location**: Humid tropical region (Kalimantan, Indonesia)
**Date initiated**: May 2026
**Status**: Design phase, drawer carpentry in progress

---

## 1. Overall Dimensions

| Parameter | Value | Notes |
|---|---|---|
| Total width | 256 cm | 3 sections × 80cm clear + 4 outer columns × 4cm |
| Section clear width | 80 cm | Drawer fits inside this (carpenter ordered) |
| Depth | 50 cm | Front to back |
| Height | 200 cm | Floor to top of beam |
| Number of sections | 3 | Side by side |
| Number of columns total | 8 | 4 column lines × (front + back pair); inner lines shared |

---

## 2. Materials

### Primary structure: Meranti Putih (Pakit)
- Used for: columns, top beam, bottom beam, side beams
- Already purchased
- Concerns: medium-soft hardwood, susceptible to bolt-hole creep, requires generous washer use

### Plywood
- Back panel: full height, full width (256cm × 200cm or sectional)
- Side partitions between sections: full height (200cm × 50cm)
- Both panels nailed to columns and beams

### Iron/Steel
- Drawer slider adapter (for heavy fastener drawers): 3-5mm flat bar, 25-30mm wide
- T-brackets and L-brackets (Sellery 19-511 4-inch model considered)

---

## 3. Column Specifications

| Parameter | Value | Notes |
|---|---|---|
| Cross section | 4 × 6 cm | Already purchased |
| Length | 200 cm | Full height |
| Number | 8 | 4 lines × (front + back); inner lines shared between sections |
| Hole diameter | 8 mm | For M8 bolts |
| Hole spacing | 10 cm | Vertical spacing along column |
| Hole face | 6 cm face only | NOT the 4cm face |
| Holes drilled on | Both front and back columns | For shelf level installation |

**Hole positioning rule**: Holes are on the 6cm face. This leaves 2.6cm of wood on each side of the hole, providing safe margin for Meranti Putih. The 4cm face faces front (visible side).

**Why 8 columns (resolved 2026-07-09)**: every level is an 80cm platform bolted at its
4 corners, so each bay needs front AND back columns on both flanking lines. At the two
inner lines one front/back pair is shared by the adjacent bays (the bolt axis runs along
the width, so one bolt can serve both sides).

---

## 4. Beam Specifications

### Top beam (1 piece per shelf group)
- Length: 256 cm (full width of grouped sections)
- Cross section: 4 × 6 cm
- Wall anchored along full length
- Joints to columns: dado/lap

### Bottom beam — back line only (1 piece per shelf group)
- Length: 256 cm
- Cross section: 4 × 6 cm
- Runs along the BACK column line only; secured to the hardwood floor from top-down with 5× heavy-duty structural wood screws (6.0 × 80 mm, Torx drive, zinc-plated) spaced ~50 cm. Holes are pre-drilled and counterbored 1 cm so screw heads sit below the beam's surface. No crawlspace access needed, completely reversible.
- Joints to columns: dado/lap (captures the back column feet)
- Front face doubles as the mounting surface for the rolling sprocket unit's rear
  rubber bumper (§13)

### Front rail — raised brace (the front line has NO floor beam) *(decided 2026-07-09)*
- Purpose: the ground zone must stay clear so the rolling sprocket unit (§13) rolls
  in/out on the bare floor. The rail replaces the front floor beam as the brace that
  captures the front columns and holds the 80 cm bay gaps true (the columns are the
  unit's side guides). It carries no shelf load — levels bolt to the columns, and the
  columns bear straight on the floor.
- Length: 256 cm, cross section 4 × 6 cm **laid flat** (4 cm vertical, 6 cm in depth)
- Position: top flush with the 40 cm bolt row → underside at 36 cm, giving 3 cm
  clearance over the parked unit (33 cm tall, §13). Confirm the hole-grid datum
  (GEOMETRY.md §U7) before cutting; underside must stay ≥ 35 cm.
- Fitted against the inside (bay side) of the front columns, lap-notched 2 cm over
  each column (columns are NOT cut), fixed with 2 structural screws (~80 mm) per
  column driven from the bay side
- Never through-bolt front-to-back — that would drill the 4 cm face
  (REFERENCE_DATA §4 Error 1)
- Bonus: its top edge supports the front of the first platform level
- Front column feet: bear directly on the hardwood floor (0.20 MPa, SF ≈ 25×, §11);
  one L-bracket per front foot screwed to the floor (4×) for positive location

### Side beams (left and right outer edges)
- Length: 50 cm (matches depth)
- Cross section: 4 × 6 cm
- Position: slightly above bottom main beam (offset to avoid three-way joint conflict)
- Joint to column: stepped lap joint
- Optional T-bracket reinforcement (vertical arm along column, horizontal arm onto side beam)

### Top bracing — NO front top beam, NO top depth ties *(decided 2026-07-09)*
- The top bracing is the wall-anchored back top beam (§9) **plus the platform levels
  themselves**: every level bolts to a front and a back column at its 4 corners, so
  each occupied bolt row ties the front columns back to the wall-anchored frame.
- In a bay with no high platform, the front column tips are deliberately unbraced above
  the front rail. Checked (§11 lateral bump check): a 5 kg sideways bump at the tip
  flexes it ≈ 2.4 cm and stresses the wood to 5.0 MPa vs 60 MPa MOR — safety factor
  12× dry, ~8× wet. The flex is accepted, and is useful: it doubles as installation
  tolerance, letting a column spring ±1–2 cm to engage the bolt holes of a slightly
  missized platform.
- **Upgrade path (documented, not built):** if top wobble ever proves objectionable in
  use, add a front top beam (256 cm, 4 × 6, lap-notched over the front column tops —
  columns uncut, same detail as the front rail) plus one 50 cm depth tie per bay,
  lap-jointed onto the front and back top beams and **offset mid-bay from the columns**
  (keeps the column-to-beam dados clean; no fastener ever near a 4 cm face). Fully
  retrofittable without disassembly. Pin GEOMETRY.md §U2 (top-beam orientation) before
  cutting any of it.

---

## 5. Joint Specifications

| Joint Location | Joint Type | Rationale |
|---|---|---|
| Column to top beam (inner columns) | Dado/lap | Mechanical interlock, captures column |
| Column to bottom beam (inner columns) | Dado/lap | Same |
| Column to top beam (outer columns) | Lap + L-bracket | Outer corner geometry |
| Column to bottom beam (outer columns) | Lap + L-bracket | Same |
| Side beam to column | Stepped lap joint | Avoids three-way joint conflict |
| Front rail to front columns | Rail lap-notched 2cm over column + 2 structural screws | Brace only; keeps ground zone clear for §13 unit |
| Top depth ties (upgrade path ONLY — not built) | Lap onto front + back top beams, offset mid-bay from columns | See §4 Top bracing; retrofit only if top wobble proves objectionable |
| Lap joint depth | Half thickness rule | 2cm into 4cm beam, or 3cm into 6cm beam |

---

## 6. Fastener Specifications

### Bolts
- Size: M8
- Length: varies by location (typically 60-80mm)
- Through-bolt with nut and washer on opposite side
- Washer size: fender washers preferred (24-30mm OD) for distribution
- Tightening: firm but not crushing wood fibers

### Screws (where bolt-through not feasible)
- Type: structural construction screws, NOT drywall screws
- Drive: star/Torx preferred over Phillips
- Length: minimum 1.5× wood thickness penetration

### Nails (limited use)
- Bottom beam to floor: yes, top-down structural screws (removable)
- Other locations: avoid for structural connections
- Used only where direction of loading favors nail holding (compression, not withdrawal)

---

## 7. Bracket Reinforcement

### T-brackets (Sellery 19-511 4-inch, 3mm steel minimum)
- Location: column bases (inner columns where beam material exists on both sides)
- Orientation: horizontal arms along the beam, vertical arm onto column
- Alternative orientation for side beam joints: vertical arm along column, single horizontal arm onto beam
- Quantity: ~8 brackets

### L-brackets
- Location: outer corners (4 top + 4 bottom = 8 corners)
- Material: 3mm steel minimum, zinc plated for humidity
- Mounted on inside corner (hidden behind plywood)
- Quantity: ~12-16 brackets

### Total bracket budget
- Approximate cost: Rp 320,000 - 480,000
- Buy spares (~10% extra)

---

## 8. Panel Specifications

### Back panel
- Material: plywood (thickness 9-12mm typical)
- Coverage: full width × full height
- Fastening: nails or screws every 15-20cm along edges
- Purpose: anti-racking, dust barrier, anchor surface

### Side partitions (between shelf sections)
- Material: plywood
- Coverage: full height × full depth (200cm × 50cm)
- Purpose: section separation, additional racking resistance

---

## 9. Anchor System

### Wall anchor (top)
- The entire 256cm top beam is anchored to the wall behind the shelf
- Wall provides continuous support, prevents beam sagging
- Anchor every 50-60cm along the beam length

### Floor anchor (bottom)
- BACK bottom beam secured to the hardwood floor top-down with 5× heavy-duty structural wood screws (6.0 × 80 mm, Torx drive, zinc-plated) spaced ~50 cm
- Fully reversible and removable without floor damage or crawlspace access
- Front column feet: no floor beam (see §4 front rail) — feet bear directly on the
  floor, located by 1 L-bracket each (4×) screwed to the floor

---

## 10. Drawer System

### Standard drawer (light to medium load)
- Dimensions: 80cm clear width × 50cm depth
- Variable heights (6cm to 15cm typical)
- Structural frame with 4 corner bolt holes for column mounting
- Wood divider system with slotted splitter walls
- Solid plywood floor (not wire grid)

### Drawer sliders
- Width: 45mm (standard purchased)
- Weight rating concern: typically 15-25kg
- For heavy drawers: upgrade to 50kg+ rated industrial sliders
- **Safety rule**: Use 70% of rated capacity max

### Drawer adapter (light drawers)
- Material: wood plank
- Thickness: 2-3cm
- Bolted to column via M8 system
- Slider screwed into plank face

### Drawer adapter (heavy drawers — fasteners, sprockets)
- Material: iron flat bar
- Thickness: 3-5mm
- Width: 25-30mm
- Bolted through column with M8 bolt + nut + washer
- Slider screwed into iron face

### Pre-installation testing
- Weigh fully-loaded drawer on scale before installing
- Compare to slider rating × 0.7 safety factor
- Redistribute contents if over limit
- Mark filled weight on drawer for future reference

---

## 11. Load Specifications

| Parameter | Value |
|---|---|
| Max load per shelf level | 25 kg |
| Max total load per section | 200 kg |
| Load distribution rule | Heavier items on lower levels |
| Floor type | Hard wood floor (load capacity not a concern) |

### Calculated stress check
- Vertical load per column: ~50 kg (200kg ÷ 4 columns)
- Contact area at joint: 24 cm² (4 × 6 cm column footprint)
- Stress: 0.20 MPa
- Limit (Meranti perpendicular to grain): 5-7 MPa
- Safety factor: ~25×
- **Verdict**: vertical compression is NOT a concern

### Lateral bump check — unbraced front column tip (no-platform bay; §4 Top bracing)
- Case: 5 kg (50 N) sideways bump at the free tip; column cantilevers L = 160 cm above
  the front rail (Z 40 → 200); weak axis governs (4 cm dimension along X)
- I = b·h³/12 = 6 × 4³/12 = 32 cm⁴ = 3.2×10⁻⁷ m⁴; E = 9,000 MPa (Meranti low end)
- Deflection: δ = PL³/3EI = (50 × 1.6³) / (3 × 9×10⁹ × 3.2×10⁻⁷) ≈ 2.4 cm (elastic, springs back)
- Stress: M = 50 N × 1.6 m = 80 N·m; S = I/c = 16 cm³; σ = 80 / 1.6×10⁻⁵ = 5.0 MPa
- Limit: 60 MPa MOR → safety factor 12× dry, ~8× wet (−30% humid strength)
- **Verdict**: tip wobble is a stiffness matter only; strength is NOT a concern

---

## 12. Storage Zone Allocation

### Topmost (above 1.5m — lightweight, bulky, infrequent)
- Fenders
- Air filters
- Carburetors (full units)

### Mid-level (waist height, frequent access)
- Cables, bearings, seals, valves, pistons
- Electrical parts, injection parts, carburetor parts
- Race steering kit, brake parts
- Clutch components, engine parts
- Roller weight

### Lower (below 1m, heavy and frequent)
- Chains
- Sprockets
- Brake pads
- Battery
- Bushings

### Ground level — Rolling Sprocket Unit
- See section 13 below

---

## 13. Rolling Sprocket Storage Unit

Separate sub-design for the heaviest items (sprockets):

| Element | Specification |
|---|---|
| Concept | Floor-level pull-out unit with top-down access |
| Wheels | 4× fixed casters, 50kg+ rated each, hard rubber/polyurethane, ≥5cm diameter |
| Wheel configuration | All fixed (no swivel) |
| Guidance | Shelf columns act as side guides; unit width = column gap - 2cm. Inner column faces protected by sacrificial Ulin/hardwood rub strips (1.0 × 4.0 × 33 cm) with a 45° entry bevel to act as an alignment funnel |
| Stop mechanism | Friction strip (rubber mat) + rubber bumper at back |
| Optional | Slight floor incline inward for gravity-assisted stopping |
| Front access | Solid pull handle, physical pull-out limit stop |
| Internal layout | Vertical slot dividers (thin plywood, ~1.5cm spacing) |
| Sprocket orientation | Stand on edge in slots |
| Organization | By motorcycle model + teeth count |
| Dust protection | Solid bottom, top cover when closed |
| Max sprocket diameter | 22 cm (largest in stock — owner-confirmed 2026-07-09) |
| Unit overall height | ≤ 33 cm = caster ≤7 + bottom 1.5 + sprocket 22 + clearance 1 + cover 1.5 |
| Caster mounting height | ≤ 7 cm overall (purchase constraint; wheel ≥5 cm still applies) |
| Parked clearance | 3 cm under the front rail (rail underside at 36 cm, §4) |
| Rolls on | Bare floor — no beam or rail in its path (front rail is raised, §4) |

---

## 14. Specialized Sub-Designs Pending

### Bearing storage cabinet (within one shelf bay)
- Many small drawers (15-18cm wide × 50cm deep × 6-8cm tall)
- One bearing part number per drawer
- Tier 1 (high movers like 6201, 6301, 6203): larger drawers, possible bulk bins
- Tier 2 (medium movers like 6004, 6302, 6001): standard drawers
- Tier 3 (rare bearings): multi-part-number drawers
- Front working stock + back backup stock organization
- Add silica gel for humidity

### Piston kit storage
- Pigeon hole grid system
- Rows = motorcycle model
- Columns = oversizes (STD, 0.25, 0.50, 0.75, 1.00)
- Cubby size: 12cm × 10cm × 9cm (slightly larger than box)

### Fastener storage (Standalone Heavy-Duty Unit)
- **Concept**: A dedicated, standalone shelving unit separate from the main M8 modular shelf.
- **Handling**: Restricted to owner/clerk access (no mechanics). This guarantees careful slider operation without slam-shocks, validating the use of the 0.7 cyclic safety factor on the Huben sliders, and keeps greasy tools off the hardwood.
- **Height**: 100 cm (waist-height, acting as a sturdy top work surface).
- **Material**: Upgraded hardwood (e.g., Bengkirai/Yellow Balau or Kapur) instead of Meranti, for superior compression and screw-holding strength under heavy static loads.
- **Drawer Sliders**: Standard Huben ball-bearing slides (rated 35 kg per pair).
- **Load Limit**: Applying the 0.7 cyclic safety factor, the maximum safe load per drawer is **24.5 kg** (drawer + contents).
- **Drawer Sizing**: To stay under 24.5 kg limit with a 4 cm fill depth of bolts (packing efficiency ~45%), max drawer width is roughly 35 cm (at 40 cm slider depth). Therefore, the dedicated shelf will be built with narrower bays (e.g., 35 cm internal clear width) to naturally cap the weight per drawer.
- **Organization**: Slotted partition drawers, labeled precisely.

### Desk-side stationary drawer organizer (standalone — NOT on the modular shelf)
Small free-standing tool/stationery box that sits inside a 28cm-tall × 30cm-deep
shelf opening beside the work table. Light-duty; no M8 bolt/adapter interface.
- External: ~24cm W × 25cm D × 20cm H (fits opening with ~8cm height, ~5cm depth spare)
- 3 drawers, all shallow (items lie flat). Internal usable ~17cm W × 22cm D:
  - Drawer 1 (4cm): pens + refills, cutter + blades
  - Drawer 2 (5cm): PH2 screwdriver, 7" combination pliers
  - Drawer 3 (4cm): receipts (8×13cm) + stamps (8×7cm laid flat)
- Slides: 200mm zinc-plated ball-bearing, full-extension (humidity-proof, fast access).
  Load ~1kg/drawer is far below rating; width grew from 20→24cm to absorb slide clearance.
- Build: carpentry workshop (glued dados + precise slide mounting).
- Material: 12mm plywood (scrap where available), all cut edges sealed. Plywood chosen for
  dimensional stability — keeps slide clearance constant year-round in Kalimantan humidity.
- Climate: seal wood; silica-gel packet in the paper/stamp drawer.
- Diagram: `02-designs/desk-drawer-organizer.svg`

---

## 15. Open Design Questions

- [ ] Final layout drawing of shelf section assignments (which section gets bearings vs pistons vs fasteners)
- [ ] Decision on bearing cabinet build (custom 50cm depth vs movable off-shelf cabinet)
- [ ] Drawer slider purchasing plan (which weight ratings for which drawers)
- [ ] T-bracket vs L-bracket final count and locations
- [ ] Wall anchor hardware selection (anchor type depends on wall material)
- [ ] Treatment plan for Meranti Putih (varnish? wood preservative? for humidity)
- [ ] Confirm piston-kit box dimensions with supplier before finalizing cubby size (12×10×9cm)
- [ ] Mechanic tool cart (§17): confirm 3-way corner brackets are available locally; else fall back to 2× 90° L-brackets per bottom corner
- [ ] Mechanic tool cart (§17): confirm the 4 lane widths (A/B/C/D) against the actual wrench/ratchet/driver lengths & counts before cutting the dividers
- [ ] Mechanic tool cart (§17): caster purchase (100mm, 50kg, 2 rigid + 2 swivel-brake) and plank / 8mm rubber-mat sourcing
- [x] Pin desk-organizer material in §14 — resolved: 12mm plywood, all edges sealed

---

## 16. Reference Diagrams

The following SVG blueprints have been generated:
- Front elevation with all 3 sections, columns, joints
- Side elevation showing depth and holes
- Top plan view
- Dado joint detail
- T-plate detail
- Rolling sprocket unit summary
- Mobile mechanic tool cart (front elevation + top plan + 3-way corner-bracket detail) — `02-designs/mechanic-tool-cart.svg`
- Whole-system 3D isometric view (derived from `GEOMETRY.md`) — `02-designs/shelf-3d-isometric.svg`

These are reference documents, not part of this spec file.

---

## 17. Mobile Mechanic Tool Cart (Workshop side — D8)

Standalone rolling tool bin for the **open-air workshop** (under canopy), **shared between
mechanics**. **NOT** part of the modular M8 shelf system — it rolls freely, no bolt/adapter
interface. Designed for an **impact/abuse, toss-it-back workflow**.

**Mechanic-built from owner-supplied materials (owner directive 2026-06-20).** No carpentry
shop, no joinery: the workshop mechanics assemble it from **wood planks + off-the-shelf
brackets + bolts/nuts/screws**, all easy to find; the owner buys the materials. Form factor
simplified to a single **open plank bin, 60 × 45 × 20 cm** (box height; casters extra), riding
directly on **4 casters**.

### Concept & governing principle
- **One shallow open bin, split into 4 fixed tool-category lanes** — toss-tolerant, no
  drawers/slides to bend, breathes in humidity. It is shared, so nobody re-racks tools neatly;
  the lanes are kept **generously oversized** so a tossed tool still lands in the right one.
- **Tip resistance comes free from the low form.** The bin floor sits ~13 cm up (on the
  casters), the box is only 20 cm tall, so the **loaded CG ≈ 20 cm** over a 60 × 45 cm
  footprint. Fore-aft tip threshold `a/g ≥ b/h_cg ≈ 0.19/0.20 ≈ 0.95 g` → it **slides before
  it tips**. No push handle or leg frame needed (those were for the earlier 50 cm-deck idea,
  now retired).
- **Compliant impact surface.** Tools land in the bottom → an **8 mm rubber mat** on the floor
  cuts peak thrown-tool force ~6× vs bare wood and stops the bottom plank splitting
  (impact-energy method, `REFERENCE_DATA.md` §3.4). Rigidity in the frame, compliance at the
  contact.

### Overall dimensions
| Parameter | Value | Notes |
|---|---|---|
| Box W × D × H | 60 × 45 × 20 cm | open top; box height only (casters extra) |
| Deck height | ~13 cm | bin floor above ground = caster height |
| Rim height | ~33 cm | deck 13 + 20 cm box |
| Loaded CG height | ~20 cm | trivially tip-stable |
| Caster | 100 mm wheel | + plate |

### Structure & materials (plank box, no joinery)
- **Wood planks (~2 cm)**, butt-jointed, held by brackets + screws — no dados/rabbets. Use the
  **thickest plank for the bottom** (it takes the thrown-tool impact and carries the caster bolts).
- **Cleats** (~2 × 2 cm strips) screwed inside the lower edge of all four walls; the bottom
  board rests on them so impact is carried in **shear by the cleat**, not by bracket screws.
- **Caster blocks** (4× solid offcut ~8 × 8 × 4 cm) under the bottom corners give the caster
  bolts real wood to bite — don't bolt casters through a single plank alone.
- **Internal dividers double as anti-racking ribs** (the *Fixed compartments* below): braced
  to the long walls, they keep the box from parallelogramming — compartments and carcase
  reinforce each other.
- Already-owned Meranti planks are fine here (framing/compression; the mat keeps impact off the wood).
- **Seal all wood incl. cut edges** (open-air humidity).

### Corner brackets (the 3-axis question)
- **The 4 bottom corners are true 3-axis corners** (two walls + the floor meet at a point) →
  **4× 3-way corner brackets**, one flange screwed to each of the three faces. A single L or a
  flat brace **can't restrain the third (vertical) axis** — see `REFERENCE_DATA.md` §6.
  ⚠️ **Source-check 3-way brackets locally first**; if unavailable, substitute **2× 90°
  L-brackets per corner** (one on the vertical wall-to-wall edge, one tying a wall to the floor).
- **The 4 top corners** (vertical edge, 2-axis) → **4× 90° L-brackets** to keep the rim from splaying.
- Zinc-plated/galvanized, 2–3 mm steel; buy ~10 % spares.
- **Why no edge-parallel L-bracing** (considered and declined): the bottom seams are already
  **continuously braced by the cleats**, the rim is **tied by the 3 full-height dividers**, and
  racking is resisted by that triangulation/diaphragm — **not** by straps lying along an edge
  (`REFERENCE_DATA.md` §6). Adding edge L's would be redundant and just punches more split-prone
  holes in soft Meranti. Corners + cleats + dividers already triangulate the box.

### Wheels
- **100 mm hard rubber/PU**, non-marking. **2 rigid + 2 swivel-with-brake**, **50 kg+ each**
  (cheap, robust, rolls over workshop grit; far above the ~9 kg/caster static load).
- Swivel is **correct here** — the cart steers around the workshop. This is **NOT** the
  fixed-axis rolling-sprocket-unit case (§4 Error 5).
- Caster bolts: **M8 × 40 + nut + 2 washers** (one fender washer into wood for plank creep),
  4 per caster; **nyloc / thread-locker** against rolling shock.

### Fixed compartments (A/B/C/D)
Three **full-height (~20 cm) dividers** run **front-to-back** (so ~35 cm tools lie flat),
splitting the ~56 cm internal width into four category lanes:

| Lane | Tool group | Nominal width |
|---|---|---|
| A | Wrenches (combination/open/ring) | ~16 cm |
| B | Sockets & ratchets | ~16 cm |
| C | Screwdrivers & hex/Allen keys | ~12 cm |
| D | Pliers, cutters & grips | ~12 cm |

- Dividers ~1.5 cm plank, 41 × 20 cm; usable lane ≈ 1.5 cm less where a divider lands. Keep
  lanes oversized for toss-tolerance — **don't cut tool-shaped slots**. Confirm widths against
  the actual tool sets before cutting (see §15).
- **Bracing — and why brackets, not just screws:** tie **each divider end to the front/back
  wall with a small 90° L-bracket** (6 total). The flanges land on **face grain** of both
  boards (strong); a screw driven straight into the divider's **end grain would be weak**.
  Also screw **up through the bottom plank** into each divider's lower edge.
- **Structural bonus:** braced this way the dividers are **internal ribs** that tie the long
  60 cm front and back walls together, resisting racking and wall-bow.
- Each lane gets its own **8 mm rubber mat** strip (the bottom mat, cut to the lanes).

### Load & stability check
- **Caster load:** tools (one shallow bin) ≈ 20–25 kg + cart ≈ 12 kg = **~35 kg ÷ 4 ≈
  9 kg/caster** static. 50 kg casters → **SF ≈ 5× static**.
- **Tip:** loaded CG ~20 cm, half-wheelbase ~19 cm fore-aft → tips only past ~0.95 g; it
  slides first. Tipping is a non-issue at this height — that is why the low bin was chosen.
- **Dividers:** add ~1–2 kg low in the box → no change to CG (~20 cm) or the numbers above;
  net effect is extra racking stiffness, not a stability penalty.

### Bill of materials (cut list, ≈ 2 cm planks)
| Item | Spec | Qty |
|---|---|---|
| Bottom panel | 60 × 45 cm (thickest stock) | 1 |
| Front / back wall | 60 × 20 cm | 2 |
| Side wall | 41 × 20 cm (fits between front/back) | 2 |
| Cleat strip | ~2 × 2 cm: 56 cm ×2, 41 cm ×2 | 4 |
| Caster block | ~8 × 8 × 4 cm solid offcut | 4 |
| Divider (full height) | 41 × 20 cm, ~1.5 cm plank | 3 |
| 3-way corner bracket | bottom corners, 2–3 mm zinc/galv | 4 (+spares) |
| 90° L-bracket | top corners, 2–3 mm zinc/galv | 4 (+spares) |
| Small 90° L-bracket | divider ends → front/back wall | 6 (+spares) |
| Caster | 100 mm, 50 kg+, 2 rigid + 2 swivel-brake | 4 |
| Wood screws | 4 × 30–40 mm structural (not drywall) | ~100–120 |
| Caster bolt set | M8 × 40 + nut + 2 washers (1 fender), nyloc/locker | 16 |
| Rubber mat | 8 mm, ~56 × 41 cm total, cut into 4 lane strips | 1 |
| Exterior varnish/sealer | all wood + cut edges | as needed |

### Climate
- Open-air canopy = wetter than the parts shop → seal all wood incl. edges, galvanized/zinc
  brackets & fasteners. No silica gel (open bin, no enclosed precision tools).

### Status: `designed`. Diagram: `02-designs/mechanic-tool-cart.svg`.