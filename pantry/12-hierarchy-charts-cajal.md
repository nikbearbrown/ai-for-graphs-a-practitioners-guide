# CAJAL Figure Intelligence — Chapter 12: Hierarchy Charts

**Source:** `chapters/12-hierarchy-charts.md`
**Mode:** `/scan silent`
**Domain note:** AI+1 practitioner guide / data visualization with D3 and Claude. Chapter walks the hierarchy family (treemap, sunburst, circle packing, tree diagram) through the three-property framework (proportions, depth, structure), the squarified treemap algorithm, depth limits as geometry, and the Gestalt figure-ground mechanism. Six author-placed figures.

---

## Density Recommendation

**6 figures, Mechanistic density.** All six are abstract chart-type skeletons demonstrating structural choices: question-driven form selection, four-form reference grid, rectangles-vs-circles alignment, depth-limit geometry, squarification effect, irregular-depth handling.

---

## Zone Map

- **MC:** Three-property framework (proportions, depth, structure). Squarified algorithm minimizes worst aspect ratio. Treemap depth limit = 3 (geometry). Sunburst depth limit = 5 (radial width). Gestalt figure-ground in sunbursts. Circle-packing structural honesty for irregular depth.
- **VG:** Nested rectangles vs concentric rings vs nested circles vs node-link. Aligned-edge anchoring in rectangles. Sub-pixel collapse at deep treemap levels.
- **PQ:** 0.1 × 0.1 × 0.1 = 0.001 of total area at three 10% levels. 800×600 → 0.48 sq px at 3 levels of 10%. Sunburst at 400px radius, 6 levels = 67px ring width. 50 leaves → 50px outer segment; 200 → 12px.

---

## Figure 12.1 — Same Hierarchy, Two Questions

**Priority: Critical.** The chapter's opening argument: form follows question.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition. Left panel: a treemap composed of nested rectangles. One large dominant rectangle in the upper-left filled Blue `#0072B2` occupying about 40% of the panel area, subdivided internally into 3–4 smaller rectangles in Sky Blue `#56B4E9`. Adjacent to it, a medium rectangle filled Bluish Green `#009E73` subdivided into 2 smaller pieces. Three more progressively smaller rectangles in Orange `#E69F00`, Reddish Purple `#CC79A7`, and again Sky Blue, each subdivided into 2–3 smaller cells. All rectangles separated by thin Black `#000000` 1pt borders. Right panel: a top-to-bottom tree diagram. A single Black 1pt outlined rounded rectangle node at top (root). Three Black 1pt outlined rectangles below it, connected by Black 1pt straight edges. Each of those has 2–3 child rectangles below it, also connected by Black 1pt edges. All nodes the same uniform size, all white-filled, demonstrating uniform-size node convention. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same hierarchy shown two ways. Left: treemap with nested rectangles where area encodes value. Right: tree diagram where all nodes are uniform size and edges encode reporting structure.
[O] Two panels horizontal. Equal panel widths. Treemap fills its panel; tree diagram top-down with three levels.
[P] Treemap rectangles Blue, Sky Blue, Bluish Green, Orange, Reddish Purple. Treemap borders Black 1pt. Tree-diagram nodes white-filled with Black 1pt outline. Tree-diagram edges Black 1pt straight.
[E] No category labels, no value annotations, no level labels, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, category names, value annotations, level labels, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 12.2 — Four-Form Reference Grid

**Priority: Critical.** The chapter's central typology. Hold-open reference.

### Block 1 — Illustrae paste block

A 2×2 grid of four equal-sized panels. Top-left panel (treemap): nested rectangles — a large Blue `#0072B2` rectangle in the upper-left, a medium Sky Blue `#56B4E9` rectangle below it, smaller Bluish Green `#009E73` and Orange `#E69F00` rectangles to the right, each subdivided once into 2–3 smaller cells, all bordered by Black `#000000` 1pt thin lines. Top-right panel (sunburst): a circular composition with three concentric rings — innermost ring a single Blue circle (center root), middle ring divided into four wedge segments in Sky Blue / Bluish Green / Orange / Reddish Purple `#CC79A7`, outermost ring divided into 8–10 smaller wedges in mixed luminances of the same hues, all separated by thin Black 1pt radial lines. Bottom-left panel (circle packing): a large outer Sky Blue 1pt-outline circle containing 4 medium Blue filled circles of varying sizes, each containing 1–3 smaller Bluish Green filled circles, demonstrating irregular nesting depth. Bottom-right panel (tree diagram): a left-to-right tree — one root rectangle on the far left, two child rectangles to its right connected by Black 1pt edges, each branching into 2 grandchildren rectangles, all nodes uniform-size white-filled with Black 1pt outline. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Four hierarchy forms in one reference grid: treemap, sunburst, circle packing, tree diagram. Each shows the form's distinctive layout.
[O] 2×2 grid. Equal panel sizes. One form per panel.
[P] Treemap rectangles Blue, Sky Blue, Bluish Green, Orange. Sunburst rings Blue / Sky Blue / Bluish Green / Orange / Reddish Purple. Circle packing Sky Blue outer / Blue mid / Bluish Green inner. Tree diagram white-fill Black 1pt outline nodes and edges.
[E] No form names rendered as graphic text, no labels, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, form names, panel titles, category labels, node labels, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 12.3 — Rectangles vs Circles Alignment

**Priority: Important.** The aligned-edge anchoring argument.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition. Left panel: two Blue `#0072B2` filled rectangles standing on a shared Black `#000000` 1pt horizontal baseline. The left rectangle small (representing 100 sq units); the right rectangle exactly twice the area (representing 200 sq units), achieved by doubling the height while keeping the same width — so the eye anchors on the shared bottom edge and reads the height difference directly. Right panel: two Bluish Green `#009E73` filled circles, the left small (100 sq units) and the right larger (200 sq units area, radius scaled by sqrt(2)). The two circles float without a shared edge, centered roughly on a horizontal midline. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Two pairs of shapes encoding the same area ratio (100 vs 200). Left pair: rectangles on shared baseline (alignment anchor available). Right pair: circles with no shared edge (no alignment anchor).
[O] Two panels horizontal. Rectangles on baseline left; circles floating right.
[P] Rectangles Blue. Circles Bluish Green. Baseline Black 1pt.
[E] No size annotations, no ratio numbers, no Stevens-exponent text, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, size annotations, ratio numbers, exponent text, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 12.4 — Depth Limit Geometry

**Priority: Important.** Why depth limits exist — geometry, not taste.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition. Left panel: a five-level nested treemap. The outermost level is a large rectangle filled pale Sky Blue `#56B4E9` border Black `#000000` 1pt. Inside it, a smaller Blue `#0072B2` filled rectangle (level 2). Inside that, a smaller Bluish Green `#009E73` filled rectangle (level 3). Inside that, an Orange `#E69F00` filled tiny rectangle (level 4). Inside that, a Reddish Purple `#CC79A7` filled sub-pixel-thin sliver (level 5) — clearly too narrow to read. Each level outlined Black 1pt. Right panel: a seven-ring sunburst. From center outward: a small Blue circle (root), then concentric Sky Blue / Bluish Green / Orange rings each about 30px wide, then a much thinner Reddish Purple ring, then an even thinner Black-outlined ring, and finally an outermost Sky Blue ring sliced into 30 hairline wedges so thin they read as a single textured band. Each ring separated by Black 1pt radial lines (more visible on inner rings, blurred on outer). White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Geometric depth limits made visible. Left: 5-level treemap with innermost sliver collapsed sub-pixel-thin. Right: 7-ring sunburst with outermost ring sliced into many narrow wedges.
[O] Two panels horizontal. Treemap fills its panel left. Sunburst centered in its panel right.
[P] Treemap levels Sky Blue / Blue / Bluish Green / Orange / Reddish Purple from outer to inner. Sunburst rings Blue center / Sky Blue / Bluish Green / Orange / Reddish Purple / outer Sky Blue. Borders Black 1pt.
[E] No pixel-arithmetic annotations, no level labels, no segment counts, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, pixel arithmetic, level labels, segment counts, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 12.5 — Slice-and-Dice vs Squarified

**Priority: Important.** The squarification algorithm's perceptual payoff.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition, both panels showing treemaps with twelve nodes of the same set of values. Left panel (slice-and-dice): all rectangles oriented as tall thin vertical columns or wide thin horizontal strips — several rectangles with extreme aspect ratios. Three of them outlined with a thicker Vermillion `#D55E00` 2pt border to flag the elongated outliers; the remainder filled with Blue `#0072B2`, Sky Blue `#56B4E9`, Bluish Green `#009E73`, Orange `#E69F00`, Reddish Purple `#CC79A7` (mixed assignment). Internal boundaries between rectangles Black `#000000` 1pt. Right panel (squarified): same twelve rectangles, same areas, but each near-square in aspect ratio. The same three rectangles (matching by area) again highlighted with the thicker Vermillion 2pt border — but now they look near-square. Remaining rectangles filled with the same palette mapping by area-rank. Internal boundaries Black 1pt. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same 12-node treemap rendered two ways. Left: slice-and-dice producing extreme aspect ratios with three nodes highlighted Vermillion. Right: squarified producing near-square aspect ratios with the same three nodes highlighted, now near-square.
[O] Two panels horizontal. Same panel size. Same set of node areas.
[P] Nodes Blue, Sky Blue, Bluish Green, Orange, Reddish Purple cycling. Highlighted nodes Vermillion 2pt border. Internal boundaries Black 1pt.
[E] No node labels, no aspect-ratio annotations, no algorithm names, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, node labels, aspect-ratio numbers, algorithm names, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 12.6 — Treemap vs Circle Packing for Irregular Depth

**Priority: Important.** Structural honesty when branches differ in depth.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition. Left panel (treemap): five rectangles tiled to fill the panel — all rendered as flat single-level rectangles in Blue `#0072B2`, Sky Blue `#56B4E9`, Bluish Green `#009E73`, Orange `#E69F00`, Reddish Purple `#CC79A7`. None of them subdivided. Internal boundaries Black `#000000` 1pt. Visually uniform: the form forces flat treatment regardless of underlying depth. Right panel (circle packing): one large outer Sky Blue `#56B4E9` 1pt-outline circle containing five medium-sized circles of distinct treatments: one large Blue circle with three nested Bluish Green circles inside it, and inside one of those a single Orange tiny circle (3 levels deep); one medium Reddish Purple circle with two Bluish Green nested circles (2 levels deep); and three smaller bare Blue circles with no children (1 level deep). Each circle has a thin Black 1pt outline. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same irregular-depth dataset. Left: treemap renders all five organizations as flat rectangles, hiding internal depth differences. Right: circle packing preserves the topology — one 3-level branch, one 2-level branch, three 1-level branches.
[O] Two panels horizontal. Treemap fills its panel. Circle packing centered with concentric circles.
[P] Five categories Blue, Sky Blue, Bluish Green, Orange, Reddish Purple. Nested circle outlines Black 1pt. Treemap borders Black 1pt.
[E] No organization labels, no depth annotations, no level labels, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, organization labels, depth annotations, level labels, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## What CAJAL Declines to Architect

- **Key Terms block.** Glossary text.
- **Prompt code blocks.** Code samples, not figures.
- **Ben Shneiderman portrait.** AI Wayback Machine reference image, generated by separate pipeline.

---

## Video Candidate Pass

**FIGURE 12.1 (Same hierarchy, two questions):** STATIC SUFFICIENT.
**FIGURE 12.2 (Four-form reference grid):** STATIC SUFFICIENT.
**FIGURE 12.3 (Rectangles vs circles alignment):** STATIC SUFFICIENT.
**FIGURE 12.4 (Depth limit geometry):** **MILD VIDEO CANDIDATE.** Animating depth increment-by-increment, watching the innermost level shrink to a sub-pixel sliver, would make the geometric inevitability visceral. Static labeled comparison serves the chapter.
**FIGURE 12.5 (Slice-and-dice vs squarified):** STATIC SUFFICIENT.
**FIGURE 12.6 (Treemap vs circle packing):** **STRONG VIDEO CANDIDATE.** Animating the click-to-zoom mechanism in a sunburst or circle-packing chart — clicking a branch, watching it expand to fill the view — is the chapter's recommended interaction pattern for deeper hierarchies. The mechanism-as-learning-target criterion is met. Best implemented as an interactive demo in the companion pantry.

**Video candidates identified: 1 strong + 1 mild.** Recommended: keep all six figures static; treat 12.6 (click-to-zoom) as a candidate for the interactive pantry.

---

## Split-point note

Chapter cross-references Chapter 3 (Stevens' power law on area; channel hierarchy supplying the rectangles-win-on-alignment argument) and Chapter 10 (bubble-chart d3.scaleSqrt area encoding, applied identically here for any size-encoding hierarchy form). Color palette across all six figures should remain consistent: Blue = largest / dominant, Sky Blue = secondary, Bluish Green = tertiary, Orange and Reddish Purple = smaller categories.
