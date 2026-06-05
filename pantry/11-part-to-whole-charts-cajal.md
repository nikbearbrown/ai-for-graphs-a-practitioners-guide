# CAJAL Figure Intelligence — Chapter 11: Part-to-Whole Charts

**Source:** `chapters/11-part-to-whole-charts.md`
**Mode:** `/scan silent`
**Domain note:** AI+1 practitioner guide / data visualization with D3 and Claude. Chapter walks the part-to-whole family (pie, donut, waffle, single stacked bar, Marimekko, Nightingale rose) through the five-slice rule, Cleveland & McGill angle accuracy, Cairo's rhetorical-vs-analytical frame, and Few's clarity-first position. Five author-placed figures.

---

## Density Recommendation

**5 figures, Concept-density.** All five are abstract chart-type skeletons demonstrating the channel mechanism behind each form. Each carries an argument the prose cannot: angle-perception threshold, channel substitution, advocacy distortion, decision logic, design-decision callouts.

---

## Zone Map

- **MC:** Five-slice rule traced to angle-perception threshold (~30°). Pie uses angle (rank 4); waffle uses position via cell count (rank 1). Single stacked bar uses segment length within total. Nightingale rose's area-as-radial-length-squared distortion. Cairo's rhetorical-vs-analytical advocacy frame.
- **VG:** Pie failure mode (12 small wedges below threshold). Waffle 10×10 cell grid. Nightingale polar wedges. Decision tree branching compositional vs comparative.
- **PQ:** 30°–150° readable angle range. 8% slice ≈ 28.8° below threshold. 10×10 = 100 cells, one cell = 1%. Cleveland & McGill channel ranks.

---

## Figure 11.1 — Five-Slice vs Twelve-Slice Pie

**Priority: Critical.** The five-slice rule made visual. Anchors the chapter's central perceptual argument.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition. Left panel: a pie chart with five wedges of distinctly different sizes — the largest wedge approximately half the circle filled Blue `#0072B2`, the next about a quarter filled Sky Blue `#56B4E9`, then progressively smaller wedges in Bluish Green `#009E73`, Orange `#E69F00`, and Reddish Purple `#CC79A7`. Each wedge clearly large enough to compare visually. The largest wedge starts at 12 o'clock, slices decreasing clockwise. A thin Black `#000000` 1pt arc outside the upper-right of the circle marks the 30°–150° readable angular range (post-typography annotation will sit here). Right panel: a pie chart with twelve roughly equal small wedges, all filled with the same Sky Blue `#56B4E9` (no hue differentiation needed), separated by thin Black 1pt boundaries. Most wedges visibly below the 30° threshold. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Pie chart with five wedges (above 30° threshold) on the left; pie chart with twelve roughly equal wedges (below threshold) on the right.
[O] Two panels horizontal. Equal circle diameters. Left clockwise from largest at 12 o'clock; right twelve equal slices.
[P] Left wedges Blue / Sky Blue / Bluish Green / Orange / Reddish Purple. Right wedges all Sky Blue. Wedge boundaries Black 1pt. Range-arc marker Black 1pt.
[E] No category labels, no percentage labels, no legend, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, category names, percentages, legend, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 11.2 — Pie vs Waffle

**Priority: Important.** The angle-to-position channel substitution made visible.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition. Left panel: a five-slice pie chart with the largest wedge at 12 o'clock — wedges filled with Blue `#0072B2` (largest), Sky Blue `#56B4E9`, Bluish Green `#009E73`, Orange `#E69F00`, Reddish Purple `#CC79A7` (smallest), clockwise from largest, separated by Black `#000000` 1pt thin lines. Right panel: a 10×10 waffle grid — 100 small uniform square cells arranged in 10 rows and 10 columns, color-coded to match the same five-category distribution: Blue cells occupy approximately 40 cells in the upper portion, Sky Blue cells the next 25, Bluish Green next 18, Orange next 10, Reddish Purple final 7. Cells filled flat, separated by thin Black 0.5pt lines between cells. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same five-category proportions. Left: pie with wedges (angle channel). Right: 10×10 waffle grid with cells color-coded in five contiguous regions (position-via-cell-count channel).
[O] Two panels horizontal. Equal panel widths. Pie diameter ≈ waffle grid edge.
[P] Five categories share palette: Blue, Sky Blue, Bluish Green, Orange, Reddish Purple. Boundaries Black 0.5–1pt thin.
[E] No category labels, no percentages, no legend, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, category names, percentages, legend, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 11.3 — Nightingale Polar Area

**Priority: Important.** The honest distortion. Advocacy form with named distortion.

### Block 1 — Illustrae paste block

A single circular composition centered on the panel. Twelve sector wedges fan out evenly around the full 360° (monthly cycle), each wedge a 30° angular slice. Within each wedge, three concentric radial bands of different lengths represent three causes: an innermost short band filled with Sky Blue `#56B4E9` (other), a middle band filled with Orange `#E69F00` (wounds), and an outermost longest band filled with Reddish Purple `#CC79A7` (preventable disease) — the outer band's radial length is dramatically greater than the inner two in most months, illustrating the area-as-radial-length-squared amplification. A few months show the bands all small (winter, fewer deaths). Each wedge separated by thin Black `#000000` 1pt radial lines. A thin Black 1pt central circle marks the origin. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Twelve-wedge polar area chart. Each wedge split into three concentric radial bands of distinct lengths. Outermost band consistently longest, illustrating Nightingale's area amplification.
[O] Circular composition. Twelve equal angular wedges. Concentric bands radial from center outward.
[P] Innermost band Sky Blue, middle band Orange, outermost band Reddish Purple. Radial dividers Black 1pt. Center circle Black 1pt.
[E] No month labels, no count annotations, no legend, no chart title, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, month names, count annotations, legend, chart title, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 11.4 — Composition vs Comparison Decision Tree

**Priority: Important.** The audit before the chart, visualized as a flow.

### Block 1 — Illustrae paste block

A top-down two-branch decision tree composition. At the top: a single Black `#000000` 1pt outlined rounded rectangle (the root question node) filled white. Two Black 1pt arrows descend from the root — one to the lower-left labeled with an arrow only, leading to a Blue `#0072B2` filled rounded rectangle (compositional branch); one to the lower-right, leading to an Orange `#E69F00` filled rounded rectangle (comparative branch). From the Blue compositional node, two further arrows split downward to two intermediate Sky Blue `#56B4E9` filled rectangles (five-slice check, then precision-vs-familiarity), which in turn split to three leaf rectangles filled Bluish Green `#009E73` (waffle, pie/donut, aggregate+bar). From the Orange comparative node, a single arrow descends directly to a Reddish Purple `#CC79A7` filled leaf rectangle (sorted bar chart). All connectors Black 1pt arrows. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Two-branch decision tree. Root → compositional (left) and comparative (right). Compositional branch splits to five-slice check, then precision-vs-familiarity, terminating in waffle / pie / aggregate+bar leaves. Comparative branch terminates directly in sorted bar chart leaf.
[O] Top-down layout. Root centered top. Two main branches splitting downward. Compositional branch deeper than comparative.
[P] Root white-fill Black 1pt outline. Compositional Blue. Sub-decisions Sky Blue. Compositional leaves Bluish Green. Comparative Orange. Comparative leaf Reddish Purple. Connectors Black 1pt arrows.
[E] No node labels rendered as graphic text, no edge labels, no titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, node labels, edge labels, decision text rendered as graphic, titles, captions, gibberish letters, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 11.5 — Five Design Decisions in a Pie Chart

**Priority: Important.** Annotation overlay showing the five deliberate choices.

### Block 1 — Illustrae paste block

A single five-slice pie chart centered in the panel, with the largest wedge filled Blue `#0072B2` starting at 12 o'clock and slices decreasing clockwise: Sky Blue `#56B4E9`, Bluish Green `#009E73`, Orange `#E69F00`, Reddish Purple `#CC79A7`. Wedges separated by Black `#000000` 1pt thin lines. Around the pie, five small Black `#000000` 1pt outlined circular numbered callout markers (small empty circles, no text rendered) positioned at: top-left (aggregation note), 12 o'clock (sort-order start), the dominant Blue wedge (direct-label position), the boundary between two adjacent wedges (color-hue note), and the bottom of the dominant slice (headline-signal note). Each callout connected to its referenced location by a thin Black 1pt leader line. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Five-slice pie with the largest wedge at 12 o'clock and five numbered callout markers (empty circles) surrounding it, leader lines pointing to the specific design-decision locations.
[O] Pie centered. Callout markers positioned around the perimeter, leader lines to specific features.
[P] Wedges Blue, Sky Blue, Bluish Green, Orange, Reddish Purple. Wedge boundaries Black 1pt. Callout markers Black 1pt outlined circles, white-fill. Leader lines Black 1pt.
[E] No callout numbers rendered as graphic, no decision text, no legend, no chart title, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, callout numbers, decision text, category names, percentages, legend, chart title, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## What CAJAL Declines to Architect

- **Form-comparison table (Pie / Donut / Waffle / Stacked / Marimekko / Nightingale).** Typography reference table; belongs in body text or sidebar.
- **Key Terms block.** Glossary text.
- **Prompt code blocks.** Code samples, not figures.
- **Georg von Mayr portrait.** AI Wayback Machine reference image, generated by separate pipeline.

---

## Video Candidate Pass

**FIGURE 11.1 (Five-slice vs twelve-slice):** STATIC SUFFICIENT.
**FIGURE 11.2 (Pie vs waffle):** **MILD VIDEO CANDIDATE.** Animating the morph from pie wedges to waffle cells (one slice flowing into its corresponding cell count) would teach the channel substitution directly. Static is sufficient.
**FIGURE 11.3 (Nightingale polar area):** **MILD VIDEO CANDIDATE.** Animating the wedges growing from center outward could dramatize the rhetorical force Nightingale exploited. Static serves the chapter.
**FIGURE 11.4 (Decision tree):** STATIC SUFFICIENT.
**FIGURE 11.5 (Five design decisions):** STATIC SUFFICIENT.

**Video candidates identified: 0 strong + 2 mild.** Recommended: keep all five static; treat 11.2 and 11.3 as candidates for live-presentation supplements.

---

## Split-point note

Chapter cross-references Chapter 3 (Cleveland & McGill channel hierarchy), Chapter 4 (chart selection, Cairo's rhetorical-vs-analytical frame), Chapter 10 (bubble charts share the area-perception mechanism that drives Nightingale's distortion). Color palette for the five-slice pie (Fig 11.1, 11.2, 11.5) should remain consistent across the three figures for visual coherence.
