# CAJAL Figure Intelligence — Chapter 7: Comparison Charts

**Source:** `chapters/07-comparison-charts.md`
**Mode:** `/scan silent`
**Domain note:** AI+1 practitioner guide / data visualization with D3 and Claude. Bar chart family chapter — zero-baseline rule grounded in proportional ink, Cleveland-McGill channel ranking, multiset/stacked/small-multiples decision, radial-vs-linear, design-decisions walk-through. Seven author-placed figures, all MINIMAL abstract chart skeletons showing structural form — not specific datasets.

---

## Density Recommendation

**7 figures, Mechanism + structure density.** The chapter is a long systematic argument about a single chart family. Each figure isolates one structural decision: baseline, channel ranking, defenders' alternatives, orientation, sub-category form, radial vs linear, design decisions.

---

## Zone Map

- **MC:** Zero-baseline rule from Stevens' power law and proportional ink. Channel ranking (position > length > angle > area > color). Multiset / stacked / small-multiples maps to within-category / total / cross-sub-category question.
- **VG:** Bar-chart skeletons in their structural variants. Orientation choice. Radial-vs-linear contrast.
- **PQ:** No tables in this chapter — all argument is prose plus the figures.

---

## Figure 7.1 — Zero Baseline vs Truncated Baseline

**Priority: Critical.** The chapter's opening evidence and the rule's mechanism.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition on white. Both panels show the same eight vertical bar skeletons — eight Sky Blue `#56B4E9` to Blue `#0072B2` filled rectangles arranged left-to-right in a luminance ramp (darker = taller). Left panel: a Black `#000000` 1pt horizontal baseline drawn at the bottom of the panel (zero baseline). The bar heights span from short to tall in correct proportion. Right panel: a Black 1pt baseline drawn partway up the panel (truncated baseline marked by a thin Vermillion `#D55E00` 1pt horizontal indicator line at the panel's true zero, well below the visible baseline). The same eight bars now appear stretched: the shortest bar is a tiny sliver; the tallest looks dramatically larger than the left-panel version. A small Vermillion `#D55E00` filled triangle marker in the upper right of the right panel signals distortion. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same eight-bar skeleton, two baselines. Left = zero baseline (honest). Right = truncated baseline (distorted), with a thin true-zero reference line below the visible baseline.
[O] Two equal panels side by side.
[P] Bars Sky Blue to Blue luminance ramp. Honest baseline Black. Truncated baseline Black. True-zero reference Vermillion 1pt. Distortion marker Vermillion triangle.
[E] No axis tick text, no domain names, no numerical values, no chart titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, axis tick numbers, domain names rendered as graphics, score values, chart titles, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 7.2 — Perceptual Channel Accuracy Ranking

**Priority: Important.** The Cleveland-McGill ranking visualized.

### Block 1 — Illustrae paste block

A vertical ladder composition on white. Six rungs arranged top-to-bottom, each a horizontal Sky Blue `#56B4E9` filled rounded rectangle of decreasing width — top rung widest (most accurate channel: position along common scale); bottom rung narrowest (least accurate: color luminance / hue). Each rung is separated by a thin Black `#000000` 1pt horizontal rule. To the left of the ladder, a vertical Blue `#0072B2` 1pt arrow pointing downward indicates the accuracy gradient. To the right of the top rung, a small Bluish Green `#009E73` filled circle highlights the bar-chart channel position. A small Vermillion `#D55E00` 1pt curved arrow points from the top rung downward, indicating "truncation drops the chart out of this channel." White background, flat vector, single-column 89mm.

### Block 2 — Full SCOPE prompt

[S] Single-column 89mm, vector, white background.
[C] Six-rung accuracy ladder, top to bottom. Top rung widest (best channel) highlighted as the bar-chart channel. Side arrow shows the truncation cost.
[O] Vertical stack of progressively narrower bars. Accuracy gradient arrow on the left.
[P] Rungs Sky Blue. Gradient arrow Blue. Bar-chart-channel marker Bluish Green. Truncation cost arrow Vermillion. Separators Black.
[E] No channel names rendered as text, no Cleveland-McGill citation, no rank numerals, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, channel names rendered as graphics, citation text, rank numerals, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 7.3 — Three Responses to Nearly-Identical Values

**Priority: Important.** Three-panel structural alternatives to truncated bars.

### Block 1 — Illustrae paste block

A three-panel horizontal composition on white. Each panel shows three values close in magnitude. Left panel (wrong): three Vermillion `#D55E00` filled vertical bars with a visibly truncated Black `#000000` 1pt baseline well above the panel bottom, bars appearing dramatically different in height. Center panel (right alternative #1): three Sky Blue `#56B4E9` filled small circles (dot plot) plotted against a Black 1pt vertical axis line on the left, axis range zoomed to show small variation honestly. Right panel (right alternative #2): three Bluish Green `#009E73` filled small horizontal bars extending right from a central Black 1pt vertical baseline (difference chart, zero baseline meaningful as "no change"). Each panel framed with a small colored corner mark — Vermillion (wrong) on left, Bluish Green (right) on center and right panels. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Three panels showing the same near-identical values. Left = truncated bars (wrong). Center = dot plot with zoomed axis (right). Right = difference chart from zero (right).
[O] Three equal panels in a row.
[P] Wrong-bars Vermillion. Dot plot points Sky Blue. Difference bars Bluish Green. Axis lines and baselines Black 1pt. Corner verdicts Vermillion / Bluish Green.
[E] No quarterly values rendered, no axis ticks, no chart titles, no verdict text, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, quarter labels rendered as graphics, percentage values, chart titles, verdict text, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 7.4 — Vertical Columns vs Horizontal Bars (Label-Length Rule)

**Priority: Important.** Orientation as structural decision.

### Block 1 — Illustrae paste block

A two-panel composition on white. Left panel: five vertical Sky Blue `#56B4E9` filled column bars arranged left-to-right on a Black `#000000` 1pt baseline, with five small Bluish Green `#009E73` filled short horizontal placeholders beneath each column at a slight angle (short labels, rotated). A small Blue `#0072B2` 1pt arrow points from each label to its bar (proximity arrow). Right panel: five horizontal Sky Blue filled bars arranged top-to-bottom from a Black 1pt vertical left baseline, with five Bluish Green filled longer horizontal placeholders to the left of each bar (long labels, read normally). A small Blue 1pt arrow points horizontally from each label to its bar. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Two orientation panels. Left = vertical columns with short rotated labels beneath. Right = horizontal bars with long labels to the left. Proximity arrows mark label-to-bar paths.
[O] Two equal panels side by side.
[P] Bars Sky Blue. Label placeholders Bluish Green. Proximity arrows Blue 1pt. Baselines Black 1pt.
[E] No category names rendered as text, no axis values, no chart titles, no Gestalt annotation text, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, category names rendered as graphics, axis values, chart titles, Gestalt annotation text, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 7.5 — Multiset vs Stacked vs Small Multiples

**Priority: Critical.** The three-form decision for sub-categorized data.

### Block 1 — Illustrae paste block

A three-panel horizontal composition on white. Left panel (stacked): five vertical bars on a Black `#000000` 1pt baseline, each segmented into four colored layers — bottom Sky Blue `#56B4E9`, then Bluish Green `#009E73`, then Orange `#E69F00`, top Reddish Purple `#CC79A7`. Center panel (multiset): five groups of four adjacent vertical bars on a Black 1pt baseline, each group's four bars colored Sky Blue / Bluish Green / Orange / Reddish Purple in the same order. Right panel (small multiples): four small sub-panels in a 2×2 mini-grid, each containing five vertical Sky Blue bars on a Black 1pt baseline (or color-coded per panel to match sectors). White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same five-category, four-sub-category structure rendered three ways. Left = stacked. Center = multiset (grouped). Right = small multiples (2×2 mini-grid).
[O] Three equal panels in a row.
[P] Sub-categories Sky Blue / Bluish Green / Orange / Reddish Purple consistent across panels. Baselines Black 1pt.
[E] No country names rendered as text, no sector names rendered, no axis values, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, country names rendered as graphics, sector names, axis values, panel titles, legend text, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 7.6 — Radial vs Linear Bars

**Priority: Important.** Channel cost of radial form.

### Block 1 — Illustrae paste block

A two-panel composition on white. Left panel (radial): eight Sky Blue `#56B4E9` to Blue `#0072B2` filled radial wedges fanning outward from a small Black `#000000` filled center point, each wedge's outer arc length varying with the encoded value, arranged around a circle. Two wedges with similar radial extent highlighted with thin Vermillion `#D55E00` 1pt outlines, with a small Vermillion 1pt curved arc between them indicating the visual-angle disparity. Right panel (linear): eight horizontal Sky Blue to Blue filled bars on a Black 1pt vertical baseline at left, sorted descending top-to-bottom, with luminance ramp matching the radial version. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same eight values rendered two ways. Left = radial bars with two equal-length wedges highlighted to show unequal visual angle. Right = linear horizontal bars on a common scale.
[O] Two equal panels side by side.
[P] Bars Sky Blue to Blue luminance ramp. Center point and baselines Black. Disparity callout Vermillion thin outline + curved arc.
[E] No domain names rendered, no score values, no chart titles, no perceptual annotation text, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, domain names rendered as graphics, score values, chart titles, perceptual annotation text, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 7.7 — Six Design Decisions in One Bar Chart

**Priority: Important.** Annotated structural breakdown.

### Block 1 — Illustrae paste block

A single horizontal bar chart skeleton occupying the center of the panel: eight horizontal Sky Blue `#56B4E9` to Blue `#0072B2` filled bars sorted descending top-to-bottom from a Black `#000000` 1pt vertical baseline at left. Each bar has a small Bluish Green `#009E73` filled tick at its right end (value annotation marker). Six numbered Orange `#E69F00` filled small circles arranged around the chart, each connected by a thin Black 1pt leader line to the design element it labels: sort order, zero baseline, luminance ramp, value tick, light gridline (drawn as a thin Black 0.5pt vertical guide at 50% opacity behind the bars), and a left-margin label area (a Bluish Green 8% opacity zone on the left edge). White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Annotated horizontal bar chart skeleton. Six numbered callouts mark sort order, zero baseline, luminance encoding, value ticks, light gridlines, label-margin treatment.
[O] Central chart with callout circles arrayed around it on leader lines.
[P] Bars Sky Blue to Blue luminance ramp. Value ticks Bluish Green. Callout circles Orange. Label zone Bluish Green light fill. Baseline and leaders Black. Gridline Black 0.5pt at 50% opacity.
[E] No domain names rendered, no score values, no callout text labels, no rule names rendered, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, domain names rendered as graphics, score values, callout text, rule names rendered, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## What CAJAL Declines to Architect

- **Code snippets and HTML references.** Not figures.
- **AI Wayback portrait of William Playfair.** Editorial portrait, separate pipeline.

---

## Video Candidate Pass

**FIGURE 7.1 (baseline contrast):** STATIC SUFFICIENT.
**FIGURE 7.2 (channel ranking):** STATIC SUFFICIENT.
**FIGURE 7.3 (three responses):** STATIC SUFFICIENT.
**FIGURE 7.4 (orientation):** STATIC SUFFICIENT.
**FIGURE 7.5 (multiset/stacked/small multiples):** STATIC SUFFICIENT.
**FIGURE 7.6 (radial vs linear):** STATIC SUFFICIENT.
**FIGURE 7.7 (six decisions):** STATIC SUFFICIENT.

**Video candidates identified: 0.** All figures are taxonomic/structural skeletons. No mechanism unfolds in time.

---

## Split-point note

Chapter is the structural anchor of Part II (chart-family chapters). Visual style must match Ch 08 (temporal) and Ch 09 (distribution) — same Okabe-Ito grammar, same minimal abstract-skeleton approach. Sub-category coloring convention (Sky Blue / Bluish Green / Orange / Reddish Purple in Fig 7.5) should recur across chapters as a consistent sub-category palette.
