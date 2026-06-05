# CAJAL Figure Intelligence — Chapter 18: The Brutalist Claude Project

**Source:** `chapters/18-brutalist-claude-project.md`
**Mode:** `/scan silent`
**Domain note:** AI+1 practitioner guide / data visualization with D3 and Claude. This chapter is an appendix-style installation manual — most of its body is a single pasteable system prompt for a Claude Project. CAJAL-eligible figures explain the architecture the prompt enforces: the three governing files, and the five-phase gate.

---

## Density Recommendation

**2 figures, Schematic density.** The system-prompt text is the chapter's product, not its argument. The argument is structural: three files govern, five phases gate. Both are taxonomic relationships that a diagram clarifies faster than the prose around them. Avoid architecting anything inside the prompt itself — the prompt is typography.

---

## Zone Map

- **MC:** Phase cascade Audit → Schema → Generate → Verify → Handoff, with a real gate between each pair. The schema is built before generation; nothing ships without explicit human acceptance.
- **VG:** Three-file constitutional split — `CLAUDE.md` governs the stack, `DESIGN.md` governs appearance, `PROJECT.md` governs intent + technical state. The project sits inside this trio.
- **PQ:** Five phases. Three files. Two PROJECT.md layers (Intent + Technical). One principle (maximally informed, minimally autonomous). These are taxonomy counts, not data quantities.

---

## Figure 18.1 — The Three Governing Files

**Priority: Important.** The chapter's central architectural claim. Readers need to see that the three files surround the project — not sit beside it — and that PROJECT.md has two distinct layers.

### Block 1 — Illustrae paste block

A centred composition. A central Black `#000000` 1pt square labeled positionally as the project (left empty — no text in image). Three outer panels surround it, each connected to the centre by a Black `#000000` 1pt orthogonal line. Top panel (CLAUDE.md, the coding constitution): a Blue `#0072B2` filled rectangle with a small notched corner suggesting a code file. Right panel (DESIGN.md, the visual constitution): a Reddish Purple `#CC79A7` filled rectangle. Bottom panel (PROJECT.md, the project state): an Orange `#E69F00` filled rectangle subdivided by a single horizontal Black 1pt line into two stacked sub-panels — the upper sub-panel (Layer 1, intent) and the lower (Layer 2, technical). Around the entire trio runs a thin Bluish Green `#009E73` 1pt dashed outer frame representing the principle ("maximally informed, minimally autonomous") that encloses the architecture. White background, flat vector, single-column 89mm.

### Block 2 — Full SCOPE prompt

[S] Single-column 89mm, vector, white background.
[C] Central project square surrounded by three governing-file panels. CLAUDE.md top, DESIGN.md right, PROJECT.md bottom. PROJECT.md is subdivided into two stacked layers.
[O] Centred composition. Three orthogonal connection lines from project to each file. Outer dashed frame encloses the trio.
[P] CLAUDE.md Blue. DESIGN.md Reddish Purple. PROJECT.md Orange with internal Black divider. Connections and project frame Black 1pt. Outer principle frame Bluish Green 1pt dashed.
[E] No file names rendered as text, no field-by-field contents shown, no decorative ornament, no shadows, no gradients.

### Block 3 — Negative prompt

text labels, file names, field contents, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 18.2 — The Five-Phase Gate

**Priority: Important.** The operational claim. Each phase ends in a gate that must be confirmed by the human; the gate is real, not a suggestion.

### Block 1 — Illustrae paste block

A horizontal cascade composition. Five sequential panels left to right — each panel a Sky Blue `#56B4E9` filled rounded rectangle (phase block). Between every adjacent pair of panels, a small Vermillion `#D55E00` filled diamond sits on the connecting line — the gate marker. A Black `#000000` 1pt arrow runs through each gate diamond, but the diamond visibly interrupts the line, suggesting "must pass through". The phases left to right: Audit (smallest, leftmost), Schema (larger, contains three small internal squares to indicate it produces the three files — Blue, Reddish Purple, Orange small filled squares), Generate (subdivided by Black 1pt vertical lines into multiple narrow internal columns to suggest one-unit-at-a-time output), Verify (contains a small Bluish Green `#009E73` checkmark glyph and a small Vermillion `#D55E00` flag glyph side by side), Handoff (rightmost, narrowest, with a small Black 1pt outline lock glyph). Below the cascade, a Bluish Green `#009E73` 1pt horizontal underline runs the full width with a single small Black `#000000` arrowhead at the right end, suggesting the human-confirmation throughline. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Five-panel left-to-right phase cascade — Audit, Schema, Generate, Verify, Handoff — with a Vermillion gate diamond between every adjacent pair. Each phase carries one internal visual signature: Schema shows three coloured squares, Generate shows internal columns, Verify shows a check + a flag, Handoff shows a lock outline.
[O] Horizontal cascade. Gate diamonds interrupt the connecting line. Human-confirmation throughline runs beneath.
[P] Phase panels Sky Blue. Gate diamonds Vermillion. Internal Schema files Blue/Reddish Purple/Orange. Verify check Bluish Green. Verify flag Vermillion. Throughline Bluish Green underline. Outlines Black 1pt.
[E] No phase names rendered, no gate condition text, no decorative ornament, no shadows, no gradients.

### Block 3 — Negative prompt

text labels, phase names, gate condition text, command names, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## What CAJAL Declines to Architect

- **The full system prompt body.** Code/prose typography. The pasteable block is the chapter's product and lives in a fenced code region; it is not a CAJAL figure.
- **The command reference table (`/list` block).** A typography table. Render in print typography, not as a graphic.
- **Per-command flow charts (`/init`, `/research`, `/claude`, `/design`, `/project`, `/update`, `/verify`, `/handoff`).** Each is a sub-process inside the broader cascade. The cascade figure handles the architecture; individual command flows would multiply figure count without earning their place in a single-chapter book section.
- **The Phase Gate verbatim text examples.** Sample dialogue. Typography.
- **AI Wayback Machine — Le Corbusier portrait.** Already an AI-generated portrait file referenced in the chapter. Out of CAJAL scope.
- **The "Three suggested titles" list.** Editorial scaffolding.
- **Hard-NOs and Pushback-Layer examples.** These are voice/persona specifications inside the prompt — typography.

---

## Video Candidate Pass

**FIGURE 18.1 (Three governing files):** STATIC SUFFICIENT.
**FIGURE 18.2 (Five-phase gate):** **MILD VIDEO CANDIDATE.** A short animation walking through one project — Audit lights up, then a gate confirmation pulse, then Schema produces the three files (small squares appear one at a time), then Generate, then Verify check/flag, then Handoff lock click — dramatizes the "the gate is real" claim and the one-unit-at-a-time discipline. The argument works statically; the motion adds rhythm.

**Video candidates identified: 0 strong + 1 mild.** Recommended: keep both static for print. If the book ships a digital companion, the Fig 18.2 walk-through is a natural 8–12 second educational loop.

---

## Split-point note

Chapter is an appendix delivering the working tool that the rest of the book has argued toward. The CAJAL figures are intentionally architectural, not operational — the operational view is the system prompt itself, and the prompt does not need to be diagrammed because the reader copies it directly. Keep the figure budget tight here: two diagrams that name the architecture, no more. The seven-tier taxonomy referenced by the connecting "fundamental themes" chapter belongs there, not here.
