# CAJAL Figure Intelligence — Chapter 8: Time Series and Temporal Charts

**Source:** `chapters/08-time-series-and-temporal-charts.md`
**Mode:** `/scan silent`
**Domain note:** AI+1 practitioner guide / data visualization with D3 and Claude. Temporal chart family — seven forms (line, area, stacked area, stream, spiral, Gantt, timeline), the channel-determines-baseline split, skipped-interval problem, stacked-area accuracy gradient, cyclic-data trade-off. Six author-placed figures, all MINIMAL abstract chart skeletons.

---

## Density Recommendation

**6 figures, Structural density.** The chapter's central technical claim — area-channel requires zero baseline; position-channel does not — is encoded across multiple figures showing the same data in different forms. Each figure isolates one structural distinction.

---

## Zone Map

- **MC:** Zero-baseline rule splits the temporal family by channel (area vs position). Skipped intervals violate Gestalt continuity. Stacked area accuracy degrades layer by layer. Spiral plot trades trend visibility for cycle visibility.
- **VG:** Bar vs line baseline contrast. Seven-form reference grid. Three-encoding temperature comparison. Compressed vs gap-marked axis. Stacked-area accuracy gradient. Line vs spiral.
- **PQ:** No tables — argument is prose plus the figures.

---

## Figure 8.1 — Bar vs Line, Same Truncated Y-Range

**Priority: Critical.** The chapter's central technical claim made visible.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition on white. Both panels share an identical truncated y-range (a Black `#000000` 1pt baseline drawn partway up each panel, with a thin Vermillion `#D55E00` 0.5pt dashed line at the panel bottom indicating where true zero would sit). Left panel: twelve vertical Vermillion `#D55E00` filled bar columns rising from the truncated baseline — the same modest data variation looks dramatically exaggerated; a small Vermillion filled triangle in the upper corner marks "channel violation." Right panel: a single Blue `#0072B2` 1.5pt continuous line connecting twelve Sky Blue `#56B4E9` filled small circle points across the same truncated y-range — the variation reads as gentle and honest; a small Bluish Green `#009E73` filled checkmark-equivalent dot in the upper corner marks "channel honest." White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same twelve monthly values, same truncated y-range, two forms. Left = bar columns (length channel violated by truncated baseline). Right = line with point markers (position channel survives truncation).
[O] Two equal panels side by side. True-zero reference line in each panel.
[P] Bar columns Vermillion (violation). Line Blue with Sky Blue point markers (honest). True-zero reference Vermillion 0.5pt dashed. Baselines Black 1pt. Corner verdicts Vermillion / Bluish Green small markers.
[E] No axis tick text, no month names, no dollar values, no chart titles, no verdict text, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, month names rendered as graphics, dollar values, axis ticks, chart titles, verdict text, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 8.2 — Seven Temporal Forms Reference Grid

**Priority: Important.** Taxonomic overview.

### Block 1 — Illustrae paste block

A 2×4 grid (eighth cell collapses to a summary). Each of the first seven cells contains a minimal skeleton: (1) line chart — a single Blue `#0072B2` 1.5pt path crossing a panel with a Black `#000000` 1pt baseline. (2) area chart — a Sky Blue `#56B4E9` filled region below a Blue 1.5pt line on a Black baseline. (3) stacked area — three layered filled regions: bottom Sky Blue, middle Bluish Green `#009E73`, top Orange `#E69F00`. (4) stream graph — three filled regions centered vertically with a faint Black 0.5pt dashed midline. (5) spiral plot — a tight Blue 1.5pt Archimedean spiral curling from center outward. (6) Gantt chart — five short horizontal Sky Blue filled bars stacked vertically at varying x-positions and lengths. (7) timeline — a single Black 1pt horizontal axis with five small Vermillion `#D55E00` filled circle event markers. The eighth cell (bottom right) is a Bluish Green `#009E73` filled rounded rectangle (summary card). White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] 2×4 grid of temporal-form skeletons: line, area, stacked area, stream graph, spiral, Gantt, timeline, plus a summary card.
[O] Equal-sized cells in a 2×4 arrangement.
[P] Line Blue. Area Sky Blue fill + Blue line. Stacked area Sky Blue / Bluish Green / Orange. Stream graph Sky Blue / Bluish Green / Orange centered. Spiral Blue. Gantt bars Sky Blue. Timeline markers Vermillion on Black axis. Summary card Bluish Green.
[E] No form names rendered as text, no axis labels, no card title text, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, form names rendered as graphics, axis labels, summary card text, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 8.3 — Three Encodings, One Temperature Series

**Priority: Critical.** Zero-baseline rule applied to area vs position.

### Block 1 — Illustrae paste block

A three-panel horizontal composition on white. Left panel (area chart, truncated y): a Sky Blue `#56B4E9` filled region rises from a Black `#000000` 1pt baseline drawn well above the panel bottom, with a thin Vermillion `#D55E00` 0.5pt dashed line at the panel bottom marking true zero — the filled area looks visually substantial; a small Vermillion filled triangle marks distortion. Center panel (area chart, zero baseline): the same data as a Sky Blue filled region rising from a Black 1pt baseline at the true zero at the panel bottom — the filled region occupies only the upper band of the panel, leaving much of the panel empty; a small Bluish Green `#009E73` checkmark-dot marks honest. Right panel (line chart, zoomed y): a Blue `#0072B2` 1.5pt path crossing the panel with a Black 1pt baseline cut well above true zero; no area is filled, only point-position is encoded; a small Bluish Green checkmark-dot marks honest. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Three panels of the same temperature series. Left = area with truncated baseline (channel violation). Center = area with zero baseline (honest, mostly empty plot). Right = line with zoomed y-range (honest, position channel).
[O] Three equal panels in a row.
[P] Area fills Sky Blue. Line Blue. Honest baselines Black 1pt. True-zero reference Vermillion 0.5pt dashed. Verdict markers Vermillion triangle / Bluish Green dot.
[E] No temperature values, no axis labels, no chart titles, no day-number labels, no verdict text, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, temperature values, axis labels, chart titles, day numbers, verdict text, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 8.4 — Compressed Axis vs Gap-Marked Axis

**Priority: Important.** The skipped-interval problem.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition on white. Left panel (compressed axis): a Blue `#0072B2` 1.5pt continuous line crossing the panel without interruption, connecting Sky Blue `#56B4E9` filled small circle points; the visible slope is steep across the missing region (axis compressed, no gap visible); a small Vermillion `#D55E00` filled triangle marks distortion. Right panel (gap-marked axis): the same data but the line breaks across a vertically shaded Vermillion `#D55E00` 15% opacity narrow band positioned where March would sit (the gap is visible); the line resumes after the band; the slopes before and after the gap reflect the true two-month change; a small Bluish Green `#009E73` checkmark-dot marks honest. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same 24-month series with March missing, two axis treatments. Left = compressed axis (false steep slope). Right = gap preserved with a shaded missing-data band, line broken across it.
[O] Two equal panels side by side.
[P] Line Blue with Sky Blue point markers. Gap band Vermillion 15% opacity. Baselines Black 1pt. Verdict markers Vermillion triangle / Bluish Green dot.
[E] No month names rendered, no axis tick numerals, no chart titles, no verdict text, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, month names rendered as graphics, axis tick numerals, chart titles, verdict text, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 8.5 — Stacked Area Accuracy Gradient

**Priority: Important.** Why bottom layer is most readable.

### Block 1 — Illustrae paste block

A single panel showing a stacked-area chart skeleton on white. Five layered filled regions stacked from bottom to top: bottom Sky Blue `#56B4E9` (most stable, fixed zero baseline on a Black `#000000` 1pt horizontal line), then Bluish Green `#009E73`, then Orange `#E69F00`, then Reddish Purple `#CC79A7`, top Blue `#0072B2`. The layer boundaries are visible as thin Black 0.5pt lines. To the right of the chart, a vertical column of five small bracket markers — each a thin Blue `#0072B2` 1pt vertical bar — sized progressively from tallest (bottom layer = highest accuracy) to shortest (top layer = lowest accuracy). At the top edge of the stack, a thin Bluish Green `#009E73` 1pt horizontal line continues to the right of the chart, marked with a small Bluish Green filled dot (the total trajectory, which recovers high accuracy). White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Five-layer stacked-area chart with right-side accuracy brackets showing degradation from bottom (high) to top (low). Total trajectory along the top edge marked separately as a recovery line.
[O] Single chart panel with a right-side bracket column.
[P] Layers Sky Blue / Bluish Green / Orange / Reddish Purple / Blue. Baseline Black 1pt. Layer separators Black 0.5pt. Accuracy brackets Blue 1pt. Total-trajectory marker Bluish Green 1pt + dot.
[E] No sector names rendered, no month labels, no chart title, no annotation text, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, sector names rendered as graphics, month labels, chart titles, accuracy annotation text, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 8.6 — Line Chart vs Spiral Plot

**Priority: Important.** The cyclic-data trade-off.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition on white. Left panel (line chart): a Blue `#0072B2` 1.5pt path crossing the panel with a clear sawtooth pattern (recurring peaks and valleys over five repeated periods) and a gentle upward overall slope; the baseline is a Black `#000000` 1pt horizontal line. Right panel (spiral plot): a Blue 1.5pt Archimedean spiral curling from a small Black filled center point outward through five complete rotations; the spiral's radial distance from center varies — five clusters of Vermillion `#D55E00` filled small circle markers at the top of the spiral (winter peaks) and five clusters of Sky Blue `#56B4E9` filled small circle markers at the bottom of the spiral (summer dips); the cyclic clusters at the top form a visible vertical band, as do those at the bottom. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same five-year monthly series rendered two ways. Left = line chart showing trend and recurring sawtooth. Right = spiral plot with five rotations, peaks clustered at top, dips clustered at bottom.
[O] Two equal panels side by side.
[P] Line Blue. Spiral Blue. Winter-peak markers Vermillion small circles. Summer-dip markers Sky Blue small circles. Center point Black. Baseline Black 1pt.
[E] No month names rendered, no clock-position labels, no axis values, no chart titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, month names rendered as graphics, clock-position labels, axis values, chart titles, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## What CAJAL Declines to Architect

- **Code snippets and follow-up-prompt quotes.** Not figures.
- **MBTA Marey diagram (referenced in text).** Not an author-placed figure in this chapter — appears as discussion.
- **AI Wayback portrait of Étienne-Jules Marey.** Editorial portrait, separate pipeline.

---

## Video Candidate Pass

**FIGURE 8.1 (bar vs line truncation):** STATIC SUFFICIENT.
**FIGURE 8.2 (seven forms grid):** STATIC SUFFICIENT.
**FIGURE 8.3 (three temperature encodings):** STATIC SUFFICIENT.
**FIGURE 8.4 (compressed vs gap-marked):** STATIC SUFFICIENT.
**FIGURE 8.5 (stacked area accuracy):** STATIC SUFFICIENT.
**FIGURE 8.6 (line vs spiral):** **MILD VIDEO CANDIDATE.** A sweeping animation of one year traveling around the spiral while the line chart simultaneously draws left-to-right could make the "same data, two views" relationship feel inevitable. Optional.

**Video candidates identified: 1 mild.** Recommended only if the line-to-spiral correspondence needs reinforcement beyond the static side-by-side.

---

## Split-point note

Chapter is the temporal sibling to Ch 07 (comparison) and Ch 09 (distribution). The zero-baseline argument established in Ch 07 for bars is extended here to area charts — same Stevens'-power-law mechanism, new application. Sub-category color order (Sky Blue / Bluish Green / Orange / Reddish Purple / Blue) used in Fig 8.5 should match Ch 07 Fig 7.5 stacked-bar convention for visual consistency across chapters.
