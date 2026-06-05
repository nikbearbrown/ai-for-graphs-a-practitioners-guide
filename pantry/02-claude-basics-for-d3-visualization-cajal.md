# CAJAL Figure Intelligence — Chapter 02: Claude Basics for D3 Visualization

**Source:** `chapters/02-claude-basics-for-d3-visualization.md`
**Mode:** `/scan silent`
**Domain note:** AI+1 practitioner guide / data visualization with D3 and Claude. META-book — CAJAL figures here are abstract diagrams about the prompting workflow, NOT chart artifacts. The chapter's bar chart, scatterplot, and dashboard examples are exhibits the *reader* will build; CAJAL declines them. The chapter author placed five figures: vague-vs-specific comparison, instruction budget, four-move prompt, verification stack, and audit-prompt-build-verify workflow.

---

## Density Recommendation

**5 figures, Mechanistic density.** This is the long cut of the chapter and the foundational methodology chapter of the whole book. Each placed figure carries a different piece of the four-stage discipline (specify → budget → prompt → verify → iterate). All five earn their place.

---

## Zone Map

- **MC:** Five-decision specificity gap (Fig 2.1). The four-move prompt structure with Move 3 as the load-bearing constraint move (Fig 2.3). The three-layer verification stack (Fig 2.4). The audit-prompt-build-verify workflow (Fig 2.5).
- **VG:** Where Claude lives — four-product taxonomy. Stays in Table 2.1.
- **PQ:** Instruction budget — system prompt ~50, CLAUDE.md ~100, DESIGN.md as separate on-demand block, ~150–200 reliable-tracking ceiling (Fig 2.2). Single quantitative diagram.

---

## Figure 2.1 — Five decisions in every chart prompt

**Priority: Critical.** Opening visual claim. Same data, two prompts, five decisions delegated vs controlled.

### Block 1 — Illustrae paste block

A two-column comparison composition. Left column header: a Vermillion `#D55E00` filled rectangle (the vague-prompt side). Inside, five small Orange `#E69F00` filled rounded tiles stacked vertically — chart type, mark, channel-for-score, channel-for-domain, sort order and baseline. Right column header: a Blue `#0072B2` filled rectangle (the specific-prompt side). Inside, the identical five rounded tiles in Sky Blue `#56B4E9` filled. Connecting each pair across the columns: a thin Black `#000000` 1pt arrow with a small Bluish Green `#009E73` filled diamond at its midpoint indicating which side owns the decision — Vermillion side for the left, Blue side for the right. A single vertical Black `#000000` 1pt boundary line down the center separates the columns. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Vague vs specific prompt comparison. Five decisions per side. Left: model-decided. Right: author-controlled.
[O] Two columns separated by a vertical boundary. Five paired tiles per column, stacked vertically. Connecting arrows cross the boundary; midpoint diamonds indicate which side owns the decision.
[P] Vague-prompt header Vermillion. Vague-prompt tiles Orange. Specific-prompt header Blue. Specific-prompt tiles Sky Blue. Connecting arrows Black. Decision-side diamonds Bluish Green. Central boundary Black 1pt.
[E] No prompt text rendered as graphics, no D3 syntax, no chart thumbnails, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, prompt text rendered as graphics, code snippets, D3 syntax, chart thumbnails, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 2.2 — The instruction budget

**Priority: Critical.** Quantifies the budget claim. Two-bar comparison showing split-file vs merged-file overflow.

### Block 1 — Illustrae paste block

A two-row composition of horizontal stacked bars representing the 150–200 instruction tracking ceiling. Top row: the split-file scenario. A horizontal bar divided into three segments — Blue `#0072B2` filled (Anthropic system prompt, ~50 instructions), Sky Blue `#56B4E9` filled (`CLAUDE.md` coding rules, ~100 instructions). To the right of the same row, separated by a small gap, an independent shorter bar in Bluish Green `#009E73` filled (`DESIGN.md`, ~30–50 instructions, on-demand). A vertical Black `#000000` 1pt dashed line at the right edge of the combined Blue + Sky Blue portion marks the reliable-tracking ceiling. The split-file row fits within ceiling; the on-demand block sits separately. Bottom row: the merged-file scenario. A single horizontal bar with the same Blue system-prompt segment, then Sky Blue, then a continuing Vermillion `#D55E00` filled segment (merged coding + design rules) that extends past the dashed ceiling line. The overflow zone past the ceiling is filled with Vermillion at 25% opacity diagonal hatching (the degradation zone). Reddish Purple `#CC79A7` short marker tick on the bottom bar at the line-100 position indicates where reliability begins to fall. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Two horizontal stacked bars comparing instruction budget consumption. Top: split (system + CLAUDE.md within ceiling, DESIGN.md separate on-demand). Bottom: merged (system + combined rules overflowing ceiling, overflow zone hatched). Single ceiling line at ~150–200 tracking limit.
[O] Top bar at top, bottom bar below, sharing a vertical ceiling reference. On-demand DESIGN.md block sits to the right of the top bar, separated by a gap.
[P] System prompt Blue. CLAUDE.md Sky Blue. DESIGN.md Bluish Green. Merged-overflow Vermillion. Hatched overflow zone Vermillion 25%. Degradation tick Reddish Purple. Ceiling line Black 1pt dashed.
[E] No specific instruction counts rendered as text, no D3 syntax, no Anthropic logos or brand assets, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, instruction counts rendered as numbers, brand logos, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 2.3 — The four-move prompt

**Priority: Critical.** Move 3 is the highest-leverage methodology claim in the chapter.

### Block 1 — Illustrae paste block

A vertical four-panel composition, each panel one move, connected top-to-bottom by Black `#000000` 1pt arrows. Panel 1 (Show): Sky Blue `#56B4E9` filled rounded rectangle containing a small Blue `#0072B2` filled grid icon (data shape). Panel 2 (Say): Sky Blue rounded rectangle containing a small Blue filled rectangle-with-bars icon (chart-type pick). Panel 3 (Constrain): rendered as the load-bearing move — a larger Blue `#0072B2` filled rounded rectangle with a thicker Black `#000000` 2pt border, containing four small Bluish Green `#009E73` filled tiles (mark, channel, layout, accessibility). Panel 4 (Verify): Sky Blue rounded rectangle containing a small Reddish Purple `#CC79A7` filled checkmark glyph. Right-side rail beside each panel: a thin Vermillion `#D55E00` 1pt callout box (one per panel) representing the failure mode triggered if the move is skipped — Move 1 callout points to data-shape guess, Move 2 to chart-type mismatch, Move 3 to channel mismatch (Vermillion at full opacity, heaviest), Move 4 to silent specification drift. White background, flat vector, single-column 89mm preferred.

### Block 2 — Full SCOPE prompt

[S] Single-column 89mm, vector, white background.
[C] Four vertically stacked move panels (Show, Say, Constrain, Verify) connected by arrows. Move 3 visually emphasized — larger panel, heavier border. Each panel has a paired skip-failure callout on the right.
[O] Vertical cascade top-to-bottom. Side rail of failure callouts on the right, one per panel.
[P] Move panels Sky Blue. Move 3 Blue with thicker border. Move 3 sub-tiles Bluish Green. Verify checkmark Reddish Purple. Failure-mode callouts Vermillion. Connecting arrows Black 1pt.
[E] No prompt text rendered as graphics, no specific D3 code, no example bar chart, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, prompt text rendered as graphics, code snippets, D3 syntax, chart thumbnails, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 2.4 — The three-layer verification stack

**Priority: Important.** Encodes the discipline that prevents shipping wrong charts.

### Block 1 — Illustrae paste block

A vertical three-layer stack composition, each layer a wide rounded horizontal rectangle, stacked top-to-bottom with graduated luminance — top layer (Layer 1, format check) Sky Blue `#56B4E9` filled with 20% opacity (lightest), middle layer (Layer 2, fact check) Sky Blue at 50% opacity, bottom layer (Layer 3, test the work) Blue `#0072B2` filled (darkest). Each layer contains three small Bluish Green `#009E73` filled tiles representing what the layer checks — format tiles (file, version, inline CSS), fact tiles (values, labels, palette, encoding), test tiles (browser, resize, color-blind sim). Side rail to the right: vertical "catches earlier failures first" gradient bar in graduated Sky Blue → Blue. Small Vermillion `#D55E00` filled tick marks on the left of each layer indicating approximate time-cost (1 tick → 3 ticks → 5 ticks). Below the stack: a thin Reddish Purple `#CC79A7` 1pt horizontal rule with a Vermillion arrow pointing rightward labeled (post-typography) "do them in order; don't skip ahead." White background, flat vector, single-column 89mm preferred.

### Block 2 — Full SCOPE prompt

[S] Single-column 89mm, vector, white background.
[C] Three-layer verification stack — Layer 1 (format), Layer 2 (facts), Layer 3 (test). Stacked vertically with graduated luminance. Each layer carries three check tiles. Right rail indicates ordering / coverage. Left ticks indicate time cost per layer.
[O] Top-to-bottom stack of three layers. Side rail on the right. Tick marks on the left of each layer.
[P] Layer 1 Sky Blue 20%. Layer 2 Sky Blue 50%. Layer 3 Blue. Layer check-tiles Bluish Green. Time-cost ticks Vermillion. Bottom ordering rule Reddish Purple.
[E] No specific D3 code, no browser screenshots, no real chart artifacts, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, browser screenshots, code snippets, D3 syntax, chart thumbnails, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 2.5 — Audit, prompt, build, verify

**Priority: Important.** Encodes the four-stage workflow as a single horizontal sequence.

### Block 1 — Illustrae paste block

A horizontal four-stage workflow composition. Four rounded rectangle nodes arranged left-to-right, connected by Black `#000000` 1pt arrows: Audit (Sky Blue `#56B4E9` filled), Prompt (Blue `#0072B2` filled), Build (Bluish Green `#009E73` filled), Verify (Reddish Purple `#CC79A7` filled). Each node has a small white inner icon — Audit: a small magnifying-glass glyph; Prompt: a small four-tile glyph echoing Figure 2.3; Build: a small file-output glyph; Verify: a small layered-stack glyph echoing Figure 2.4. Beneath each node, a thin Vermillion `#D55E00` 1pt callout box names the failure mode triggered if that stage is skipped — without audit, channel guessing; without prompt, vague specification; without build, no artifact; without verify, ship on hope. Bottom band: a thin Black `#000000` 0.5pt horizontal rule labeled (post-typography) "the cognitive-domain scatterplot example walks all four stages." White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Horizontal four-stage workflow — Audit, Prompt, Build, Verify — connected by arrows. Each stage has a paired skip-failure callout. Bottom band marks the worked-example walk-through.
[O] Left-to-right node sequence with arrows. Failure callouts below each node. Bottom rule beneath the entire workflow.
[P] Audit Sky Blue. Prompt Blue. Build Bluish Green. Verify Reddish Purple. Inner glyphs White. Skip-failure callouts Vermillion. Bottom rule Black.
[E] No real chart thumbnails, no real prompt text, no D3 code, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, prompt text rendered as graphics, chart thumbnails, code snippets, D3 syntax, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## What CAJAL Declines to Architect

- **The opening example bar chart and scatterplot.** Reader artifacts. The book teaches the reader to build them; CAJAL does not render them as figures.
- **Table 2.1 — Where Claude lives.** Four-product, four-column typography reference. Stays a table.
- **The code-style box showing CLAUDE.md / DESIGN.md loading rules (lines 77–83).** Code-style typography. Folded into Figure 2.2 conceptually.
- **The audit prompt block (lines 228–247).** Prose with embedded prompt text. Not a figure.
- **Table of failure modes (lines 170–174).** Three-row four-column typography reference — stays a table.
- **Margaret Hamilton portrait (line 450).** Photographic asset, not a CAJAL figure.

---

## Video Candidate Pass

**FIGURE 2.1 (Five decisions):** STATIC SUFFICIENT.
**FIGURE 2.2 (Instruction budget):** STATIC SUFFICIENT. The overflow ceiling is the point and is visible at a glance.
**FIGURE 2.3 (Four-move prompt):** STATIC SUFFICIENT. Sequence is read top-to-bottom; animation adds nothing.
**FIGURE 2.4 (Verification stack):** STATIC SUFFICIENT. Layered stack is conceptual, not temporal.
**FIGURE 2.5 (Audit-prompt-build-verify workflow):** **MILD VIDEO CANDIDATE.** Process / workflow criterion barely met — the four stages could animate left-to-right with each failure callout fading in when its stage is skipped. But the static version reads in one glance, so animation is decorative rather than load-bearing.

**Video candidates identified: 1 mild.** Recommended: prefer static unless the book ships an interactive companion site.

---

## Split-point note

Five figures inside one chapter is dense; this is the methodological foundation of the book and the density is earned. The Blue / Sky Blue / Vermillion / Bluish Green / Orange / Reddish Purple Okabe-Ito palette assignments here become the book's house style — Blue for author-controlled and code-side, Vermillion for failure modes and risk, Bluish Green for verified / passing, Reddish Purple for human-in-the-loop checkpoints. Maintain these semantic associations across Chapter 03 (marks and channels), Chapter 04 (chart selection), and beyond. This chapter near-duplicates `02-claude-basics-for-d3-visualization-updated.md` (which keeps only Figure 2.1). Editorial decision required.
