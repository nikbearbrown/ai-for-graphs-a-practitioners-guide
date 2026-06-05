# CAJAL Figure Intelligence — Chapter 15: Specialized and Financial Charts

**Source:** `chapters/15-specialized-and-financial-charts.md`
**Mode:** `/scan silent`
**Domain note:** AI+1 practitioner guide / data visualization with D3 and Claude. Chapter argues specialized chart forms (candlestick, OHLC, Kagi, Point & Figure, bullet graphs, radar, polar area) must "earn their strangeness" — bundle real analytical value via honest perceptual channels for an audience that has internalized the convention. Four author-placed figures.

---

## Density Recommendation

**4 figures, Conceptual-conventional density.** All four earn their place. Each figure is the visual argument for one of the chapter's claims about specialized forms (encoding compactness, channel-rank failure, axis-order artifact, the earn-your-strangeness test).

---

## Zone Map

- **MC:** The earn-your-strangeness test (does a specialized form answer a specific question better than a standard form, using honest channels, for an audience that knows the convention?). Position-vs-angle as the recurring channel-rank argument.
- **VG:** Candlestick anatomy (body = open-to-close, wicks = high/low, color = direction). Gauge-vs-bullet footprint difference. Radar polygon shape as a function of axis order. The decision tree itself.
- **PQ:** Cleveland & McGill ranks named in the table (position 1, length 2, angle 4, area 5). 180° gauge arc, 70% needle position, $4.2M vs. $4.0M target. The 4–7% Kagi reversal threshold.

---

## Figure 15.1 — Candlestick Anatomy vs. Closing-Price Line

**Priority: Critical.** The chapter's opening argument — four variables per glyph versus one. Must read at a glance.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition. Left panel: a single enlarged candlestick. The rectangular body is drawn as a Bluish Green `#009E73` filled rectangle (rising day convention) with a Black `#000000` 0.75pt stroke. A thin Black 1pt vertical wick extends above the body to a high tick and below the body to a low tick. Four small Sky Blue `#56B4E9` filled dots mark the four price levels (open at body bottom, close at body top, high at upper wick tip, low at lower wick tip). Right panel: a line chart of eight closing-price points across the same eight periods, drawn as a Blue `#0072B2` 1.5pt polyline with small Blue filled dots at each closing-price node. A light Black 0.5pt horizontal axis line beneath. Both panels sit on the same vertical price scale (implied alignment). White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Left: single annotated candlestick showing body (open-to-close), upper wick (to high), lower wick (to low), color encoding direction. Right: line chart of closing prices for the same eight periods. Argument: four variables per glyph versus one.
[O] Two horizontal panels, left and right, sharing a vertical price scale.
[P] Candle body Bluish Green (rising). Body stroke Black 0.75pt. Wicks Black 1pt. Price-level dots Sky Blue. Line chart Blue 1.5pt with Blue node dots.
[E] No tick mark numbers, no price labels, no date axis, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, price numbers, date labels, ticker symbols, axis numbers, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 15.2 — Gauge vs. Bullet Graph

**Priority: Critical.** Few's central argument made visual. Footprint, channel rank, and position-vs-angle in one comparison.

### Block 1 — Illustrae paste block

A side-by-side composition. Left: a semicircular gauge. The dial arc spans 180° drawn as a Black `#000000` 1pt arc, divided into three sequential-luminance bands (light Sky Blue `#56B4E9` 20% opacity, medium 40%, dark 60%). A Blue `#0072B2` 1.5pt needle radiates from the arc's center at roughly 70% of the sweep (positioned near the right end). A small Orange `#E69F00` filled tick on the arc marks the target. Right: a horizontal bullet graph. Three stacked sequential-luminance gray bands (Sky Blue 20%, 40%, 60%) form the background strip. A thick Blue `#0072B2` filled horizontal bar extends from the left baseline to 70% of the strip width. A short Orange `#E69F00` 2pt vertical tick crosses the bar at the 85% target position. Below each panel, a small Vermillion `#D55E00` 1pt outlined bounding box indicates the form's footprint, with the gauge box clearly larger than the bullet box. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Gauge versus bullet graph for the same KPI. Gauge uses angle (channel rank 4); bullet uses position along a common scale (channel rank 1). Footprint comparison shown via bounding boxes.
[O] Two horizontal panels, left (gauge) and right (bullet). Footprint outlines below each.
[P] Gauge arc Black, bands sequential Sky Blue luminance, needle Blue, target Orange. Bullet bar Blue, bands Sky Blue luminance, target Orange. Footprint outlines Vermillion.
[E] No numeric values, no percentage labels, no axis tick numbers, no band names, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, percentage numbers, axis tick numbers, band names, KPI names, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 15.3 — Radar Axis-Order Failure

**Priority: Important.** Demonstrates the Bertin-class encoding failure where polygon shape is partly a design decision. Three polygons from identical data.

### Block 1 — Illustrae paste block

Three radar charts arranged horizontally, each on a six-spoked wheel. Each wheel has six Black `#000000` 0.5pt radial axis lines extending from a central node to outer dots, and three concentric Black 0.25pt circular gridlines at 33%, 66%, and 100% radius. Each chart plots the same six attribute values but with the axes in a different sequence around the wheel. The polygon is drawn as a closed Blue `#0072B2` 1.5pt polyline with a Blue 20% opacity fill. Small Blue filled dots mark each vertex. The three polygons look visibly different in shape — one spiky on the right, one spiky on the top, one nearly symmetric — even though the underlying values are identical. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Three radar charts of identical six-attribute data shown in three different axis orders. Polygon shapes differ visibly. Argument: shape is partly a design decision.
[O] Three horizontal panels left-to-right. Each wheel sized identically.
[P] Axes Black 0.5pt. Gridlines Black 0.25pt. Polygons Blue 1.5pt outline with 20% Blue fill. Vertex dots Blue.
[E] No attribute names, no axis labels, no scale numbers, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, attribute names, axis labels, scale numbers, polygon labels, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 15.4 — Earn-Your-Strangeness Decision Tree

**Priority: Important.** The chapter's synthesis instrument. Two example paths traced through the tree.

### Block 1 — Illustrae paste block

A horizontal decision tree composition. Root node at top-left: a Sky Blue `#56B4E9` filled rounded rectangle representing the question "does this specialized form answer the question better than a standard form?". From the root, a Blue `#0072B2` 1pt arrow labels post-typography as YES branches down-right to a second decision node (Sky Blue rounded rectangle: "does the audience know the convention?"). From that node, a YES arrow branches further to a Bluish Green `#009E73` filled terminal rectangle ("use it"). A NO arrow from each decision node branches to a Vermillion `#D55E00` filled terminal rectangle ("replace with standard form"). Two example paths are traced as thicker 2pt highlighted lines: the candlestick path (YES → YES → use it) drawn in Bluish Green, and the gauge path (NO → replace) drawn in Vermillion. Small Orange `#E69F00` filled dots mark the example entry points at each path's start. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Decision tree starting from a root question, branching by yes/no through an audience-graphicacy check, terminating in either "use it" or "replace with standard form". Two example paths highlighted: candlestick (positive) and gauge (negative).
[O] Left-to-right tree with root at left, terminals at right.
[P] Decision nodes Sky Blue. Arrows Blue 1pt. Use-it terminals Bluish Green. Replace terminals Vermillion. Example paths Bluish Green / Vermillion 2pt. Entry-point dots Orange.
[E] No node text labels, no arrow labels, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, node text, decision text, arrow labels, terminal labels, example names, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## What CAJAL Declines to Architect

- **The form/channel/rank/question/failure table (lines 39–46).** Typography reference table. Belongs as a layout table, not a figure.
- **The OHLC bar variant.** Described in prose but not author-placed; if needed, it would duplicate Figure 15.1's logic.
- **Kagi line thickness diagram and Point & Figure X/O column diagram.** Both are discussed verbally but no author figure exists. The conventions are typographic glyphs; defer unless a future revision adds explicit visual treatment.
- **Polar area / Nightingale references.** Already covered by Chapter 11's figure; not duplicated here.
- **Munehisa Homma AI Wayback portrait.** Existing AI-generated portrait reference, not a CAJAL architectural target.

---

## Video Candidate Pass

**FIGURE 15.1 (Candlestick vs. line):** STATIC SUFFICIENT.
**FIGURE 15.2 (Gauge vs. bullet):** STATIC SUFFICIENT.
**FIGURE 15.3 (Radar axis-order):** **MILD VIDEO CANDIDATE.** Cycling through axis permutations with the same data values would dramatize the artifact — three frozen frames already capture the argument, but an animated rotation could land it for skeptics.
**FIGURE 15.4 (Decision tree):** STATIC SUFFICIENT.

**Video candidates identified: 0 strong + 1 mild.** Recommended: hold; the static three-panel version of Fig 15.3 is the cleaner instructional artifact. Reserve animation budget for chapters where the mechanism itself is dynamic.

---

## Split-point note

Chapter cross-references Chapter 01 (Cleveland & McGill hierarchy), Chapter 07 (zero-baseline and proportional ink), Chapter 11 (polar area / Nightingale rhetorical-vs-analytical frame). Figures here should share a visual language with Chapter 01's channel-rank figure and Chapter 07's truncated-bar figure — same palette, same stroke weights, same flat-vector treatment — so the position-vs-angle argument reads as one continuous thread.
