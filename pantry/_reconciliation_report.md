# Reconciliation Report — AI for Graphs

**Generated:** 2026-05-18
**Auditor:** Reverse-engineering pass over `chapters/` against the TIKTOC.md just produced.
**Status:** Findings only. No file moves yet — that is the rewrite pass.

---

## 1. Duplicate 02 chapters

- **File A:** `chapters/02-claude-basics-for-d3-visualization.md` — 5,899 words. Full chapter. Opening case (2:14 PM, eight cognitive domain scores, vague vs. specific prompt), section flow through Where Claude lives → Instruction budget → Four-move prompt → Three failure modes → Multi-LLM comparison → Verification stack → Worked example → What you can now do → Exercises (Warm-up / Application / Synthesis / Challenge) → A note about AI → LLM Exercise (`CLAUDE.md` + `DESIGN.md`) → Further reading → AI Wayback Machine (Margaret Hamilton). Complete with image references and tagged.
- **File B:** `chapters/02-claude-basics-for-d3-visualization-updated.md` — 1,350 words. Partial.

**Comparison.** File B is byte-for-byte identical to File A up to roughly the end of the "Three notes specific to D3" section, then truncates. The only substantive change is the insertion of two `infographic-table` placeholder blocks (`Figure 2.1` and `Figure 2.2`) — both blocks contain the same skeleton:

```
| | **Property** | **Value** |
|---|---|---|
| **Row 1** | _fill in_ | _fill in_ |
| **Row 2** | _fill in_ | _fill in_ |

: {.infographic-table}
```

These look like a mechanical pre-processing step — a build script's attempt to convert HTML `<!-- → [INFOGRAPHIC: ...] -->` author comments into pandoc-style table placeholders. The pre-processor ran on the opening comparison figure and on the products table, then stopped (or was halted) partway through the chapter. The placeholders are empty templates, not actual content — `_fill in_` is unedited.

**Why the -updated version was made.** Best inference: someone is experimenting with how the book's infographic comments should be rendered in the compiled output. The `-updated` file is the work-in-progress, not a content revision. There is no editorial change to the prose itself.

**Recommendation.** Keep `chapters/02-claude-basics-for-d3-visualization.md` (File A) as canonical. **Archive** `chapters/02-claude-basics-for-d3-visualization-updated.md` to `_working/` or delete. The infographic-table conversion experiment should be handled at the build-script layer (in `build.sh` or a separate filter), not by maintaining a parallel draft. If the conversion approach is settled, the build script should run it on canonical files; if not, the experiment belongs outside `chapters/` where it cannot be mistaken for a content draft.

---

## 2. Duplicate 18 chapters

- **File A:** `chapters/18-arc-diagram.md` — 1,468 words. Two purposes braided into one file:
  1. The header reads `# Part II — Examples` and contains a one-paragraph framing statement for an alphabetical catalog of "sixty-one chart types." This is the **catalog section opener**, not the arc diagram entry itself.
  2. Below the framing paragraph, the first catalog entry begins: `# Arc Diagram`, with subtitle "Co-occurrence reveals who shares the most scenes," subsections (What this chart type is / How to read this chart / Why arc diagrams — not force-directed graphs / Strengths and limitations / Framework reference / About this example / Prompt / Original code link / AI Wayback Machine with Leonhard Euler).

  The Arc Diagram entry follows a consistent, short-form catalog template: 800 words of pedagogical prose, one Claude Code prompt, one external link. It is clearly designed to be the first of many such entries.

- **File B:** `chapters/18-brutalist-claude-project.md` — 6,639 words. Full long chapter. Header reads `# Chapter 16 — The Brutalist Claude Project` (note: header says Ch 16, not Ch 18 — this is a number-renumbering inconsistency from an earlier draft). The chapter delivers a complete Brutalist Claude Project system prompt with installation instructions, named commands (`/init`, `/research`, `/claude`, `/design`, `/project`, `/update`, `/verify`, `/handoff`), refusal behaviors, and the `/silent` modifier. It is a working tool delivered inside a chapter, not a tutorial about the tool.

**These are not duplicates in the same sense as the 02 case.** They are two completely different chapters that happen to share a number — one is the seed of a Part IV catalog, the other is a Part III synthesis chapter.

**Recommendation.**

1. **Promote `18-brutalist-claude-project.md` to canonical Chapter 18.** This chapter is the natural synthesis cap of Part III — it delivers the working tool the book has been building toward. The TIKTOC slots it as Chapter 18.
2. **Fix the in-file header.** The file's H1 currently reads `# Chapter 16 — The Brutalist Claude Project`. Update to `# Chapter 18 — The Brutalist Claude Project`. (Header numbers across the chapters file set are inconsistent — `06-working-with-claude-code.md` has an H1 of "Chapter 6" but references its own LLM Exercise as "Chapter 5" near the end. A cross-chapter header-number sweep is needed in the rewrite pass.)
3. **Move `18-arc-diagram.md` out of the numbered chapter sequence.** The Part II catalog (now Part IV in the TIKTOC, to avoid clashing with the existing chart-families "Part II") is structurally distinct from the numbered chapters. Two options:
   - **Option A (recommended):** Split the file. Extract the "Part II — Examples" framing paragraph into a new short chapter or appendix opener (e.g., `chapters/part-iv-catalog-intro.md`). Move the Arc Diagram entry to `catalog/arc-diagram.md` (or `chapters/catalog/arc-diagram.md`) where it becomes the first of ~60 short entries.
   - **Option B (preserve filename):** Rename `18-arc-diagram.md` to `catalog-01-arc-diagram.md` or `99-catalog-arc-diagram.md`. Less clean but lower disruption to existing references.
4. **Do not discard the Arc Diagram entry.** The catalog template it establishes (short pedagogical text + Claude Code prompt + external link + Wayback figure) is the right model for the Part IV catalog. Sixty more entries to be written against this template.

---

## 3. Missing 01-introduction

The chapter sequence currently jumps from `00-frontmatter.md` to `02-claude-basics-for-d3-visualization.md`. There is no `01-*.md`. The Practitioner's AI Series convention (visible in `ai-for-students-a-practitioners-guide/`) is that Chapter 1 is a proper roadmap chapter — what's the argument, who is the reader, how does the book apply the series framework, what does the reader do with the book.

**Recommendation.** Create `chapters/01-why-a-chart-built-by-claude-code-still-needs-you.md` (or a shorter slug — `01-introduction.md` would also work).

**Proposed title:**
*Why a Chart Built by Claude Code Still Needs You*

(Alternative titles: *The Specification Skill*; *What Claude Code Cannot Decide for You*; *The Chart, the Code, and the Judgment in Between*.)

**Proposed one-line:**
Claude Code can write D3 in seconds; deciding whether the chart works is the job that did not get faster — and this book teaches the job that did not get faster.

**Proposed learning outcomes:**
1. State the labor separation principle: Claude Code writes D3 syntax; the human writes the specification.
2. Name the five Brutalist phases (Audit / Schema / Generate / Verify / Handoff) and the human-vs-AI assignment for each.
3. Identify the parts of a chart-building task that belong to Claude Code, the parts that belong to the human, and the dangerous middle that requires explicit handoff.
4. Apply the "did Claude Code decide this, or did I?" diagnostic to a recent chart output.
5. Locate the book in the Practitioner's AI Series and the Brutalist module series, and explain what each contributes.

**Notes for the writer.**
- Should reference the **series** (Practitioner's AI Series for the framework; Brutalist for the renderer-agnostic architecture) without re-explaining the framework in detail — that is Appendix F's job.
- Should preview the **AI+1 argument** specifically — let Claude Code do the syntax, use the saved time to learn the design layer.
- Should preview the **Brutalist application** — this book is the data-viz application of the framework; the human focuses on chart design while AI handles execution.
- Should preview the **themes appendix (Appendix F)** as a forward reference for readers who want the series-wide context now.
- Should *not* attempt to re-teach the four-move prompt or the channel ranking — those are Chapters 2 and 3. The introduction is the roadmap.
- Hook candidate: the same "vague prompt → broken chart" failure case Chapter 2 uses, but framed at the level of *what kind of book is this and why does it exist*, not *what is the four-move prompt*. The Chapter 2 hook stays specific to mechanism; the Chapter 1 hook should be specific to the responsibility the book is teaching.
- Length target: 4,000–5,000 words. Shorter than the chart-family chapters but long enough to do all five learning outcomes properly.

---

## 4. Voice and coherence observations

**Voice across the chapter set is more consistent than expected.** The chapters share several reliable moves:
- Opening with a concrete failure case (vague prompt, fourteen-slice pie, two maps of insured vs. uninsured, scatterplot with r=0.79, etc.) rather than abstraction
- A `## What you can now do` section that names the capability transfer
- An `## Exercises` section with Warm-up / Application / Synthesis / Challenge subsections
- A `## A note about AI` paragraph that flags where the model genuinely helps and where it does damage
- An `## LLM Exercise` section that produces a real deliverable
- A `## Further reading` section keyed to the named references
- An `## AI Wayback Machine` section with an AI-generated portrait of a historical figure (Hamilton, Bertin/Bostock, Euler, etc.) and a starter prompt the reader can run against any model

This is a strong, distinctive structural signature. The rewrite pass should preserve it.

**Voice drift observations:**
- **Chapter 2 (`02-claude-basics`)** has the most polished voice — tight, instrument-checking, mechanism-first. Chapter 8 (temporal) and Chapter 10 (relationship) are nearly as tight.
- **Chapters 11 (part-to-whole) and 13 (flow/network)** are slightly more catalog-like — they spend more pages on form taxonomy and less on a single deep mechanism. This is appropriate for those families (each has many forms with meaningfully different trade-offs) but reads as flatter prose than the tighter chapters.
- **Chapter 17 (`17-building-a-complete-project`)** opens with a Feynman frame and explicitly invokes the test-at-end-of-course move. This is the most overtly pedagogical opening; it works because the chapter *is* the test.
- **Chapter 18 (`18-brutalist-claude-project`)** has a different voice — closer to product documentation than chapter prose. This is appropriate given that the chapter delivers a working tool, but it is worth flagging: a reader expecting the chapter voice of Chapters 7–15 will find this chapter feels different. The rewrite pass should either (a) accept the documentation register for the deliverable section and add a more chapter-voice frame around it, or (b) consider relegating the system prompt to an appendix and keeping the chapter prose in the chapter.

**Scope inconsistencies:**
- The frontmatter calls the book *Brutalist d3 x Claude* and locates it in the Brutalist series. The directory name is `ai-for-graphs-a-practitioners-guide` and locates it in the Practitioner's AI Series. Both are real series claims. The TIKTOC handles this by treating the book as a member of both, but the final title decision (Open Question #1) needs Nik's call.
- Chapter 6 (`06-working-with-claude-code`) has an internal numbering inconsistency — its `## LLM Exercise — Chapter 5` heading says Ch 5 but the H1 says Ch 6. There are several of these across the chapter set:
  - `06-working-with-claude-code.md` H1 says Ch 6, LLM Exercise says Ch 5
  - `18-brutalist-claude-project.md` H1 says Ch 16, file says Ch 18
  - Some chapter cross-references (e.g., in Ch 17) point at the wrong upstream chapter (Ch 5 instead of Ch 6, Ch 3 instead of Ch 5)
- A cross-chapter renumbering sweep is required in the rewrite pass.

**Thin chapters / anatomy skips:** None of the chapters skip the chapter anatomy entirely. The closest thing to a thin chapter in the existing set is `18-arc-diagram.md`, but that file is doing two things at once (catalog opener + first catalog entry) and is appropriately short for what it is. The Brutalist Project chapter is long but the bulk of its word count is the system prompt itself — the framing prose is shorter than other chapters.

---

## 5. Themes weaving recommendation

**Where the themes framework already appears in the existing chapters:**

- **Frontmatter (`00-frontmatter.md`)** invokes the full Brutalist architecture — phase model, labor separation, supervisory capacities, three-file system. The Brutalist theme is established as the book's organizing lens before Chapter 1.
- **Chapter 2** names the **labor separation principle** explicitly and walks through the four-move prompt as the operational form of "AI executes a human specification."
- **Chapter 6** walks the **five-phase pipeline** (Audit / Schema / Generate / Verify / Handoff) at chapter scale and is the most theme-integrated chapter in Part I.
- **Chapter 17** runs the same five-phase pipeline at project scale on a UNHCR dataset.
- **Chapter 18** delivers the **Brutalist Claude Project** as the system-prompt form of all the themes — phase gate as refusal behavior, labor separation as named commands, three files as enforced prerequisites.
- **`97-fundamenta-themes.md`** is the full framework essay; it sits at the back of the chapter sequence but is currently positioned to read as a chapter rather than as an appendix. The TIKTOC moves it to Appendix F.

**Where the themes framework does *not* appear and probably should:**

- **Chapters 3, 4, 5 (marks/channels, chart selection, reading a dataset)** are mechanism-heavy and theme-light. They could explicitly name the **Frictional** principle — the cognitive friction of reading a dataset and naming channels is the work AI cannot do for the human, and that friction is the mechanism by which chart-design judgment is built. A single paragraph in each of these chapters connecting the chapter's discipline to the Frictional theme would tighten the through-line.
- **Chapters 7–15 (chart families)** each name a family-specific failure mode (truncated baseline, Gestalt continuity, overplotting, area-size distortion, etc.). Each failure mode is a **Phase Gate** failure — the gate was placed too late, or not placed at all. A consistent paragraph at the end of each chart-family chapter naming the Phase Gate that prevents the family's most common failure would make the series framework operationally present in Part II.
- **The chart-family chapters do not currently reference the Humans+AI Tiers framework.** They could, briefly: chart-type selection is Tier 4 (metacognitive), channel decomposition is Tier 4 (metacognitive), audit is Tier 5 (causal/counterfactual). One annotation per chapter would land the framework without disrupting the mechanism focus.

**For the eventual rewrite pass, the chapters that most need the Frictional / Phase Gate / Humans+AI lens added are:**

1. **Chapter 1 (to be written)** — should set up the framework explicitly so subsequent chapters can cite it without re-explaining.
2. **Chapter 3 (marks/channels)** — the perceptual ranking is exactly the Frictional case: the friction of reading the channel ranking is the friction that builds the muscle.
3. **Chapter 4 (chart selection)** — familiarity bias is a textbook Boondoggling failure (the human accepts what is fast over what is right).
4. **Chapter 5 (reading a dataset)** — the analyst-vs-reader question distinction is a Phase Gate decision (whose question is the chart answering?).
5. **Chapters 7–15 (chart families)** — one Phase Gate paragraph each, naming the most common gate failure for that family.

The rewrite pass should resist the temptation to bolt theme references onto every paragraph. The themes work when they are named at the moment the chapter's mechanism reveals them — not before, not after, not as decoration.

---

## Summary of recommended file moves (for the rewrite pass)

- `chapters/02-claude-basics-for-d3-visualization-updated.md` → archive to `_working/` (or delete). Keep `chapters/02-claude-basics-for-d3-visualization.md` as canonical.
- `chapters/18-brutalist-claude-project.md` → keep at this path; fix H1 to read "Chapter 18 — The Brutalist Claude Project."
- `chapters/18-arc-diagram.md` → split. Move the "Part II — Examples" intro paragraph into a new file (recommended: `chapters/19-part-iv-catalog-intro.md` or similar). Move the Arc Diagram entry into a `catalog/` subdirectory (recommended: `chapters/catalog/arc-diagram.md` as the first of ~60 catalog entries).
- `chapters/97-fundamenta-themes.md` → rename to `appendices/appendix-f-fundamental-themes.md` (or similar). Update cross-references throughout the book.
- New file: `chapters/01-introduction.md` (slug to be decided). 4,000–5,000 words. See §3 above for the proposal.
- Sweep all chapter files for header-number / cross-reference inconsistencies (Ch 5 vs. Ch 6, Ch 16 vs. Ch 18, etc.). This is mechanical but tedious.

---

*End of reconciliation report.*
