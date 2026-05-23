---
name: putter-anatomy-extended
description: Visual + vocabulary reference for putter head families, hosel families, face technologies, and alignment-aid systems. EXTENDS the `putter-domain` skill — it does not replace it. `putter-domain` owns the base glossary (face / heel / toe / sole / hosel / offset / lie / loft / sweet spot), the two-family split (blade vs mallet), the feel decomposition (balance / forgiveness / sound / impact response), the coordinate system, and the conformance basics; this skill adds the named families, named hosel variants, face-tech vocabulary, and alignment-aid vocabulary that briefs and PR reviews need to commit to specific anatomy. Use this skill any time GolfPro is writing §2 (head family + variant), §6 (hosel + toe hang naming), §7 (face geometry vocabulary), or §8 (alignment-aid naming) of a `putter-design-brief-format` brief; any time GE needs to look up what a named family or hosel looks like; any time CR is grading geometry-vs-brief fidelity for naming consistency. Do NOT use this skill for the base glossary or feel decomposition (read `putter-domain` first), for stroke-arc → toe-hang fitting (that lives in `putter-fitting`), for market cataloging (that will live in `putter-market-reference`), or for USGA conformance rules (that will live in `usga-rules-putters`).
---

# Putter Anatomy (Extended)

This skill is the vocabulary layer between `putter-domain` (base glossary, families, feel decomposition) and the design-brief itself. It names the head families, hosel families, face technologies, and alignment-aid systems that briefs commit and PRs implement.

**Read `putter-domain` first.** Everything below assumes the glossary, the blade/mallet split, the feel decomposition (balance / forgiveness / sound / impact response), and the coordinate system from `putter-domain` are already in your head. This skill extends; it does not duplicate.

**Read `putter-fitting` alongside.** Every hosel family in §2 ties back to a toe-hang band cited from `putter-fitting` §2. The fitting matrix is authoritative on stroke-arc → toe-hang coherence; this skill only catalogs the named hardware that lands in each band.

## 1. Head family taxonomy

The `putter-domain` split is **blade vs mallet**. That is the structural distinction (mass near the face vs mass behind it). Briefs commit a finer grain — six families that GE builds against. Bands below are working ranges for each family; a specific brief lands inside the band per `putter-fitting` and per the player profile.

### 1.1 Blade

- Silhouette: thin, narrow head; near-rectangular footprint; small back cavity or none.
- Mass concentrated at and immediately behind the face.
- Low MOI by design.
- Toe and heel ends look approximately symmetric; the head reads as a single bar from above.
- Top-line is thin (3–5 mm visible at address).
- **Weight band:** 340–360 g at 34–35 in.
- **MOI band (yaw):** 2500–4000 g·cm². Low end of the `putter-domain` reference range.
- **Hosel pairing:** plumber's-neck, short slant, heel-shafted Anser-lineage, flow neck. Hangs sit 30–70° (slight-to-strong arc per `putter-fitting` §2).
- **Market DNA reference:** PING Anser-lineage (the original heel-shafted blade — see PING's product pages at ping.com); Scotty Cameron Newport / Newport 2 (Titleist Vokey / Scotty Cameron product pages at scottycameron.com).

### 1.2 Mid-mallet

- Silhouette: deeper than a blade (face-to-back depth ~50–70% of heel-to-toe length) but not full mallet depth.
- Modest back flange or short rear-extension cavity; not winged.
- Reads as a "blade with more back" at address.
- Top-line typically still visible as a defined edge, not a curved crown.
- **Weight band:** 345–365 g at 34–35 in.
- **MOI band (yaw):** 3500–4800 g·cm². Sits between blade and full mallet.
- **Hosel pairing:** short slant, mid slant, single-bend, plumber's-neck. Hangs 20–45° (straight-stroke to slight-arc per `putter-fitting` §2).
- **Market DNA reference:** PING Tyne family (ping.com); Bettinardi Inovai compact variants (bettinardi.com).

### 1.3 Mallet

- Silhouette: deep head, face-to-back depth ≥70% of heel-to-toe length, often equal or greater.
- Continuous body — no wings, no fangs; the back is one solid or cavitied volume.
- Crown frequently rounded or contoured rather than sharp-edged top-line.
- Room for substantial alignment aids on the crown.
- **Weight band:** 350–370 g at 34–35 in. Tungsten heel/toe weighting common.
- **MOI band (yaw):** 4500–5800 g·cm². Sits comfortably in `putter-domain`'s reference mallet range.
- **Hosel pairing:** single-bend, double-bend, mid slant, center-shafted. Hangs 0–35° (face-balanced to slight-arc per `putter-fitting` §2).
- **Market DNA reference:** Odyssey Two-Ball lineage (odysseygolf.com); Scotty Cameron Phantom family (scottycameron.com).

### 1.4 Tour-mallet

- Silhouette: mallet-depth head with **tour-blade-style top-line cues** — squared edges, defined sight surfaces, cleaner address profile than a full rounded mallet.
- Body is mallet-class in MOI but visually disciplined; aimed at players who want mallet forgiveness without a "tech" look at address.
- Often paired with milled steel construction and tour-weighted heel/toe ports.
- **Weight band:** 350–365 g at 34–35 in.
- **MOI band (yaw):** 4800–5600 g·cm². Mallet-class forgiveness, mid-band.
- **Hosel pairing:** single-bend, short slant, plumber's-neck variants. Hangs 15–40° (slight-arc dominant per `putter-fitting` §2).
- **Market DNA reference:** TaylorMade Spider Tour family (taylormadegolf.com); Scotty Cameron Phantom T-series (scottycameron.com).

### 1.5 Wing-back mallet

- Silhouette: mallet with **distinct rear wings** — two mass-loaded extensions trailing from the heel and toe behind the face, separated by a central channel or sight surface.
- The wings are the MOI-raising feature: mass pushed as far heel/toe and as far back as the head envelope allows.
- The channel between the wings is itself usable as an alignment surface.
- Reads as a mallet at address, but the wings are visible peripherally.
- **Weight band:** 355–370 g at 34–35 in. Wings frequently tungsten-weighted at the extremes.
- **MOI band (yaw):** 5400–6500 g·cm². High-band per `putter-domain`'s reference range.
- **Hosel pairing:** single-bend, double-bend, center-shafted. Hangs 0–25° (face-balanced to low slight-arc per `putter-fitting` §2).
- **Market DNA reference:** Odyssey Triple Track Ten / Ten-class mallets (odysseygolf.com — verify specific model + year against the live product pages, see §6 anti-pattern); TaylorMade Spider Tour X / wing-back Spider variants (taylormadegolf.com).

### 1.6 Fang mallet

- Silhouette: mallet with **two separated rear prongs** ("fangs") extending behind the face, with significant open space between them.
- Distinct from wing-back: fangs are narrower, more isolated, and the channel between them is much wider — the cavity is the alignment surface.
- Most aggressive MOI-per-gram architecture in production: mass at the extreme rear-heel and rear-toe with a hollow centre.
- Address profile is unmistakable — the fangs are part of the alignment system, not just structure.
- **Weight band:** 355–370 g at 34–35 in.
- **MOI band (yaw):** 5800–7000 g·cm². Top of the `putter-domain` reference range; some production fangs exceed 7000.
- **Hosel pairing:** single-bend, double-bend, center-shafted. Hangs 0–20° (face-balanced dominant per `putter-fitting` §2).
- **Market DNA reference:** PING Fetch / Tyne-fang variants (ping.com); Odyssey #7-class fang mallets (odysseygolf.com — verify specific model + year against the live product pages).

### Head-family choice — what the brief commits

§2 of `putter-design-brief-format` commits the family **and a variant cue** (e.g., "wing-back mallet, single-bend hosel variant"). The family fixes the silhouette and the MOI band; the variant cue points at the hosel + alignment combination. Family alone is underspecified — two wing-back mallets with different hosels are different products to GE.

## 2. Hosel family taxonomy

The hosel is where the shaft meets the head. It governs three things: **toe hang** (per `putter-fitting` §2), **offset** (per `putter-domain` glossary), and **the address-perception of where the face is aimed** (per `putter-fitting` §5).

This section catalogs the named hosel families a brief commits in §6. Toe-hang bands below are cited from `putter-fitting` §2 — that document is authoritative on the stroke-arc coherence claim; this skill only names the hardware that lands in each band.

### 2.1 Plumber's-neck

- Visual signature: an L-shaped or stepped neck — the shaft descends, bends forward, then re-bends down into the heel. From above the bend is a clear right angle.
- Shaft enters: heel.
- Offset: full shaft offset — the leading edge of the face sits one full shaft-diameter behind the shaft axis.
- **Toe hang band:** 30–45° (slight arc, high-band per `putter-fitting` §2).
- **Canonical example:** Scotty Cameron Newport 2 with plumber's-neck (scottycameron.com).

### 2.2 Slant — short

- Visual signature: the shaft enters the heel via a short, gently angled slant — a straight section of hosel tilted back from vertical, no step or bend.
- Shaft enters: heel.
- Offset: roughly half shaft offset.
- **Toe hang band:** 20–35° (low-band slight arc per `putter-fitting` §2).
- **Canonical example:** TaylorMade Spider Tour short-slant variants (taylormadegolf.com).

### 2.3 Slant — mid

- Visual signature: longer slant section, more pronounced angle back from vertical than the short slant. Still no step; a single straight tilt.
- Shaft enters: heel.
- Offset: roughly half shaft offset.
- **Toe hang band:** 30–45° (mid-band slight arc per `putter-fitting` §2).
- **Canonical example:** Scotty Cameron mid-slant Newport variants (scottycameron.com).

### 2.4 Slant — long

- Visual signature: the slant is the entire neck — a long, pronounced tilt connecting shaft directly to the heel of the head with no intermediate step. Sometimes called a "full slant" or "long slant."
- Shaft enters: heel.
- Offset: roughly half to two-thirds shaft offset.
- **Toe hang band:** 45–60° (strong arc per `putter-fitting` §2).
- **Canonical example:** Scotty Cameron long-slant Newport variants (scottycameron.com).

### 2.5 Single-bend

- Visual signature: the shaft has **one** smooth bend near the head, entering the head from above the centre-of-mass — not from the heel. Reads as a near-vertical shaft with a single forward kink.
- Shaft enters: centre-of-head (above the CoM, not at the heel).
- Offset: zero or near-zero shaft offset — the face leading edge sits roughly under the shaft axis.
- **Toe hang band:** 0–25° (face-balanced to low slight-arc per `putter-fitting` §2). The exact hang depends on where above the CoM the bend lands.
- **Canonical example:** TaylorMade Spider single-bend variants (taylormadegolf.com).

### 2.6 Double-bend

- Visual signature: the shaft has **two** bends — a first bend forward, then a second bend back to vertical, before entering the head. The shaft enters fully vertical despite the offset.
- Shaft enters: centre-of-head, vertically.
- Offset: full shaft offset, but achieved by the bends, not by an L-neck.
- **Toe hang band:** 0–15° (face-balanced per `putter-fitting` §2).
- **Canonical example:** Odyssey Two-Ball double-bend variants (odysseygolf.com).

### 2.7 Flow neck

- Visual signature: a smooth, curved neck — no discrete bend or step. The shaft transitions into the head via a continuous arc, like a swan's neck. Hand-finished aesthetic, common on tour-issue putters.
- Shaft enters: heel.
- Offset: half to full shaft offset, depending on the curve.
- **Toe hang band:** 40–60° (high slight-arc to strong arc per `putter-fitting` §2).
- **Canonical example:** Scotty Cameron Tour-issue flow-neck Newport builds (scottycameron.com — note these are tour-only or limited-release in many years; treat as DNA reference rather than commodity product).

### 2.8 Centre-shafted

- Visual signature: the shaft enters the head **at the geometric centre of the face**, not the heel. No neck or hosel in the conventional sense — the shaft attaches directly through the crown above the centre.
- Shaft enters: centre of head, directly above the sweet spot.
- Offset: zero — face leading edge is centred under the shaft axis.
- **Toe hang band:** 0–10° (face-balanced per `putter-fitting` §2). The CoM is directly under the shaft, so gravity produces minimal torque about the shaft axis.
- **Canonical example:** Bettinardi BB-Series centre-shafted variants (bettinardi.com).

### 2.9 L-neck

- Visual signature: a sharper, more compact L than the plumber's-neck — a single right-angle bend without the additional forward step. Reads as "plumber's-neck minus the second bend."
- Shaft enters: heel.
- Offset: half to full shaft offset.
- **Toe hang band:** 35–50° (mid-to-high slight-arc per `putter-fitting` §2).
- **Canonical example:** Scotty Cameron L-neck Newport variants (scottycameron.com).

### 2.10 Heel-shafted Anser-lineage

- Visual signature: the shaft enters the head **directly into the heel**, with a short, near-vertical neck — sometimes with a small bend, sometimes none. The defining cue is that the shaft axis and the heel of the head are visually aligned at address.
- Shaft enters: heel, near-vertical.
- Offset: minimal — small or no shaft offset.
- **Toe hang band:** 50–70° (strong arc per `putter-fitting` §2). With the shaft entering at the heel and the CoM displaced toward the toe-side of that point, the head wants to rotate strongly under gravity.
- **Canonical example:** PING Anser (the original heel-shafted blade — ping.com).

### Hosel choice — what the brief commits

§6 of `putter-design-brief-format` commits a hosel family **plus a toe-hang band in degrees**. The hosel name fixes the silhouette and the offset; the degree band fixes the stroke-arc match per `putter-fitting` §2. Hosel name alone is underspecified — a plumber's-neck can be tuned across a ~15° hang range by where the bends land relative to the CoM.

**Visual reference test:** A reader of this skill, shown a photograph of a putter and the head straight-on plus three-quarter view, should be able to name the hosel family from the visual signatures above without seeing a label. If two families are confusable in a given photograph (e.g., short-slant vs L-neck from heel-on view), the brief should still commit a band by naming the family + the target toe-hang degrees — the degrees are the unambiguous spec.

## 3. Face technologies

Face technology is the face's **material and geometry** — not the face's loft (loft is a `putter-domain` spec, set independently). Brief §7 commits the face technology and the intended impact response.

Every claim below names the feel axis it lands on per `putter-domain`'s decomposition (balance / forgiveness / sound / impact response). **Do not bundle.** "Soft feel" is not a spec; "lower-frequency dominant impact mode" is.

### 3.1 Milled face

A milled face is cut directly into the head material (typically 303 / 304 stainless steel, carbon steel, or aluminium for blade and mid-mallet bodies). Groove geometry is set by the milling tool path.

**Groove pattern variables a brief commits:**

- **Depth.** Typical 0.3–0.7 mm. Deeper grooves displace more energy into vertical ball-launch on impact; shallower grooves transmit more energy into forward ball speed for the same stroke.
- **Pitch.** Spacing between groove centres, typical 0.6–1.2 mm. Tighter pitch = more grooves per face = more aggregate edge contact at impact.
- **Orientation.** Horizontal (most common — aligned with the heel-toe axis), vertical, or angled. Horizontal is the convention; deviations are a brief-noted choice, not a default.
- **Dimples / pocked patterns.** An alternative to linear grooves — a regular array of round depressions. Used on some Scotty Cameron Phantom and Odyssey milled inserts (scottycameron.com, odysseygolf.com).

**Feel-axis mapping (per `putter-domain`):**

- **Balance.** Unaffected. Milling removes a small, uniform mass from the face surface; CoM shift is negligible.
- **Forgiveness.** Unaffected by groove geometry directly. (MOI is set by the head body, not the face surface.)
- **Sound.** Affected. A milled steel face produces a higher-frequency, brighter impact sound than an insert face of comparable head. Tighter pitch and shallower depth bias the modal response toward the higher frequencies.
- **Impact response.** Affected. Deeper grooves produce a slightly softer perceived impact (some impact energy is absorbed by the grooves' edges in shear); shallower grooves produce a firmer, more direct impact response.

**Default-truth pending verification:** The depth-vs-pitch contribution to impact response above is the working understanding shared by milling-house publications (Bettinardi, Scotty Cameron) and golf-media measurements. TapIn has not run controlled measurements on its own milled faces; treat the specific contribution of depth vs pitch as default-truth pending CEM-side verification.

### 3.2 Insert face

An insert face is a separate piece of material seated into a cavity in the head's face plate. Insert materials in current production:

- **Urethane** (thermoplastic elastomer). Soft, polymer-class material. Used by Odyssey on White Hot / White Hot OG inserts (odysseygolf.com).
- **Aluminium honeycomb.** A bonded aluminium structure with hexagonal voids, behaving as a tuned stiffness layer. Used in some TaylorMade Spider models (taylormadegolf.com).
- **Dual-density.** Two materials stacked face-to-back — typically a softer outer face layer over a firmer backing. Allows tuning impact response and sound independently. Used in Odyssey 2-Ball Eleven and recent White Hot variants (odysseygolf.com).
- **Co-molded.** Multiple polymers chemically bonded in a single insert during moulding (not stacked layers). Used in some Odyssey White Hot Pro generations (odysseygolf.com).
- **Polymer-over-metal.** A thin polymer face over a metal sub-face. Behaves as a high-stiffness metal face with surface compliance for sound and impact response. Used in Bettinardi Inovai insert variants (bettinardi.com).

**Feel-axis mapping (per `putter-domain`):**

- **Balance.** Affected indirectly. Insert materials have lower density than steel, so a thick insert reduces face-plate mass and shifts CoM slightly back into the head body. The shift is small but real and the brief should note when the insert is thick enough to matter (>4 mm).
- **Forgiveness.** Largely unaffected. Inserts do not change head-body MOI; some marketing claims that "inserts improve forgiveness" by spreading impact across more face area are a contested claim — treat as default-truth pending TapIn measurement. Do not put forgiveness-via-insert language in a brief.
- **Sound.** Strongly affected. Urethane and dual-density inserts produce a markedly lower-frequency, more damped impact sound than a milled steel face. Aluminium honeycomb sits in between. Polymer-over-metal sits closer to the metal face's sound profile.
- **Impact response.** Strongly affected. Urethane gives the softest perceived impact in current production; dual-density tunes the impact response independently of the outer face material. Polymer-over-metal gives a firm impact response with a softened high-frequency edge.

### 3.3 Choosing milled vs insert

Brief §7 commits the choice. The decision logic:

- **Tour-aspirant, slight-or-strong-arc, feedback-rich preference.** Milled face. Sound is brighter; impact response is firmer and more informative.
- **Higher-handicap, forgiveness-prioritised, soft-feedback preference.** Insert face. Sound is damped; impact response is softer.
- **Hybrid or custom feel preference.** Dual-density or polymer-over-metal insert — gives soft outer touch with firmer underlying response.

The choice ties to player profile per `putter-fitting` §1 (the weakness designed against). It does not tie to head family — a blade can be milled or insert-faced; a fang mallet can be milled or insert-faced. Do not assume.

## 4. Alignment-aid systems

The alignment aid is the **visual system on the crown and back of the head** that the player uses to aim the face and confirm setup. Brief §8 commits the aid family and its geometry.

Every aid has a **visual logic** — a reason this aid suits this head architecture and this player perception. A bolted-on aid (an aid that does not serve the head's architecture) is a smell, per `putter-design-brief-format` §8.

### 4.1 Single line (sight line)

- **Geometry:** A single straight line, contrasting colour (typically white on dark head), running fore-aft on the crown from the top-line back. Length 30–80 mm typical; width 1.5–3 mm typical; position centred on the head's heel-toe midpoint.
- **Variants:** Short line (terminates at flange edge), long line (extends across full back depth), top-line line (the top-line edge itself painted as a line, no back-extension), through-line (continues over the back of the head).
- **Visual logic:** Lowest visual noise; serves players who want a clean address profile and trust their natural alignment instinct. The line shows the target direction without adding parallax cues.
- **Best suited to:** Blades, mid-mallets, mallets where the crown is the alignment surface. Less effective on wing-backs (the wings already provide horizontal reference; a single line competes) and fang mallets (the cavity is the natural alignment surface).
- **Production example:** Scotty Cameron Newport 2 sight-dot-and-line variants (scottycameron.com); PING Anser sight-line variants (ping.com).

### 4.2 T-line

- **Geometry:** A fore-aft sight line **plus** a perpendicular cross-bar at the face — together forming a T shape. Cross-bar length 15–30 mm; sight-line length per §4.1.
- **Variants:** Cross-bar at face edge (most common), cross-bar set back from face (less common), reversed T (cross-bar at the back, line at the face) — rare.
- **Visual logic:** The cross-bar gives a **face-square confirmation** — a visible orthogonal reference. Players who need to confirm face squareness at address (commonly straight-back-straight-through stroke players) benefit; players whose stroke arc rotates the face through the stroke can find the cross-bar's apparent rotation distracting.
- **Best suited to:** Mid-mallets and mallets with a flat top-line where the cross-bar reads as a single defined edge. Less effective on rounded mallet crowns.
- **Production example:** PING Tyne family T-line variants (ping.com).

### 4.3 Double-bar — Two-Ball / Triple Track family

- **Geometry:** Two or three parallel bars (or balls) running fore-aft on the crown. **Two-Ball** uses two white circular discs spaced one ball-width apart with the actual ball at address completing a three-ball line. **Triple Track** uses three parallel lines — one central red, two outer blue — running the full back depth.
- **Variants:** Two-Ball (Odyssey 2-Ball / 2-Ball Eleven on odysseygolf.com); Two-Ball Ten (an extended mallet variant); Triple Track (Triple Track #7, Triple Track Ten, and other Triple Track family models on odysseygolf.com — verify specific model + year against the live product pages before citing a specific year in a brief).
- **Visual logic:** Parallel-line systems exploit a perceptual phenomenon ("vernier acuity") — the eye is unusually sensitive to parallel alignment. The system serves players who struggle to aim a single line consistently and who benefit from a redundant alignment cue.
- **Best suited to:** Mallets and tour-mallets with enough crown real estate to render the system at scale. Does not suit blades (insufficient crown surface) or fang mallets (the cavity is the natural alignment surface; parallel lines fight the cavity).
- **Production example:** Odyssey 2-Ball Ten (odysseygolf.com); Odyssey Triple Track Ten family (odysseygolf.com — model + year verification required before brief citation, per the discipline below). **Default-truth pending verification:** TapIn does not have independent measurement of the vernier-acuity benefit of double-bar systems; treat the perceptual claim as the manufacturer's positioning, accepted in industry and golf-media writing but not TapIn-verified.

### 4.4 Sight dot

- **Geometry:** A single round dot (typically 3–6 mm diameter), contrasting colour, positioned on the top-line directly above the sweet spot.
- **Variants:** Dot at top-line edge (Scotty Cameron Newport classic — scottycameron.com), dot set back from face on flange, paired dot (two dots flanking the line).
- **Visual logic:** Minimalist alignment — marks the impact point without imposing a directional line. Serves players whose alignment is instinctive and who want the dot as a swing-thought anchor, not as a directional cue.
- **Best suited to:** Blades. The classic single-dot blade aesthetic.
- **Production example:** Scotty Cameron Newport 2 sight-dot variants (scottycameron.com).

### 4.5 Fang-channel

- **Geometry:** The space **between the two fangs** of a fang mallet (per §1.6) is the alignment surface itself — no painted line, no dot. The channel's parallel inside edges, plus any contrasting colour at the channel base, do the work.
- **Variants:** Open-channel (the channel is empty, the inside edges of the fangs are the cue); painted-floor channel (a contrasting paint at the bottom of the channel between fangs); ridged-floor channel (a moulded ridge runs fore-aft along the channel floor — effectively a sight line inside the cavity).
- **Visual logic:** A fang mallet's architecture **is** the alignment system. Adding a top-line sight line to a fang mallet competes with the fangs visually and dilutes the address signature. The cavity gives the player two parallel reference edges (the inside faces of the fangs) plus a clear directional axis.
- **Best suited to:** Fang mallets exclusively. Bolting a fang-channel onto a non-fang head is geometrically meaningless.
- **Production example:** PING Fetch (ping.com); Odyssey #7-class fang mallets with channel cavities (odysseygolf.com — model + year verification per the discipline).

### 4.6 Top-edge contrast

- **Geometry:** No painted aid. Instead, the **top-line edge itself** is made visually prominent — either by being squared and crisply finished (so it reads as a sharp line at address), by being a contrasting material colour to the crown (e.g., milled steel top-line over a darker anodised crown), or by carrying a chamfer that catches light.
- **Variants:** Squared top-line (most common — sharp 90° edge between face and crown), milled top-line band (a defined 2–4 mm strip of milled metal along the top-line), chamfered top-line (a 30–45° bevel along the face/crown edge).
- **Visual logic:** The top-line edge is **already** an aim cue for many players — squaring it or contrasting it amplifies what the player already uses, without adding visual elements that compete with the architecture. Serves players who alignment-aim "off the top-line" rather than "off a sight line."
- **Best suited to:** Blades, mid-mallets, and tour-mallets where the top-line is a defined edge. Less effective on rounded-crown mallets where there is no sharp top-line to amplify.
- **Production example:** Scotty Cameron Newport-class top-line treatments (scottycameron.com); Bettinardi BB-Series milled top-line (bettinardi.com).

### Alignment-aid choice — what the brief commits

§8 of `putter-design-brief-format` commits the **aid family** + **geometry of the aid** (length, width, position) + **a sentence of visual logic** tying it to head architecture and player perception. The visual-logic sentence is the test that the aid is not bolted on. If the brief cannot explain why this aid suits this head and this player, the aid is decoration, not design.

## 5. Anti-patterns

What bad anatomy reasoning looks like. Each one names the brief failure it produces.

1. *"Plumber's-neck on a wing-back mallet because both look tour."* Hosel chosen by aesthetic, ignoring head-family hang pairing. Plumber's-neck sits at 30–45° toe hang (slight arc); wing-back mallets sit at 0–25° (face-balanced to low slight-arc). The combination is mechanically incoherent and produces a face-open delivery for a face-balanced head's intended player. Per `putter-fitting` §2, the matrix fights itself.

2. *"Milled face for soft feel."* Undecomposed feel, wrong axis. Milled faces produce a **brighter** impact sound and a **firmer** impact response than insert faces. "Soft feel" decomposes into lower-frequency sound and softer impact response (per `putter-domain`) — both of which point to an insert, not a mill. Naming "milled" while targeting "soft" violates the feel decomposition.

3. *"Sight line because it looks clean on the crown."* Aid chosen by aesthetic on a head where the architecture already supplies alignment. On a fang mallet, the cavity is the alignment surface; adding a sight line competes visually with the fangs and dilutes the address signature. On a wing-back, the wings already give parallel horizontal cues. The brief should commit fang-channel (§4.5) or accept the wings as the aid, not paint a line over the architecture.

4. *"Use the player's current putter family because it's familiar."* Head family chosen by player history, not by fitting. Per `putter-fitting` §7, players adapt around mis-fit putters; preserving the family preserves the mis-fit. Family commits in §2 should come from the stroke-arc + MOI-band reasoning per `putter-fitting`, not from "this is what the player currently uses."

5. *"Centre-shafted for a strong-arc player because it removes hosel offset complexity."* Centre-shafted produces 0–10° toe hang (face-balanced per §2.8). A strong-arc player needs 45–70° hang per `putter-fitting` §2. Pairing centre-shafted with a strong-arc stroke produces consistent face-open misses — the head cannot rotate during the stroke because gravity does not torque it.

6. *"Triple Track because it's a popular alignment system."* Aid chosen by market popularity, not by head architecture or player perception. Triple Track requires crown real estate (suits mallets and tour-mallets per §4.3); on a blade the system cannot render at scale. The brief should commit a Triple Track-family aid only when the head is a mallet or tour-mallet with the surface for it.

7. *"Insert face for forgiveness."* Wrong feel axis. Inserts affect **sound** and **impact response**; forgiveness lives in the head-body MOI (per `putter-domain`'s decomposition). Marketing claims that inserts "improve forgiveness by spreading the strike" are default-truth pending verification, not engineering basis. The brief should ground forgiveness in §5 (MOI band) and use §7 (face technology) only for sound + impact response.

## 6. Worked example

This example exercises a different profile from `putter-fitting` §8 to show the skills compose across different player types.

**Player profile (intake):**

- Right-handed, 5'9", hunched/forward-tilted posture.
- 8-handicap; current putter is a 35in mallet with a single-bend hosel and a Triple Track aid.
- SAM PuttLab report: 5.8° face rotation through stroke → strong-arc band per `putter-fitting` §1.
- Misses right consistently on 6–12ft pressure putts; lag distance control is good.
- Smooth, deliberate tempo — describes own stroke as "rhythmic."

**Anatomy choices for the brief:**

- **§2 Head family and variant** (per §1 of this skill): **Blade, plumber's-neck variant.** The strong-arc stroke pairs with the blade family's hang range (30–70° per §1.1) and with the player's "rhythmic" tempo (lighter MOI band suits feedback-rich strokes per `putter-fitting` §5's Impact response axis). The current mallet + single-bend + Triple Track is a fitting mismatch — face-balanced head fighting a strong-arc stroke (anti-pattern #5 inverted). The push-right pattern on pressure putts is the misfit signature, not a tendency to design *against* — designing *for* the strong arc removes the misfit.
- **§6 Hosel and toe hang** (per §2 of this skill, citing `putter-fitting` §2): **Plumber's-neck hosel, toe hang 35–45° below horizontal.** Mid-band slight-arc per the matrix; sits at the lower end of the strong-arc band, which fits a 5.8° rotation comfortably without committing to the highest-hang flow-neck builds. Plumber's-neck visual signature (§2.1 of this skill) — L-shape from above, full shaft offset, shaft enters the heel.
- **§7 Face geometry** (per §3 of this skill): **Milled face, 0.5 mm depth grooves at 0.9 mm pitch, horizontal orientation.** Brighter impact sound and firmer impact response per §3.1's feel-axis mapping — matches the player's rhythmic, feedback-rich stroke preference. Explicit not-an-insert choice, against the current putter's likely insert.
- **§8 Alignment aid** (per §4 of this skill): **Top-edge contrast, squared and milled.** Aid family per §4.6. Visual logic: blade silhouette (§1.1) has a defined top-line; amplifying that edge with a milled top-line band suits a player whose alignment reads off the top-line and removes the visual noise of the current Triple Track system (§4.3 is wrong for a blade per anti-pattern #6).

**How the skills compose:**

- `putter-domain` supplied the feel decomposition that §3 of this skill maps face technology against, and the blade/mallet structural split that §1 refines into six families.
- `putter-fitting` §2 supplied the strong-arc → toe-hang band that §2 of this skill catalogs hosel hardware against.
- `putter-fitting` §5 supplied the tempo → MOI-band reasoning that §1 of this skill expresses as per-family MOI ranges.
- This skill (`putter-anatomy-extended`) named the specific families, hosels, face tech, and alignment aids the brief commits — without re-deriving the fitting or feel theory.

The worked example produces §2, §6, §7, and §8 of the brief. §1 (player profile), §3 (dimensions), §4 (head-weight target), §5 (MOI band), §9 (market references), and §10 (non-goals) come from `putter-fitting` and from the brief author's design judgement — not from this skill.

## What this skill does not cover

- **Base glossary** (face, heel, toe, sole, hosel, offset, lie, loft, sweet spot, insert in the glossary sense, sight line in the glossary sense). Read `putter-domain`.
- **Feel decomposition** (balance, forgiveness, sound, impact response as the four axes). Read `putter-domain`.
- **Coordinate system, units, reference dimensions.** Read `putter-domain`.
- **Stroke-arc bands, length × lie matrix, head-weight by length, L.A.B. exception.** Read `putter-fitting`.
- **Specific currently-produced model catalog** (every Newport variant, every Spider variant, every Inovai variant, with specs and years). That will live in `putter-market-reference` (skill #4).
- **USGA conformance for face roughness, head dimensions, MOI, anchoring.** That will live in `usga-rules-putters` (skill #5).

When a brief needs anything in the list above, cite the right skill. This skill names the families and the hardware; the other skills do the rest.

