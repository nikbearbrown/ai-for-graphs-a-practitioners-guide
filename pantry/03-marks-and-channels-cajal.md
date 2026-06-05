# CAJAL Figure Intelligence — Chapter 03: Marks and Channels

**Source:** `chapters/03-marks-and-channels.md`
**Mode:** `/scan silent`
**Domain note:** AI+1 practitioner guide / data visualization with D3 and Claude. META-book about graphs. This chapter is the perceptual-foundations chapter — Bertin's grammar, Cleveland & McGill's ranking, Stevens' power law, Munzner's expressiveness / effectiveness principles. Five author-placed figures (Figs 3.1–3.5). All five are abstract perceptual / taxonomic diagrams, NOT chart artifacts that depict particular datasets. CAJAL renders the architecture; the example scatterplots and bubble charts are perceptual demonstrations, not data deliverables.

---

## Density Recommendation

**5 figures, Mechanistic density.** This is the perceptual grammar of the book — every later chapter depends on the channel ranking and the expressiveness / effectiveness cut. All five placed figures earn their place. The Bertin marks-and-channels foundation is the key figure (Fig 3.5 / Fig 3.2 jointly).

---

## Zone Map

- **MC:** Position-vs-luminance perceptual gap on identical data (Fig 3.1). Stevens' power law — radius-vs-area distortion mechanism (Fig 3.3). Nightingale's polar-area perceptual amplification, radius-linear vs area-corrected (Fig 3.4).
- **VG:** The four mark types — point, line, area, glyph (Fig 3.2). The magnitude-vs-identity channel taxonomy with expressiveness / effectiveness principles (Fig 3.5).
- **PQ:** Stevens' exponents — length a≈1.0, area a≈0.7, luminance a≈0.33. Bubble-chart numbers: data 2×, area 4×, perceived 2.6× under radius scaling. These live inside Fig 3.3.

---

## Figure 3.1 — Position (rank 1) vs. luminance (rank 6)

**Priority: Critical.** Opening puzzle. Same data, two channels, one chart works, one doesn't.

### Block 1 — Illustrae paste block

A two-panel side-by-side scatter composition. Left panel: a standard scatterplot frame with Black `#000000` 1pt axes. Approximately 50 small Blue `#0072B2` filled circles arranged in a positively-correlated cloud — x-axis position (GDP per capita) and y-axis position (life expectancy) both vary. The high-y cluster in the upper right is visually obvious. Right panel: an identical Black 1pt axis frame, x-axis the same (GDP per capita), but every dot now collapsed onto a single horizontal line at the vertical midpoint. The same 50 dots are now Sky Blue `#56B4E9` filled at the low-luminance end and Blue `#0072B2` filled at the high-luminance end, with a sequential luminance gradient between them encoding life expectancy. A small Vermillion `#D55E00` filled badge in the corner of each panel marks the channel rank — left panel "1" (position), right panel "6" (luminance), referencing Cleveland & McGill. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Two scatterplots of identical data. Left: position-encoded life expectancy (rank 1). Right: luminance-encoded life expectancy collapsed onto a single horizontal line (rank 6). Channel rank badges in each panel.
[O] Side by side. Identical x-axes. Left panel uses full 2D position; right collapses to a single horizontal row.
[P] Left scatter dots Blue. Right scatter sequential Sky Blue → Blue luminance. Axes Black 1pt. Channel-rank badges Vermillion.
[E] No specific country labels, no axis numbers, no chart titles, no legend graphics, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, country names, axis numbers, chart titles, legends rendered as graphics, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 3.2 — The four mark types

**Priority: Important.** Vocabulary anchor. Point, line, area, glyph in one reference panel.

### Block 1 — Illustrae paste block

A four-panel grid composition (2x2). Top-left panel: point mark — a small Black `#000000` 1pt axis frame containing six Blue `#0072B2` filled small circles scattered across the field. Top-right panel: line mark — a Black 1pt axis frame containing a single Sky Blue `#56B4E9` 2pt connected polyline with six small Blue filled circles at vertices. Bottom-left panel: area mark — a Black 1pt axis frame containing one Bluish Green `#009E73` filled rectangle (a single bar). Bottom-right panel: glyph mark — a Black 1pt axis frame containing a single composite mark, a Reddish Purple `#CC79A7` filled small rectangle (candlestick body) with thin Black `#000000` 1pt vertical line extending above and below (wicks). Each panel has a small Vermillion `#D55E00` filled corner badge with the mark-type ordinal (1, 2, 3, 4). White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Four panels showing the four mark types — point, line, area, glyph — one canonical example each. Numbered ordinal badges in each panel.
[O] 2x2 grid. Equal-sized panels with thin Black axis frames. Single mark exemplar per panel.
[P] Point-mark dots Blue. Line mark Sky Blue with Blue vertices. Area mark Bluish Green. Glyph mark Reddish Purple with Black wicks. Panel frames Black 1pt. Ordinal badges Vermillion.
[E] No mark-type labels rendered, no axis numbers, no data values, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, mark-type names rendered as graphics, axis numbers, data values, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 3.3 — Radius-vs-area distortion in bubble encoding

**Priority: Critical.** Stevens' power law made visible. The chapter's strongest mechanism diagram.

### Block 1 — Illustrae paste block

A two-pair composition arranged in a 2x2 grid. Top-left: a small Blue `#0072B2` filled circle (the reference bubble). Top-right: a larger Blue `#0072B2` filled circle, twice the radius — the radius-linear encoding for a data value that has doubled. The visual area is four times the reference. Bottom-left: the same small reference bubble in Sky Blue `#56B4E9` filled. Bottom-right: a Sky Blue filled circle whose *area* is exactly twice the reference, so its radius is √2 ≈ 1.41× the reference. To the right of each pair, three small stacked Vermillion `#D55E00` filled rectangles of graduated width acting as numeric magnitude marks (post-typography labels: data ratio, area ratio, perceived ratio) — top pair shows mismatched widths (data 2×, area 4×, perceived 2.6×); bottom pair shows aligned widths (data 2×, area 2×, perceived ~1.5×). A thin Bluish Green `#009E73` 1pt horizontal rule between the two pairs visually separates the radius-linear (wrong) from the area-linear (less wrong). White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Two bubble-encoding pairs. Top pair: radius-linear scaling — data 2× produces area 4× and perceived 2.6×. Bottom pair: area-linear scaling — data 2× produces area 2× and perceived ~1.5×. Three magnitude marks per pair show the three ratios.
[O] 2x2 grid of circle pairs. Magnitude-mark stacks to the right of each pair. Horizontal separator rule between top and bottom pairs.
[P] Top (radius-linear) circles Blue. Bottom (area-linear) circles Sky Blue. Magnitude-mark stacks Vermillion. Separator rule Bluish Green.
[E] No exponent equations, no specific Stevens-law text, no axis lines, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, equations rendered as graphics, Stevens-law formula text, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 3.4 — Nightingale's rose, radius-linear vs. area-corrected

**Priority: Important.** A historical mechanism case — the same chart rendered twice, with and without the perceptual amplification.

### Block 1 — Illustrae paste block

A two-panel side-by-side polar-area composition. Each panel is a circle subdivided into 12 wedges, one per month, arranged clockwise. Left panel (radius-linear, the published form): wedge radii vary proportionally to the underlying value. Three nested wedge layers per month, in three different palette assignments — outer (preventable disease) Vermillion `#D55E00` filled, middle (wounds) Reddish Purple `#CC79A7` filled, inner (other) Sky Blue `#56B4E9` filled. The winter-month outer wedges (Jan, Feb, March, Nov, Dec) reach far outward, dwarfing the others. Right panel (area-corrected): same data but with each wedge's radius now proportional to the square root of the value, so the visible *area* is honest. Same three palette assignments. The winter-month outer wedges still dominate, but less dramatically — the perceptual amplification has been removed. Both panels framed by a thin Black `#000000` 1pt circle. Small Bluish Green `#009E73` filled corner badge per panel (left: "r ∝ v" — radius-linear; right: "r ∝ √v" — area-honest), rendered as a colored shape only (no equation text). White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Two polar-area roses of identical data. Left: radius-linear (published, perceptually amplified). Right: area-corrected (radius proportional to √value, perceptually honest). Three nested cause-of-death layers per panel.
[O] Side by side. Each panel a 12-wedge clockwise polar arrangement. Three nested layers per wedge.
[P] Preventable-disease layer Vermillion. Wounds layer Reddish Purple. Other-causes layer Sky Blue. Panel frame Black 1pt. Corner badges Bluish Green.
[E] No month names rendered as graphics, no equation text, no annotations, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, month names, equation text, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 3.5 — Magnitude vs. identity channels

**Priority: Critical.** The Munzner cut. Position / length / area / luminance on the left; hue / shape / texture on the right. Foundation reference for the rest of the book.

### Block 1 — Illustrae paste block

A two-column taxonomy composition divided by a central vertical Black `#000000` 1pt line. Left column header: a Blue `#0072B2` filled rectangle (magnitude channels). Inside the left column, four small panels stacked vertically — each containing one channel exemplar. Panel 1 (Position): a small frame with two Sky Blue `#56B4E9` filled dots at different y-positions. Panel 2 (Length): two Bluish Green `#009E73` filled rectangles of different lengths from a shared baseline. Panel 3 (Area): two Bluish Green filled circles of different areas. Panel 4 (Luminance): two Sky Blue filled squares, one at 30% opacity and one at full opacity. Right column header: a Vermillion `#D55E00` filled rectangle (identity channels). Inside the right column, three small panels stacked vertically. Panel 1 (Hue): three small filled circles in three distinct hues — Orange `#E69F00`, Reddish Purple `#CC79A7`, Bluish Green `#009E73` — same size. Panel 2 (Shape): three Orange filled marks of different shapes (circle, square, triangle), same size. Panel 3 (Texture): three Orange filled rectangles with different fill textures (solid, diagonal-line hatched, dot-stippled), same size. At the bottom of each column, a thin Reddish Purple `#CC79A7` 1pt horizontal rule with a small Bluish Green filled diamond marker — left rule represents the expressiveness principle (quantity belongs here); right rule represents the same principle for categorical attributes. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Two-column channel taxonomy. Left (magnitude): position, length, area, luminance. Right (identity): hue, shape, texture. Bottom rules carry the expressiveness principle marker per column. Central boundary line.
[O] Two columns separated by a vertical boundary. Four stacked panels in the left column; three in the right. Bottom principle rule per column.
[P] Magnitude header Blue. Magnitude exemplars Sky Blue / Bluish Green / Blue depending on channel. Identity header Vermillion. Identity exemplars Orange / Reddish Purple / Bluish Green (the hue triad). Boundary Black 1pt. Principle rule Reddish Purple. Principle marker Bluish Green.
[E] No principle text rendered as graphics, no channel names rendered, no Cleveland-McGill rank numbers, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, channel names rendered as graphics, principle text, rank numbers, equations, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## What CAJAL Declines to Architect

- **The Cleveland & McGill ranking table (lines 87–95).** Ranked numbered list with Stevens' exponents. Stays a table — the rank ordering is typographic, not pictorial.
- **The full Stevens' power-law equation Ψ = k · I^a.** Equation typography belongs in the prose. The mechanism diagram (Fig 3.3) carries the visible consequence.
- **John Snow's cholera map, Minard's Napoleon flow map, and the original Nightingale published rose.** Historical artifacts mentioned in worked-examples prose. CAJAL renders the abstract mechanism behind them (Fig 3.4 for Nightingale's distortion mechanism); the historical images themselves are not CAJAL figures and may be licensed reproductions if the book uses them.
- **The box-plot specification code block (lines 171–184).** Prose specification, not a figure.
- **Jock Mackinlay portrait (line 360).** Photographic asset, not a CAJAL figure.

---

## Video Candidate Pass

**FIGURE 3.1 (Position vs luminance):** STATIC SUFFICIENT.
**FIGURE 3.2 (Four mark types):** STATIC SUFFICIENT.
**FIGURE 3.3 (Radius-vs-area distortion):** **MILD VIDEO CANDIDATE.** Mechanism-as-learning-target — animation could show data value rising while the radius-linear bubble grows quartically and the area-linear bubble grows linearly, with all three magnitude bars (data, area, perceived) tracking in sync. But the static still teaches the mechanism in one glance.
**FIGURE 3.4 (Nightingale rose):** **MILD VIDEO CANDIDATE.** A morph between radius-linear and area-corrected versions would viscerally show how much of the chart's drama is perceptual distortion. Risk: makes the original historical artifact look like a mistake when Nightingale's rhetorical choice was deliberate.
**FIGURE 3.5 (Magnitude vs identity channels):** STATIC SUFFICIENT. Taxonomy.

**Video candidates identified: 2 mild.** Recommended: prefer static for the first edition. If an interactive companion ships, the Stevens' law bubble morph is the highest-leverage interactive moment in the chapter.

---

## Split-point note

The semantic palette established in Chapter 02 (Blue = author/code, Sky Blue = supporting, Vermillion = failure / risk / amplification, Bluish Green = verified / honest, Orange = identity-channel exemplars, Reddish Purple = human-in-the-loop / principle marker) continues here. Specifically, Fig 3.3 and Fig 3.4 use Vermillion for the perceptual distortion (the failure surface) and Bluish Green for the area-honest correction — consistent with Chapter 02's use of Vermillion for failure modes and Bluish Green for passing the verification stack. Chapter 04 will inherit these assignments for the chart-selection decision tree.
