# CAJAL Figure Intelligence — Chapter 16: Design Principles in Practice

**Source:** `chapters/16-design-principles-in-practice.md`
**Mode:** `/scan silent`
**Domain note:** AI+1 practitioner guide / data visualization with D3 and Claude. Chapter synthesizes Tufte (heuristics: data-ink, proportional ink), Few (clarity-over-minimization), Cairo (ethical/responsibility frame), and Gestalt (perceptual mechanism) into the Evergreen/Emery 22-point checklist. Four author-placed figures.

---

## Density Recommendation

**4 figures, Synthesis density.** All four earn their place. The chapter is a synthesis; the figures index the synthesis. Each figure shows a different kind of conceptual move: failure enumeration (16.1), source attribution (16.2), color vocabulary classification (16.3), before/after redesign (16.4).

---

## Zone Map

- **MC:** The four-source synthesis (Tufte + Few + Cairo + Gestalt → 22-point checklist). Few's "does this support the message?" as the working criterion. Proportional ink grounded in Stevens' power law. Color as three vocabularies (categorical, sequential, diverging).
- **VG:** The seven failure modes in the opening chart. The before/after visual contrast of the redesign. The three color-vocabulary panels. Each source's distinct contribution.
- **PQ:** 22 checklist items across 5 categories (text 5, arrangement 4, color 5, lines 4, overall 4). 14 of 22 fail in the opening case. ~200 ms reading penalty for rotated labels. ~8% of male readers excluded by colorblind-unsafe palettes. 4.5:1 WCAG AA contrast ratio. 9pt minimum text size.

---

## Figure 16.1 — Seven Visible Failures in the Opening Chart

**Priority: Critical.** The chapter's opening case. Must show a chart and seven labeled failure points simultaneously.

### Block 1 — Illustrae paste block

A flawed bar chart of five regional sales values shown with seven numbered callouts. The chart core: a horizontal row of five vertical bars rendered with exaggerated 3D perspective foreshortening — each bar drawn as a slanted Vermillion `#D55E00` filled parallelogram with a Black `#000000` 0.5pt outline, the front face visibly shorter than the implied bar height. Bars sit on a y-axis that does not start at zero — the axis baseline visibly cuts off at roughly 60% of the bar heights. Heavy Black 1.5pt gridlines run horizontally at every increment. Below each bar, a placeholder mark indicating rotated labels (a small Sky Blue `#56B4E9` 45° tick). Seven small Orange `#E69F00` filled numbered circle callouts arrange around the chart pointing to: (1) truncated baseline, (2) 3D perspective, (3) rainbow gradients — indicated by varying Vermillion/Orange/Bluish Green/Sky Blue/Reddish Purple bar fills, (4) heavy gridlines, (5) rotated labels, (6) the title placeholder, (7) the missing comparison reference (a small dashed Blue `#0072B2` 1pt outlined empty box where the reference would be). White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] A deliberately flawed bar chart of five regional values with seven numbered failure callouts indicating: truncated y-axis, 3D perspective, rainbow gradients, heavy gridlines, rotated labels, occasion-named title, no comparison reference.
[O] Bar chart centered. Numbered callouts arrayed around the chart with Black 0.5pt leader lines.
[P] Bars Vermillion / Orange / Bluish Green / Sky Blue / Reddish Purple (deliberately rainbow). Bar outlines Black 0.5pt. Gridlines Black 1.5pt (deliberately heavy). Callout circles Orange. Leader lines Black 0.5pt. Missing-reference box Blue dashed.
[E] No region names, no dollar values, no axis numbers, no title text, no callout text, no decorative ornament, no shadows beyond the inherent 3D-perspective shading that is itself the failure being illustrated.

### Block 3 — Negative prompt

text labels, region names, dollar values, axis numbers, title text, callout text, legend, gibberish letters, decorative ornament, photographic elements, realistic textures, drop shadows beyond the perspective failure itself, gradient fills as backgrounds, gradient page backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter beyond the seven failures, fuzzy borders, watermarks, red-green color combinations, rainbow color scales as data encoding for non-categorical data, 3D perspective distortion as background (it appears inside the flawed chart deliberately, not in the figure frame)

---

## Figure 16.2 — Four Sources Converge on the Checklist

**Priority: Important.** Names the four contributing traditions and the synthesis they produce.

### Block 1 — Illustrae paste block

A four-quadrant composition arranged around a central node. Four equal rectangular quadrants on a 2×2 grid, each with a Black `#000000` 0.5pt border. Top-left quadrant: a Blue `#0072B2` filled small icon representing Tufte (a simplified bar chart with high data-ink ratio). Top-right: a Sky Blue `#56B4E9` filled icon representing Few (a checkmark over a chart). Bottom-left: a Bluish Green `#009E73` filled icon representing Cairo (a balanced scale glyph). Bottom-right: a Reddish Purple `#CC79A7` filled icon representing Gestalt (four small dots grouped into two pairs by proximity). From each quadrant, a Black 0.75pt arrow converges toward a central Orange `#E69F00` filled rounded rectangle representing the 22-point checklist. The central node is larger than any single quadrant icon. White background, flat vector, single-column 89mm or double-column acceptable.

### Block 2 — Full SCOPE prompt

[S] Single-column 89mm or double-column 174mm, vector, white background.
[C] Four-quadrant infographic showing the four contributing sources (Tufte heuristics, Few working criterion, Cairo ethical frame, Gestalt perceptual mechanism) converging on a central node representing the 22-point checklist.
[O] 2×2 grid of quadrants around a central convergence node. Arrows from each quadrant to the center.
[P] Tufte icon Blue. Few icon Sky Blue. Cairo icon Bluish Green. Gestalt icon Reddish Purple. Arrows Black 0.75pt. Central checklist node Orange. Quadrant borders Black 0.5pt.
[E] No source names rendered as text, no quadrant labels, no checklist item names, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, source names, quadrant labels, checklist item text, principle names, gibberish letters, titles, captions, decorative ornament, photographic portraits of theorists, realistic textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 16.3 — Three Color Vocabularies

**Priority: Critical.** The pedagogical core of the color section. Three vocabularies, three data types, side by side.

### Block 1 — Illustrae paste block

A three-panel horizontal composition. Each panel contains a small simplified chart demonstrating one color vocabulary. Panel 1 (Categorical): a row of five short vertical bars at matched height, filled with five distinct Okabe-Ito hues — Blue `#0072B2`, Sky Blue `#56B4E9`, Bluish Green `#009E73`, Orange `#E69F00`, Reddish Purple `#CC79A7` — all at matched luminance to convey "no hue is more important than any other". Bars sit on a Black `#000000` 0.5pt baseline. Panel 2 (Sequential): a row of seven short vertical bars in a single-hue Blue luminance ramp, progressing from light Sky Blue `#56B4E9` at left through Blue `#0072B2` toward a deeper Blue at right, encoding a quantitative increase. Black 0.5pt baseline. Panel 3 (Diverging): a row of nine short vertical bars centered on a midpoint, with the left half running from deep Vermillion `#D55E00` to pale Vermillion near the center, and the right half running from pale Sky Blue to deep Blue `#0072B2`. A small Black 1pt vertical tick marks the midpoint. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Three side-by-side panels demonstrating categorical (five distinct hues at matched luminance), sequential (single-hue luminance ramp), and diverging (two hues meeting at a neutral midpoint) color vocabularies.
[O] Three horizontal panels left-to-right.
[P] Categorical: Blue, Sky Blue, Bluish Green, Orange, Reddish Purple at matched luminance. Sequential: Sky Blue → Blue luminance ramp. Diverging: deep Vermillion → pale → deep Blue with Black midpoint tick. Baselines Black 0.5pt.
[E] No data values, no axis labels, no panel titles, no category names, no scale numbers, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, data values, axis labels, panel titles, category names, scale numbers, gibberish letters, captions, decorative ornament, photographic elements, realistic textures, drop shadows, gradient fills as decoration (only within the sequential and diverging bars as the encoding itself), gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 16.4 — Before-and-After Redesign

**Priority: Critical.** The chapter's payoff figure. Same data, two encoding decisions, all 22 items checked.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition showing the same data twice. Left panel (BEFORE): the flawed chart from Figure 16.1 in reduced form — five rainbow 3D-perspective bars on a truncated baseline with heavy Black `#000000` 1.5pt gridlines. The chart appears visually cluttered. A small Vermillion `#D55E00` outlined badge sits beside it indicating extensive failure. Right panel (AFTER): a clean horizontal bar chart of the same five regions sorted descending by value. Five horizontal Blue `#0072B2` filled bars of varying lengths, all from a zero baseline. A single Black 0.5pt y-axis line on the left edge and a single Black 0.5pt x-axis line at the bottom. Light Black 0.25pt gridlines at axis tick positions. Small Orange `#E69F00` filled dots at each bar's right end indicating direct value labels (the values themselves are not rendered). A small Bluish Green `#009E73` filled badge sits beside it indicating compliance. Between the two panels, a Bluish Green 1.5pt arrow points from BEFORE to AFTER. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same five-region data shown twice: BEFORE (flawed 3D rainbow truncated bar chart) and AFTER (horizontal bar chart sorted descending, zero baseline, single muted hue, light gridlines, direct value indicators). Compliance badges flank each panel.
[O] Two horizontal panels with a transition arrow between them.
[P] Before: rainbow Vermillion/Orange/Bluish Green/Sky Blue/Reddish Purple bars, heavy Black gridlines, Vermillion failure badge. After: single Blue bars, Black 0.5pt axes, light Black 0.25pt gridlines, Orange value-label dots, Bluish Green compliance badge. Transition arrow Bluish Green 1.5pt.
[E] No region names, no dollar values, no axis numbers, no title text, no badge text, no decorative ornament, no shadows beyond the deliberate 3D failure inside the BEFORE chart.

### Block 3 — Negative prompt

text labels, region names, dollar values, axis numbers, title text, badge text, subtitle text, gibberish letters, captions, decorative ornament, photographic elements, realistic textures, drop shadows beyond the BEFORE 3D failure itself, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter beyond what BEFORE deliberately demonstrates, fuzzy borders, watermarks, red-green color combinations, rainbow color scales as background, 3D perspective distortion as background (deliberately inside BEFORE only)

---

## What CAJAL Declines to Architect

- **The Tufte-vs-Few visual-element table (lines 89–97).** Typography reference table. Belongs as a layout table.
- **The 22-point checklist tables across five categories (lines 156–202).** Five large reference tables — typography, not figures. The visual synthesis is delivered by Figure 16.2 and the redesign in Figure 16.4.
- **A standalone Stevens' power law curve.** Not author-placed; if added later, it would be a single-axis log-log plot.
- **Edward Tufte AI Wayback portrait.** Existing AI-generated portrait reference, not a CAJAL architectural target.

---

## Video Candidate Pass

**FIGURE 16.1 (Seven failures):** STATIC SUFFICIENT.
**FIGURE 16.2 (Four sources):** STATIC SUFFICIENT.
**FIGURE 16.3 (Three color vocabularies):** STATIC SUFFICIENT.
**FIGURE 16.4 (Before-and-after redesign):** **MILD VIDEO CANDIDATE.** A short morph animation showing the flawed chart transforming into the redesign — each failure dropping away one at a time as the bars rotate horizontal, the baseline drops to zero, the rainbow collapses to a single hue — would dramatize the cumulative effect of the checklist. The static two-panel version is already strong; the animation would be a teaching enhancement, not a necessity.

**Video candidates identified: 0 strong + 1 mild.** Recommended: hold; the static before/after is the cleaner instructional artifact and pairs naturally with the in-text walk-through of the 22 items. Reserve animation budget for chapters where the mechanism itself is dynamic.

---

## Split-point note

Chapter cross-references Chapter 01 (Cleveland & McGill, Stevens' power law, Bertin's channel framework), Chapter 05 (data audit), Chapters 07–15 (chart-family-specific design rules), Chapter 11 (Cairo's proportional ink and the rhetorical-vs-analytical frame), and Chapter 17 (the project pipeline that operationalizes the checklist). Figures here must share a visual language with all prior chapter figures — same Okabe-Ito palette, same flat-vector treatment, same stroke weights — because this chapter's job is to make every preceding figure feel like part of the same synthesis. Figure 16.4's "AFTER" panel should specifically match the visual register used in Chapter 06's canonical bar chart.
