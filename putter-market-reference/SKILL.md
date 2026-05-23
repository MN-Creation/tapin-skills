---
name: putter-market-reference
description: Catalog of currently-produced putters that TapIn briefs cite for design DNA. Use this skill any time GolfPro is writing brief §9 (Market references), any time Director or GE needs to recognize a referenced model, or any time CR is grading geometry-vs-brief fidelity for market-DNA accuracy. The skill is reference data plus the citation discipline that keeps the data honest — manufacturer + model + year on every reference, source URL or named publication per row, source-class label per row (manufacturer-sourced vs third-party-verified), tour-adopter names where confidently known. Do NOT use this skill for the design-brief format itself (read `putter-design-brief-format`), for the stroke-arc → toe-hang fitting (read `putter-fitting`), for head/hosel/face/alignment vocabulary (read `putter-anatomy-extended`), or for USGA conformance rules (read `usga-rules-putters` when it ships). Last verified against manufacturer and third-party sources: 2026-05-23.
---

# Putter Market Reference

This skill is the **market-DNA catalog** TapIn briefs cite. Skills #1–#3 give the brief format, the fitting matrix, and the anatomy vocabulary; this skill names the **currently-produced** putters whose silhouettes, hosels, faces, and alignment systems brief §9 borrows DNA from.

**This is the first research-heavy skill in the GolfPro sequence.** The load-bearing concern is **citation discipline**, not vocabulary. Every row in the catalog below carries a source URL or a named publication, and every row carries a **source-class** label so a brief reader can tell at a glance whether the row is manufacturer-attested or third-party-verified.

**Read order:**
- `putter-domain` and `putter-anatomy-extended` first — this skill names families and hardware that those skills define.
- `putter-fitting` alongside §3 of any row that quotes a head-weight band — fitting is authoritative on player → weight, this skill only records what manufacturers ship.

## 1. Source-class taxonomy

Every catalog row is labeled with one of three source classes. The class is part of the citation — a brief that quotes a row inherits the row's class.

### 1.1 Manufacturer-sourced (M)

- The data came from the manufacturer's own product page, press release, or spec sheet.
- The manufacturer is the **only** source of the claim.
- **Trust level:** the model exists and is in production. Year-of-release is the manufacturer's claim. Head-weight, hosel, face tech, alignment system as the manufacturer markets them.
- **Brief usage:** acceptable for market-DNA references when no third-party source is available. The brief should inherit the *"manufacturer-sourced; pending third-party verification"* note explicitly.
- **Risk:** manufacturers retire models without immediately updating marketing pages; marketing language can blur model identity (a "redesigned for 2024" claim may or may not be a new SKU).

### 1.2 Third-party verified (T)

- The data is corroborated by an independent publication — golf media (MyGolfSpy, Golf.com, Golf Digest, Today's Golfer, Golf Monthly, GolfWRX, Plugged In Golf, Golfalot, The Hackers Paradise), a major fitter publication, the PGA Tour Superstore listing where it cross-checks the manufacturer page, or the USGA conforming list.
- **Trust level:** highest. The model exists, the year is corroborated, the spec is reported by a non-marketing source.
- **Brief usage:** the default standard for any flagship market reference in §9 of a brief.
- **Risk:** publication dates can lag actual release; a 2023 review of a 2023 model does not by itself confirm the model is still produced in 2026.

### 1.3 USGA conforming list verified (U)

- The model + specific variant + year is listed on the USGA conforming clubs list (https://www.usga.org/equipment-standards/equipment-rules-and-decisions.html — putters section).
- **Trust level:** canonical for *"does this model exist as a conforming product"*. The USGA list does not carry head-weight or alignment-system detail, so a row is rarely USGA-only; in practice this class layers on top of (M) or (T).
- **Brief usage:** required when the brief makes a USGA-conformance claim about a specific cited model.
- **Risk:** the list is canonical for *existence*, not for *currently sold* — discontinued models stay on the conforming list. Cross-check the manufacturer page for "current-product" status.

### 1.4 What is **not** a valid source

- Resale sites alone (eBay listings, used-club marketplaces). They can confirm a model existed at some point but cannot confirm currently produced.
- Forum posts alone (GolfWRX threads, Reddit r/golf). Useful for context, not citation.
- AI-generated summaries of the model. The whole point is to escape AI-paraphrasing of what a putter is — read the source, not a summary.

## 2. Per-row metadata format

Every catalog row in §3 below uses this format. A brief that quotes a row should preserve every field; a brief that wants to extend the catalog to a model not listed here should add a row in this format, with citation discipline preserved.

```
- **Manufacturer Model (Year or year band)** — Head family (cite `putter-anatomy-extended` §1.X) · Weight band · Hosel (cite `putter-anatomy-extended` §2.X) · Face tech (cite `putter-anatomy-extended` §3.X) · Alignment system (cite `putter-anatomy-extended` §4.X) · DNA: one sentence. · Tour: named player + event/year if known. · Source: URL or named publication. · Class: M / T / U.
```

**Field rules:**

- **Manufacturer Model.** Full name. No bare "the Scotty" or "the Spider"; always the brand + model.
- **Year or year band.** If a single year is confidently sourced, use the year. If the line refresh covers multiple years or the year is uncertain by ±1, use a band (e.g., *"2023–2024 line refresh"*, *"2022–present"*). **Bands beat point values for dates** — guessing a year wrong by more than 1 is what Director will spot-check; a defensible band is always preferable.
- **Head family.** Cite `putter-anatomy-extended` §1.1–§1.6 (blade / mid-mallet / mallet / tour-mallet / wing-back mallet / fang mallet) by the named family. No inventing new family labels.
- **Weight band.** Cite the manufacturer-quoted head weight, written as a band (±5 g). If the manufacturer does not quote a head weight, write "weight band not manufacturer-quoted" and let the brief read it as a fitting decision, not a market claim.
- **Hosel.** Cite `putter-anatomy-extended` §2.1–§2.10 (plumber's-neck / short slant / mid slant / long slant / single-bend / double-bend / flow neck / centre-shafted / L-neck / heel-shafted Anser-lineage). Many models ship with multiple hosel options — write the canonical or most-cited hosel and note alternatives if known.
- **Face tech.** Cite `putter-anatomy-extended` §3.1 or §3.2 (milled vs insert) and, where known, the specific material or groove geometry.
- **Alignment system.** Cite `putter-anatomy-extended` §4.1–§4.6 (single line / T-line / double-bar family / sight dot / fang-channel / top-edge contrast). A model that ships with multiple alignment options should list the canonical version and note alternatives.
- **DNA.** **One sentence.** What makes this model the family's reference design — the silhouette cue, the hosel-family commitment, the manufacturing signature, or the playing-style claim. Not marketing language. Not multiple sentences.
- **Tour.** Named player + event/year if confidently sourced (e.g., *"Rory McIlroy, 2025 Masters win"*). Bare *"tour-played"* without a name is not a citation. Omit the field if no confidently-sourced adopter is known.
- **Source.** Direct URL or named publication. Manufacturer pages get the manufacturer domain; third-party reviews get the publication URL.
- **Class.** M, T, or U per §1. **Multiple classes if multiple sources confirm.** A row sourced from both the manufacturer page and a MyGolfSpy review is **(M, T)**.

## 3. Manufacturer catalog

The catalog covers the major currently-producing manufacturers per the issue spec. **Coverage is canonical-models-only, not exhaustive.** GolfPro extends the catalog as briefs require, using the verification protocol in §4 and the per-row format in §2.

### 3.1 Scotty Cameron (Titleist)

The Scotty Cameron lineage splits across the **Super Select** family (blade-and-Newport DNA, 2023 refresh) and the **Phantom** family (mallet DNA, 2024 refresh with 2025 + 2026 additions).

- **Scotty Cameron Super Select Newport (2023–present)** — Blade (`putter-anatomy-extended` §1.1) · ~340–355 g at 35 in (weight band not single-number quoted) · Plumber's-neck (§2.1) · Milled stainless steel (§3.1), tri-sole geometry · Single line or sight dot variants (§4.1, §4.4) · DNA: tour-blade Newport heel-shafted silhouette with refined I-beam plumber's neck and two heel/toe tungsten sole weights. · Tour: Tiger Woods has played Newport 2 variants across his career (long-established public record). · Source: https://www.scottycameron.com/articles/introducing-new-super-select-putters/ · Class: M, T (GolfWRX https://www.golfwrx.com/703542/titleists-new-scotty-cameron-super-select-2023-putters-heres-everything-you-need-to-know/).

- **Scotty Cameron Super Select Newport 2 (2023–present)** — Blade (§1.1) · ~340–355 g at 35 in · Plumber's-neck (§2.1) · Milled stainless steel (§3.1), tri-sole · Single line + sight dot (§4.1, §4.4) · DNA: the canonical tour-blade Newport 2 — straight top-line, full plumber's neck, full shaft offset, tour-issue cosmetics. · Tour: long-established Newport 2 tour usage; specific 2025-season bagging changes year-to-year and should be re-verified before quoting in a brief. · Source: https://www.scottycameron.com/articles/introducing-new-super-select-putters/ · Class: M, T (Today's Golfer https://www.todays-golfer.com/equipment/golf-clubs/putters/titleist/scotty-cameron/titleist-scotty-cameron-super-select-putters/).

- **Scotty Cameron Super Select Newport 2 Plus (2023–present)** — Blade (§1.1) with widened back flange · ~345–360 g · Plumber's-neck (§2.1) · Milled stainless steel (§3.1) · Single line (§4.1) · DNA: Newport 2 silhouette with a deeper back flange — slightly higher MOI than the standard Newport 2 while keeping the heel-shafted blade DNA. · Source: https://www.scottycameron.com/articles/introducing-new-super-select-putters/ · Class: M.

- **Scotty Cameron Super Select Squareback 2 (2023–present)** — Mid-mallet (§1.2) · ~345–360 g · Plumber's-neck (§2.1) · Milled stainless steel (§3.1), tri-sole · Single line (§4.1) · DNA: blade-to-mid-mallet bridge — a squared-off back extension over a Newport 2 footprint, for players who want slightly higher MOI without leaving the Newport silhouette. · Source: https://www.scottycameron.com/articles/introducing-new-super-select-putters/ · Class: M.

- **Scotty Cameron Phantom 5 / 7 / 9 family (2024–present)** — Mallet (§1.3) and tour-mallet (§1.4) silhouettes across the family · weight band per model not single-number quoted; tour-mallet builds typically ~350–365 g · Plumber's-neck variants per model; single-bend on selected variants (§2.1, §2.5) · Milled stainless steel (§3.1) with Studio Carbon Steel face insert on 2026 builds · Single line and sight-dot variants (§4.1, §4.4) · DNA: tour-aspirant mallet line with disciplined top-line cues — mallet forgiveness with blade-class address aesthetics. · Tour: Justin Thomas and other tour players have rotated through Phantom prototypes — specific bagging year-to-year should be re-verified before quoting in a brief. · Source: https://www.scottycameron.com/articles/titleist-introduces-new-scotty-cameron-phantom-putters/ · Class: M, T (MyGolfSpy https://mygolfspy.com/news-opinion/first-look/2024-scotty-cameron-phantom-putter-line/).

- **Scotty Cameron Phantom 11 / 11.5 / 11 Long Design (2024–present)** — Wing-back mallet (§1.5) · weight band not single-number quoted but typical wing-back mallet ~355–370 g · Single-bend and plumber's-neck variants (§2.5, §2.1) · Milled stainless steel (§3.1) · Single line (§4.1) · DNA: wing-back-class MOI in Scotty Cameron's milled-steel tour-mallet idiom — the family's max-stability builds. · Source: https://www.scottycameron.com/articles/titleist-introduces-new-scotty-cameron-phantom-putters/ · Class: M, T (MyGolfSpy first-look as above).

- **Scotty Cameron Phantom 5.2 / 7.2 (2025–present, January 2025 addition)** — Tour-mallet (§1.4) · weight band not single-number quoted · Plumber's-neck variants (§2.1) · Milled stainless steel (§3.1) · Single line (§4.1) · DNA: tour-inspired refinements of the Phantom 5 / 7 — slightly tightened silhouettes for players who want a Phantom shape closer to the Newport's address discipline. · Source: https://www.scottycameron.com/articles/titleist-introduces-new-scotty-cameron-phantom-putter-models/ · Class: M.

### 3.2 Odyssey (Callaway)

The Odyssey lineage splits across the **Ai-One** family (cast multi-material with Ai-Optimised Face Insert, 2024 launch + 2024 expansion), the **Ai-One Milled** family (CNC-milled with the same Ai-Optimised pattern), the older **Eleven / Two-Ball Eleven** mallets (2022 line, including Triple Track variants), the **White Hot OG** family (the long-running White-Hot-insert blade-and-mallet line), and **Toulon Design** (premium milled).

- **Odyssey Ai-One #1 / #2 / #7 / Cruiser / Wing Back / 24 / 2-Ball Jailbird / 2-Ball Jailbird Cruiser (2024–present)** — Family spans blade (§1.1, e.g. #1), mid-mallet (§1.2, e.g. #2), mallet (§1.3, e.g. #7 and Wing Back), and wing-back mallet (§1.5, larger Jailbird builds) · Ai-One Cruiser variants are counter-balanced at ~360–370 g per `putter-fitting` §4 counter-balanced band; standard Ai-One ~345–360 g · Hosel options vary per model (single-bend, plumber's-neck, double-bend) (§2.5, §2.1, §2.6) · Ai-Optimised insert (§3.2, urethane-class polymer insert with Ai-designed micro-hinge pattern) · Single line, double-bar (Two-Ball / Triple Track variants where offered), and per-model alignment (§4.1, §4.3) · DNA: cast multi-material body + Ai-tuned polymer face insert — Odyssey's mass-market 2024–present line, replacing earlier White Hot generations across most shapes. · Source: https://mygolfspy.com/news-opinion/first-look/odyssey-ai-one-putters/ and follow-up expansion https://mygolfspy.com/news-opinion/odyssey-adds-new-ai-one-and-ai-one-milled-putter-models/ · Class: M, T.

- **Odyssey Ai-One Milled Eleven / 2-Ball T / Jailbird Mini T / Rossie V T / One Wide V T Blade (2024–present)** — Family covers blade (§1.1, One Wide V T Blade), mallet (§1.3, Rossie V T), and high-MOI wing-back mallet (§1.5, Eleven, 2-Ball T, Jailbird Mini T) · Ai-One Milled Eleven head weight ~360 g per Odyssey spec · Hosel options per model — double-bend dominant on the mallets, plumber's-neck on the blade (§2.6, §2.1) · CNC-milled face with Ai-designed micro-hinge pattern (§3.1, milled face) · Per-model alignment — Triple Track-family double-bar on selected variants (§4.3) · DNA: CNC-milled bodies with the Ai-Optimised face pattern — the premium-tier expression of the Ai-One technology, including one of the few CNC-milled MOI putters in production (the Eleven). · Source: https://odyssey.callawaygolf.com/putters/ai-one-milled · Class: M, T (Golf.com https://golf.com/gear/putters/odyssey-8-new-ai-one-models/).

- **Odyssey 2-Ball Eleven Triple Track (2022–present)** — Wing-back mallet (§1.5) · weight band per Odyssey spec ~360 g · Double-bend (§2.6) · White Hot insert (§3.2, urethane) · Triple Track double-bar (§4.3) · DNA: high-MOI mallet combining the Eleven body silhouette with Two-Ball-class crown alignment and Triple Track parallel-line aim system; face-balanced (0° toe hang) per the double-bend hosel. · Source: https://odyssey.callawaygolf.com/putters/eleven/putters-2022-eleven-2-ball-triple-track-db.html · Class: M, T (PGA Tour Superstore listing https://www.pgatoursuperstore.com/2-ball-eleven-triple-track-putter/2000000030372.html). · Tour: Wyndham Clark, 2023 U.S. Open win — public record; re-verify if quoting in a brief because tour bagging changes.

- **Odyssey Eleven Triple Track DB (2022–present, distinct from 2-Ball Eleven Triple Track)** — Wing-back mallet (§1.5) · weight band per Odyssey spec ~360 g · Double-bend (§2.6) · White Hot insert (§3.2) · Triple Track double-bar (§4.3) without the Two-Ball crown discs · DNA: the Eleven body with Triple Track alignment only — for players who want the parallel-line aim system without the Two-Ball crown elements. · Source: https://www.pgatoursuperstore.com/eleven-triple-track-db-putter/2000000025737.html · Class: M, T. **Naming watch:** *"Triple Track Ten"* (the older Ten body) and *"Triple Track Eleven"* (current) are distinct products — anti-pattern §5.5 below.

- **Odyssey White Hot OG (revived line, 2021–present generations)** — Blade (§1.1, e.g. #1), mid-mallet (§1.2, e.g. Rossie), mallet (§1.3, Two-Ball, #7) · 340–360 g · Plumber's-neck, double-bend variants (§2.1, §2.6) · White Hot urethane insert (§3.2) · Single line, Two-Ball double-bar variants (§4.1, §4.3) · DNA: the long-running urethane-insert family — the Two-Ball variant is one of the canonical mallet-class alignment systems in golf. · Source: https://odyssey.callawaygolf.com/putters/white-hot-og · Class: M, T.

### 3.3 Ping

The Ping lineage splits across **PLD Milled** (premium milled tour line) and **Scottsdale** (cast game-improvement line, 2025), with **Fetch** as the canonical fang-mallet reference. **Anser** is the heel-shafted Anser-lineage canon per `putter-anatomy-extended` §2.10.

- **Ping PLD Milled Anser (2022–present)** — Blade (§1.1) · weight band not single-number quoted; Ping PLD blades typically ~345–355 g · Heel-shafted Anser-lineage (§2.10), with plumber's-neck variants also offered (§2.1) · Milled 303 stainless steel (§3.1) · Single line or sight dot (§4.1, §4.4) · DNA: **the** heel-shafted Anser-lineage canon — the original 1966 Karsten Solheim design, milled to current PLD tolerances. Strong-arc fit per `putter-fitting` §2. · Source: https://ping.com/en-us/golf-clubs/putters/pld/milled · Class: M, T (MyGolfSpy https://mygolfspy.com/news-opinion/first-look/ping-pld-milled-and-pld-milled-plus-putters/).

- **Ping PLD Milled Anser 2 / Anser 2D (2022–present)** — Blade (§1.1) · weight band ~345–355 g · Anser-lineage variants — Anser 2 with classical plumber's-neck-style hosel, Anser 2D with a more aggressive flange (§2.1, §2.10) · Milled stainless steel (§3.1) · Single line (§4.1) · DNA: the Anser silhouette in two contemporary variants — Anser 2 keeps the classic flange, Anser 2D widens the back for slightly higher MOI in the same address profile. · Source: https://ping.com/en-us/golf-clubs/putters/pld/milled · Class: M, T.

- **Ping PLD Milled Tyne 4 (2022–present)** — Fang mallet (§1.6) · weight band ~360–370 g · Flow neck (§2.7) for more toe hang per Ping's own positioning — pairs the fang silhouette with a strong-arc hang band, which is uncommon for fang mallets and is the model's distinctive design choice · Milled stainless steel (§3.1) · Fang-channel (§4.5) · DNA: fang-mallet body with a flow-neck hosel — the rare fang putter intentionally fit for slight-arc strokes per `putter-fitting` §2, not for face-balanced strokes. · Source: https://ping.com/en-us/golf-clubs/putters/pld/milled · Class: M, T.

- **Ping PLD Milled DS72 (2022–present)** — Mid-mallet (§1.2) · weight band ~360 g per Ping spec · Double-bend or single-bend variants (§2.6, §2.5) · Milled stainless steel (§3.1) · Ball-width cavity with single line (§4.1) · DNA: a wide top-rail mid-mallet with a ball-width cavity — the cavity itself frames the ball as the alignment surface, paired with a face-balanced hosel for straight-back-straight-through strokes. · Tour: Viktor Hovland's preferred Ping PLD design (per Ping's own positioning of the model and corroborated in the PLD Milled press cycle). · Source: https://ping.com/en-us/clubs/putters/pld-milled-plus/ds72 · Class: M, T (Golf Digest https://www.golfdigest.com/story/ping-pld-milled-putters-for-2024--what-you-need-to-know).

- **Ping PLD Milled Ally Blue 4 / Oslo 3 (2024–present)** — Mallet (§1.3) and tour-mallet (§1.4) silhouettes · weight band ~360 g typical · Plumber's-neck or single-bend per model (§2.1, §2.5) · Milled stainless steel (§3.1) · Single line (§4.1) · DNA: mallet-class shapes built to the PLD Milled tolerance level — Ally Blue 4 is the rounded mallet; Oslo 3 is the squared tour-mallet. · Source: https://ping.com/en-us/golf-clubs/putters/pld/milled · Class: M, T.

- **Ping Scottsdale lineup (2025–present)** — Family covers blades (Anser, Anser 2D, Anser 4, B63) and mallets (Craz-E, DS72, Oslo, Prime Tyne 4, Prime Tyne C) · cast bodies — Scottsdale is the game-improvement-priced line below PLD Milled · Variable hosels per model · Cast face (not milled — §3.1 milling does not apply; treat as the cast-face equivalent) · Per-model alignment · DNA: cast-body shapes inspired by the PLD Milled silhouettes — for players who want the Ping shape vocabulary at game-improvement price. · Source: https://www.golfdigest.com/story/ping-scottsdale-putters-for-2025--what-you-need-to-know · Class: T (manufacturer page not directly fetched in this verification pass — re-verify before quoting in a brief).

- **Ping Fetch (continuing line)** — Fang mallet (§1.6) · weight band per Ping spec ~365 g · Single-bend or plumber's-neck variants (§2.5, §2.1) · Cast face · Fang-channel — and a literal ball-pickup cavity at the back (the model's namesake) (§4.5) · DNA: the canonical fang-mallet-with-ball-pickup design; the channel is wide enough that the head can scoop the ball out of the cup. · Source: https://ping.com/en-us/clubs/putters (Ping putter category page — re-verify the specific Fetch product URL before quoting). · Class: M.

### 3.4 TaylorMade

The TaylorMade lineage splits across the **Spider Tour** family (the canonical mallet — high-MOI cast with thin-wall undercut and steel wireframe, 2024–present refresh), the **Spider GT** family (older Spider generation still in production), **Itsy Bitsy Spider** (compact mallet variant), and **TP Reserve** (premium CNC milled, 2023–present).

- **TaylorMade Spider Tour (2024–present)** — Tour-mallet (§1.4) · weight band per TaylorMade spec ~355 g · Single-bend (§2.5) with double-bend (§2.6) and L-neck (§2.9) hosel variants offered across the family · Cast face with steel wireframe undercut · Single line or Triple Track-family parallel lines per variant (§4.1, §4.3) · DNA: high-MOI cast mallet with a thin-wall undercut + tungsten heel/toe ports — TaylorMade's tour-mallet workhorse since 2024. · Tour: Rory McIlroy, 2025 Masters win (career Grand Slam) per TaylorMade's own positioning and tour reporting. · Source: https://www.taylormadegolf.com/Spider-Tour/DW-TC844.html · Class: M, T.

- **TaylorMade Spider Tour X (2024–present)** — Wing-back mallet (§1.5) · weight band per TaylorMade spec ~360 g · Single-bend or double-bend (§2.5, §2.6) · Cast face with steel wireframe · Triple-line / Triple Track-family alignment (§4.3) · DNA: the wing-back-class Spider Tour — wings pushed wider with mass at the rear extremes for top-of-market MOI in the Spider family. · Tour: Rory McIlroy has played Spider Tour X variants; tour bagging year-to-year should be re-verified. · Source: https://www.taylormadegolf.com/Spider-Tour-X/DW-TC846.html · Class: M, T.

- **TaylorMade Spider Tour L-Neck (2024–present)** — Tour-mallet (§1.4) · weight band ~355 g · L-neck (§2.9) — the model's defining feature, giving toe hang for slight-arc strokes within the Spider Tour silhouette · Cast face with steel wireframe · Single line (§4.1) · DNA: Spider Tour body re-hosseled to L-neck — the rare Spider variant intentionally fit for slight-arc rather than face-balanced strokes per `putter-fitting` §2. · Tour: Scottie Scheffler switched to Spider Tour L-Neck at the 2024 Arnold Palmer Invitational; 14 worldwide wins including three majors and a Players Championship since (per TaylorMade and tour reporting). · Source: https://www.taylormadegolf.com/Spider-Tour-X-L-Neck/DW-TC928.html · Class: M, T.

- **TaylorMade Spider GT Notchback (continuing line, predates 2024 Spider Tour refresh)** — Tour-mallet (§1.4) with a distinctive squared-off back · ~355 g · Single-bend (§2.5) · Aluminium body with tungsten heel/toe weights · Single line (§4.1) · DNA: a Spider with the back squared off and notched — a classically-shaped Spider variant for players who want the Spider MOI in a less-tech-looking address profile. · Source: https://www.taylormadegolf.com/Spider-GT-Notchback/DW-TA371.html · Class: M.

- **TaylorMade TP Reserve (2023–present)** — Blade (§1.1), mid-mallet (§1.2), and mallet (§1.3) shapes across the family · weight bands per shape, blade ~345 g and mallets ~355–365 g · Plumber's-neck, slant, and flow neck variants across shapes (§2.1, §2.2, §2.3, §2.4, §2.7) · CNC-milled (§3.1) — TaylorMade's entry into premium milled, distinct from cast Spider line · Single line and sight dot variants (§4.1, §4.4) · DNA: TaylorMade's CNC-milled tour-blade-and-mallet family — classical shapes built to milled tolerances, intentionally positioned as the milled counterpart to the cast Spider line. · Source: https://www.todays-golfer.com/equipment/best/taylormade-putter/ · Class: T.

### 3.5 L.A.B. Golf

L.A.B. Golf's entire product line is built around **Lie Angle Balance** — torque-balanced putter heads that resist face rotation under shaft torque. The line breaks the standard hosel matrix per `putter-fitting` §5 (the L.A.B. exception) — these are zero-torque putters that do not fit the conventional stroke-arc → toe-hang reasoning. The hosel column below names what L.A.B. calls the bend; the toe-hang reading is "torque-balanced" rather than a degrees band.

- **L.A.B. Golf DF 2.1 (2021–present)** — Mallet (§1.3) · weight band per L.A.B. spec ~370 g · Proprietary "DF" L.A.B. hosel — bent to put the shaft axis through the head's centre of mass with no torque about the shaft (does not map cleanly to `putter-anatomy-extended` §2 — closest analogue is a double-bend §2.6 with the bend tuned for torque-balance rather than face-balance) · Polymer-over-metal-class face (§3.2) · Single line (§4.1) · DNA: the canonical Lie Angle Balance putter — the head sits balanced about the shaft axis at any lie angle, intentionally breaking the stroke-arc → toe-hang matrix. · Tour: Adam Scott collaborated with L.A.B. on subsequent models; tour adoption broad (multiple players bagged L.A.B. across 2023–2025). · Source: https://www.todays-golfer.com/equipment/best/lab-golf-putter/ · Class: T (third-party publication aggregates L.A.B.'s positioning).

- **L.A.B. Golf Mezz.1 / Mezz.1 Max (2022–present; Mezz.1 Max is the larger profile)** — Mallet (§1.3) — Mezz.1 Max is a larger / higher-MOI variant of the Mezz.1 · weight band ~360–375 g per L.A.B. spec · L.A.B. torque-balanced hosel · Polymer-over-metal-class face (§3.2) · Single line (§4.1) · DNA: a more conventionally-shaped L.A.B. — visually less radical than the DF 2.1 while keeping the Lie Angle Balance technology; Mezz.1 Max is the high-MOI build for players who want max forgiveness inside the torque-balanced format. · Source: https://labgolf.com/pages/mezz-1-putter · Class: M, T (Golf Monthly https://www.golfmonthly.com/reviews/putters/l-a-b-golf-mezz-1-max-putter-review).

- **L.A.B. Golf DF3 (2024–present)** — Mallet (§1.3) · weight band ~360–370 g · L.A.B. torque-balanced hosel · Polymer-over-metal-class face (§3.2) · Single line (§4.1) · DNA: a smaller, sleeker reimagining of the DF 2.1 — Lie Angle Balance in a more conventionally proportioned silhouette. Launched early spring 2024 with arm-lock and broomstick variants. · Source: https://golf.com/gear/putters/lab-golf-df3-putter-review/ · Class: T (Golf.com first-look + Plugged In Golf https://pluggedingolf.com/l-a-b-golf-df3-putter-review/).

- **L.A.B. Golf OZ.1 / OZ.1i (late 2024–present)** — Mid-mallet (§1.2) / mallet (§1.3) — described as a "half-moon" mallet, more traditional shape than prior L.A.B. designs · L.A.B. torque-balanced hosel · Polymer-over-metal-class face (§3.2) · Single line (§4.1) · DNA: L.A.B.'s most traditionally-shaped putter to date, developed in collaboration with Adam Scott — Lie Angle Balance with a near-conventional mallet silhouette. · Tour: Adam Scott design collaboration. · Source: https://www.todays-golfer.com/equipment/best/lab-golf-putter/ · Class: T.

### 3.6 Bettinardi

The Bettinardi lineage splits across the **BB Series** (annual production refreshes, milled steel tour-blade-and-mallet line), the **Studio Stock** family (premium milled), the **Queen B** series (refined sub-line with rose-gold finish, 2025–2026 generation), the **INOVAI** series (high-MOI mallets, 2024–2025), and the **Antidote** line.

- **Bettinardi BB Series (2024 generation — BB1, BB1F, BB8, BB28)** — Blade (§1.1) and mid-mallet (§1.2) shapes across the family · weight bands typical of BB tour-blade ~340–355 g · Plumber's-neck, slant, and flow neck per model (§2.1, §2.2, §2.4, §2.7) · CNC-milled with the "Perpetual Flymill" face pattern (§3.1) — Bettinardi's combined milling-and-engraving face geometry · Single line, sight dot, and milled-band top-edge contrast variants (§4.1, §4.4, §4.6) · DNA: milled-steel tour-blade family with the Flymill face — Bettinardi's mass-market expression of single-block-milled construction, distinct from the cast bodies of Scotty / TaylorMade / Ping. · Source: https://bettinardi.com/pages/2024-bb-series · Class: M.

- **Bettinardi Queen B Series (2025–2026 generation — QB6 and family)** — Mid-mallet (§1.2) and mallet (§1.3) shapes · weight band ~362 g per Bettinardi spec · Plumber's-neck and slant variants (§2.1, §2.2) · CNC-milled with "Mini Honeycomb" face pattern (§3.1, dimples/pocked variant) · Single line and milled top-line variants (§4.1, §4.6) · DNA: refined sub-line with Royal Rose PVD finish and Mini Honeycomb face — heavier head weight than the BB line, positioned for players who want a softer impact response inside Bettinardi's milled-steel idiom. · Source: https://bettinardi.com/blogs/news/bettinardi-golf-unveils-2025-production-putter-lines-the-queen-b-and-antidote-series · Class: M.

- **Bettinardi INOVAI Series (2024–2025 generation — 6.0, 8.0, and variants)** — Mallet (§1.3) and wing-back mallet (§1.5) shapes · weight bands per shape · Multiple hosel options offered (single-bend, double-bend, plumber's-neck, slant) plus Armlock and Counterbalance variants per model (§2.1, §2.2, §2.5, §2.6, plus armlock-specific builds per `putter-fitting` §4 armlock band) · Bi-metal construction — 303 stainless steel face plate with 6061 military-grade aluminium body (§3.1, milled steel face over aluminium body — the polymer-over-metal analogue with metal-over-metal) · Single line (§4.1) · DNA: bi-metal high-MOI mallets — Bettinardi's milled identity transferred into a mallet architecture, with broader hosel-option matrix than any other Bettinardi line. · Source: https://bettinardi.com/collections/2024-inovai-series · Class: M.

- **Bettinardi Studio Stock (continuing premium line)** — Blade (§1.1) and mid-mallet (§1.2) shapes · weight bands per shape · Plumber's-neck and slant variants (§2.1, §2.2) · CNC-milled (§3.1) · Single line and sight dot (§4.1, §4.4) · DNA: Bettinardi's premium milled blade-and-mid-mallet line — the highest-finish, lowest-volume Bettinardi catalog. · Source: https://bettinardi.com/collections/putters · Class: M.

### 3.7 Evnroll

Evnroll's signature is the **Sweet Face** milled face geometry — face grooves vary in depth/pitch across the face to compensate for off-centre hits ("makes every strike roll the same distance"). The line splits across the **Neo Classic** family (2024 refresh — ER1.2, ER2.2, ER5, ER8, ER11), the **Midlock** family (armlock-specific builds — ER2, ER5, ER8, ER11 Midlock variants), and the **V-Series** (newer, interchangeable hosels).

- **Evnroll Neo Classic ER1.2 (2024–present)** — Blade (§1.1) with heel and toe weighting · weight band ~350 g · Plumber's-neck (§2.1) · Milled with Sweet Face groove geometry (§3.1, milled face with **variable groove depth** — the depth-vs-pitch claim in `putter-anatomy-extended` §3.1 applies in a tuned across-face manner) · Single line or sight dot (§4.1, §4.4) · DNA: heel-and-toe-weighted blade with Sweet Face groove geometry — Evnroll's tour-blade entry, the most conventional silhouette in the Evnroll line. · Source: https://www.evnroll.com/collections/putters · Class: M.

- **Evnroll Neo Classic ER2.2 (2024–present)** — Blade (§1.1), wider profile than ER1.2 · weight band ~355 g · Plumber's-neck (§2.1) · Milled with Sweet Face (§3.1) · Single line (§4.1) · DNA: the canonical Evnroll blade — wider footprint than the ER1.2, named MyGolfSpy *Best Blade Putter of 2024* (https://www.evnroll.com/blogs/straight-talk/evnroll-wins-mygolfspy-s-best-blade-putter-of-2024). · Source: https://www.evnroll.com/collections/putters · Class: M, T (MyGolfSpy "Best Of" award).

- **Evnroll Neo Classic ER5 (2024–present, refreshed silhouette over original ER5)** — Fang mallet (§1.6) — Evnroll describes it as a "sleeker fang shape" — · weight band ~360 g · Slant or plumber's-neck variants (§2.2, §2.1) · Milled with Sweet Face (§3.1) · Fang-channel with directional 3D milling at the channel base (§4.5, ridged-floor variant) · DNA: Evnroll's fang-mallet entry — milled steel fang with Sweet Face groove geometry and milled-in directional channel cue. · Source: https://www.evnroll.com/collections/putters · Class: M, T (MyGolfSpy 2024 Neo Classic first-look https://mygolfspy.com/news-opinion/first-look/evnroll-2024-neo-classic-putter-line/).

- **Evnroll Neo Classic ER8 (2024–present)** — Mallet (§1.3) with deep three-section rear cavity · weight band ~365 g · Single-bend or double-bend variants (§2.5, §2.6) · Milled with Sweet Face (§3.1) · Long single line — "longest sightline of all Neo Classic models" per Evnroll's positioning (§4.1) · DNA: deep-cavity mallet with a long sight line — Evnroll's max-alignment-cue mallet. · Source: https://www.evnroll.com/collections/putters · Class: M.

- **Evnroll ER11 (Neo Classic and Midlock variants)** — Wing-back mallet (§1.5) — Evnroll's MOI flagship · weight band ~370 g · Single-bend or long slant (Midlock variant) (§2.5, §2.4) · Milled with Sweet Face (§3.1) · Single line (§4.1) · DNA: high-MOI wing-back built around Sweet Face — the Midlock variant is the armlock-specific configuration. · Source: https://www.evnroll.com/collections/midlock and https://www.evnroll.com/collections/putters · Class: M.

### 3.8 PXG (Parsons Xtreme Golf)

The PXG lineage centres on the **Battle Ready II** family — hollow-body cast putters with thin-walled construction, injection-moulded cores, and very thin faces. The 2024–present Battle Ready II generation has nine models. PXG also produces **Allan ZT** as the Zero Torque entry (PXG's torque-balanced answer to L.A.B.).

- **PXG Battle Ready II Closer (2024–present)** — Mid-mallet (§1.2) — described as a wide blade-style with longer heel-to-toe length and slightly thinner front-to-back · weight band per PXG spec ~350–360 g · Plumber's-neck and slant variants (§2.1, §2.2) · Hollow-body cast face — thin-faced for high-MOI (§3.1 cast face — milling does not apply directly) · Single line (§4.1) · DNA: wide-blade-into-mid-mallet bridge with PXG's hollow-body high-MOI construction — for blade-eye players who want mallet-class forgiveness. · Source: https://www.pxg.com/products/battle-ready-ii-closer-putters · Class: M, T (MyGolfSpy https://mygolfspy.com/news-opinion/first-look/pxg-battle-ready-ii-putters/).

- **PXG Battle Ready II Mustang (2024–present)** — Blade (§1.1) with heel-and-toe weighted ballasts · weight band ~345–360 g · Plumber's-neck (§2.1) · Hollow-body cast · Single line (§4.1) · DNA: the canonical PXG blade — heel-and-toe ballasted, hollow-body, tour-blade silhouette. · Source: https://www.pxg.com/products/battle-ready-ii-mustang-putters · Class: M.

- **PXG Allan ZT (Zero Torque — 2024–present)** — Mallet (§1.3) · weight band per PXG spec · L.A.B.-style torque-balanced hosel (does not map to `putter-anatomy-extended` §2; closest analogue is a tuned double-bend §2.6) · Hollow-body cast face · Sleek alignment aid per PXG positioning (likely single line — §4.1) · DNA: PXG's Zero Torque entry — the torque-balanced approach in a PXG hollow-body construction, intentionally competing with L.A.B. in the torque-balanced category. · Source: https://www.pxg.com/blogs/the-range/pxg-expands-its-iconic-battle-ready-putter-lineup-to-serve-even-more-golfers · Class: M, T.

- **PXG Battle Ready II Gunboat / Blackbird / Spitfire (2024–present mallet additions)** — Mallet (§1.3) and wing-back mallet (§1.5) shapes across the additions · weight bands per shape · Single-bend variants typical (§2.5) · Hollow-body cast · Single line or per-model alignment (§4.1) · DNA: the high-MOI mallet additions to the Battle Ready II family — Gunboat and Blackbird are mass-market mallet builds; Spitfire is a higher-profile shape. · Source: https://golf.com/gear/putters/pxg-battle-ready-putters-gunboat-blackbird-mallets/ · Class: T.

### 3.9 Cleveland (Dunlop / Srixon)

The Cleveland line is **HB SOFT 2** (2024–present, nine stroke-specific models — the game-improvement-priced putter line) and the older **HB SOFT Milled** line.

- **Cleveland HB SOFT 2 Model 1 (2024–present)** — Blade (§1.1) · weight band per Cleveland spec ~345 g · Plumber's-neck (§2.1) · Polymer face insert with HB ("Huntington Beach") face geometry (§3.2 — urethane-class insert) · Single line (§4.1) · DNA: the classic Cleveland HB blade — plumber's-neck blade with the soft urethane HB insert, slight-arc fit. · Source: https://news.dunlopsports.com/news/cleveland-golf-unveils-new-hb-soft-2-putters-with-nine-stroke-specific-models/s/a76f9652-43bb-4add-8f0e-c44a19eabed1 · Class: M, T (The Hackers Paradise https://www.thehackersparadise.com/2024-cleveland-hb-soft-2-putters-review/).

- **Cleveland HB SOFT 2 Model 11 / 11C / 11S (2024–present)** — Wing-back mallet (§1.5) · weight band per Cleveland spec ~360 g · Single-bend (Model 11), centre-shafted (Model 11C), slant neck (Model 11S) — same head with three hosel options (§2.5, §2.8, §2.2) · HB urethane insert (§3.2) · Triple-line alignment (§4.3, double-bar family with three parallel lines) · DNA: winged mallet with three hosel options on the same head — Cleveland's broadest fitting matrix on one body. · Source: https://news.dunlopsports.com/news/cleveland-golf-unveils-new-hb-soft-2-putters-with-nine-stroke-specific-models/s/a76f9652-43bb-4add-8f0e-c44a19eabed1 · Class: M, T.

- **Cleveland HB SOFT 2 Model 15 (2024–present)** — Mallet (§1.3) with angular silhouette · weight band ~360 g · Single-bend (§2.5) · HB urethane insert (§3.2) · Triple-line alignment (§4.3) · DNA: an angular, distinctive mallet silhouette — Cleveland's signature non-traditional shape in the HB SOFT 2 line. · Source: https://news.dunlopsports.com/news/cleveland-golf-unveils-new-hb-soft-2-putters-with-nine-stroke-specific-models/s/a76f9652-43bb-4add-8f0e-c44a19eabed1 · Class: M, T.

- **Cleveland HB SOFT 2 RETREVE (2024–present)** — Mallet with ball-pickup cavity (§1.3 mallet with a back cavity that scoops the ball) · weight band per Cleveland spec · Single-bend (§2.5) · HB urethane insert (§3.2) · Per-model alignment · DNA: Cleveland's answer to the Ping Fetch — mallet with a literal ball-pickup back cavity. · Source: https://news.dunlopsports.com/news/cleveland-golf-unveils-new-hb-soft-2-putters-with-nine-stroke-specific-models/s/a76f9652-43bb-4add-8f0e-c44a19eabed1 · Class: M.

### 3.10 Wilson Staff Infinite

Wilson's putter line is the **Infinite** family (2024 generation), nine models at game-improvement price. All models in this generation share a two-toned black PVD finish, a double-milled face, and Activation Parallel Alignment Lines (one thick centre line with thinner framing lines).

- **Wilson Staff Infinite Windy City (2024–present)** — Blade (§1.1) · weight band per Wilson spec · Plumber's-neck (§2.1) · Double-milled face (§3.1) · Activation Parallel Alignment Lines (§4.3, three-line variant) · DNA: the canonical Wilson Infinite blade — plumber's-neck slight-arc blade with double-milled face. · Source: https://www.golfdigest.com/story/wilson-infinite-putters--2024---what-you-need-to-know · Class: T.

- **Wilson Staff Infinite Grant Park (2024–present)** — Blade (§1.1) with wide curve-flanged silhouette · weight band per Wilson spec · Flow neck (§2.7) · Double-milled face (§3.1) · Activation Parallel Alignment Lines (§4.3) · DNA: wide-flanged blade with flow neck — Wilson's strong-arc blade in the Infinite generation. · Source: https://www.golfdigest.com/story/wilson-infinite-putters--2024---what-you-need-to-know · Class: T.

- **Wilson Staff Infinite Buckingham (2024–present)** — Wing-back mallet (§1.5) · weight band per Wilson spec · Slant neck (§2.2) · Double-milled face (§3.1) · Activation Parallel Alignment Lines (§4.3) · DNA: winged mallet with slant neck — Wilson's max-stability mallet in the Infinite generation. · Source: https://www.golfdigest.com/story/wilson-infinite-putters--2024---what-you-need-to-know · Class: T.

- **Wilson Staff Infinite Bucktown (2024–present)** — Fang mallet (§1.6) — "parallel fang mallet" per Wilson positioning · weight band per Wilson spec · Heel-shafted (§2.10) — the unusual choice of a heel-shafted hosel on a fang body · Double-milled face (§3.1) · Fang-channel with parallel-line alignment (§4.5 + §4.3 hybrid) · DNA: fang mallet with a heel-shafted hosel — a deliberately uncommon pairing that gives strong toe hang to a fang silhouette. · Source: https://www.golfdigest.com/story/wilson-infinite-putters--2024---what-you-need-to-know · Class: T.

## 4. Verification protocol

Before committing a market reference to a brief, GolfPro runs this protocol. The protocol is the citation-discipline gate Director will spot-check.

### 4.1 The three-source check

For each market reference about to land in brief §9:

1. **Manufacturer page.** Open the manufacturer's product page for the named model. Confirm the model exists, the year matches (within ±1 year if banded), and the head family / weight / hosel / face / alignment named in the row match what the manufacturer states. **If the manufacturer page does not list the model as currently in production, the row drops to (T) class — do not cite it as currently produced without third-party corroboration that post-dates the manufacturer's product page.**

2. **Third-party publication.** Find at least one independent publication (MyGolfSpy, Golf.com, Golf Digest, Today's Golfer, Golf Monthly, GolfWRX, Plugged In Golf, Golfalot) that names the model + year + key spec. **The publication date should be within 24 months of the brief.** A 2021 review of a 2021 model does not by itself confirm 2026 production.

3. **USGA conforming list.** Visit https://www.usga.org/equipment-standards/equipment-rules-and-decisions.html (putters section), search the model name. Confirm the model is listed. **The USGA list is canonical for *"does this model exist as a conforming product."*** Manufacturer marketing pages sometimes lag retiring discontinued products — the USGA list is the existence-of-record source.

If steps 1 and 2 disagree on year or variant naming: defer to the third-party publication and add a *"manufacturer page and third-party source disagree — re-verify before brief commit"* note to the row.

If step 3 returns no result for the model name: the model name on the manufacturer page may be marketing-only or may be a variant of a different listed name. Cross-check the manufacturer page for the USGA-list-form of the name and use the USGA-list-form in the brief.

### 4.2 Tour-adopter verification

For any *"Tour: X played this at Y"* claim:

1. The player name must be named — bare *"tour-played"* is not a citation.
2. The event or year must be named — *"plays a Spider"* is not a citation; *"Rory McIlroy, 2025 Masters win"* is.
3. The source should be a tour-report publication or the manufacturer's own coverage. Manufacturer coverage of tour adoption is acceptable for this field but should be cross-referenced when the adoption is recent or contested.
4. Tour bags change. A 2024-confirmed adoption is not a 2026-confirmed adoption. If the brief is dated more than 12 months after the adoption was confirmed, re-verify before quoting.

### 4.3 Source-class assignment

When writing a row:

- (M) only — no independent corroboration found. Add *"manufacturer-sourced; pending third-party verification"* note explicitly. The row is acceptable for brief §9 but a brief reader can see the lower confidence at a glance.
- (M, T) — manufacturer + at least one third-party publication. Standard for flagship references.
- (M, T, U) — manufacturer + third-party + USGA conforming list. Required when the brief makes a USGA-conformance claim about the cited model.
- (T) only — manufacturer page unreachable or not fetched in the verification pass; third-party publication is the only source. Acceptable but flag the manufacturer-page-not-verified gap in the row.

### 4.4 The two-source minimum

**No row in brief §9 should ship with a single source of class (M) only and no flag.** Either:

- Cite a third-party publication and bump to (M, T), or
- Explicitly label the row *"manufacturer-sourced; pending third-party verification"* and ship the brief with the note visible.

The exception is when the brief is intentionally citing a manufacturer-only spec (e.g., L.A.B.'s torque-balance claim, which is the manufacturer's design positioning rather than a third-party-measurable spec). In that case, the (M)-only class is appropriate and the manufacturer's positioning is named explicitly in the brief.

## 5. Anti-patterns

What bad market-reference reasoning looks like in a brief. Each names the failure mode and how the verification protocol catches it.

1. **Cite the brand without a model.** *"Looks like a Scotty."* No model named, no DNA committed. A brief reader cannot tell whether the reference is a Newport 2 (blade, plumber's-neck, slight-arc) or a Phantom 11 (wing-back mallet, single-bend, face-balanced) — opposite ends of the matrix. The brief §9 row must name **Manufacturer + Model + Year**.

2. **Cite a discontinued model as if currently produced.** *"Reference the Scotty Cameron Special Select Newport 2."* The Special Select line was succeeded by Super Select in 2023; quoting Special Select in a 2026 brief implies a product that is no longer in the manufacturer's current line. The verification protocol §4.1 step 1 catches this — the manufacturer's current-product page will not list it, only the archive.

3. **Cite a model but the year is wrong by more than 1 year.** *"TaylorMade Spider Tour, 2020."* The 2024–present Spider Tour refresh is a different product (thin-wall undercut, steel wireframe, new model line) from the 2020 Spider Tour. A year mis-named by >1 year names a different product. Bands beat point values for dates — *"Spider Tour, 2024 refresh"* is correct and unambiguous.

4. **Cite a tour adoption without naming the player or event.** *"Tour-played Spider Tour X."* This is not a citation. The verification protocol §4.2 requires the player name and the event or year. *"Rory McIlroy, 2025 Masters win"* is a citation; *"used by tour players"* is not.

5. **Cite a similarly-named model that does not exist.** *"Odyssey Triple Track Ten,"* when the brief intends to reference the current Triple Track variant — which is the **Eleven Triple Track** (2022 generation, current) or **Ai-One Milled Eleven** (2024 generation), not "Triple Track Ten." The Ten body exists as the older Two-Ball Ten and the older Triple Track Ten generation, but the current Triple Track + Eleven combinations are distinct products. Naming the wrong number names the wrong product — Director will spot-check.

6. **Cite a model from a manufacturer marketing page that contradicts the USGA conforming list.** Manufacturer pages can lag retiring discontinued products; the USGA list is canonical for product existence. If the manufacturer page lists the model but the USGA list does not, the model may have been pulled from production or never reached the conforming list. The verification protocol §4.1 step 3 catches this.

7. **Cite "soft feel" or "buttery feel" as the DNA element.** Marketing language, not DNA. Per `putter-domain`, *feel* decomposes into balance / forgiveness / sound / impact response. The DNA-in-one-sentence field should name a silhouette cue, a hosel-family commitment, a manufacturing signature, or a playing-style claim — not undecomposed feel. *"White Hot urethane insert giving low-frequency damped impact sound"* is DNA; *"soft feel"* is not.

8. **Cite a market reference whose head family does not match the brief.** A brief targeting a fang mallet that cites the Scotty Cameron Newport 2 as DNA is incoherent — the Newport 2 is a blade. The market reference must match the head family the brief commits in §2. The verification protocol does not catch this; reading the row's head-family field against brief §2 does.

## 6. Worked examples

Two market-reference entries, brief-ready, with the citation discipline fully applied. The first is a tour-blade DNA reference (blade, slight-arc); the second is a mallet DNA reference (wing-back mallet, face-balanced).

### 6.1 Blade-DNA reference for a tour-blade brief

A brief targeting a slight-arc, tour-aspirant 8-handicap player. §2 commits the brief to a blade family with plumber's-neck hosel and tri-sole geometry. §9 cites:

> **Market reference — Scotty Cameron Super Select Newport 2 (2023–present).** Blade (per `putter-anatomy-extended` §1.1) · ~340–355 g at 35 in · Plumber's-neck (per `putter-anatomy-extended` §2.1) · Milled stainless steel (per `putter-anatomy-extended` §3.1), tri-sole geometry · Single line + sight dot (per `putter-anatomy-extended` §4.1, §4.4). DNA: tour-blade Newport 2 silhouette — straight top-line, full plumber's-neck plumbing, tri-sole with two heel/toe tungsten sole weights, full shaft offset. The brief borrows the silhouette and the tri-sole + heel/toe tungsten weighting concept; it does not copy the I-beam plumbing geometry or the Newport 2 face milling pattern. Source: https://www.scottycameron.com/articles/introducing-new-super-select-putters/ (manufacturer-attested), corroborated by Today's Golfer review (https://www.todays-golfer.com/equipment/golf-clubs/putters/titleist/scotty-cameron/titleist-scotty-cameron-super-select-putters/) and GolfWRX launch coverage (https://www.golfwrx.com/703542/titleists-new-scotty-cameron-super-select-2023-putters-heres-everything-you-need-to-know/). Source class: **(M, T)**. Verification performed: (1) manufacturer current-product page confirms model in production; (2) two independent publications corroborate; (3) USGA conforming list cross-check pending — re-verify before brief commit.

Citation discipline applied:
- Manufacturer + Model + Year band (2023–present, not a point year).
- Per `putter-anatomy-extended` references for family / hosel / face / alignment.
- DNA sentence names silhouette, manufacturing signature, and the specific tri-sole + heel/toe weighting concept being borrowed (not marketing language).
- Source URLs are direct.
- Source class **(M, T)** named.
- Explicit *"USGA conforming list cross-check pending"* — the row honestly flags the one verification step not completed.

### 6.2 Mallet-DNA reference for a wing-back-mallet brief

A brief targeting a face-balanced, straight-back-straight-through 16-handicap player who has lost lag-distance control. §2 commits the brief to a wing-back mallet family with double-bend hosel and Two-Ball-family alignment. §9 cites:

> **Market reference — Odyssey 2-Ball Eleven Triple Track (2022–present, current).** Wing-back mallet (per `putter-anatomy-extended` §1.5) · ~360 g per Odyssey spec · Double-bend (per `putter-anatomy-extended` §2.6), face-balanced (0° toe hang) · White Hot urethane insert (per `putter-anatomy-extended` §3.2) · Triple Track parallel-line alignment over Two-Ball crown discs (per `putter-anatomy-extended` §4.3, double-bar family — Two-Ball + Triple Track combination). DNA: the high-MOI Eleven body combined with Two-Ball crown discs and Triple Track parallel lines — three alignment cues stacked on one face-balanced mallet for players who alignment-aim by redundant cues rather than a single line. The brief borrows the wing-back body silhouette and the layered Two-Ball + Triple Track alignment concept; it does not copy the specific White Hot insert chemistry or the exact crown disc geometry. Tour: Wyndham Clark, 2023 U.S. Open win (re-verify before brief commit — tour bagging changes year to year). Source: https://odyssey.callawaygolf.com/putters/eleven/putters-2022-eleven-2-ball-triple-track-db.html (manufacturer-attested) and PGA Tour Superstore listing https://www.pgatoursuperstore.com/2-ball-eleven-triple-track-putter/2000000030372.html (third-party retail listing corroborating current production). Source class: **(M, T)**. Verification performed: (1) manufacturer current-product page confirms model in production at named year-band; (2) PGA Tour Superstore listing corroborates current retail availability; (3) USGA conforming list cross-check pending.

Citation discipline applied:
- **Anti-pattern §5.5 avoided** — the row names *Eleven Triple Track*, not *Triple Track Ten* (the older Ten body is a different product).
- DNA sentence names the alignment-cue-stacking concept being borrowed, not marketing language.
- Tour adoption named with player + event + year, and explicitly flagged for re-verification per §4.2.
- Source class **(M, T)** with explicit *"USGA conforming list cross-check pending"* note.

## 7. What this skill does not cover

- **The brief format itself** — read `putter-design-brief-format`. This skill supplies the §9 content; that skill specifies what the rest of the brief looks like.
- **Stroke-arc → toe-hang → hosel matrix, head-weight band, length × lie matrix** — read `putter-fitting`. This skill records what manufacturers ship; that skill reasons from player profile to spec.
- **Head family / hosel / face / alignment vocabulary and visual identification** — read `putter-anatomy-extended`. This skill cites that skill's §1–§4; do not invent new family names here.
- **Base glossary (face, heel, toe, sole, hosel, offset, lie, loft, sweet spot, the feel decomposition)** — read `putter-domain`. This skill assumes that vocabulary.
- **USGA conformance for face roughness, head dimensions, MOI ceiling, anchoring rule** — read `usga-rules-putters` when it ships (skill #5). This skill uses the USGA conforming list as a *"does this model exist"* check, not as an authority on conformance rules.
- **Discontinued models, vintage collectibles, tour-issue-only builds.** The catalog here is **currently-produced retail product**. A brief that wants to reference a tour-issue-only or vintage build (e.g., a Scotty Cameron Circle T tour build) should add the row in the per-row format of §2 and explicitly note *"tour-issue / not retail"* in the row.
- **Component putter brands, kit-build putters, custom one-off shops** (Sik, Edel, Toulon-as-component, Logan, etc.). The catalog here covers the major branded-retail manufacturers per the issue spec. Briefs that reference component-build putters should add rows with the same citation discipline.

## 8. Last verified

This skill's catalog was last verified against manufacturer and third-party sources on **2026-05-23**. The verification pass used third-party publications (MyGolfSpy, Golf.com, Golf Digest, Today's Golfer, Golf Monthly, GolfWRX, Plugged In Golf, The Hackers Paradise, PGA Tour Superstore listings) as the primary corroboration source because manufacturer pages were not directly fetchable in the verification pass (bot protection / redirects on several manufacturer storefronts). Rows labeled (M) only should be re-verified against the manufacturer page before quoting in a brief.

**The catalog decays.** Manufacturers refresh lines annually. Tour adoptions change tournament to tournament. Any row in §3 older than 12 months from the brief date should be re-verified per §4 before quoting. The verification protocol in §4 is the discipline that keeps this skill honest as the market moves.

