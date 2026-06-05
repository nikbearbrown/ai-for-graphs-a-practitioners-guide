# CAJAL Figure Intelligence — Chapter 10: Relationship and Correlation Charts

**Source:** `chapters/10-relationship-and-correlation-charts.md`
**Mode:** `/scan silent`
**Domain note:** AI+1 practitioner guide / data visualization with D3 and Claude. Chapter walks the relationship-chart family (scatterplot, bubble, heatmap, parallel coordinates, connected scatterplot) through Cleveland & McGill channel theory, Stevens' power law on area, and Cairo's correlation-is-not-causation annotation. Six author-placed figures.

---

## Density Recommendation

**6 figures, Concept-density.** All six are abstract chart-type skeletons demonstrating perceptual mechanisms (caveat-vs-no-caveat scatterplot, four-cloud r-ambiguity, overplotting strategies, radius-vs-area bubbles, sort-order heatmaps, axis-order parallel coordinates). Each earns its place by carrying a perceptual or ethical argument the prose cannot make alone.

---

## Zone Map

- **MC:** Cleveland & McGill channel hierarchy (position > length > angle > area > luminance > hue). Stevens' power law for bubble area perception. Cairo's correlation-is-not-causation as ethical annotation requirement. Munzner's axis-order-dependence problem.
- **VG:** Scatterplot as canonical two-position-channel form. Overplotting failure modes and three mitigations (alpha, jitter, hexbin). Bubble radius-vs-area encoding distortion. Heatmap sort order revealing/hiding clusters.
- **PQ:** r = 0.79 example. r ≈ 0.7 fits all four cloud shapes. 50,000-point overplotting threshold. Six-variable parallel coordinates → 720 orderings (6!). Stevens' exponent ≈ 0.7.

---

## Figure 10.1 — Caveat vs No-Caveat Scatterplot

**Priority: Critical.** Cairo's ethical frame made visible. The chapter's opening argument.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition. Both panels show identical scatterplots: an upward-sloping cloud of small Blue `#0072B2` filled circles, roughly 80 points, distributed in a band around a Black `#000000` 1pt diagonal OLS trend line running lower-left to upper-right. Both panels have the same axes — x-axis horizontal Black 1pt baseline, y-axis vertical Black 1pt baseline, no tick labels rendered as text. Left panel: bare cloud and trend line only. Right panel: identical content plus a Vermillion `#D55E00` 1pt outlined rectangular callout box positioned near the trend line, filled with light Vermillion 15% opacity, holding empty space (annotation post-typography). A thin Vermillion 1pt leader line connects the callout to the trend line. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Identical scatterplots side by side. Left: cloud + trend line only. Right: same plus visible Vermillion callout box near the trend line indicating the correlation-is-not-causation annotation position.
[O] Two panels horizontal. Same axes, same cloud, same trend line. Callout box visible only on the right.
[P] Points Blue. Trend line Black 1pt. Axes Black 1pt. Callout outline Vermillion 1pt with 15% Vermillion fill. Leader line Vermillion 1pt.
[E] No text labels, no r-value rendered as graphic, no tick labels, no specific dataset, no axis titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, r-value rendered as graphic, tick mark numbers, axis titles, dataset names, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 10.2 — Four Clouds, Same r

**Priority: Critical.** The summary-statistic-vs-cloud-shape lesson. Anscombe-style argument made visual.

### Block 1 — Illustrae paste block

A 2×2 grid of small scatterplot panels, each with the same Black `#000000` 1pt axes (no tick labels). Top-left: a linear cloud of small Blue `#0072B2` filled circles forming a clean band along a diagonal Black 1pt OLS trend line. Top-right: a curved (quadratic) cloud of Blue circles forming a parabolic shape with the same diagonal trend line cutting through it. Bottom-left: a fan-shaped heteroscedastic cloud — Blue circles tightly grouped at low x, spreading wider toward high x, with the same trend line. Bottom-right: a tight Blue cluster at the lower-left plus a single Vermillion `#D55E00` filled circle far in the upper-right (outlier) with the trend line pulled toward it. Each panel's trend line and axes identical in style. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Four small scatterplots — linear, curved, fan-shaped, outlier-dominated — all sharing the same diagonal OLS trend line, demonstrating that one summary statistic fits visually distinct clouds.
[O] 2×2 grid. Equal panel sizes. Same axis scale across all four.
[P] Cloud points Blue. Outlier point Vermillion. Trend line Black 1pt. Axes Black 1pt.
[E] No tick labels, no r-value text, no panel titles, no specific dataset, no axis titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, r-value rendered as graphic, tick numbers, panel titles, axis titles, dataset names, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 10.3 — Overplotting Strategies

**Priority: Important.** Four-panel comparison of mitigation strategies for dense scatterplots.

### Block 1 — Illustrae paste block

A 2×2 grid of small panels, each showing the same dense scatter. Top-left: a solid Black `#000000` filled blob occupying the center-diagonal of the panel — overplotting failure, individual points invisible. Top-right: the same diagonal cloud but rendered as many small Blue `#0072B2` circles at 15% opacity, with darker accumulated regions visible toward the center and individual points visible on the periphery. Bottom-left: a grid-like scatter where Blue points are placed at slightly jittered positions in discrete clusters — each cluster a small group of overlapping circles indicating a count at that grid cell. Bottom-right: a hexagonal binning view — Sky Blue `#56B4E9` to Blue `#0072B2` filled hexagons tiling the diagonal cloud region, lighter hexagons at the edges, darker hexagons at the center, all without point marks. Each panel framed by Black 1pt axes. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Four overplotting strategies on the same cloud: full opacity black mass, alpha transparency revealing cloud shape, jittered discrete grid, hexagonal 2D binning.
[O] 2×2 grid. Equal panel sizes. Same underlying distribution in each.
[P] Black mass for failure panel. Blue points for alpha and jitter. Sky-Blue-to-Blue luminance ramp for hexbin. Axes Black 1pt.
[E] No tick labels, no panel titles, no axis titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, tick numbers, panel titles, axis titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 10.4 — Radius vs Area Bubble Encoding

**Priority: Critical.** Stevens' power law made visible. The d3.scaleSqrt argument.

### Block 1 — Illustrae paste block

A horizontal composition divided into two halves. Left half: two Blue `#0072B2` filled circles representing radius-linear encoding — a small circle on the left and a much larger circle on the right whose radius is twice the small one's. The large circle's area is four times the small one's. Both circles aligned on a shared Black `#000000` 1pt baseline. Right half: two Bluish Green `#009E73` filled circles representing area-linear encoding — a small circle on the left and a moderately larger circle on the right whose area is exactly twice the small one's (radius scaled by sqrt(2) ≈ 1.41). Both aligned on the same baseline. A vertical Black 1pt dashed divider separates the two halves. Each pair shares the small-circle size. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Two pairs of circles. Left pair: radius doubled, area quadrupled (Blue, radius-linear). Right pair: area doubled, radius scaled by sqrt(2) (Bluish Green, area-linear). Both pairs share the same small-circle reference.
[O] Two halves side by side. Each half shows small-circle then larger-circle on shared baseline. Vertical dashed divider.
[P] Radius-linear pair Blue. Area-linear pair Bluish Green. Baseline Black 1pt. Divider Black 1pt dashed.
[E] No size annotations, no ratio numbers rendered, no panel titles, no axis titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, ratio numbers, size annotations, scale legends, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 10.5 — Heatmap Sort Order

**Priority: Important.** Sort order as design decision, not default.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition. Both panels show an 8×6 grid of square cells (8 rows × 6 columns) filled with luminance variations from very pale Sky Blue `#56B4E9` (low) through mid Blue to dark Blue `#0072B2` (high). Left panel: cells in apparently random order — no visible pattern, scattered light and dark cells distributed throughout the grid. Right panel: same cell values but rearranged so the darkest cells cluster in the upper-left corner of the grid, gradually lightening toward the lower-right — a clear diagonal gradient of luminance revealing a sorted cluster. Each grid bordered by Black `#000000` 1pt thin lines between cells. No row or column labels. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same 8×6 heatmap data shown two ways. Left: unsorted, no pattern. Right: sorted by row max and column mean, dark cluster surfaces in upper-left.
[O] Two panels horizontal. Equal grid sizes. Identical cell counts.
[P] Cell luminance ramp from pale Sky Blue (low) to dark Blue (high). Cell borders Black 1pt thin.
[E] No row labels, no column labels, no legend bar, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, row labels, column labels, legend bar, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 10.6 — Parallel Coordinates Axis Order

**Priority: Important.** Munzner's axis-order-dependence problem made concrete.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition. Both panels contain six vertical Black `#000000` 1pt axes evenly spaced left to right, each axis as a thin vertical line. Connecting the axes are about 60 thin Blue `#0072B2` polylines at 25% opacity, each polyline crossing all six axes with one point on each. Left panel: polylines form a dense, tangled mass with many crossings between axes — no visible pattern, lines going in all directions between adjacent axes. Right panel: the same number of polylines but now they resolve into two clearly visible clusters — an upper band of polylines staying near the top of each axis, and a lower band of polylines staying near the bottom, with minimal crossing between bands. Each axis a clean vertical Black 1pt line. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same 200-observation, 6-variable parallel coordinates dataset shown two ways. Left: alphabetical axis order produces tangled mass. Right: correlated pairs adjacent produces two clean cluster bands.
[O] Two panels horizontal. Six vertical axes per panel, evenly spaced.
[P] Axes Black 1pt. Polylines Blue 25% opacity 1pt.
[E] No axis labels, no tick labels, no variable names, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, axis labels, variable names, tick numbers, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## What CAJAL Declines to Architect

- **Channel hierarchy table (Cleveland & McGill ranking).** Typography reference; belongs in Chapter 3.
- **Key Terms block.** Glossary text.
- **Prompt code blocks.** Code samples, not figures.
- **Francis Galton portrait.** AI Wayback Machine reference image, generated by separate pipeline.

---

## Video Candidate Pass

**FIGURE 10.1 (Caveat vs no-caveat):** STATIC SUFFICIENT.
**FIGURE 10.2 (Four clouds, same r):** STATIC SUFFICIENT.
**FIGURE 10.3 (Overplotting strategies):** STATIC SUFFICIENT.
**FIGURE 10.4 (Radius vs area):** **MILD VIDEO CANDIDATE.** An animation that morphs the radius-linear pair into the area-linear pair as the encoding rule changes could dramatize Stevens' power law for live presentations. Static is sufficient for the printed/web textbook.
**FIGURE 10.5 (Heatmap sort order):** **MILD VIDEO CANDIDATE.** An animation rearranging cells from unsorted to sorted reveals the cluster appearing. Static comparison serves the chapter.
**FIGURE 10.6 (Parallel coordinates axis order):** **MILD VIDEO CANDIDATE.** Drag-to-reorder interactive demo would teach the chapter's argument directly. The chapter already prescribes brushing interaction for working charts.

**Video candidates identified: 0 strong + 3 mild.** Recommended: keep all six static for the chapter; treat 10.5 and 10.6 as candidates for the companion interactive pantry.

---

## Split-point note

Chapter cross-references Chapter 3 (channel hierarchy, Stevens' power law) and Chapter 4 (chart selection, Cairo's ethical frame). Bubble-chart geometry (Fig 10.4) reappears in Chapter 14 for proportional-symbol maps; keep the radius/area visual convention identical across chapters.
