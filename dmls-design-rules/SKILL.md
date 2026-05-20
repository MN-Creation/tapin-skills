---
name: dmls-design-rules
description: Design rules for metal additive manufacturing (DMLS / SLM laser powder-bed fusion) printing of TapIn's putter heads. Use this skill when designing or reviewing geometry that will be metal-printed, evaluating printability of a CEM output, building the design-rule checker, or interpreting `print-readiness.json` results. Single source of truth for rule thresholds — the JSON schema and the checker module mirror this file. Do NOT use this skill for plastic FDM/SLA printing or for casting/machining design rules.
---

# DMLS / Metal AM Design Rules

This skill is the **single source of truth** for TapIn's DMLS printability rules. The Studio's `print-readiness.json` schema and the kernel checker mirror the rule set defined here.

Spec of record: [TAP-106](/TAP/issues/TAP-106). Wave: Print Readiness ([TAP-101](/TAP/issues/TAP-101)).

## Status: populated (v1)

Goal 2 ships verifiable printability. Rules are conservative across published handbooks (Materialise, Protolabs, Xometry, Renishaw, EOS). Vendor-specific tightening will be tracked under Goal 4 when a print house is contracted.

## What DMLS / SLM is

Laser powder-bed fusion (L-PBF) processes:
1. A bed of fine metal powder (~30–50 μm grain) is laid down.
2. A laser fuses powder where the part should exist for that layer.
3. The bed lowers, more powder is laid, the next layer is fused.
4. Repeat for thousands of layers (typical layer thickness 30–60 μm).
5. Excess powder is removed, the part is cut from the build plate, surface treated.

Binder jet is similar but uses a binding fluid + a sintering oven step instead of laser fusion. Rules below assume L-PBF unless noted.

## Materials TapIn targets (density only this wave)

| Material | Density (g/cc) | Notes |
|---|---|---|
| 316L stainless steel | 8.00 | Default. Good corrosion resistance, common, moderate cost. |
| 17-4PH stainless | 7.80 | Higher strength, age-hardenable. |
| Ti6Al4V (titanium) | 4.43 | Light, strong; ~3× the cost of stainless. |
| Tungsten (inserts only) | 19.30 | Weight ports only — not the parent print material. |

Full material database (modulus, yield, modal coefficients) is **out of scope** this wave (Physics Depth wave).

## The rule set

Each rule has an id, a name, a threshold pair (`recommended` and `minimum`), units, severity bands, what it checks, and a public citation. The checker emits one result per rule per evaluated orientation.

**Severity semantics (uniform across rules):**
- `green` — measured value meets or exceeds `recommended`. Pass.
- `yellow` — measured value between `minimum` and `recommended`. Caution; print likely possible with care.
- `red` — measured value below `minimum`. Fail; geometry must be corrected.

Conservatism rule: when sources disagree, the **tighter** value wins. Both numbers are recorded in the `comment` field of the rule definition.

### WALL_MIN — Minimum wall thickness

- **Threshold:** `recommended` 1.0 mm, `minimum` 0.5 mm
- **Units:** mm
- **What it checks:** Local thickness of every voxel-shell wall in the part. Minimum-thickness sampling along surface normals; reports the thinnest measurement in mm.
- **Source:** Materialise, *Stainless Steel SS316L design guidelines*, section "Wall thickness" — Standard Grade 1 mm, Performance Grade 0.5 mm, structural recommendation 2 mm.
  - URL: https://www.materialise.com/en/academy/industrial/design-am/stainless-steel-ss316l
- **Cross-reference (looser):** Protolabs cites 0.1524 mm for high-resolution metals (https://www.protolabs.com/resources/design-tips/7-mistakes-to-avoid-when-designing-3d-printed-parts/). Materialise's tighter value is used.
- **Comment:** Putter faces routinely run 2.5–4.0 mm and are not at risk. The thin-section risk is in cavity-back walls and weight-port walls.

### WALL_STRUCTURAL — Recommended structural wall thickness

- **Threshold:** `recommended` 2.0 mm (advisory; no `minimum` band — degrades to WALL_MIN below 2.0 mm)
- **Units:** mm
- **What it checks:** Walls supporting loaded geometry (not cosmetic detail). Emits `yellow` below 2.0 mm, `green` at or above. No red band — WALL_MIN owns the red band.
- **Source:** Materialise, *SS316L*, section "Wall thickness" — "a thickness of 2 mm is recommended to create structural walls or features".
  - URL: https://www.materialise.com/en/academy/industrial/design-am/stainless-steel-ss316l
- **Comment:** Quality hint, not a hard fail.

### FEATURE_MIN — Minimum positive feature size (pin / boss / raised detail)

- **Threshold:** `recommended` 1.0 mm, `minimum` 0.5 mm
- **Units:** mm
- **What it checks:** Diameter (or smallest cross-section) of any positive feature standing proud of the parent surface: pins, bosses, sight-line ridges, alignment dots. Engraved (recessed) details are exempt.
- **Sources (multi-source; tighter chosen):**
  - Materialise SS316L "Detail size" — minimum detail 0.5 mm. URL: https://www.materialise.com/en/academy/industrial/design-am/stainless-steel-ss316l
  - Xometry, *DMLS Design Tips*, "Pin/Feature size" — minimum reliable pin diameter 1.0 mm. URL: https://xometry.pro/en/articles/dmls-design-tips/
- **Comment:** Sight lines should be **engraved** (recessed), not raised — engraved features tolerate lower limits.

### OVERHANG_ANGLE — Self-supporting overhang angle

- **Threshold:** `recommended` ≥ 45°, `minimum` ≥ 35°
- **Units:** degrees from build plate (horizontal = 0°, vertical = 90°)
- **What it checks:** Every triangle's down-facing angle relative to the build plate, in the evaluated orientation. Areas below 35° require external supports → red; areas between 35° and 45° → yellow (printable with supports, surface quality penalised); ≥ 45° → green.
- **Source:** Materialise SS316L, section "Surface quality and orientation" — "Angles < 45° from the build platform result in poorer surface quality and typically require support; angles > 45° produce better, smoother surfaces."
  - URL: https://www.materialise.com/en/academy/industrial/design-am/stainless-steel-ss316l
- **Cross-reference (looser):** EOS-aligned literature notes 35° is achievable on tuned machines (Cambridge / Renishaw review: https://www.cambridge.org/core/services/aop-cambridge-core/content/view/3969D4E6D526FCCB38B78AC0990EA2DF/S2732527X21005423a.pdf). Materialise's stricter 45° baseline is the green threshold.
- **Comment:** Orientation-dependent. Evaluated per build orientation.

### TRAPPED_VOLUME — Trapped / un-drained internal volume

- **Threshold:** `recommended` 0 enclosed cavities; `minimum` (red) any fully-enclosed cavity with no escape path of diameter ≥ 3 mm reaching the exterior in the evaluated build orientation.
- **Units:** cm³ (volume) and mm (escape-path diameter)
- **What it checks:** Connected-component analysis of internal void space. For each enclosed void, trace the largest connected free-surface path to exterior. No ≥ 3 mm path → red. 2.0–3.0 mm path → yellow.
- **Source:** Materialise SS316L, section "Powder removal" — "When making a hollow model, it is important to include at least one hole … minimum diameter of 3 mm, with larger and complex cavities needing multiple holes with larger diameters, preferably 7 mm."
  - URL: https://www.materialise.com/en/academy/industrial/design-am/stainless-steel-ss316l
- **Comment:** Trapped powder is unrecoverable mass inside the part — it wrecks MOI/balance and is a USGA conformance risk. Blocks ship.

### HOLE_PRINTED_MIN — Minimum printed hole diameter

- **Threshold:** `recommended` 2.0 mm, `minimum` 1.0 mm
- **Units:** mm (diameter)
- **What it checks:** Diameter of any cylindrical/near-cylindrical void in the part intended to be **printed** rather than drilled post-process. Smaller holes risk sealing during the print.
- **Sources:**
  - Materialise SS316L "Holes" — 2 mm minimum diameter for printed holes. URL: https://www.materialise.com/en/academy/industrial/design-am/stainless-steel-ss316l
  - Xometry DMLS Design Tips — printed-hole support-free range 0.5–6.0 mm; minimum reliable diameter 1.0 mm. URL: https://xometry.pro/en/articles/dmls-design-tips/
- **Comment:** Distinct from HOLE_DRILLED_MIN. Tag holes intended for post-process drilling with `mode=drilled` in the geometry input.

### HOLE_DRILLED_MIN — Minimum hole diameter when post-process drilled

- **Threshold:** `recommended` 1.0 mm, `minimum` 0.5 mm
- **Units:** mm (diameter)
- **What it checks:** For holes flagged as "drilled" (printed undersized then opened by machining), the threshold relaxes — the print needs only a pilot. Pilot < 0.5 mm risks seal-shut.
- **Source:** Protolabs DMLS guidance — "Holes less than 0.025 in. (0.635 mm) will be susceptible to sealing shut or coming smaller than designed."
  - URL: https://www.protolabs.com/resources/design-tips/7-mistakes-to-avoid-when-designing-3d-printed-parts/
- **Comment:** Defaults to HOLE_PRINTED_MIN unless geometry input marks the hole as drilled.

### ASPECT_RATIO — Aspect ratio of slender pin / wall / boss

- **Threshold:** `recommended` ≤ 8 : 1 (height : section), `minimum` ≤ 10 : 1 (red above 10 : 1)
- **Units:** dimensionless ratio
- **What it checks:** For any feature whose vertical (build-Z) extent exceeds 8× its narrowest cross-section, emit yellow; above 10× red. Flags hosels, long thin sight ridges, or cantilevers that whip during the print.
- **Source:** Xometry DMLS Design Tips, "Aspect ratio" — "maximum ratio of vertical height to section is 8 : 1, which will ensure stability of printing parts on build plate."
  - URL: https://xometry.pro/en/articles/dmls-design-tips/
- **Cross-reference:** Forge Labs DMLS Design Guide cites the same 8 : 1. URL: https://forgelabs.com/dmls-design-guide/
- **Comment:** Hosels are the obvious risk. `heel-down` orientation typically reduces the worst-case aspect-ratio path.

### UNSUPPORTED_SPAN — Unsupported horizontal bridge / span

- **Threshold:** `recommended` ≤ 1.0 mm, `minimum` ≤ 2.0 mm
- **Units:** mm
- **What it checks:** Length of any horizontal (≤ 35° to build plate) span of solid material connecting two supported regions, where the span itself is not supported from beneath. Above 2.0 mm sag is likely — span must be supported or redesigned.
- **Sources:**
  - Xometry DMLS Design Tips — "Limit unsupported bridge spans to 2 mm." URL: https://xometry.pro/en/articles/dmls-design-tips/
  - Protolabs DMLS — overhang > 0.5 mm requires support. URL: https://www.protolabs.com/resources/design-tips/7-mistakes-to-avoid-when-designing-3d-printed-parts/
- **Comment:** Distinct from OVERHANG_ANGLE: an angled overhang ≥ 45° is fine at any length; a horizontal span has its own limit.

### CLEARANCE_MIN — Minimum clearance between distinct features

- **Threshold:** `recommended` ≥ 0.5 mm, `minimum` ≥ 0.4 mm
- **Units:** mm
- **What it checks:** Smallest gap between two distinct features that must remain distinct after print (e.g., two adjacent pins; a pin and adjacent wall). Below 0.4 mm features can fuse during sintering.
- **Source:** Xometry DMLS Design Tips, "Feature spacing" — "minimum distance between features: 0.5 mm." URL: https://xometry.pro/en/articles/dmls-design-tips/
- **Cross-reference:** Materialise general design-for-AM notes a 0.4–0.5 mm gap recommendation. The 0.5 mm green threshold is conservative across both.
- **Comment:** Putter heads rarely run this close, but weight-port walls and sight-line groove edges can.

### FILLET_RADIUS — Fillet radius at sharp internal corners

- **Threshold:** `recommended` ≥ 3.0 mm (advisory; no red band)
- **Units:** mm
- **What it checks:** Internal corner fillet radius at major load paths (face-to-sole, hosel-to-head joint). Below 3.0 mm yellow; below 1.0 mm yellow + stress-warning flag. No red band — small fillets do not block a print, they accelerate fatigue.
- **Source:** Materialise SS316L, section "Thermally induced stresses" — "minimum fillet radius: 3 mm on edges."
  - URL: https://www.materialise.com/en/academy/industrial/design-am/stainless-steel-ss316l
- **Comment:** Advisory only this wave — Physics Depth wave will replace this with FEA-derived hot-spot detection.

## Build-plate orientations TapIn ships

The checker runs **all four** orientations on every part and reports per-orientation results. The verdict picks the best-scoring orientation. Rotations are in degrees, **intrinsic XYZ** (applied X→Y→Z), starting from the design frame.

**Design frame** (fixed convention):
- `+X` = heel → toe
- `+Y` = back → face (face-normal direction)
- `+Z` = sole → top (the direction the shaft points in playing pose)

| Preset | Rotation (deg, intrinsic XYZ) | Rationale | Trade-offs |
|---|---|---|---|
| `sole-down` | `(0, 0, 0)` | Default playing pose; sole bonds to plate. Stable, broad footprint. | Face is vertical — likely needs supports on the face side. Hosel cantilevers off the heel. |
| `face-down` | `(90, 0, 0)` | Face bonds to plate; face comes out flattest, post-process polish removes plate-contact texture. For cavity-back families this also orients the cavity opening upward → free powder removal (acts as `cavity-up`). | Hosel sticks out laterally — long cantilever, may warp. Internal cavity walls become downward-facing → supports inside cavity, expensive to remove (note: this only applies to cavities that face the same direction as the print face; for cavity-back the cavity is upward and clean). |
| `face-up` | `(-90, 0, 0)` | Face is on top; no support contact on face. Sole bonds to plate cleanly. | Face surface roughness is the as-printed worst case — must be milled flat anyway. Cavity-back cavity opens downward → unsupported cavity ceiling, supports needed. |
| `heel-down` | `(0, 90, 0)` | Putter stands on its heel. Long axis (heel→toe) is vertical → reduces worst-case aspect-ratio path. Hosel points laterally instead of cantilevering. | Smaller plate-contact footprint → less stable, more warpage risk. Side surfaces of toe and face are downward-facing → many small support contacts. |

The checker computes the **best-verdict orientation** and surfaces it as `recommendedOrientation`. Ties broken by lexical order above.

## STL validation policy (mesh-integrity checks)

These checks run **before** any rule scoring. A red failure halts further evaluation — no point checking thresholds on a non-manifold mesh.

| Check | Pass/Fail definition | Severity on fail |
|---|---|---|
| `MANIFOLD` | Every edge in the mesh is shared by **exactly two** triangles. Edges shared by 1 (boundary) or 3+ (T-junctions / non-manifold edges) fail. | `red` |
| `WATERTIGHT` | The mesh has zero boundary edges (every edge is interior). Closed-surface check. | `red` |
| `NORMAL_CONSISTENT` | All face normals point outward; no inverted triangles. Detected by signed-volume sign and adjacency walk. | `red` |
| `NO_DEGENERATE_TRIS` | Every triangle has area > 1e-6 mm² and no two vertices coincident. | `red` |
| `NO_SELF_INTERSECT` | No pair of non-adjacent triangles intersect. **Advisory** — expensive O(n²) check, may be skipped on very large meshes. | `yellow` if found, `info` if skipped |
| `BOUNDED_VERTEX_COUNT` | Vertex count ≤ 5,000,000 (Studio's export ceiling). Prevents accidental over-tessellation. | `yellow` |
| `UNITS_MM` | STL header/metadata asserts millimetre units. STL has no native units field, so this is a contract check between exporter and validator. | `yellow` (default-assume mm) |

If `MANIFOLD`, `WATERTIGHT`, `NORMAL_CONSISTENT`, or `NO_DEGENERATE_TRIS` fail, overall verdict is **red** regardless of rule scores, and rule scoring may be skipped.

## `print-readiness.json` schema (v1) — summary

See [TAP-106](/TAP/issues/TAP-106) for the canonical schema; this section is a non-normative summary.

```json
{
  "schemaVersion": "1.0.0",
  "geometrySource": {
    "family": "mallet-half-moon",
    "parameters": { /* family-specific parameter map */ },
    "geometryHash": "sha256:..."
  },
  "material": { "name": "316L", "density_g_cc": 8.00 },
  "stlValidator": {
    "checks": [
      { "id": "MANIFOLD", "status": "pass", "count": 0 },
      { "id": "WATERTIGHT", "status": "pass", "count": 0 }
    ]
  },
  "orientations": [
    {
      "preset": "heel-down",
      "rotationDeg": [0, 90, 0],
      "rules": [
        {
          "id": "WALL_MIN",
          "status": "green",
          "measured": 1.42,
          "thresholdRecommended": 1.0,
          "thresholdMinimum": 0.5,
          "units": "mm",
          "source": "Materialise SS316L Wall thickness",
          "sourceUrl": "https://www.materialise.com/en/academy/industrial/design-am/stainless-steel-ss316l"
        }
      ],
      "verdict": "green",
      "drivenBy": null
    }
  ],
  "recommendedOrientation": "heel-down",
  "overallVerdict": "green",
  "overallDrivenBy": null
}
```

`overallDrivenBy` / `drivenBy` reference the rule id that produced the worst severity (e.g. `"OVERHANG_ANGLE"`) — null when everything is green.

## Putter-specific gotchas

- **Hosel** is a long thin cantilever → triggers ASPECT_RATIO in `sole-down`; `heel-down` typically clears it.
- **Weight-port cavities** with tungsten inserts → trigger TRAPPED_VOLUME unless a powder-removal channel is modelled. CEM must emit the channel.
- **Cavity-back interior** → triggers OVERHANG_ANGLE in `face-up` (cavity ceiling unsupported); `face-down` orients cavity upward and is the cavity-back family's preferred orientation.
- **Sight lines**: engraved, not raised. A 0.5 mm raised line trips FEATURE_MIN at yellow on most fonts/strokes.
- **Face flatness**: every orientation produces a face that requires milling (~0.5 mm stock removal). Post-process, not a print-rule violation.

## When to use this skill

- Reviewing any putter geometry for printability.
- Building or extending the design-rule checker module.
- Choosing print orientation in the export pipeline.
- Estimating print cost (rough: cost ≈ mass × material rate × 1.5–2.0).
- Investigating why a specific design failed to print.

## When NOT to use this skill

- For non-AM processes (machining, casting, forging).
- For plastic prototyping (FDM, SLA).
- For finished-product surface specs after polishing.
- For full material strength / modal analysis (Physics Depth wave).

## Open TODOs (Goal 4 — out of scope this wave)

- [ ] **Researcher:** Choose primary print house. Candidates: Shapeways, Sculpteo, Protolabs, i.materialise. Compare on putter-relevant materials, minimum wall thickness, post-processing options, lead time, cost per kg, MOQ.
- [ ] **Researcher:** Obtain chosen vendor's published design guide. Tighten any rule whose value is conservatively above the vendor minimum.
- [ ] **Researcher:** Source physical samples — print at least one putter head per orientation family. Document deltas between published rules and real prints.
- [ ] **CEM Engineer:** Wire the rule checker to consume PicoGK voxel fields directly so checks run on the kernel's native representation, not on the exported STL.
