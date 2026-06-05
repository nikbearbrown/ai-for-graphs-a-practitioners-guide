# CAJAL Figure Intelligence — Chapter 9: Distribution Charts

**Source:** `chapters/09-distribution-charts.md`
**Mode:** `/scan silent`
**Domain note:** AI+1 practitioner guide / data visualization with D3 and Claude. Distribution chart family — histogram (bin-width problem), box plot (Tukey's 1.5×IQR, what it hides), violin plot (shape), stem-and-leaf, density. Cairo's graphicacy constraint. Five author-placed figures, all MINIMAL abstract chart skeletons.

---

## Density Recommendation

**5 figures, Mechanism + structure density.** Each figure isolates one structural insight: a feature visible/invisible in one form, the consequence of a binning decision, Tukey's design, what violin adds.

---

## Zone Map

- **MC:** Mean hides what distribution reveals. Bin-width determines what histogram shows. Tukey's 1.5×IQR fence makes outliers visible. Violin shows shape; box hides it. Graphicacy gates form choice.
- **VG:** Box plot vs violin contrast. Three-binwidth histogram comparison. Annotated Tukey box. Hybrid box-violin.
- **PQ:** Graphicacy-vs-form table.

---

## Figure 9.1 — Cluster Visible, Meaning Not

**Priority: Important.** Box-plot limitation made visible.

### Block 1 — Illustrae paste block

A single panel showing five box-plot skeletons side by side on a Black `#000000` 1pt horizontal baseline. Each box plot has: a Sky Blue `#56B4E9` filled box (Q1 to Q3), a Blue `#0072B2` 1pt horizontal median line inside the box, thin Black 1pt whisker lines extending above and below, and a small horizontal cap at each whisker end. The second box from the left has a cluster of three Vermillion `#D55E00` filled small circles plotted well above its upper whisker (the outlier cluster). A Vermillion 1pt curved leader line points from outside the panel to the cluster, ending in a small Orange `#E69F00` filled question-mark circle (the "what does this mean?" annotation marker). White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Five side-by-side box plots. The second box has a visible cluster of outlier points above its upper whisker, called out with a leader to a question-marker.
[O] Five box plots in a row. Annotation arrow from outside the panel.
[P] Boxes Sky Blue filled. Median lines Blue 1pt. Whiskers Black 1pt with caps. Outlier points Vermillion small filled circles. Annotation leader Vermillion 1pt. Question marker Orange filled circle.
[E] No zone names rendered, no income values, no axis labels, no annotation text, no chart titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, zone names rendered as graphics, income values, axis labels, annotation text, chart titles, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 9.2 — Same Summary, Different Shapes (Box vs Violin)

**Priority: Critical.** The chapter's central trade-off.

### Block 1 — Illustrae paste block

A four-panel composition arranged in a 2×2 grid on white. Top-left: a box-plot skeleton with Sky Blue `#56B4E9` filled box, Blue `#0072B2` 1pt median line, Black `#000000` 1pt whiskers (representing a normal-distribution sample). Top-right: an identical box-plot skeleton (representing a bimodal sample — visually indistinguishable from the left). Bottom-left: a violin-plot skeleton — a Sky Blue filled symmetrical lobe (single bulge in the middle, representing normal). Bottom-right: a violin-plot skeleton — a Sky Blue filled shape with two distinct bulges, one upper and one lower (representing bimodal). The two top panels are bracketed together by a thin Vermillion `#D55E00` 1pt arc with a small Vermillion filled triangle (signaling "indistinguishable"). The two bottom panels are bracketed by a thin Bluish Green `#009E73` 1pt arc with a small Bluish Green filled dot (signaling "shape visible"). White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] 2×2 grid. Top row: two box plots of different underlying distributions, visually identical. Bottom row: two violin plots of the same distributions, where one shows a single bulge and the other shows two bulges.
[O] 2×2 grid with bracket arcs marking the contrast between rows.
[P] Boxes Sky Blue filled. Median lines Blue. Whiskers Black 1pt. Violins Sky Blue filled. Indistinguishable bracket Vermillion arc + triangle. Visible-shape bracket Bluish Green arc + dot.
[E] No axis labels, no chart titles, no shape annotation text, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, axis labels, chart titles, shape annotation text, sample-size labels, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 9.3 — Three Bin Widths, Two Lie

**Priority: Critical.** The histogram bin-width problem.

### Block 1 — Illustrae paste block

A three-panel horizontal composition on white. Left panel (wide bins): three wide Vermillion `#D55E00` filled columns of similar height standing on a Black `#000000` 1pt baseline — no bimodality visible; a small Vermillion filled triangle marks distortion. Center panel (Freedman-Diaconis bins): ten Sky Blue `#56B4E9` to Blue `#0072B2` filled columns of varying heights forming two clearly visible peaks with a valley between them; a small Bluish Green `#009E73` filled dot marks honest. Right panel (narrow bins): roughly thirty thin Vermillion filled columns with jagged irregular heights, noisy and busy, peaks lost in jitter; a small Vermillion filled triangle marks distortion. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Three histograms of the same bimodal data. Left = wide bins (bimodality hidden). Center = Freedman-Diaconis bins (two peaks visible). Right = narrow bins (peaks lost in noise).
[O] Three equal panels in a row.
[P] Wrong-binning columns Vermillion. Honest-binning columns Sky Blue to Blue luminance ramp. Baselines Black 1pt. Verdict markers Vermillion triangle / Bluish Green dot.
[E] No axis labels, no bin-width values, no chart titles, no rule names rendered, no verdict text, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, axis labels, bin-width values, chart titles, rule names rendered as graphics, verdict text, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 9.4 — Tukey Box Plot vs Range Chart Imposter

**Priority: Important.** The fence is what makes outliers visible.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition on white. Left panel (Tukey design): a single box-plot skeleton with a Sky Blue `#56B4E9` filled box (Q1 to Q3), Blue `#0072B2` 1pt horizontal median line inside, Black `#000000` 1pt whiskers extending to a fence with small horizontal end caps, and three Vermillion `#D55E00` filled small circles above the upper cap (genuine outliers). Six small Orange `#E69F00` filled circle callouts arranged around the chart, each connected by thin Black 1pt leader lines to: Q3 (top of box), Q1 (bottom of box), median line, IQR box height (bracket on right side of box, thin Blue 1pt), 1.5×IQR fence cap, outlier points. A small Bluish Green `#009E73` filled dot in the corner marks honest. Right panel (range chart imposter): a similar box-plot skeleton but the whiskers extend all the way to the panel top and bottom (min/max), with no end caps and no outlier points visible — looks like a box plot but isn't one; a small Vermillion filled triangle in the corner marks distortion. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Two box-plot skeletons side by side. Left = annotated Tukey design with six numbered callouts (Q3, Q1, median, IQR, fence, outliers). Right = imposter with whiskers extending to data min/max and no outliers.
[O] Two equal panels side by side. Callout circles arrayed around the left chart.
[P] Box Sky Blue filled. Median Blue 1pt. Whiskers + caps Black 1pt. Outlier points Vermillion. Callouts Orange filled circles on Black leaders. IQR bracket Blue 1pt. Verdict markers Bluish Green dot / Vermillion triangle.
[E] No callout text, no Q1/Q3/median labels rendered, no chart titles, no fence-rule annotation, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, callout text, Q1/Q3/median labels rendered as graphics, chart titles, fence-rule annotations, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 9.5 — Box, Violin, Hybrid

**Priority: Important.** Each form reveals what others hide.

### Block 1 — Illustrae paste block

A three-panel horizontal composition on white. Left panel (box plot of bimodal data): a Sky Blue `#56B4E9` filled box with Blue `#0072B2` median line and Black `#000000` 1pt whiskers — shape entirely hidden. Center panel (violin plot of same bimodal data): a Sky Blue filled symmetrical violin shape with two clearly distinct bulges (upper bulge and lower bulge), no quartile marks. Right panel (hybrid): the same Sky Blue violin envelope as the center, but with a thin Bluish Green `#009E73` filled narrow box overlaid in the center (Q1 to Q3), a Blue 1pt horizontal median line inside the box, and small Black 1pt cap whiskers within the violin shape. The hybrid panel framed by a thin Orange `#E69F00` 1pt outline emphasizing the combined form. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Three panels of the same bimodal distribution. Left = box plot (shape hidden). Center = violin (shape visible, quartiles absent). Right = hybrid (thin box overlaid inside the violin).
[O] Three equal panels in a row. Hybrid panel framed for emphasis.
[P] Box and violin fills Sky Blue. Hybrid inner box Bluish Green. Median lines Blue. Whiskers Black 1pt. Hybrid frame Orange 1pt.
[E] No axis labels, no quartile values, no chart titles, no form names rendered, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, axis labels, quartile values, chart titles, form names rendered as graphics, sample-size labels, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## What CAJAL Declines to Architect

- **Graphicacy-by-form table (lines 113–119).** Typography reference table.
- **Code snippets and follow-up prompts.** Not figures.
- **AI Wayback portrait of Adolphe Quetelet.** Editorial portrait, separate pipeline.

---

## Video Candidate Pass

**FIGURE 9.1 (cluster visible):** STATIC SUFFICIENT.
**FIGURE 9.2 (box vs violin):** STATIC SUFFICIENT.
**FIGURE 9.3 (three bin widths):** **MILD VIDEO CANDIDATE.** A morph through bin widths — wide → Freedman-Diaconis → narrow — could dramatize the structure-emerging / structure-vanishing dynamic better than three static panels. Optional.
**FIGURE 9.4 (Tukey vs imposter):** STATIC SUFFICIENT.
**FIGURE 9.5 (box, violin, hybrid):** STATIC SUFFICIENT.

**Video candidates identified: 1 mild.** Recommended only if the bin-width sensitivity benefits from a continuous demonstration.

---

## Split-point note

Chapter completes the chart-family triad with Ch 07 (comparison) and Ch 08 (temporal). All three chapters share the minimal abstract-skeleton approach and the Okabe-Ito palette discipline. Bimodal-distribution illustration in Figs 9.2, 9.3, 9.5 should remain consistent in shape across the three figures so the reader recognizes "the same bimodal data" across forms. Cairo's graphicacy concept gets named here and should be visible as a recurring constraint in the chapter-family chapters going forward.
