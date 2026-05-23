---
name: putter-design-brief-format
description: How GolfPro writes a putter design brief — the source-of-truth document GeometryEngineer (GE) builds parametrically in PicoGK. Use this skill any time GolfPro is commissioned to produce a design brief (issue titled "Design brief: <putter family> for <player profile>"). The brief is GolfPro's only deliverable on a design commission and the only document GE is contractually bound to honor. Get the format right. Do NOT use this skill for advisory PR reviews (those grade an implementation against an already-ratified brief), Director Briefings, or any non-putter design work.
---

# Putter Design Brief Format

The design brief is the contract between design intent and geometry. GolfPro writes it. Director ratifies it. GE implements against it. CR + Director merge against it.

## Audience and constraints

- **Primary reader:** GeometryEngineer. Builds the head parametrically in PicoGK. Needs bands, not point values, and rationale for every band so edge cases resolve sensibly.
- **Ratifier:** Director (Mike). Reads in 5 minutes to ratify or send back with redlines. No jargon without a one-line gloss.
- **Length:** One scrollable document. 300–500 words of prose plus the structured spec. If a brief exceeds two screens, it has crept into implementation detail.
- **Tone:** TapIn voice. Direct. No optimism padding. No marketing language.
- **Format:** Markdown. Saved as an issue document with key `design-brief` on the commissioning Issue.

## Structure

Use exactly these ten sections, in this order, with these exact headings:

### 1. Target player profile

Handedness, height range, posture (upright / neutral / hunched), stroke arc (straight / slight-arc / strong-arc with degree band), and the **specific putting weakness this head is designed against** (e.g., "pull-misses on mid-range lag putts" — not "wants to putt better").

### 2. Head family and variant

Name the family (`blade` / `mid-mallet` / `mallet` / `tour-mallet` / `wing-back mallet` / `fang mallet`) and the variant (e.g., "wing-back mallet, single-bend hosel variant"). One sentence on the market DNA being borrowed if any (Anser lineage, Newport heel-shafted blade, Spider rear-weighted, L.A.B. lie-angle-balanced).

### 3. Dimensions

Bands with tolerances. Never point values. Cover at minimum:
- Blade length (heel-to-toe) — mm ± mm
- Blade depth (face-to-back) — mm ± mm
- Top-line thickness — mm ± mm
- Overall height — mm ± mm

If a dimension is unconstrained by intent, write "GE discretion within DMLS rule envelope" — do not pad with fake numbers.

### 4. Head-weight target

A band in grams with rationale tied to length and player profile. Standard ~340g for a 35in driver-length putter; counter-balanced builds run 360–370g; broomstick 400g+. State the band, then one sentence linking it to length, grip choice, and stroke tempo.

### 5. MOI band

g·cm² as a range (e.g., 5000–5400). One sentence of rationale citing the **MOI vs feel tradeoff** lens: high-MOI forgives mis-hits but mutes feedback. The band is the design choice; explain where on that tradeoff this player lives.

### 6. Hosel and toe hang

Hosel family (plumber's-neck / slant / single-bend / double-bend / flow / center-shafted) and the toe-hang band in degrees. Cite the **stroke-arc → toe-hang coherence** lens: straight stroke → face-balanced; slight arc → ~30–40° hang; strong arc → ~45–70° hang. The hosel must serve the stroke, not the head shape.

### 7. Face geometry

Milled face vs insert. If milled: groove pattern (depth × pitch, plus orientation if not horizontal). If insert: material family (urethane / aluminum-honeycomb / co-molded) and intended impact response. One sentence on **sound and impact response** (per `putter-domain` feel decomposition) the face is targeting.

### 8. Alignment aid

Single line / T-line / fang-channel / sightdot / triple-track. State the geometry of the aid (length, width, position) and a sentence of **visual logic** — why this aid for this head architecture and this player. A bolted-on aid is a smell.

### 9. Market references

Two to four putters currently in production that share design DNA with this brief. Each as `Manufacturer Model (Year)` — e.g., `Odyssey Triple Track Ten (2023)`. One sentence per reference naming the specific DNA element being borrowed (rear weighting, plumber's-neck hang, fang alignment, etc.). No bare model names without manufacturer or year.

### 10. Explicit non-goals

What this putter is **not** trying to be. Three to six bullets. This is the section GE relies on most when an ambiguous tradeoff appears mid-implementation. Examples: "not face-balanced", "not counter-balanced", "not an insert face", "not a tour-blade silhouette".

## Format rules

- **Bands, not point values.** A point value is false precision GE cannot honor exactly. Every dimensional, mass, MOI, and angle spec is a range with a tolerance.
- **Cite, do not assert.** Market references carry manufacturer + model + year. Stroke-arc and toe-hang claims cite the `putter-fitting` matrix. Rule-of-Golf claims cite Rule number + version date. If a citation is missing, the line does not ship — surface the gap as a known unknown in the relevant section.
- **Decompose "feel".** "Feels soft" is not a spec. Per `putter-domain`, feel decomposes into balance, forgiveness, sound, and impact response. Any feel claim names which axis.
- **Reads in 5 minutes.** No preambles. No history lessons. No marketing voice. If a sentence does not change what GE builds, delete it.
- **Plain numerals.** "340±5g" not "around three hundred and forty grams".
- **Manufacturability respect.** If a brief asks for geometry that fails the DMLS rule checker, CR + GE win — revise the brief, do not pressure the rule envelope.

## Worked example

> ## 1. Target player profile
> Right-handed, 5'10"–6'2", neutral-to-upright posture, slight-arc stroke (3–5° face rotation), tour-aspirant amateur. Weakness designed against: pull-misses on 15–25ft lag putts under tournament pressure.
>
> ## 2. Head family and variant
> Tour-mallet, wing-back variant, single-bend hosel. DNA borrowed from the rear-weighted tour-mallet lineage popularised by Spider Tour-class heads.
>
> ## 3. Dimensions
> - Blade length: 112 ± 2 mm
> - Blade depth: 98 ± 3 mm
> - Top-line thickness: 4.2 ± 0.3 mm
> - Overall height: 25 ± 1 mm
>
> ## 4. Head-weight target
> 350 ± 5 g. Paired with a 34in length and a standard pistol grip, this band keeps tempo stable on lag-length strokes without forcing a counterbalance.
>
> ## 5. MOI band
> 5000–5400 g·cm². Sits high on the forgiveness curve for off-center lag strikes, but stays below the band where impact feedback flattens out — the player still wants to feel a heel miss.
>
> ## 6. Hosel and toe hang
> Single-bend hosel, toe hang 30–40° below horizontal. Matches the slight-arc stroke band per the `putter-fitting` matrix.
>
> ## 7. Face geometry
> Milled face, 0.5 mm depth grooves at 0.8 mm pitch, horizontal. Target a crisp mid-frequency impact sound — feedback-rich without ringing.
>
> ## 8. Alignment aid
> Single 60 mm white sightline running fore-aft across the flange, terminating at the top-line. Visual logic: high-MOI wing-back heads benefit from a long line that uses the cavity as the alignment surface; a T-line would compete with the wings.
>
> ## 9. Market references
> - `Odyssey Triple Track Ten (2023)` — rear-weighted wing-back silhouette.
> - `TaylorMade Spider Tour X (2022)` — single-bend hosel paired with mid-arc-friendly toe hang.
> - `Ping Tyne 4 (2023)` — milled-face mid-MOI mallet reference for impact response.
>
> ## 10. Explicit non-goals
> - Not face-balanced.
> - Not counter-balanced — head weight stays in the 340–355g working band.
> - Not insert-faced.
> - Not a tour-blade silhouette — this is a mallet, not a Newport derivative.
> - Not a high-toe-hang head — anything above ~45° is out of scope.

## Anti-patterns

What a bad brief looks like, and why each line fails:

- *"Make it feel soft and forgiving."* — undecomposed feel; "forgiving" without an MOI band; no axis named.
- *"MOI: high."* — not a band; not implementable; GE has to guess.
- *"Like the Scotty putter."* — no manufacturer + model + year; "the Scotty putter" names a brand, not a design.
- *"Head weight 350g."* — point value masquerading as precision; no tolerance; no rationale.
- *"Plumber's neck for clean look."* — hosel chosen by aesthetic, not by stroke arc; violates **stroke-arc → toe-hang coherence**.
- *"USGA conforming."* — assertion without Rule number or version. The conformance contract is non-negotiable; cite it properly or do not cite it.
- *Brief has no §10.* — without explicit non-goals, GE has to invent them mid-implementation, and CR has no basis to push back.

## Ratification workflow

After the brief is posted as an issue document with key `design-brief`:

1. Move the commissioning Issue to `in_review`.
2. Create a `request_confirmation` issue-thread interaction targeting Director with:
   - title: "Ratify design brief: <brief title>"
   - body: link to the `design-brief` document, summary of player profile + head family in one sentence, one sentence on the headline design tradeoff being made.
   - `continuationPolicy: wake_assignee` so GolfPro is woken on the decision.
   - decline-with-reason enabled.
3. Leave the Issue in `in_review`. The Issue is in a real waiting path — not abandoned.
4. On Director **accept**: post a comment confirming ratification, hand back to CEO for GE-Issue filing (CEO files `Geometry: implement <brief title>` against GE with the ratified brief linked as source-of-truth), then mark the GolfPro Issue `done`. Do NOT file the GE Issue yourself — that routing is CEO's lane.
5. On Director **decline-with-reason**: read the decline, revise the `design-brief` document on the same Issue (update, do not replace — preserve revision history), then raise a fresh `request_confirmation` against the new revision. Stay `in_review`. If revisions exceed two rounds, flag the impasse back to CEO instead of grinding a third revision.

A brief that has not been ratified is not a brief. Do not let GE start work against an unratified draft, even informally on a PR thread.
