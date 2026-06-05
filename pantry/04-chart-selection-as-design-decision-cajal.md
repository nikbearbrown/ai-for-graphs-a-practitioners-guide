# CAJAL Figure Intelligence — Chapter 04: Chart Selection as Design Decision

**Source:** `chapters/04-chart-selection-as-design-decision.md`
**Mode:** `/scan silent`
**Domain note:** AI+1 practitioner guide / data visualization with D3 and Claude. META-book about graphs. This chapter is the chart-selection / decision-tree chapter — pie-vs-bar opening case, the FT Visual Vocabulary's eight functional categories, Cairo's four-step framework, the three failure modes (familiarity, aesthetic-first, software-default), the same-data three-charts demonstration, and the chart-type invention timeline. Six author-placed figures (Figs 4.1–4.6). The Cairo four-step framework (Fig 4.2) and the FT eight-category navigation tool (Fig 4.5) are the central figures.

---

## Density Recommendation

**6 figures, Mechanistic density.** This is the practitioner's decision-tree chapter — the largest leverage point in the whole book. The author placed six figures, each carrying a distinct piece of the chart-selection discipline. All six earn their place. Fig 4.2 (Cairo's four-step framework) and Fig 4.5 (FT eight categories) are critical; Figs 4.1, 4.3, 4.4, 4.6 are important.

---

## Zone Map

- **MC:** Pie-chart channel failure on a ranking task (Fig 4.1). Cairo's four-step decision flow (Fig 4.2). The three failure-mode redesigns (Fig 4.3). One dataset, three messages, three charts (Fig 4.4).
- **VG:** FT Visual Vocabulary eight functional categories (Fig 4.5). Chart-type invention timeline 1786–1991 (Fig 4.6).
- **PQ:** None at the figure level. The "14 slices, 21% top slice, three sectors at 8–12%" numbers from the opening case are typography facts that anchor Fig 4.1 but are not rendered numerically inside it.

---

## Figure 4.1 — Pie chart vs. sorted bar chart, 14-sector dataset

**Priority: Critical.** Opening case. Same data, two chart types, one readable, one not.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition. Left panel: a single pie circle, Black `#000000` 1pt outline, divided into 14 slices of widely varying angles. The two largest slices (around 21% and 11%) are Blue `#0072B2` filled and Sky Blue `#56B4E9` filled respectively. The remaining 12 slices are filled in graduated Sky Blue at descending opacities, with the five smallest slivers nearly indistinguishable along one edge. A small Vermillion `#D55E00` filled badge in the upper-left corner of the panel marks "rank task: fails." Right panel: a horizontal bar chart frame with Black 1pt axes. Fourteen horizontal Bluish Green `#009E73` filled bars stacked top-to-bottom, sorted descending by length. The top bar is clearly more than twice the next; the bars taper smoothly to short slivers at the bottom. The y-axis ordering is value-driven, not alphabetical. A small Bluish Green filled badge in the upper-left corner of the panel marks "rank task: succeeds." White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Two-panel comparison of the same 14-sector dataset. Left: cramped 14-slice pie chart, angle-encoded, ranking task fails. Right: horizontal bar chart sorted descending, length-encoded, ranking task succeeds. Corner badges call out the task outcome.
[O] Side by side. Equal panel sizes. Left panel is circular; right panel is rectangular.
[P] Pie's two largest slices Blue and Sky Blue. Remaining slices graduated Sky Blue. Bar chart bars Bluish Green. Axes and pie outline Black 1pt. Failure-task badge Vermillion. Success-task badge Bluish Green.
[E] No sector names rendered as text, no percentage labels, no chart titles, no legend graphics, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, sector names, percentage labels, chart titles, legends rendered as graphics, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 4.2 — Cairo's four-step chart-selection framework

**Priority: Critical.** The chapter's decision tree. The single highest-value diagram of the book's middle.

### Block 1 — Illustrae paste block

A horizontal four-stage flow composition. Four rounded rectangle nodes arranged left-to-right, connected by Black `#000000` 1pt arrows. Node 1 (Key Message): Reddish Purple `#CC79A7` filled — human-in-the-loop checkpoint, deliberately the heaviest color because this is the load-bearing step. Node 2 (Data Structure): Sky Blue `#56B4E9` filled. Node 3 (Functional Category): Blue `#0072B2` filled. Node 4 (Specific Form): Bluish Green `#009E73` filled — the verified end state. Each node has a small white inner glyph: Node 1 a small pen-on-paper glyph; Node 2 a small grid icon; Node 3 a 2x4 small-grid icon echoing the FT eight categories; Node 4 a small bar-chart icon. Below each node, a thin Vermillion `#D55E00` 1pt callout box names the failure if the step is skipped — without Step 1, chart on a hope; without Step 2, structure mismatch; without Step 3, wrong functional category; without Step 4, software default. Bottom band: a thin Black `#000000` 0.5pt horizontal rule with a small Orange `#E69F00` filled marker indicating the worked example (humanitarian funding) walks all four steps. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Horizontal four-step decision flow — Key Message → Data Structure → Functional Category → Specific Form. Step 1 visually emphasized as the load-bearing human checkpoint. Each step has a skip-failure callout below. Bottom band marks the worked-example walk-through.
[O] Left-to-right node sequence with arrows. Failure callouts below each node. Bottom rule beneath the entire workflow.
[P] Step 1 Reddish Purple (human checkpoint). Step 2 Sky Blue. Step 3 Blue. Step 4 Bluish Green. Inner glyphs White. Skip-failure callouts Vermillion. Worked-example marker Orange.
[E] No prompt text rendered, no chart thumbnails inside the nodes, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, prompt text rendered as graphics, chart thumbnails inside nodes, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 4.3 — Three failure modes, three redesigns

**Priority: Important.** Failure-mode taxonomy made visible with before / after pairs.

### Block 1 — Illustrae paste block

A three-row composition. Each row is a before/after pair separated by a thin Black `#000000` 1pt arrow pointing right. Row 1 (Familiarity bias): Left, a small 5-slice pie circle outlined in Black 1pt, slices filled in Vermillion `#D55E00` and Orange `#E69F00` shades. Right, a sorted horizontal bar chart with 5 Bluish Green `#009E73` filled bars descending by length. Row 2 (Aesthetic-first): Left, a stylized exploded-donut shape — Vermillion-filled ring with a wedge separated outward and exaggerated thickness. Right, a flat 100% stacked bar in three Bluish Green graduated segments. Row 3 (Software-default): Left, a tangled line-chart frame with six Orange / Vermillion / Reddish Purple `#CC79A7` overlapping wavy lines suggesting rainbow palette clutter. Right, a 2x3 small-multiples grid of six tiny clean Bluish Green line charts, each in its own framed panel. Each row's left side carries a small Vermillion filled corner badge (the failure mode); each row's right side carries a small Bluish Green filled corner badge (the redesign). White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Three failure-mode rows. Row 1: familiarity bias (pie → sorted bar). Row 2: aesthetic-first (exploded donut → flat stacked bar). Row 3: software-default (rainbow tangled lines → small multiples). Each row pairs left=failure, right=redesign.
[O] Three horizontal rows, each with a before/after pair separated by a rightward arrow. Corner badges per side per row.
[P] Failure-side fills Vermillion / Orange / Reddish Purple. Redesign-side fills Bluish Green. Frames and arrows Black 1pt. Failure-mode badges Vermillion. Redesign badges Bluish Green.
[E] No real datasets, no axis numbers, no chart titles, no specific company or sector names, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, chart titles, axis numbers, dataset names, company names, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 4.4 — One dataset, three questions, three charts

**Priority: Important.** The same-data demonstration. Shows that chart type follows message, not table.

### Block 1 — Illustrae paste block

A three-panel side-by-side composition. Top label per panel post-typography, but the diagram itself shows three different chart forms of the same source dataset. Panel 1: line chart — Black `#000000` 1pt axes, a single Blue `#0072B2` 2pt line tracing a rising-then-falling temporal trend across 36 x-positions (months). Small Blue filled dots at the vertices. Panel 2: horizontal bar chart — Black 1pt axes, five Bluish Green `#009E73` filled horizontal bars sorted descending, longest at the top. Panel 3: 100% stacked column chart — three Black 1pt-framed columns (one per year), each subdivided into five horizontal segments stacked vertically, segments filled in graduated Sky Blue `#56B4E9` (lightest = food) through Blue `#0072B2` (darkest = protection). All three columns sum to the same full height. Small Reddish Purple `#CC79A7` filled corner badges per panel mark the message (post-typography label, but the badge itself indicates question-type assignment). White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Three-panel demonstration of one humanitarian funding dataset rendered three ways. Panel 1: line chart (change over time). Panel 2: horizontal sorted bar chart (comparison). Panel 3: 100% stacked column chart (part-to-whole with temporal sub-message).
[O] Three equal-sized panels side by side. Each panel framed by thin Black axes. Corner message-badges in each panel.
[P] Line chart Blue. Bar chart Bluish Green. Stacked column graduated Sky Blue → Blue. Frames Black 1pt. Message badges Reddish Purple.
[E] No real sector names rendered, no axis numbers, no chart titles, no legend graphics, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, sector names, axis numbers, chart titles, legends rendered as graphics, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 4.5 — The eight FT Visual Vocabulary functional categories

**Priority: Critical.** The navigation tool the book leans on for the rest of Part II.

### Block 1 — Illustrae paste block

A 4x2 grid of eight category cards arranged in two rows of four. Each card is a rounded rectangle with a thin Black `#000000` 1pt outline. Top row left-to-right: Comparison (Blue `#0072B2` filled), Change over time (Sky Blue `#56B4E9` filled), Distribution (Bluish Green `#009E73` filled), Relationship (Orange `#E69F00` filled). Bottom row left-to-right: Part-to-whole (Reddish Purple `#CC79A7` filled), Hierarchy (Vermillion `#D55E00` filled), Flow (Blue `#0072B2` filled with 60% opacity), Spatial (Sky Blue `#56B4E9` filled with 60% opacity). Inside each card, a small white iconic glyph distinguishes the category: Comparison a small horizontal-bar glyph; Change over time a small rising-line glyph; Distribution a small histogram glyph; Relationship a small two-axis scatter glyph; Part-to-whole a small pie-wedge glyph; Hierarchy a small nested-square treemap glyph; Flow a small arrow-with-bands Sankey glyph; Spatial a small map-outline glyph. Below each card, a thin Black `#000000` 0.5pt rule with a small Bluish Green `#009E73` filled diamond marker representing the reader's question for that category. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] 4x2 grid of FT Visual Vocabulary categories — Comparison, Change over time, Distribution, Relationship, Part-to-whole, Hierarchy, Flow, Spatial. Each card holds an iconic glyph distinguishing the category. Below each card, a reader's-question marker.
[O] Two rows of four cards. Card fills assigned per category. Iconic glyphs inside; question markers below.
[P] Comparison Blue. Change over time Sky Blue. Distribution Bluish Green. Relationship Orange. Part-to-whole Reddish Purple. Hierarchy Vermillion. Flow Blue 60%. Spatial Sky Blue 60%. Inner glyphs White. Question markers Bluish Green.
[E] No category names rendered as graphics, no chart-type lists rendered, no reader-question text, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, category names rendered as graphics, chart-type lists rendered as text, reader-question text, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 4.6 — A short history of chart-type invention, 1786–1991

**Priority: Important.** Origin-story timeline. Useful reference for the "each chart type is a solution to a specific problem" claim.

### Block 1 — Illustrae paste block

A horizontal timeline composition. A single Black `#000000` 1pt horizontal rule spans the full width, with year tick marks at 1786, 1826, 1854, 1858, 1869, 1949 / 1950s (treated as one cluster mark for Tukey's box plot), 1991. Seven event markers along the timeline, each rendered as a small filled circle of distinct Okabe-Ito hue with a thin Black 1pt connecting line rising up to a small iconic glyph: 1786 (Playfair bar / line — Blue `#0072B2` filled with a tiny bar-and-line glyph above), 1826 (Dupin choropleth — Sky Blue `#56B4E9` filled with a tiny shaded-region glyph), 1854 (Snow dot map — Bluish Green `#009E73` filled with a tiny dot-cluster glyph), 1858 (Nightingale polar area — Reddish Purple `#CC79A7` filled with a tiny rose-wedge glyph), 1869 (Minard flow — Orange `#E69F00` filled with a tiny tapering-band glyph), 1950s (Tukey box plot — Vermillion `#D55E00` filled with a tiny box-and-whisker glyph), 1991 (Shneiderman treemap — Blue `#0072B2` filled at 60% opacity with a tiny nested-rectangle glyph). The line is not even — markers cluster in the late 19th century and again in the 20th. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Horizontal timeline 1786–1991 with seven chart-type invention markers. Playfair (bar / line, 1786), Dupin (choropleth, 1826), Snow (dot map, 1854), Nightingale (polar area, 1858), Minard (flow, 1869), Tukey (box plot, mid-20th-century cluster), Shneiderman (treemap, 1991). Each marker has a distinguishing iconic glyph rising above the timeline.
[O] Horizontal axis with year tick marks. Filled-circle markers on the axis. Small iconic glyphs above each marker.
[P] Playfair Blue. Dupin Sky Blue. Snow Bluish Green. Nightingale Reddish Purple. Minard Orange. Tukey Vermillion. Shneiderman Blue 60%. Timeline rule and connectors Black 1pt.
[E] No inventor names rendered as text, no year numbers rendered as graphics, no chart titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, inventor names, year numbers rendered as graphics, chart titles, gibberish letters, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## What CAJAL Declines to Architect

- **The four-move Claude Code prompt block (lines 184–205).** Prose-format prompt specification. Not a figure.
- **The Cairo prompt block (lines 307–339).** LLM Exercise prompt template. Stays as code-style typography.
- **Calvin F. Schmid portrait (line 371).** AI Wayback Machine biographical asset. Not a CAJAL figure.
- **The eight-category bulleted list (lines 47–60).** Typography reference. The diagrammatic version is Fig 4.5.
- **The reasonable-defaults bullet list (lines 87–94).** Typography reference inside the chapter's prose; the eight category cards already encode the same lookup.

---

## Video Candidate Pass

**FIGURE 4.1 (Pie vs sorted bar):** STATIC SUFFICIENT.
**FIGURE 4.2 (Cairo's four steps):** **MILD VIDEO CANDIDATE.** Workflow / process criterion barely met — the four nodes could animate left-to-right with the skip-failure callouts fading in when the corresponding step is bypassed. Static reads in one glance; animation adds little.
**FIGURE 4.3 (Three failure modes):** STATIC SUFFICIENT.
**FIGURE 4.4 (One dataset, three charts):** **MILD VIDEO CANDIDATE.** A morph between the three forms could dramatize that the data is the same. Risk: the morph dilutes the point — the chart-type choice is the message, not a fluid transformation.
**FIGURE 4.5 (Eight FT categories):** **STRONG VIDEO CANDIDATE for an interactive companion.** As a static reference card, this is perfect. As an interactive grid where clicking a category reveals chart subtypes, this becomes the spine of the book's online companion. The static and the interactive are not competing — they serve different reading modes.
**FIGURE 4.6 (Chart-type timeline):** STATIC SUFFICIENT.

**Video candidates identified: 1 strong (interactive) + 2 mild.** Recommended: **Fig 4.5 (FT eight categories)** for the interactive companion site if one ships. Print uses static.

---

## Split-point note

This chapter is the navigational hub for Part II of the book. The eight categories in Fig 4.5 each open onto chart-family chapters (comparison → Ch 07, change over time → Ch 08, distribution → Ch 09, relationship → Ch 10, part-to-whole → Ch 11, hierarchy → Ch 12, flow → Ch 13, spatial → Ch 14, per the chapter list in the Introduction). The color assignments in Fig 4.5 should be carried forward to the part-opener pages or sidebar markers of those chapters so the reader sees Comparison-Blue when they reach the comparison chapter. The Cairo Step 1 = Reddish Purple "human checkpoint" semantics established here matches the Verify-step Reddish Purple from Chapter 02's Fig 2.5 — keep that association: Reddish Purple = the human is responsible here.
