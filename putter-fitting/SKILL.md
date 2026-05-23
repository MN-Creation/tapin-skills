---
name: putter-fitting
description: How GolfPro reasons from a player profile to the four putter-fitting choices a design brief must commit — stroke-arc → toe-hang → hosel family, length × lie, head-weight band, and the modern exceptions that intentionally break the matrix. Use this skill any time GolfPro is writing a brief's §1 (Target player profile), §4 (Head-weight target), §6 (Hosel and toe hang), or evaluating an existing brief's fitting coherence. Cited by `putter-design-brief-format` for the stroke-arc → toe-hang lens. Do NOT use this skill for face geometry, alignment aids, MOI band selection, market-reference cataloging, or non-putter clubs — those have their own skills or are out of scope.
---

# Putter Fitting

The fitting matrix turns "who is the player?" into the small set of putter-head spec commitments a design brief must make. GolfPro uses this matrix to write §1, §4, and §6 of a brief and to red-flag a brief whose fitting decisions do not cohere with the named player profile.

The matrix is a **default**, not a law. §6 names the modern designs (notably L.A.B. Golf's lie-angle-balanced family) that intentionally void the stroke-arc → toe-hang dependency.

## 1. Stroke arc — bands and detection

Three bands, defined by **face rotation through the stroke** (degrees of face-angle change from mid-backstroke to mid-followthrough):

| Arc band | Face rotation through stroke | Visual signature |
|---|---|---|
| Straight (SBST) | 0–2° | Path stays parallel to target line; toe traces a near-straight line |
| Slight arc | 2–4° | Mild inside-square-inside path; toe drifts ~1–2 cm inside on backstroke |
| Strong arc | 4°+ | Pronounced inside-square-inside path; toe drifts >2 cm inside; rotation visible to a coach across the green |

**Detection sources, in order of trust:**

1. SAM PuttLab (Science & Motion Sports) or Quintic Ball Roll session report — gives face rotation in degrees.
2. Coach-observed path during a 20-putt session at 10 ft.
3. Player self-report ("I take it inside" / "I keep it straight back") — least reliable, often wrong; verify before committing brief copy.

## 2. Stroke arc → toe hang → hosel family

Toe hang convention: balance the shaft horizontally on a finger near the head, then measure the angle of the toe below horizontal.

| Stroke arc | Toe-hang band | Compatible hosel families | Mechanical reason |
|---|---|---|---|
| Straight (SBST) | 0–15° (face-balanced to slight) | Double-bend, center-shafted, full-balanced single-bend | Head is torque-passive about the shaft axis → does not want to rotate during the stroke |
| Slight arc | 20–45° (quarter to half) | Short slant, mid-slant, single-bend with toe-bias, certain plumber's-neck variants | Head wants to rotate slightly under gravity → matches the hands' mild rotational delivery |
| Strong arc | 45–70° (half to full) | Long slant, flow neck, heel-shafted Anser-lineage, full shaft offset | Head wants to rotate strongly → matches an arc'd stroke; resists the hands "blocking" the rotation |

**Compatibility means default, not absolute.** A slight-arc player can land at 25° hang or 40° hang — both sit inside the band. The brief commits a band, not a point value, and the geometry can land anywhere inside.

**Source:** Toe-hang ↔ stroke-arc coherence is the consensus fitting principle published by PING in their public fitting resources at ping.com, and echoed in the fitting documentation of Club Champion, True Spec, and Edel Golf. The degree ranges in the table are the working bands TapIn uses; published bands vary by ~5° at the boundaries.

## 3. Length × lie — height and posture

Length sets eye position relative to the ball at address. Lie sets the angle the sole presents to the ground; a mismatched lie tilts the face at impact (toe-up → ball pushed right for a right-hander; toe-down → ball pulled left).

| Player height | Posture | Length band | Lie band |
|---|---|---|---|
| Under 5'8" | Hunched / forward-tilted | 33–34 in | 68–70° (flatter accommodates a hunched setup) |
| 5'8"–6'0" | Neutral | 34–35 in | 70° (standard) |
| 6'0"–6'4" | Neutral to upright | 35–35.5 in | 70–71° |
| Over 6'4" | Upright | 35.5–36 in | 71–72° |

**Validation step:** Impact tape on the sole after a 10-putt session. Heel-strike marks dominant → lie is too upright; toe-strike marks dominant → lie is too flat. The matrix gives the starting band; tape gives the confirmation.

**Out-of-grid systems** (separate fittings, do not interpolate from the table):

- **Armlock putters** — 41–43 in. The forearm is the lever; length follows forearm length, not body height.
- **Broomstick / long putters** — 48–52 in. Top hand anchors near the sternum; length follows torso, not full body.
- **Counter-balanced standard-length** — 35.5–36 in with a heavy grip; not the same as a player who is genuinely tall.

**Source:** Length × lie bands are working ranges from Club Champion and True Spec public fitting documentation. The impact-tape validation protocol is universal across fitting houses; PING describes the same procedure for irons in their iPing materials and extends it to putters in fitting-cart workflow.

## 4. Head weight — bands by length

Head weight and length are coupled: shorter lever → needs more head mass to keep tempo stable; longer lever → can carry less head mass for the same swing-weight.

| Length | Head-weight band | Grip class | Rationale |
|---|---|---|---|
| 33 in | 360–375 g | Standard pistol (~80–90 g) | Short lever → need more mass to load the stroke; without it, tempo gets jittery |
| 34 in | 350–365 g | Standard pistol | Working band for shorter players or hunched setups |
| 35 in | 340–355 g | Standard pistol | Reference band — what "standard" means in catalog copy |
| 35.5–36 in counter-balanced | 360–380 g | Oversize / counter-balanced grip (110–150 g) | Heavy grip shifts the balance point toward the hands; head mass increases to restore swing-weight |
| 41–43 in armlock | 380–410 g | Armlock grip (long, flat) | Forearm-anchored stroke → head needs mass to track stably through impact |
| 48–52 in broomstick | 400 g+ | Broomstick grip system | Top-hand anchor → the head is the pendulum bob; mass anchors the pendulum |

**Tempo coupling:** Players with a quicker natural tempo benefit from the lighter end of each band; slower-tempo players from the heavier end. Tempo is a player property, not a head property — the brief targets the band; the band has room for tempo bias.

**Source:** Weight-by-length bands are consistent with Edel Golf and Club Champion public fitting documentation. The grip-weight balance-point relationship is published by SuperStroke and Lamkin in their grip-spec sheets.

## 5. Why each parameter matters — by feel axis

The `putter-domain` skill decomposes "feel" into **balance**, **forgiveness**, **sound**, and **impact response**. Fitting parameters land on specific axes; a brief should never bundle them under the word "feel."

**Stroke arc / toe hang / hosel — Balance axis.** Toe hang is the static moment of the head about the shaft axis. A mismatched hang fights the stroke: a strong-arc player with a face-balanced head leaks the face open at impact because the head resists the hands' rotation; a straight-stroke player with a strong-toe-hang head closes the face because the hands cannot keep up with the head's rotational tendency. The mismatch shows up as directional misses, not as "bad feel" — but the player will describe it as "this putter doesn't feel right."

**Length × lie — Balance + Forgiveness axes.** Lie sets where on the face contact happens for a given stance. A 2° lie mismatch moves the impact point roughly 4–6 mm vertically on the face. The head's MOI about the vertical (yaw) axis is highest at the geometric center; off-center contact reduces effective MOI at the impact point and increases face twist on the mis-hit. Length sets eye-over-ball position, which sets the player's perception of the target line — a length mismatch produces alignment errors that read as fitting errors.

**Head weight — Impact response + Balance axes.** Head mass governs ball-speed-per-stroke-length (the conversion from stroke amplitude to roll distance) and the damping of the hand response at impact. Light heads on short shafts produce jittery tempo and inconsistent distance control; heavy heads on long shafts produce a stable pendulum but a slow-to-react stroke that struggles on quick greens. Head weight also shifts the system's balance point along the shaft, which is why grip choice is part of the head-weight conversation, not a separate one.

**Hosel offset — Balance axis + perception.** Offset moves the CoM of the head relative to the shaft axis and shifts where the eyes perceive the face to be aimed at address. A full-shaft-offset head appears more "square" to many players because the leading edge of the face sits behind the shaft; a no-offset head appears more "open" for the same reason. The perceptual effect is as load-bearing on putting performance as the mechanical effect, and the brief should commit to both.

## 6. Modern exceptions — designs that void the matrix

The matrix in §2 assumes the head must be torque-passive *about the shaft axis* during the stroke. **L.A.B. Golf** (Lie Angle Balanced Golf) breaks that assumption: their heads are balanced about an axis aligned with the **lie angle** of the putter, not the vertical shaft axis. When the head is supported at its proper lie angle, gravity acts through the CoM in a line such that there is no torque about the shaft axis — the face does not twist under gravity across the stroke arc.

**Practical implication for fitting:**

- A strong-arc player and a straight-stroke player can both use the same L.A.B. head; the stroke-arc → toe-hang matching is no longer a constraint.
- Toe-hang as a measurement is meaningless on a L.A.B. head — the conventional balance-on-finger test reads numbers that do not predict the head's in-stroke behavior.
- The brief still commits length, lie, and head-weight bands per §3 and §4. Only the §2 matrix is voided.

**What does not change for a L.A.B. brief:**

- Length × lie still matters — L.A.B. publishes lie-specific SKUs because the lie-balance is calibrated to a specific lie angle.
- Head-weight bands still apply — L.A.B. heads sit in standard weight bands for their length class.
- Eye position, stroke comfort, and tempo fitting are unchanged.

**Citation.** The lie-angle-balanced design principle is documented on L.A.B. Golf's product pages at labgolf.com for the current model families (Mezz, DF, Link, and successors). The principle was developed and commercialized by founder Bill Presse IV; the company has held the public-facing technical narrative since founding. **Known gap:** TapIn does not currently have independent third-party measurement confirming that conventional toe-hang testing is meaningless on L.A.B. heads — the claim is sourced to the manufacturer. Treat as default-truth pending third-party verification, and disclose the sourcing in any brief that cites L.A.B. DNA.

**Other matrix-edge designs to be aware of (do not bundle with L.A.B.):**

- **Armlock putters.** The forearm-anchored stroke constrains arc geometry; the §2 matrix applies less strongly because the forearm removes most of the hands' rotational degree of freedom. Treat armlock fittings as their own grid (length, lie, weight) and discuss toe-hang as a secondary preference, not a primary constraint.
- **Adjustable-hosel mallets.** Some current heads ship with multiple interchangeable necks (toe-hang configurable post-purchase). The brief still commits a band; the configurability is a manufacturing/UX choice GE may or may not implement.

## 7. Anti-patterns

- **"Plumber's neck because it looks tour."** Hosel chosen by aesthetic, not stroke arc. A plumber's-neck sits at the high end of the slight-arc toe-hang band; on a straight-stroke player it produces face-open pushes.
- **"Face-balanced for all players — it's the safest choice."** False. A slight-or-strong-arc player with a face-balanced head will miss left from open-faced impact. There is no "safe default" hosel.
- **"34 inches as default without checking posture."** Length must be matched to height and posture. A 6'2" upright player on a 34in putter stoops; a 5'7" hunched player on a 35in putter extends. Either way, eye-over-ball is wrong and alignment suffers.
- **"Heavier head is better — more stable."** Head weight is fitting-coupled to length and grip. A 380g head on a 35in shaft with a standard grip is over-weighted for the length; tempo bogs down and short-putt timing breaks.
- **"L.A.B. removes the need for fitting."** L.A.B. removes the stroke-arc → toe-hang dependency. It does not remove length, lie, head-weight, eye-position, or tempo fitting.
- **"Toe hang can be adjusted by shaft installation."** Toe hang is a head property determined by hosel geometry plus center-of-mass location. The shaft does not change it. (Interchangeable hosels are a separate design choice, not shaft-induced adjustability.)
- **"Use the player's current putter specs as the target."** Players adapt around mis-fit putters. A fit-from-scratch may produce specs the player has never tried; that is the work, not a red flag.
- **"Soft face means better feel."** Undecomposed feel. Face-material choice affects impact response (and sound), not balance or forgiveness. Name the axis.

## 8. Worked example — fitting a player to brief copy

**Player profile (intake):**

- Right-handed, 6'1", neutral posture
- 12-handicap; current putter is a 34in Anser-style blade with a mid-slant hosel
- SAM PuttLab report: 3.2° face rotation through stroke → slight-arc band
- Pulls 15ft+ lag putts left; pushes 4–6ft tempo putts right
- Quick natural tempo (player describes own stroke as "decisive")

**Fitting reasoning:**

- Stroke arc is confirmed slight-arc (PuttLab number sits inside §1's 2–4° band).
- Per §2, toe-hang band is 20–45° → short-slant, mid-slant, or single-bend with toe-bias. Plumber's-neck sits at the band's high edge; the player's quick tempo argues against it (over-rotation risk on short tempo strokes, consistent with the observed push-misses on 4–6ft).
- Per §3, height 6'1" + neutral posture → length 35–35.5 in, lie 70–71°. The current 34in is short for the player's height; the stoop that creates may be contributing to the pull pattern on long lag putts.
- Per §4, length 35 in + standard pistol grip → head-weight 340–355g. Quick tempo argues toward the lighter end of the band.

**Brief copy (drops directly into §1, §4, §6 of `putter-design-brief-format`):**

> **§1 Target player profile.** Right-handed, 6'1", neutral posture, slight-arc stroke (3.2° face rotation per SAM PuttLab; slight-arc band per `putter-fitting` §1). Quick natural tempo. Weakness designed against: pull-misses on 15ft+ lag putts and push-misses on 4–6ft tempo strokes — pattern consistent with a too-short current putter and a hosel hang sitting at the high end of the slight-arc band.
>
> **§4 Head-weight target.** 345 ± 5 g. Paired with a 35in length and a standard pistol grip, this band sits at the lighter end of the standard-length band per `putter-fitting` §4, accommodating the player's quick tempo without forcing a counter-balance.
>
> **§6 Hosel and toe hang.** Single-bend or short-slant hosel, toe hang 25–35° below horizontal — mid-band per the slight-arc row of `putter-fitting` §2. Explicitly avoid full plumber's-neck (sits at the high end of the slight-arc band; the player's quick tempo creates over-rotation risk on short strokes).

The worked example does not produce §2, §3, §5, §7, §8, §9, §10 of the brief — those come from head-family choice and the rest of the design intent, not from fitting. Fitting answers four questions; the brief answers ten.
