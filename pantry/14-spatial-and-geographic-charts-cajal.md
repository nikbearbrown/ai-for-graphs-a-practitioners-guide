# CAJAL Figure Intelligence — Chapter 14: Spatial and Geographic Charts

**Source:** `chapters/14-spatial-and-geographic-charts.md`
**Mode:** `/scan silent`
**Domain note:** AI+1 practitioner guide / data visualization with D3 and Claude. Chapter walks the geographic family (choropleth, dot density, bubble map, connection/flow map) through the area-size distortion, Cairo's ratio-vs-absolute rule, projection trade-offs, and Snow's 1854 cholera map as the canonical dot-map case. Six author-placed figures.

---

## Density Recommendation

**6 figures, Mechanistic density.** All six are abstract chart-type skeletons demonstrating geographic-specific mechanisms: count-vs-rate switch, four-form reference grid, preattentive area dominance, dot-vs-choropleth resolution, projection effect, and bubble-vs-choropleth severance of area-size distortion.

---

## Zone Map

- **MC:** Area-size distortion as preattentive feature (region size beats color luminance). Cairo's ratio-vs-absolute / "compared with what?" applied geographically. Equal-area projections preserve real area. Bubble map area is independent of region area, severing the distortion. Stevens' law applies to bubble area encoding (d3.scaleSqrt).
- **VG:** US state tile grid. Four-form reference grid (polygon shading, dots in regions, circles at centroids, lines between locations). Mercator vs Equal Earth world projection comparison.
- **PQ:** Wyoming 254,000 km² vs Rhode Island 4,000 km² → 63:1 ratio. Russia 17M km² vs Luxembourg 2,600 km² → 6,500:1 ratio. Greenland Mercator-distorted to look ≈ Africa-sized (actual 14× smaller).

---

## Figure 14.1 — Count vs Rate US State Choropleth

**Priority: Critical.** The chapter's opening argument — same data, different question.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition. Both panels show a stylized US state tile grid — a roughly geographic arrangement of 50 small uniform rectangular tiles representing states (about 8 columns × 7 rows including the Alaska/Hawaii inset). Each tile bordered by thin Black `#000000` 1pt lines. Left panel (absolute count): the large-population states (California, Texas, New York, Florida) shaded with the darkest Blue `#0072B2`, mid-population states shaded mid-luminance Blue, small-population states shaded pale Sky Blue `#56B4E9`, and the smallest (Wyoming, Vermont, Rhode Island, Alaska, Hawaii) palest of all. Right panel (rate): the same tile grid but Texas remains dark Blue, California now lightens significantly (mid-Blue), Wyoming becomes darker than California (mid-to-dark Blue), Rhode Island appears mid-range, and the overall pattern is geographically different — a redistribution of dark and light. Both panels use the same Sky-Blue-to-Blue sequential luminance ramp. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same 50-state tile grid shaded two ways. Left: absolute count encoding — dark in California / Texas / NY / Florida (population tracks). Right: rate encoding — Texas stays dark, California lightens, Wyoming darkens.
[O] Two panels horizontal. Equal tile-grid layouts. Roughly US-shaped tile arrangement with Alaska / Hawaii inset.
[P] Sequential luminance ramp Sky Blue (low) to Blue (high). Tile borders Black 1pt.
[E] No state abbreviations, no value annotations, no legend bar, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, state abbreviations, value annotations, legend bar, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 14.2 — Four Geographic Forms Reference Grid

**Priority: Critical.** The chapter's central typology grid.

### Block 1 — Illustrae paste block

A 2×2 grid of four equal-sized panels. Top-left (choropleth): a simplified map with five irregular polygonal regions shaded in sequential Sky Blue `#56B4E9` to Blue `#0072B2` luminance variation, regions separated by thin Black `#000000` 1pt borders. Top-right (dot density): the same five polygonal regions outlined Black 1pt with white fills, populated by many small Blue `#0072B2` filled dots scattered within each region — denser dots in one region (clear cluster), sparser in others. Bottom-left (bubble map): the same five polygonal regions outlined Black 1pt with white fills, plus one Bluish Green `#009E73` 60% opacity filled circle centered on each region centroid, with notably different circle sizes (one large, two medium, two small). Bottom-right (connection/flow map): the same five polygonal regions outlined Black 1pt with white fills, plus four curved Reddish Purple `#CC79A7` 70% opacity arcs (lines) connecting region centroids, of varying widths to indicate flow magnitudes. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Four geographic forms in one reference grid: choropleth (region shading), dot density (dots in regions), bubble map (circles at centroids), connection/flow map (curved arcs between centroids).
[O] 2×2 grid. Equal panel sizes. Same five-region base map in every panel.
[P] Choropleth Sky Blue to Blue luminance ramp. Dot density Blue dots on white-fill regions. Bubble map Bluish Green circles. Connection arcs Reddish Purple. Region borders Black 1pt.
[E] No form names rendered as graphic, no region labels, no value annotations, no legend, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, form names, region labels, value annotations, legend, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 14.3 — Uniform-Luminance World Map

**Priority: Important.** Area is preattentive. Color does not win.

### Block 1 — Illustrae paste block

A simplified world map silhouette in Equal Earth projection — the recognizable bulges of major continents drawn as filled polygons. Every country filled with the identical mid-range Sky Blue `#56B4E9` (no luminance variation across the entire map). Country borders thin Black `#000000` 1pt. Russia, Canada, Australia, Brazil, the United States, and China visibly large landmasses dominating the visual field despite identical fill. Smaller nations (Luxembourg, Switzerland, Belgium) barely visible as hairline polygons; Greenland a small island near the top. Two small Black 1pt outlined circular markers without graphic text positioned at: one over Greenland (small-under-Equal-Earth callout), one over Luxembourg (invisible callout). Each marker connected to its referenced location by a thin Black 1pt leader line. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] World map in Equal Earth projection. Every country filled with identical mid-Sky-Blue luminance. Two small callout markers — one over Greenland, one over Luxembourg.
[O] Equal Earth world projection. Continents in their familiar positions. Map centered on the panel.
[P] All countries Sky Blue uniform fill. Country borders Black 1pt thin. Callout markers Black 1pt outlined circles, white-fill. Leader lines Black 1pt.
[E] No country labels, no callout text, no value legend, no projection name, no chart title, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, country names, callout text, value legend, projection name, chart title, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 14.4 — Parish Choropleth vs Snow Dot Map

**Priority: Important.** Resolution as the determining variable.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition representing the same neighborhood-scale dataset. Left panel (parish-level choropleth): a coarse 3×3 grid of irregular polygonal parish regions, each filled with a mid-range Sky Blue `#56B4E9` to Blue `#0072B2` luminance corresponding to its parish-total death count. Parish boundaries Black `#000000` 1pt thicker (1.5pt) lines. No internal detail; the dense cluster is dissolved into a single parish's moderate fill. Right panel (dot map): the same parish boundaries drawn but thinner Black 1pt and with white fill; superimposed are about 80 small Blue `#0072B2` filled dots representing individual deaths. The dots are sparsely distributed across most of the map but tightly clustered around a specific central point — a visible dense cluster with one Vermillion `#D55E00` filled small circle marker at the cluster's center indicating the pump location. Background streets implied by a few faint Black 0.5pt thin lines forming a coarse grid pattern on both panels. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same 1854 Soho-style dataset shown two ways. Left: parish-level choropleth aggregates the cluster into a moderate parish total. Right: dot map reveals dense cluster around a marked pump location.
[O] Two panels horizontal. Same parish grid in both. Left fills parishes with luminance. Right overlays dots on white-filled parishes.
[P] Choropleth fills Sky Blue to Blue luminance ramp. Dot map dots Blue. Pump marker Vermillion. Parish borders Black 1pt (right) / 1.5pt (left). Street hints Black 0.5pt.
[E] No parish labels, no street names, no death-count annotations, no pump label, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, parish labels, street names, death-count annotations, pump label, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 14.5 — Mercator vs Equal Earth

**Priority: Critical.** The projection-choice effect on choropleth honesty.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition. Both panels show identical Sky-Blue-to-Blue luminance encoding across countries. Left panel (Mercator): the world projected with Mercator's high-latitude exaggeration. Greenland enormous in the upper region, appearing comparable in size to the African continent. Russia stretches across the top of the panel in dominant scale. Antarctica an exaggerated stretched band along the bottom. Africa visually smaller relative to Greenland and Russia than reality. Each country filled with its luminance and outlined Black `#000000` 1pt thin. Right panel (Equal Earth): the same world projected with the Equal Earth projection. Greenland now visibly a small island. Russia large but proportional. Africa clearly the larger landmass relative to Greenland. Antarctica reasonably proportioned along the bottom. Same Sky-Blue-to-Blue luminance per country and Black 1pt borders. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same world choropleth in two projections. Left: Mercator — Greenland looks ≈ Africa-sized, Russia dominates. Right: Equal Earth — Africa visibly larger than Greenland, Russia proportional.
[O] Two panels horizontal. Equal panel widths. World projected per the named projection in each.
[P] Country fills Sky Blue to Blue luminance ramp (same data across both). Country borders Black 1pt.
[E] No country labels, no projection names rendered as graphic, no legend, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, country names, projection names, legend, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 14.6 — Choropleth vs Bubble Map (Severing the Distortion)

**Priority: Critical.** The form-switch that severs the area-size distortion.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition. Both panels show the same Equal Earth world projection of country polygons. Left panel (choropleth, absolute count): countries filled with sequential Sky Blue `#56B4E9` to Blue `#0072B2` luminance. Russia, Canada, and Australia visually dominant in the frame because of their large land areas, despite low fill values (pale Sky Blue). Several smaller nations (e.g., Syria, Afghanistan, South Sudan, Turkey, Iran, Colombia) shaded dark Blue but visually muted by their small footprint. Black `#000000` 1pt country borders. Right panel (bubble map, absolute count): the same country polygons outlined Black 1pt with white fills. Centered on each country's centroid, a Bluish Green `#009E73` 70% opacity filled circle whose area is proportional to the value. Large bubbles over Turkey, Iran, Colombia, Syria, Afghanistan. Very small or invisible bubbles over Russia, Canada, Australia. Circle sizes computed via d3.scaleSqrt. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same Equal Earth absolute-count refugee-style dataset shown two ways. Left: choropleth — large low-value countries dominate visually. Right: bubble map — bubble area encodes the count, severing the area-size distortion; large bubbles over high-count countries (Turkey / Iran / Colombia / Syria / Afghanistan).
[O] Two panels horizontal. Same world projection. Left: country fills. Right: bubbles at centroids over outlined countries.
[P] Choropleth Sky Blue to Blue luminance. Bubble map countries white-fill Black 1pt outline. Bubbles Bluish Green 70% opacity. Bubble areas scaled via sqrt.
[E] No country labels, no value annotations, no legend, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, country names, value annotations, legend, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## What CAJAL Declines to Architect

- **Key Terms block.** Glossary text.
- **Prompt code blocks.** Code samples, not figures.
- **John Snow portrait.** AI Wayback Machine reference image, generated by separate pipeline.

---

## Video Candidate Pass

**FIGURE 14.1 (Count vs rate choropleth):** **MILD VIDEO CANDIDATE.** Animating the toggle between absolute and rate encoding — watching California lighten and Wyoming darken — would dramatize the chapter's opening argument. Static side-by-side serves the printed chapter.
**FIGURE 14.2 (Four geographic forms grid):** STATIC SUFFICIENT.
**FIGURE 14.3 (Uniform-luminance world):** STATIC SUFFICIENT.
**FIGURE 14.4 (Parish choropleth vs dot map):** STATIC SUFFICIENT.
**FIGURE 14.5 (Mercator vs Equal Earth):** **MILD VIDEO CANDIDATE.** Morphing from Mercator to Equal Earth — watching Greenland shrink and Africa enlarge — would viscerally teach the projection effect. Static comparison is sufficient.
**FIGURE 14.6 (Choropleth vs bubble map):** STATIC SUFFICIENT.

**Video candidates identified: 0 strong + 2 mild.** Recommended: keep all six static; treat 14.1 (rate-toggle) as the natural interactive demo for the companion pantry — it doubles as Exercise 14.6's deliverable.

---

## Split-point note

Chapter cross-references Chapter 3 (Stevens' power law on area for bubble maps; preattentive area as visual processing fact), Chapter 4 (Cairo's "compared with what?" — the ratio-vs-absolute rule is the geographic application), and Chapter 10 (bubble-chart d3.scaleSqrt rule reused identically for bubble maps in Fig 14.6). Color convention across figures: Sky-Blue-to-Blue sequential ramp = data luminance encoding; Bluish Green = bubble area magnitude; Vermillion = highlight marker (pump location); Reddish Purple = flow lines. Keep this consistent across all six figures.
