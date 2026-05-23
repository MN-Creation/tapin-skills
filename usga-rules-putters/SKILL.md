---
name: usga-rules-putters
description: USGA Rules of Golf and Equipment Rules that constrain putter design briefs — length, anchoring, face geometry, loft, MOI, materials, adjustability, and markings. Use this skill any time GolfPro is writing a brief that commits to a number, dimension, or configuration that falls inside USGA bounds (every brief). Scope is **rules-of-play awareness during design** — NOT **formal conformance certification**. Conformance certification is a separate USGA submission process that lives outside this skill and outside GolfPro's lane per the [TAP-169](/TAP/issues/TAP-169) hire spec. Do NOT use this skill for the brief format itself (read `putter-design-brief-format`), for fitting decisions inside conformance bounds (read `putter-fitting`), for anatomy vocabulary (read `putter-anatomy-extended`), or for market-DNA cataloging (read `putter-market-reference`). Cite, do not assert — every rule reference carries a Rule number, the publication version date, and the date of GolfPro's last verification.
---

# USGA Rules — Putters

This skill is the **conformance lens** every brief touches. Skills #1–#4 give the brief format, the fitting matrix, the anatomy vocabulary, and the market-DNA catalog; this skill names the **rules** a brief must not silently violate when it commits to a length, a loft, a face geometry, an alignment system, or a hosel configuration.

**This is the highest-stakes citation skill in the GolfPro sequence.** A wrong rule number, a misquoted clause, or an asserted rule that does not exist creates real liability — briefs based on a false-rule premise will ship putters that fail tournament play. The discipline is **fewer rules cited correctly, not many rules cited loosely.** Where wording or scope is uncertain, the skill names the uncertainty as an open question (§5) rather than guessing.

**Read order:**
- `putter-domain` first for the base vocabulary — face, heel, toe, sole, hosel, offset, lie, loft, sweet spot, the feel decomposition.
- `putter-fitting` alongside §2 (length) of this skill — the fitting matrix is what tells you a brief is **near** a USGA bound; this skill tells you what the bound is.
- `putter-anatomy-extended` alongside §4 (face) and §7 (markings) — anatomy names the parts; this skill says what the rules let those parts do.
- `putter-design-brief-format` is the consumer — every section of a brief that quotes a USGA limit should cite this skill using the format in §8.

## 1. Last verified against

**Verified against:** 2023 Rules of Golf (effective 1 January 2023) and Equipment Rules (effective 1 January 2024), as published jointly by the USGA and The R&A, **cached in GolfPro's training data and partially cross-checked against `usga.org` and `rules.usga.org` web content on 2026-05-23.**

**Verification status, per claim:**

- **Confirmed against live USGA content (2026-05-23):** Rule 10.1b anchoring text (USGA "Understanding Rule 10.1b" PDF, 2023 edition); Equipment Rules club length minimum/maximum and putter exemption (cross-checked via USGA Equipment FAQ and Equipment Rules Final PDF); 46-inch Model Local Rule G-10 (effective 1 January 2022); putter loft ceiling of 10°; putter face-roughness and impact-area exemption.
- **Cited from training-data-cached rule text, not freshly cross-checked against the live PDF on 2026-05-23 (because the USGA Equipment Rules PDF returned HTTP 403 during the verification pass):** the exact Part / Section numbering for the face-roughness rule, the materials rules, the adjustability rule, and the markings rule. The substance is from training; the exact subsection cites carry a *(part/section number pending fresh verification)* tag in §4, §6, §7.
- **Genuinely ambiguous in available sources — flagged as open questions in §5:** whether the 5900 g·cm² clubhead-MOI cap applies to putters at all, the specific rule text governing post-purchase adjustability for putters, the rule treatment of novel face materials (graphene-coated, ceramic-infused, polymer-over-metal composites).

**Director, before ratifying:** the citations Director told GolfPro would get spot-checked are the rule **numbers** in §2 (length, Rule 4.1a + Equipment Rules Part 2, 1c), §3 (anchoring, Rule 10.1b), and §4 (face, Equipment Rules Part 2, Section 5). Those three are the ones GolfPro most cross-checked. Subsection numbering in §6, §7, and §5 is the surface that benefits most from a fresh live-content pass.

**The skill decays.** USGA and R&A jointly refresh the Rules of Golf every four years (next refresh expected 2027) and the Equipment Rules periodically inside that window. Any brief dated more than 12 months after this verification date should re-verify the cited rules against the then-current USGA publication before quoting.

## 2. Length

> **Rule reference.** Rule 4.1a, *Rules of Golf*, 2023 edition (the *"club conforms"* rule that incorporates the Equipment Rules by reference). Equipment Rules Part 2, 1c (Length), Equipment Rules 2024 edition. Source: https://www.usga.org/equipment-standards/equipment-faq-25852.html and https://www.usga.org/content/dam/usga/pdf/Equipment/Equipment%20Rules%20Final.pdf (PDF returned 403 in the 2026-05-23 verification pass; cross-checked against USGA Equipment FAQ and third-party reporting).

**Substance:**

- **Minimum length** of any club: **18 inches** (0.4572 m). This applies to putters too — a brief targeting a very-short putter (e.g., for a junior or seated player) must keep the overall length ≥ 18 inches.
- **Maximum length** of any club other than a putter: **48 inches** (1.2192 m).
- **Putters are exempt from the 48-inch maximum.** Per the Equipment FAQ: *"The overall length of the club must be at least 18 inches and, except for putters, must not exceed 48 inches."* Broomstick and long-putter builds (50, 52, 54 inches+) remain conforming on the length dimension alone.

**The 46-inch Model Local Rule (G-10):**

- Effective **1 January 2022**, the USGA and The R&A introduced **Model Local Rule G-10**, which a tournament committee may adopt to limit the maximum length of a golf club to **46 inches**.
- **Putters are excluded from G-10** — the local rule limits non-putter clubs only.
- G-10 is **optional and local** — it is not part of the universal Equipment Rules, and it applies only at events whose committee has adopted it (the elite professional tours have adopted it for drivers; G-10 does not constrain putter design).

**Brief implication.** A brief may commit to **any putter length ≥ 18 inches** as USGA-conforming on the length dimension. There is no maximum-length cliff to design around. **The constraint that effectively bounds long putters is the anchoring rule (§3), not the length rule.** Briefs for broomstick / counter-balanced builds should commit to the length openly and pair the commitment with an explicit §3 anchoring-compliance design note.

**Anti-pattern alert:** A brief that cites *"max 48 inches"* as a putter length cap is **wrong on the law** — that is the cap for non-putters. The 48-inch number circulates widely (including in the original commission text for this skill); GolfPro must not propagate it.

## 3. Anchoring

> **Rule reference.** Rule 10.1b, *Anchoring the Club*, *Rules of Golf*, 2023 edition. Source: USGA "Anchoring the Club — Understanding Rule 10.1b" (PDF, 2023 edition), https://www.usga.org/content/dam/usga/pdf/2023/rules/2023_USGA_UnderstandingAnchoredStrokes.pdf. **Confirmed against live USGA content on 2026-05-23.**

**Verbatim text of the prohibition** (from the USGA "Understanding" guidance):

> *"In making a stroke, the player must not anchor the club, either: 'Directly,' by holding the club or a gripping hand in contact with any part of the body (except that the player may hold the club or a gripping hand against a hand or forearm), or 'Indirectly' through use of an 'anchor point,' by holding a forearm in contact with any part of the body to enable the gripping hand to hold the club against and away from the body."* — USGA, *Understanding Rule 10.1b*, 2023 edition.

**Penalty.** General penalty (loss of hole in match play; two strokes in stroke play). This is a **stroke rule**, not an **equipment rule** — the club itself remains conforming; the violation is in the act of striking the ball.

**Indirect-anchor mechanic (the part that catches design briefs out):**

For an **anchor point** to exist, **both** of the following must occur — per the USGA guidance:

1. The player must hold a forearm against the body, **and**
2. The player must grip the club so that the hands are separated and work independently from each other.

**Clothing held against the body by a club or gripping hand is treated as if it is part of the player's body** for Rule 10.1b purposes — designing a grip configuration around looped jacket cuffs does not escape the rule.

**Brief implications:**

- **Armlock grips are permitted** — the rule explicitly carves out *"the player may hold the club or a gripping hand against a hand or forearm."* Armlock-length grip designs (per `putter-fitting` §4 head-weight bands for armlock builds, typically extended grips up the lead forearm) are USGA-legal so long as the contact stays at hand-or-forearm.
- **Broomstick and long-putter geometries are not banned by Rule 10.1b** — the *length* of the club is unconstrained (§2). What is banned is the *stroke mechanic* of anchoring the upper hand against the body. A broomstick brief must explicitly note the rule and the design accommodations needed (typical: a "claw"-style upper-hand grip that hovers, with the lower hand making the actual stroke).
- **Counter-balanced builds are unaffected by Rule 10.1b** — the upper hand does not contact the body in standard counter-balanced putting.

**Anti-pattern alert:** A brief that says *"this broomstick build is non-conforming under the anchoring rule"* is wrong; the **build** is conforming, only the **stroke** with the build can be non-conforming. The distinction matters because GeometryEngineer is building the *club*, not constraining the *stroke*.

## 4. Face — loft, roughness, and the putter-specific impact-area exemption

> **Rule reference.** Equipment Rules Part 2, Section 5 (*Club Face*), Equipment Rules 2024 edition. The specific subsections governing groove geometry, roughness, and the putter-specific exemption are at Part 2, Section 5 — *exact subsection numbers pending fresh verification against the Equipment Rules PDF (which returned 403 during the 2026-05-23 pass)*. Source: https://www.usga.org/equipment-standards/equipment-rules-2019/equipment-rules/part-2-rule-6.html (*"5. Club Face"*) and https://www.usga.org/content/usga/home-page/equipment-standards/equipment-faq-25852.html. Definition of putter loft is per the Equipment Rules definition of *putter* (Part 2, Section 1 — definitions, *pending subsection verification*).

**Loft:**

- **Putter loft must not exceed 10°.** This is part of the **definition** of *putter* in the Equipment Rules. A club with loft > 10° is, by definition, not a putter — it is some other category of club and is governed by the corresponding category rules. Most production putters land 2–4°.
- **Negative loft is permitted in a putter**, but the Equipment FAQ flags that a loft of less than **−15°** would not be considered *"traditional and customary in form and make"* (the catch-all conformity standard). Briefs intentionally specifying negative loft (uncommon but not unheard-of in left-edge-of-feel experiments) must stay within this band and call it out.

**Face roughness (the general rule, before the putter exemption):**

- **Sandblasting or other surface roughness > 180 microinches (4.5 µm)** is **not permitted** in the impact area of a non-putter clubface.
- **Milling** is **not permitted** in the impact area if the crest-to-trough depth exceeds **0.001 inch (0.025 mm)**.

**The putter-specific exemption — the load-bearing point of this section:**

> *"For putter faces specifically, any markings on the face of a putter must not have sharp edges or raised lips, and the specifications with regard to roughness, material and markings in the impact area do not apply."* — USGA Equipment FAQ (paraphrased from the Equipment Rules), 2024 edition.

**Brief implications:**

- **Deep-milled patterns on putter faces are permitted.** The 0.001-inch crest-to-trough cap that constrains driver/iron face milling **does not apply** to putters. This is why Evnroll's Sweet Face variable-depth grooves and Bettinardi's Perpetual Flymill / Mini Honeycomb patterns (per `putter-market-reference` §3.6 and §3.7) are conforming despite far exceeding the non-putter milling depth limit.
- **Aggressive face treatments (sandblasting, blasting + groove, micro-hinge insert patterns) are permitted on putters** — the 180-microinch roughness cap that constrains other clubfaces does not apply.
- **The constraint that does still apply: no sharp edges or raised lips on putter face markings.** A brief that specifies a deeply-incised alignment mark on the face must keep the mark's edge geometry non-sharp.
- **Insert-based face technologies (urethane White Hot, Ai-Optimised polymer, polymer-over-metal) are permitted on putters** — the *material* specifications in the impact area also do not apply. The conformity gate is the *traditional and customary in form and make* clause (open question §5.3 below for novel materials).

**Anti-pattern alert:** A brief that quotes *"max 180 microinch roughness"* or *"max 0.001 in milling depth"* as a putter-design constraint is **wrong on the law for putters specifically**. Those are the non-putter limits. Quoting them on a putter brief over-constrains GeometryEngineer for no rules-based reason.

## 5. MOI, materials, and the open questions

**Open questions** are the rules where GolfPro's training-data-cached knowledge is genuinely uncertain or conflicts with live web sources. Each is named, framed as a question, and tagged with what verification would resolve it. **A brief that needs a position on an open question must escalate to Director with the question text before committing the number** — it must not paper over the uncertainty by guessing.

### 5.1 Open: does the 5900 g·cm² clubhead-MOI cap apply to putters?

The Equipment Rules impose a clubhead moment-of-inertia limit of **5900 g·cm² + 100 g·cm² test tolerance** (USGA Notice to Manufacturers, https://www.usga.org/equipment-standards/notice-clubhead-inertia-test-and-limit.html). Sources disagree on whether this applies to putters:

- One reading: the MOI cap was introduced for **wood-type clubheads** (drivers especially) and applies to woods only — putters are excluded from the MOI cap in the same way they are excluded from the size/volume cap.
- Another reading: the cap applies to **all clubheads including putters**.
- **Empirical signal that supports the wood-only reading:** several currently-produced production putters (Odyssey 2-Ball Eleven Triple Track, TaylorMade Spider Tour X, PXG Battle Ready II Gunboat — per `putter-market-reference` §3.2, §3.4, §3.8) report MOI numbers in the 6,000–8,000+ g·cm² range and remain on the USGA conforming list. If the 5900 cap applied to putters, those models would not conform.

**GolfPro's position:** the cap is **effectively a wood-only constraint in practice**, but the exact rule text excluding putters is what GolfPro could not pin down freshly on 2026-05-23. A brief targeting a very-high-MOI mallet (>6000 g·cm²) should commit to the MOI band and add a *"USGA MOI rule scope pending Director / live USGA verification"* note. A brief targeting a normal-MOI mallet (3500–5500 g·cm² band) is safely inside any plausible reading of the rule.

**What would resolve it:** a direct read of Equipment Rules Part 2, Section 4 (*Club Head — Size, Shape, Volume, Moment of Inertia*) against the live PDF, naming the exact subsection that scopes the MOI cap to wood-type heads.

### 5.2 Open: post-purchase adjustability for putters

Rule 4.1a covers club conformance — adjustable features must (per training-data-cached text) be designed so that the adjustment cannot readily be altered during play, all adjustable parts are firmly fixed, and there is no reasonable likelihood the configuration will change during play. The adjustable feature must not be **adjusted during a round** without the configuration being treated as a substitution of a non-conforming club.

**What GolfPro is not sure of:** the exact Equipment Rules subsection that governs putter-specific adjustability (sole-weight ports, removable-sole-plate weight kits, adjustable-hosel angle tools). Several production putters (Scotty Cameron Super Select, Ping PLD Milled, TaylorMade Spider Tour) ship with **removable sole weights** that the user changes between rounds with a torque wrench. The convention in practice is that **weight changes between rounds are conforming; weight changes during a round are not**. The exact rule text and subsection are what GolfPro could not freshly verify.

**Brief implication:** any brief that specifies adjustable sole weights or interchangeable sole plates must commit to the adjustment-only-between-rounds convention explicitly and tag the rule reference as *"pending live-verification of the specific adjustability subsection"*. The conformance practice is well-established; the citation is what GolfPro is honest about not having pinned down freshly.

### 5.3 Open: novel face materials

The Equipment Rules face-material clause (Part 2, Section 5) carves putters out of the materials-in-impact-area restriction (per §4 of this skill). The catch-all conformance test is **traditional and customary in form and make** (Equipment Rules Part 2, general). Novel face materials raise the question of where the catch-all bites:

- **Graphene-coated faces** — not yet appearing in production putters at the time of this skill's writing. Conformance status uncertain.
- **Ceramic-infused inserts** — limited production exposure (some Asian-market putters); USGA conforming list listing status varies. Conformance status: **case-by-case**.
- **Multi-density polymer composites** (polymer-over-metal-over-polymer sandwiches) — currently produced (per `putter-market-reference` references to L.A.B. and Bettinardi INOVAI bi-metal architectures, §3.5, §3.6). These appear to be conforming under current practice but no published USGA case ruling was retrievable in the 2026-05-23 verification pass.

**Brief implication:** a brief that commits to a novel face material must commit it as *"design intent pending USGA conforming-list submission"* and not assert conformance pre-submission. The USGA's conforming-clubs submission process (a separate workflow per the [TAP-169](/TAP/issues/TAP-169) boundary — outside GolfPro's lane) is the path by which novel materials become canonically conforming.

### 5.4 Open: groove geometry × loft interaction

Most putter groove patterns are advertised by their manufacturers as *roll-promoting* (top-spin-inducing) rather than *spin-altering*. The Equipment Rules groove-geometry rules for non-putters (volume, edge sharpness, pitch) are the substance behind the 0.001-inch milling cap; putters are exempt per §4. **Open question:** at what point does a milled-groove geometry on a putter face cross from *putter face treatment* (exempt) into *grooves engineered to impart spin* (which would be a different category under the Equipment Rules)? GolfPro could not retrieve a clean line from the training-data cache.

**Brief implication:** stick to manufacturer-published groove geometries on currently-conforming production putters (per `putter-market-reference`) and do not innovate beyond that envelope without flagging for Director and USGA-process consultation.

## 6. Materials and adjustability (the parts that are *not* open questions)

> **Rule reference.** Equipment Rules Part 2, Section 1 (*Material and Construction*) and Part 2, general clause (*traditional and customary in form and make*). Equipment Rules 2024 edition. *Exact subsection numbers pending fresh verification against the Equipment Rules PDF.*

**Substance, training-data-cached:**

- **The clubhead must be one piece, or it must be an assembly that meets the rules for assembly.** Multi-material putter heads (cast-aluminium body + steel face plate + tungsten weights) are explicitly permitted in current production and are well-established as conforming.
- **All adjustable features (when present) must comply with the adjustability requirements of Rule 4.1a.** During a round, an adjustable feature **must not be changed** unless the change is made before the round starts or between rounds. Changing an adjustable feature during a round is treated as deeming the club a non-conforming substitute and is itself a rules violation.
- **Adhesives, paint-fills, alignment-mark fills, and grip materials** are not constrained in any substantively-design-impacting way for putters.

**Brief implication:** standard cast / milled / multi-material / insert-faced putter constructions are conforming. The brief does not need to defend conforming materials choices — only flag novel ones (per §5.3).

## 7. Markings, alignment aids, and the head

> **Rule reference.** Equipment Rules Part 2, Section 5 (*Club Face* — for face markings) and Part 2, Section 4 (*Club Head — Markings, Plain in Shape*) for non-face markings. Equipment Rules 2024 edition. *Exact subsection numbers pending fresh verification.*

**Substance:**

- **Alignment aids on the top edge / crown of a putter are permitted.** The Two-Ball discs, the Triple Track parallel lines, the single-line sight aid, the T-line, the sight dot, the fang-channel cue — all permitted (per `putter-anatomy-extended` §4). The rules constrain the **shape of the head** to be *plain in shape*, which is interpreted to forbid wildly non-functional protrusions but not the alignment-aid systems in current production.
- **Markings on the face of a putter must not have sharp edges or raised lips** (per §4 of this skill, putter-face exemption clause). Face-mounted alignment marks (uncommon but present on a few models) must keep edge geometry non-sharp.
- **The head must conform to the *plain in shape* requirement** of the Equipment Rules — interpreted in practice as banning ornamentation that has no function and would aid the player in ways the rules consider unfair. The current-production alignment-aid systems (per `putter-anatomy-extended` §4.1–§4.6) all satisfy this in practice; novel ornamentation should be flagged.

**Brief implication:** any alignment-aid system listed in `putter-anatomy-extended` §4 is conforming-by-current-practice. A brief committing to a novel alignment-aid concept (rotating sight discs, electronic markers, anything not a passive geometric or printed cue) must flag for Director and USGA-process consultation.

## 8. Citation format for briefs

Every USGA reference in a brief uses this format. The format is what makes the reference verifiable — a brief reader can take any cited claim straight to the live USGA source.

```
Rule X.Yz / Equipment Rules Part N, Section M, USGA Rules of Golf [edition year], joint with The R&A. Source: <usga.org URL>. Last verified: YYYY-MM-DD.
```

**Field rules:**

- **Rule number.** Use the Rule reference from the body of the Rules of Golf (e.g., `Rule 10.1b`, `Rule 4.1a`) or the Equipment Rules section reference (e.g., `Equipment Rules Part 2, Section 5`). When both apply, cite both.
- **Edition year.** The 2023 Rules of Golf and 2024 Equipment Rules are the current pair as of 2026-05-23. The pair refreshes every four years (next refresh expected 2027); when in doubt, cite the edition GolfPro last verified.
- **R&A jointness.** The Rules of Golf and Equipment Rules are jointly published by the USGA and The R&A. Name both jurisdictions when citing — *"USGA Rules of Golf, joint with The R&A"*.
- **Verbatim quotes** — use quotation marks. Use verbatim only when exact wording matters (Rule 10.1b anchoring text, the putter-face-exemption sentence, the length-with-putter-exemption sentence). Paraphrases are fine for substance but lose the *"verbatim"* mark.
- **Source URL.** Direct to the USGA page or PDF when retrievable. If the URL returned an error during verification (e.g., 403 on the Equipment Rules PDF), name the alternative source actually used and tag accordingly.
- **Last verified.** Real date GolfPro verified the citation. **Not the brief's draft date** — the date the citation was checked against the source. If the verification was against training-data-cached text rather than live USGA content, say so explicitly: *"Verified against [USGA publication] cached in training data; pending fresh verification by Director or live web-content read before brief-citation use."*

## 9. Non-USGA jurisdictions

- **The R&A** governs the Rules of Golf and the Equipment Rules everywhere **except the USA and Mexico**. The USGA governs in the USA and Mexico. **The Rules of Golf and Equipment Rules are jointly published and have been substantively harmonized since 1952.** Where the joint text reads identically across the USGA and R&A publications (the normal case), cite either or both; where it diverges, name the divergence.
- **Known divergences relevant to putter design are vanishingly rare in the 2023/2024 pair.** GolfPro is not aware of any putter-design rule that reads differently between the USGA and R&A texts in the current cycle. If a brief is destined for an R&A-jurisdiction event and a divergence is in doubt, the safer move is to cite the R&A text directly (`randa.org/en/roe/the-rules-of-equipment/part-2-conformance-of-clubs`) and note that the USGA text is materially harmonized.
- **Local rules and tournament-committee rules can further restrict.** The 46-inch Model Local Rule G-10 (§2 above) is the most consequential current example — adopted by the PGA Tour and DP World Tour for non-putter clubs, not adopted at amateur events broadly. **Local rules are out of scope for this skill and out of scope for design briefs by default** — a brief targeting a specific tournament context should escalate to Director for whether to design under the local rule envelope.
- **The professional tours can further further restrict** (PGA Tour Hard Card, LIV equipment policies, LPGA / DP World local sets). All out of scope here. Flag in a brief and escalate.

## 10. Anti-patterns

What bad rule-citation reasoning looks like in a brief. Each names the failure mode and the check that catches it.

1. **Cites a rule number without an edition year.** *"Rule 10.1b prohibits anchoring."* True today; was Rule 14-1b in the pre-2019 Rules of Golf and could renumber again at the 2027 refresh. **Without the edition year, the citation is not verifiable against the right text.** Always cite *"Rule 10.1b, 2023 edition"* or the then-current edition.

2. **Paraphrases a rule without quoting where exact wording matters.** *"The rule says you cannot anchor."* Loses the indirect-anchor-via-forearm mechanic, loses the *"or a gripping hand"* clause, loses the exemption for hand-or-forearm contact. **Anchoring is a rule whose wording is the rule** — verbatim quote with quotation marks is required for §3-class citations.

3. **Asserts a rule that does not exist** (or no longer exists). *"Putters have a 48-inch maximum length per the USGA."* This is the rule for non-putters; putters are explicitly exempt. **The check that catches this is reading the rule text against the cited number, not trusting a remembered summary.** This anti-pattern appears in the original commission text for this skill and is the reason §2 has a dedicated *"anti-pattern alert"* call-out.

4. **Extends a rule by analogy without a citation.** *"Driver MOI is capped at 5900 g·cm², so putters must be too."* The 5900 cap is a wood-head rule and there is genuine uncertainty about whether it applies to putters at all (§5.1). **An analogy is not a citation; if the rule does not name the club category, do not assume it applies.**

5. **Treats a tour-committee local rule as a USGA rule.** *"USGA caps club length at 46 inches."* Wrong — 46 inches is the Model Local Rule G-10, optional and locally-adopted, not a universal USGA limit. Conflating local-rule and universal-rule scope creates spurious design constraints. **Always name the rule's scope when citing — Rule of Golf, Equipment Rule, Model Local Rule, or tour-specific.**

6. **Quotes a putter-specific exemption while ignoring its caveat.** *"Putter face roughness is unconstrained."* Almost — the impact-area roughness/material/markings rules do not apply, but the face-markings prohibition on **sharp edges and raised lips** still applies (per §4). **The exemption has a remainder; quote both halves or neither.**

7. **Writes *"per USGA"* without naming a Rule or Equipment Rules section.** A bare *"per USGA"* is not a citation. The minimum citation is *"Rule X.Yz, USGA Rules of Golf [edition]"* or *"Equipment Rules Part N, Section M, [edition]"*. If GolfPro cannot cite to that level, the claim is not yet a citation — it is a research note.

8. **Cites a USGA rule without checking the R&A jointness.** When a brief is destined for R&A jurisdiction, citing only the USGA text (without noting joint publication) implies the rule is USA-only. The 2023 Rules and 2024 Equipment Rules are jointly published — name the joint authorship.

## 11. Worked example — a broomstick-length putter brief snippet

A brief commissioned for a 14-handicap player with the yips at distance, prescribing a 50-inch broomstick build with a high-MOI mid-mallet head. The brief's §2 (head family + variant) commits to a wing-back mid-mallet with single-bend hosel; §3 (dimensions) commits to a 50-inch overall length; §4 (head weight band) commits to 380 g (counter-balanced band per `putter-fitting` §4); §11 (conformance) cites:

> **§11 — Conformance.**
>
> **Length (50 inches overall).** Conforming under Rule 4.1a, *Rules of Golf*, 2023 edition (joint with The R&A) and Equipment Rules Part 2, 1c (Length), Equipment Rules 2024 edition. Putters are exempt from the 48-inch maximum-length cap that applies to other clubs: per the Equipment FAQ, *"The overall length of the club must be at least 18 inches and, except for putters, must not exceed 48 inches."* (Source: https://www.usga.org/equipment-standards/equipment-faq-25852.html. Last verified by GolfPro: 2026-05-23.)
>
> **Anchoring (broomstick mechanic).** The 50-inch length is conforming on the equipment dimension, but the player using this putter must not make a stroke that violates Rule 10.1b, *Anchoring the Club*, *Rules of Golf*, 2023 edition (joint with The R&A): *"In making a stroke, the player must not anchor the club, either: 'Directly,' by holding the club or a gripping hand in contact with any part of the body (except that the player may hold the club or a gripping hand against a hand or forearm), or 'Indirectly' through use of an 'anchor point,' by holding a forearm in contact with any part of the body to enable the gripping hand to hold the club against and away from the body."* (Source: USGA, *Understanding Rule 10.1b*, 2023 edition, https://www.usga.org/content/dam/usga/pdf/2023/rules/2023_USGA_UnderstandingAnchoredStrokes.pdf. Last verified by GolfPro: 2026-05-23.) **Design accommodation:** the grip taper from inches 35–50 is profiled for a claw-style upper-hand grip held away from the chest, paired with a standard lower-hand stroke; the geometry intentionally does **not** invite a chest-anchor mechanic. The conformance of the stroke is the player's responsibility; the brief commits the geometry to a configuration that supports a conforming stroke.
>
> **Head weight (380 g, counter-balanced band).** No USGA rule constrains head weight for putters in the band committed. The 380 g sits inside the counter-balanced band per `putter-fitting` §4 and is well below any plausible reading of a clubhead MOI cap (see *open question* below).
>
> **MOI band (~5500 g·cm², open question on USGA cap applicability).** The Equipment Rules cap clubhead moment of inertia at 5900 g·cm² + 100 g·cm² test tolerance (USGA Notice to Manufacturers, https://www.usga.org/equipment-standards/notice-clubhead-inertia-test-and-limit.html). Per `usga-rules-putters` §5.1, the applicability of the 5900 cap to putters is a genuine open question — the cap was introduced for wood-type heads, and currently-conforming production putters (Odyssey 2-Ball Eleven Triple Track, TaylorMade Spider Tour X) report MOIs in the 6,000–8,000+ g·cm² range. This brief commits to a 5500 g·cm² band that sits below the cap on any reading and does not need to resolve the open question. **Director note: if a future revision moves the target above 5,900, escalate per `usga-rules-putters` §5.1.**
>
> **Face (CNC-milled, single line alignment).** Conforming under Equipment Rules Part 2, Section 5 (*Club Face*), Equipment Rules 2024 edition — putter faces are exempt from the impact-area roughness, milling-depth, and material specifications that constrain non-putter clubfaces. The single-line alignment marking on the face must not have sharp edges or raised lips (the putter-face caveat that survives the exemption); the brief commits to a rounded-edge incised line, not a punched-in raised-rim line. (Source: USGA Equipment FAQ, https://www.usga.org/equipment-standards/equipment-faq-25852.html. *Exact Part 2, Section 5 subsection numbering pending fresh verification per `usga-rules-putters` §1.*)

Citation discipline applied in this snippet:

- Every rule reference has **Rule number + edition year + R&A joint-authorship note + source URL + GolfPro's last-verified date**.
- The verbatim quote of Rule 10.1b is in quotation marks (the wording is the rule — anti-pattern §10.2 avoided).
- The anti-pattern of citing *"48 inches"* as the putter cap (anti-pattern §10.3) is explicitly avoided by quoting the FAQ's *"except for putters"* clause.
- The MOI commitment is structured around the open question (§5.1) — the brief commits to a value safely inside any reading, and escalates if a revision would change that.
- The face-exemption is quoted with its remainder (the no-sharp-edges-or-raised-lips caveat — anti-pattern §10.6 avoided).
- The Part 2, Section 5 subsection number is honestly tagged as *"pending fresh verification"* — anti-pattern §10.7 (bare *"per USGA"*) avoided by naming the section even with the subsection-numbering gap acknowledged.

## 12. What this skill does not cover

- **Formal USGA conformance certification submission.** The process by which a manufacturer submits a putter to the USGA for inclusion on the conforming-clubs list is a regulatory workflow that lives outside this skill and outside GolfPro's lane per the [TAP-169](/TAP/issues/TAP-169) hire spec. This skill covers **rule awareness during design** — what a brief must respect to be safely conforming when manufactured; not the certification paperwork itself.
- **The Rules of Golf in their entirety.** This skill covers only the rules that bear on putter **design**. Rules about the pace of play, the order of play, the holing-out procedure, putting on the wrong putting green, etc. are out of scope.
- **Shafts, grips, and ball rules.** TapIn's domain is putter **heads** per the project scope. Shaft and grip equipment rules are out of scope; ball equipment rules are doubly out of scope.
- **Historical rule numbering.** Rule 10.1b was Rule 14-1b in the 2016–2018 cycle. Earlier historical numberings are out of scope; cite to the **current** edition.
- **Tour-specific equipment policy and Hard Card local-rule sets.** PGA Tour Hard Card, DP World Tour Hard Card, LIV equipment policies, LPGA local-rule sets — all are out of scope by default. A brief targeting a tournament context should escalate per §9 above.
- **Penalty determination at competition.** The brief's job is to commit a design that supports conforming play; the penalty for a non-conforming club in actual competition is the tournament committee's call, not GolfPro's. Reference penalties only when the design itself carries a non-conformance risk (e.g., a novel face material flagged under §5.3) and the brief needs the player and the committee to be aware.

