# CAJAL Figure Intelligence — Chapter 18: Arc Diagram

**Source:** `chapters/18-arc-diagram.md`
**Mode:** `/scan silent`
**Domain note:** AI+1 practitioner guide / data visualization with D3 and Claude. Part II opens here — sixty-one chart types, alphabetically. The chapter's chart artifact (`../images/18-arc-diagram.jpg`) is an example output the reader will reproduce via the Claude Code prompt; it is NOT a CAJAL figure. CAJAL-eligible figures are the diagrammatic explanations of arc-diagram mechanics: anatomy, node-order trade-off, the O(n²) crossing problem.

---

## Density Recommendation

**2 figures, Mechanistic density.** The chapter's argument turns on two specific claims that a diagram clarifies faster than prose: (1) arc height is determined by horizontal distance between endpoints — a geometric fact about the encoding; (2) node ordering is the single most consequential design decision, with alphabetical maximising crossings and connection-sorted minimising them. The example chart already lives on the page as a placeholder; what is missing is the explanatory anatomy.

---

## Zone Map

- **MC:** Arc geometry — every arc's height is a deterministic function of endpoint distance on the horizontal axis. Stroke weight encodes raw count. Node area encodes a second quantitative variable. Crossings grow as O(n²) with node count.
- **VG:** Two-panel ordering comparison — alphabetical vs connection-sorted on the same data — exposes how reorderable axes change the visual hierarchy without touching the data.
- **PQ:** Eight nodes in the example; Elara 42 scenes; Elara–Fenn 18 co-occurrences, Elara–Voss 12, Fenn–Voss 14, Lena–Dax 2. Scales cleanly to 10–25 nodes; degrades past ~30. These quantities live in the data file, not in a figure.

---

## Figure 18.1 — Arc Diagram Anatomy

**Priority: Important.** Foundation for the chapter and the chapters that follow in Part II. Once the reader sees the arc-geometry rule (height ∝ endpoint distance) they understand why alphabetical ordering is hostile to the chart type.

### Block 1 — Illustrae paste block

A horizontal axis composition. A single Black `#000000` 1pt horizontal line spans the figure, with six evenly spaced node circles (Blue `#0072B2` filled, varying radii to suggest the node-size encoding) seated on the line. Above the axis, four curved arcs connect node pairs: a short shallow arc between two adjacent nodes (Sky Blue `#56B4E9` 1pt stroke, thin), a medium arc spanning three positions (Vermillion `#D55E00` 2pt stroke, medium), a tall arc spanning the full span between leftmost and rightmost nodes (Vermillion `#D55E00` 3pt stroke, heaviest), and one more medium arc between adjacent nodes (Sky Blue 1.5pt). Arc heights are visibly proportional to the horizontal endpoint distance — the geometric rule. Two small bracketed indicators at the side (Black `#000000` 1pt) call out: node radius and arc thickness as the two encoded channels. White background, flat vector, single-column 89mm.

### Block 2 — Full SCOPE prompt

[S] Single-column 89mm, vector, white background.
[C] Six-node arc diagram with four arcs of varying span and varying stroke weight. Arc height proportional to endpoint distance on the axis. Node radius varies to indicate the second quantitative encoding.
[O] Horizontal axis bottom-centre. Arcs rise above the axis. Two encoding indicators set to one side.
[P] Axis and indicators Black 1pt. Nodes Blue filled. Strong arcs Vermillion. Light arcs Sky Blue. Arc stroke weight encodes co-occurrence frequency.
[E] No character names rendered, no axis tick labels, no legend text, no decorative ornament, no shadows, no gradients.

### Block 3 — Negative prompt

text labels, character names, axis labels, legend text, tick numbers, titles, captions, gibberish letters, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 18.2 — Node-Order Trade-Off

**Priority: Important.** The chapter's single most consequential design claim. Two panels, same data, different orderings — readers see the crossing-density change without needing the proof.

### Block 1 — Illustrae paste block

A two-panel composition side by side, both panels sharing identical node sets (eight Blue `#0072B2` filled circles on a Black `#000000` 1pt axis) and identical link sets, with only the node ordering changed between panels. Left panel (alphabetical order): the same eight nodes with the strongest connections distributed across the full span — many arcs crossing each other, producing a dense visual tangle of Sky Blue `#56B4E9` and Vermillion `#D55E00` curves overlapping. Right panel (connection-sorted, descending): the most-connected nodes pulled toward the centre, producing a compact bundle of short heavy arcs at the middle and only a few light arcs reaching to the ends. Crossings dramatically reduced. A small Bluish Green `#009E73` arrow indicator between the panels suggests the toggle action. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same eight nodes and same links rendered twice — left alphabetical (high crossings), right connection-sorted (low crossings). Same arc-weight encoding in both.
[O] Two panels side by side. Identical axis baselines. Toggle indicator between them.
[P] Nodes Blue filled. Axis Black 1pt. Heavy arcs Vermillion. Light arcs Sky Blue. Toggle indicator Bluish Green.
[E] No node labels, no panel titles, no axis numbers, no decorative ornament, no shadows, no gradients.

### Block 3 — Negative prompt

text labels, character names, axis labels, panel titles, tick numbers, legend text, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## What CAJAL Declines to Architect

- **The example chart itself (`../images/18-arc-diagram.jpg`).** This is an example artifact rendered by the Claude Code prompt, with source on bearbrown.co. It is the chapter's product, not a CAJAL figure. Architecting it inside the pantry would duplicate what the prompt generates.
- **The Claude Code prompt block.** Code/prose typography. Out of CAJAL scope.
- **Framework reference paragraph (FT Visual Vocabulary / Abela / Tufte).** Typographic citation, not a figure.
- **The "About this example" character co-occurrence narrative.** Story text. The Elara/Fenn/Voss numbers are illustrative, not figure-worthy on their own.
- **AI Wayback Machine — Euler / Königsberg bridges.** Reference content with a portrait image already specified. The Königsberg-bridges schematic is interesting but belongs in a graph-theory chapter, not here.
- **Force-directed graph contrast.** The chapter mentions it for argument but defers the layout family to its own chapter elsewhere in Part II.

---

## Video Candidate Pass

**FIGURE 18.1 (Anatomy):** STATIC SUFFICIENT.
**FIGURE 18.2 (Node-order trade-off):** **MILD VIDEO CANDIDATE.** A short morph from alphabetical to connection-sorted order — nodes sliding along the axis while arcs redraw to follow — dramatizes the crossing-reduction claim and matches the chapter's `sort` button interaction. Useful as a 4–6 second loop in a digital edition, but the static two-panel comparison carries the argument in print.

**Video candidates identified: 0 strong + 1 mild.** Recommended: keep both figures static for the print edition; reserve the Fig 18.2 morph for the bearbrown.co interactive companion.

---

## Split-point note

Chapter is the first of sixty-one chart-type chapters. Establish the CAJAL pattern here: every chart-type chapter has (a) the example artifact placeholder, (b) one to two CAJAL diagrams that explain the chart's mechanics independent of the specific data, (c) the Claude Code prompt, (d) the AI Wayback Machine. The pantry CAJAL block covers only (b). Keep the anatomy-vs-trade-off pair as a template across the chart-type chapters that follow.
