# CAJAL Figure Intelligence — Chapter 02: Claude Basics for D3 Visualization (updated)

**Source:** `chapters/02-claude-basics-for-d3-visualization-updated.md`
**Mode:** `/scan silent`
**Domain note:** AI+1 practitioner guide / data visualization with D3 and Claude. META-book — CAJAL figures here are abstract diagrams about the prompting workflow, NOT chart artifacts. The chapter's example bar chart and scatterplot are exhibits the *reader* will build; CAJAL declines them. The figures that earn their place are: the five-decision vague-vs-specific comparison, and the instruction-budget diagram.

---

## Density Recommendation

**1 figure, Sparse density.** This is the shortened "updated" cut of Ch 02. Only the vague-vs-specific prompt comparison (called out in the source as Figure 2.1) is essential. The instruction-budget diagram and four-move prompt diagram live in the longer cut (`02-claude-basics-for-d3-visualization.md`); the updated cut drops them. Architect only the figure the author placed.

---

## Zone Map

- **MC:** Specificity gap — the same data prompted vaguely returns a bad chart; prompted specifically, returns a good one. Five decisions (chart type, mark, channels-for-score, channels-for-domain, sort order / baseline) are either model-decided or author-controlled.
- **VG:** Where Claude lives — four-product taxonomy (Code / chat / Chrome / API). Belongs in the table, not a figure.
- **PQ:** Instruction budget — ~50 system prompt + remainder for user rules out of 150–200 reliably tracked. This is real and quantitative, but the updated cut treats it in prose only. The diagram lives in the longer version.

---

## Figure 2.1 — Five decisions in every chart prompt

**Priority: Critical.** The chapter's load-bearing visual claim. The whole rest of the book leans on the reader understanding what "specificity" actually means.

### Block 1 — Illustrae paste block

A two-column comparison composition. Left column header: a Vermillion `#D55E00` filled rectangle (the vague-prompt side). Inside, five small Orange `#E69F00` filled rounded tiles stacked vertically, each representing one decision the model made on its own — chart type, mark, channel-for-score, channel-for-domain, sort order and baseline. Right column header: a Blue `#0072B2` filled rectangle (the specific-prompt side). Inside, the identical five rounded tiles, this time in Sky Blue `#56B4E9` filled — same decisions, now author-controlled. Connecting each pair across the columns: a thin Black `#000000` 1pt arrow with a small Bluish Green `#009E73` filled diamond at its midpoint indicating which side of the boundary the decision sits on for that prompt. Five arrows, five diamonds, all sitting on the Vermillion side for the left column and the Blue side for the right column. A single vertical Black `#000000` 1pt boundary line down the center separates the columns. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Vague vs specific prompt comparison. Five decisions per side. Left side: model-decided. Right side: author-controlled. Decisions pair across the boundary.
[O] Two columns separated by a vertical boundary. Five paired tiles per column, stacked vertically. Connecting arrows cross the boundary; midpoint diamonds indicate which side owns the decision.
[P] Vague-prompt header Vermillion. Vague-prompt tiles Orange. Specific-prompt header Blue. Specific-prompt tiles Sky Blue. Connecting arrows Black. Decision-side diamonds Bluish Green. Central boundary Black 1pt.
[E] No specific D3 syntax, no prompt text rendered as graphics, no chart-thumbnail previews, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, prompt text rendered as graphics, code snippets, D3 syntax, chart thumbnails, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## What CAJAL Declines to Architect

- **The example bar chart and scatterplot from the opening scene.** Reader artifacts. The book teaches the reader to build these; CAJAL does not render them as figures inside the chapter.
- **Table 2.1 — Where Claude lives.** Typography reference table comparing four products across four columns. Stays a table.
- **The code block showing `CLAUDE.md` vs `DESIGN.md` loading rules (lines 80–86).** Code-style typography, not a figure.
- **The instruction-budget diagram (Figure 2.2 in the long cut).** Belongs in the longer chapter file, not this updated cut. The updated cut deliberately drops it.
- **The four-move prompt diagram (Figure 2.3 in the long cut).** Same — lives in the long cut.

---

## Video Candidate Pass

**FIGURE 2.1 (Five decisions):** STATIC SUFFICIENT. The taxonomy of five decisions across a boundary is the point. No mechanism animates.

**Video candidates identified: 0.**

---

## Split-point note

This chapter has a near-duplicate (`02-claude-basics-for-d3-visualization.md`) with three additional figures (instruction budget, four-move prompt, verification stack, audit-prompt-build-verify workflow). If both files are kept in production, Figure 2.1 should be visually identical across both cuts so the reader who reads either gets the same diagram. The "updated" suffix suggests this is the shorter / more recent revision; the longer file's extra figures are the diagrams the author cut. Decision is editorial, not CAJAL's.
