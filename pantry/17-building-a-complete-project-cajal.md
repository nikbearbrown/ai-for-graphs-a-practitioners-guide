# CAJAL Figure Intelligence — Chapter 17: Building a Complete Project

**Source:** `chapters/17-building-a-complete-project.md`
**Mode:** `/scan silent`
**Domain note:** AI+1 practitioner guide / data visualization with D3 and Claude. Final chapter integrates the entire book into a five-phase pipeline (Audit → Schema → Generate → Verify → Handoff) applied to a worked UNHCR forced-displacement project. Five author-placed figures.

---

## Density Recommendation

**5 figures, Pipeline-integration density.** All five earn their place. The chapter's argument is the pipeline itself; each figure is one node of it (Phase A documentation, schema files, three-chart sequence, audit log, handoff package). The fifth figure (handoff with provenance) is the proof of "publishable."

---

## Zone Map

- **MC:** The five-phase pipeline (A Audit → B Schema → C Generate → D Verify → E Handoff), looping back via Cairo's purpose test. Question precedes data. The schema split (CLAUDE.md / DESIGN.md / PROJECT.md). A project is a sequence of charts, not a collection.
- **VG:** The pipeline flow itself. The three-question / data-audit / gap structure. The three-chart family sequence (heatmap, horizontal bar, stacked bar). The publication package with provenance blocks.
- **PQ:** Five phases. Three questions. ~5,000 rows in the UNHCR dataset. Three charts. 22-point checklist applied per chart. Three iteration rounds (v1, v2, v3, Final) in the audit log.

---

## Figure 17.1 — Five-Phase Pipeline

**Priority: Critical.** The chapter's structural figure. Must read as a pipeline at a glance.

### Block 1 — Illustrae paste block

A horizontal flow diagram. Five rounded-rectangle phase nodes arranged left-to-right: Phase A (Audit) Sky Blue `#56B4E9` filled, Phase B (Schema) Blue `#0072B2` filled, Phase C (Generate) Bluish Green `#009E73` filled, Phase D (Verify) Orange `#E69F00` filled, Phase E (Handoff) Reddish Purple `#CC79A7` filled. Each node is the same size and rendered with a Black `#000000` 0.5pt outline. Black 1pt arrows connect each node left-to-right. At the far right, a sixth element — a Vermillion `#D55E00` outlined rounded rectangle slightly larger — represents "Published artifact". A dashed Bluish Green 0.75pt curved arrow loops from the published-artifact node back to Phase A, indicating Cairo's purpose-test return. Below each phase node, a small Black 0.5pt vertical tick suggests the deliverable each phase produces (no text rendered). White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Five-phase pipeline (Audit, Schema, Generate, Verify, Handoff) flowing left-to-right into a sixth Published Artifact node. A dashed loop returns from the artifact to Phase A, representing Cairo's purpose test.
[O] Horizontal flow. Equal-sized phase nodes. Published artifact node slightly larger. Loop arrow above or below.
[P] Phase A Sky Blue, Phase B Blue, Phase C Bluish Green, Phase D Orange, Phase E Reddish Purple. Published artifact Vermillion outlined. Flow arrows Black 1pt. Return loop Bluish Green dashed 0.75pt. Deliverable ticks Black 0.5pt.
[E] No phase names rendered, no deliverable names, no chapter cross-reference labels, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, phase names, deliverable names, chapter references, project names, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 17.2 — Phase A Documentation (Questions, Audit, Gaps)

**Priority: Important.** Shows that Phase A produces documentation, not charts. Three panels for three deliverables.

### Block 1 — Illustrae paste block

A three-panel vertical-stack composition. Panel 1: three rounded-rectangle question cards stacked vertically, each Sky Blue `#56B4E9` filled with a Black `#000000` 0.5pt outline, each containing a small Blue `#0072B2` filled circular badge indicating question rank (1, 2, 3 implied by position). Panel 2: a simplified column-audit table glyph — a grid of small rectangles representing columns, each rectangle tagged with one of three Okabe-Ito badge colors indicating data type — Bluish Green `#009E73` for categorical, Orange `#E69F00` for temporal, Blue `#0072B2` for quantitative. Below the grid, four small Black 0.5pt outlined relationship icons (comparison, change-over-time, part-to-whole, spatial) sit in a row. Panel 3: a single Vermillion `#D55E00` outlined rounded rectangle labeled implicitly as the identified gap, with a small Vermillion 1pt "no" icon (a slashed circle) overlaid. White background, flat vector, single-column 89mm.

### Block 2 — Full SCOPE prompt

[S] Single-column 89mm, vector, white background.
[C] Phase A deliverables: three reader-focused questions (top panel), a data-audit grid showing categorical/temporal/quantitative typing plus supported relationships (middle panel), and an identified gap the data cannot support (bottom panel).
[O] Three stacked panels top-to-bottom.
[P] Question cards Sky Blue with Blue badges. Audit-grid type badges Bluish Green / Orange / Blue. Relationship icons Black 0.5pt outlined. Gap rectangle Vermillion with Vermillion slashed-circle.
[E] No question text, no column names, no relationship names, no gap description, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, question text, column names, relationship names, gap descriptions, dataset names, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 17.3 — The Schema Split (CLAUDE.md / DESIGN.md)

**Priority: Important.** Visualizes the instruction-budget reasoning behind the two-file split.

### Block 1 — Illustrae paste block

A two-column composition with a dashed vertical boundary. Left column: a stack of rule-card rectangles representing CLAUDE.md content — eight small Blue `#0072B2` filled rounded rectangles stacked vertically, each with a Black `#000000` 0.5pt outline. A small Bluish Green `#009E73` filled "always-load" badge sits at the top-left of the column. Right column: a stack of rule-card rectangles representing DESIGN.md content — eight small Sky Blue `#56B4E9` filled rounded rectangles stacked vertically, also with Black 0.5pt outlines. A small Orange `#E69F00` filled "visual-decision-only" badge sits at the top-left of the column. The dashed vertical boundary between columns is Black 0.75pt dashed, with a small Reddish Purple `#CC79A7` filled annotation glyph indicating the instruction-budget reason. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Two-column session-loading diagram. Left column: CLAUDE.md rules that load every session. Right column: DESIGN.md rules that load only on visual-decision sessions. A dashed boundary between them names the instruction-budget reason.
[O] Two vertical columns of stacked rule cards, with a dashed vertical boundary between them and a top-of-column badge for each.
[P] CLAUDE.md cards Blue with Bluish Green always-load badge. DESIGN.md cards Sky Blue with Orange visual-decision-only badge. Card outlines Black 0.5pt. Boundary Black 0.75pt dashed. Instruction-budget glyph Reddish Purple.
[E] No rule text, no file names rendered, no badge text, no boundary text, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, rule text, file names, badge text, boundary text, prose, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 17.4 — Three Charts, Three Families

**Priority: Critical.** The Phase C output. Three charts side-by-side answering the three questions.

### Block 1 — Illustrae paste block

A three-panel horizontal composition showing three small charts of the same UNHCR data, one per question. Panel 1 (Q1 heatmap): a 5×8 grid of small rectangles — 8 origin-country rows and 5 year columns — each cell filled with a single-hue Blue luminance value ranging from pale Sky Blue `#56B4E9` for low counts to deep Blue `#0072B2` for high counts. Rows are sorted by row-mean descending (top row darkest overall). A small Black `#000000` 0.5pt frame outlines the grid. Panel 2 (Q2 horizontal bars): eight horizontal Blue `#0072B2` filled bars of varying lengths from a left-aligned zero baseline, sorted by length descending (longest bar at top). Small Orange `#E69F00` filled dots at each bar's right end indicate direct value labels (no text). A Black 0.5pt y-axis line on the left and a Black 0.5pt x-axis line at the bottom. Panel 3 (Q3 two-segment stacked bar): a single horizontal bar with two segments — a larger Bluish Green `#009E73` filled segment on the left (internal displacement) and a smaller Reddish Purple `#CC79A7` filled segment on the right (international). Small Orange filled dots inside each segment indicate the percentage label position. A Black 0.5pt outline around the full bar. Below each panel, a small Vermillion `#D55E00` outlined badge identifies the chart family. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Three small charts answering three questions: heatmap (origin country × year), horizontal bar chart (destination ranking), two-segment stacked bar (internal vs. international). Each panel labeled below with a chart-family badge.
[O] Three horizontal panels left-to-right. Each panel sized similarly. Family badges below.
[P] Heatmap luminance Sky Blue → Blue. Bar chart Blue bars with Orange value dots. Stacked bar Bluish Green / Reddish Purple segments with Orange label dots. Axes Black 0.5pt. Family badges Vermillion outlined.
[E] No country names, no year numbers, no count values, no percentage labels, no panel titles, no axis labels, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, country names, year numbers, count values, percentage labels, panel titles, axis labels, legend, gibberish letters, captions, decorative ornament, photographic elements, realistic textures, drop shadows, gradient fills (only sequential luminance inside heatmap cells as the encoding), gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 17.5 — Publication Handoff Package

**Priority: Important.** Phase E proof — a chart is not published until provenance and reproduction live with it.

### Block 1 — Illustrae paste block

A vertically stacked composition. Top: a chart card containing a clean horizontal bar chart (echoing Figure 17.4 Panel 2 but standalone) — eight Blue `#0072B2` filled bars sorted descending from a zero baseline, with Black `#000000` 0.5pt axes and light Black 0.25pt gridlines. Small Orange `#E69F00` filled dots indicate direct labels. Above the chart, a small Bluish Green `#009E73` filled placeholder rectangle suggests title-and-subtitle typography. Below the chart, three side-by-side Vermillion `#D55E00` outlined rounded rectangles represent provenance blocks (source citation, methodology note, accessibility metadata). Below the provenance row, a slightly larger Reddish Purple `#CC79A7` outlined panel represents the project manifest — inside, six small Sky Blue `#56B4E9` filled file-card glyphs (three chart HTMLs, CLAUDE.md, DESIGN.md, PROJECT.md, README.md — six glyphs total) arranged in a single row. Each file-card has a Black 0.5pt outline. White background, flat vector, single-column 89mm preferred (vertical orientation).

### Block 2 — Full SCOPE prompt

[S] Single-column 89mm, vector, white background, vertical orientation.
[C] Publication package: a clean horizontal bar chart at the top, three provenance blocks below (source, methodology, accessibility), and a project manifest panel showing six file-card glyphs (three chart HTMLs, CLAUDE.md, DESIGN.md, PROJECT.md, README.md).
[O] Vertical stack — title/subtitle band, chart, provenance row, manifest panel.
[P] Bars Blue, value dots Orange, axes Black 0.5pt, gridlines Black 0.25pt. Title/subtitle band Bluish Green. Provenance blocks Vermillion outlined. Manifest panel Reddish Purple outlined. File-card glyphs Sky Blue with Black 0.5pt outlines.
[E] No chart title text, no axis labels, no provenance block text, no file names, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, chart title text, axis labels, provenance block text, file names, country names, value numbers, gibberish letters, captions, decorative ornament, photographic elements, realistic textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## What CAJAL Declines to Architect

- **The iteration / audit log table (lines 151–158).** Typography reference table — version / date / change / audit-item-fixed. Belongs as a layout table.
- **PROJECT.md designer-layer / technical-layer split.** Discussed verbally; no author figure called for. If added later, would mirror Figure 17.3's two-column treatment.
- **The README contents.** Discussed verbally; no figure called for.
- **Buckminster Fuller AI Wayback portrait.** Existing AI-generated portrait reference, not a CAJAL architectural target.

---

## Video Candidate Pass

**FIGURE 17.1 (Five-phase pipeline):** **MILD VIDEO CANDIDATE.** Animating the pipeline — each phase node lighting up in sequence, the Cairo loop-back arrow appearing only when the purpose test fails — would make the iteration-loop nature visible. Static version is already strong.
**FIGURE 17.2 (Phase A documentation):** STATIC SUFFICIENT.
**FIGURE 17.3 (Schema split):** STATIC SUFFICIENT.
**FIGURE 17.4 (Three charts):** STATIC SUFFICIENT.
**FIGURE 17.5 (Handoff package):** STATIC SUFFICIENT.

**Video candidates identified: 0 strong + 1 mild.** Recommended: hold; this is a synthesis chapter and the static pipeline diagram is the cleaner instructional artifact. The "loop closes" idea is already legible from Figure 17.1's dashed return arrow.

---

## Split-point note

Chapter integrates every prior chapter: Chapter 03 (data audit, channel choice), Chapter 04 (chart follows the question), Chapter 05 (Claude Code as executor), Chapters 06–14 (chart families), Chapter 15 (specialized forms), Chapter 16 (Evergreen/Emery 22-point checklist). Figures here must share a visual language with every prior chapter's figures — same Okabe-Ito palette, same flat-vector treatment, same stroke weights. Figure 17.4's three small charts should look like reductions of canonical examples from Chapters 06, 08, and 11. Figure 17.5's chart card should match the "AFTER" panel of Figure 16.4 — this is the chapter where every visual decision must echo the synthesis it embodies.
