# TIKTOC — AI for Graphs: A Practitioner's Guide

**Working title:** AI for Graphs: A Practitioner's Guide *(working frontmatter title: Brutalist d3 x Claude)*
**Series:** Practitioner's AI Series · Northeastern University College of Engineering
**Author:** Humanitarians AI · ni.brown@neu.edu · Bear Brown & Company
**Document:** Full TIKTOC — Complete Architecture, reverse-engineered from 18 existing chapter drafts
**Version:** 1.0
**Status:** Reverse-engineered from existing drafts — TIKTOC precedes rewrite pass
**Directory:** ai-for-graphs-a-practitioners-guide/

---

## The Brief

Most data visualization books were written before AI could generate D3 in seconds. Most AI books were written by people who do not build charts. This book sits in the gap: it teaches the part of data visualization that cannot be delegated to Claude Code — the channel decomposition, the chart-type selection, the audit — by treating Claude Code as the executor of a specification the human is responsible for writing.

The chapters that already exist on disk converge on a single argument. Claude Code can generate D3 v7 syntactically perfect code faster than any human can type it. What Claude Code cannot do is decide whether the chart it generated answers the communication question, whether the encoding it chose is perceptually defensible, or whether the chart is honest. Those judgments are the work this book is teaching.

The book is also the D3 module of a larger system the author has been building — **Brutalist** — a renderer-agnostic architecture for AI-assisted creative production. The Brutalist module names in the frontmatter (*Brutalist d3 x Claude*, *Brutalist After Effects x Claude*, *Brutalist Blender x Claude*, *Brutalist Remotion x Claude*) are siblings of this volume in a single series whose spine is the three-file system (`CLAUDE.md`, `DESIGN.md`, `PROJECT.md`) and the five-phase model (Audit → Schema → Generate → Verify → Handoff). This book is what Brutalist looks like when the active renderer is D3.

---

## Book Concept and Thesis

This book teaches **the supervisory practice of building data visualizations with Claude Code** — the channel decomposition, the chart-type selection, the four-move prompt structure, and the audit checklist that converts Claude Code from a fluent guesser into a reliable executor — to **analysts, journalists, designers, and engineers who already know they want to build charts and have noticed that "make me a chart" produces charts that do not work**, by **giving them the perceptual grammar from Bertin / Cleveland & McGill / Munzner, the chart-type taxonomy from the FT Visual Vocabulary, and a working pipeline that ends in a published artifact**. It fills the gap between D3 reference books (which teach syntax but not judgment) and visualization theory books (which teach judgment but predate AI code generation). It succeeds if the reader can **read a dataset, formulate the communication question, name the marks and channels, write a four-move prompt, and audit Claude Code's output before publishing.**

**One-sentence logline:**
Claude Code writes the D3. You write the specification — and this book teaches you how to write the specification.

**Theoretical spine:**
A data visualization is a perceptual artifact. Some channel-to-attribute mappings the human visual system reads accurately and quickly; others it cannot read at all. Cleveland and McGill measured this in 1984 and produced a ranking (position, length, angle, area, luminance, hue, volume) that has been replicated by Heer and Bostock and synthesized by Munzner. The ranking is not aesthetic. It is empirical. A chart that maps a quantitative attribute to hue is not a stylistic choice; it is an unreadable chart. The book's claim is that this perceptual grammar — combined with the FT Visual Vocabulary's functional taxonomy, the chart-type-message match, Cairo's ethical frame, and the Evergreen/Emery audit — constitutes a specification language Claude Code can execute reliably. Without the specification, Claude Code produces "a chart." With it, Claude Code produces *the* chart.

**The Brutalist application:**
The Practitioner's AI Series framework (Frictional · Phase Gates · Humans + AI Tiers · AI+1 · Brutalist · Boondoggling, documented in Appendix F) names six lenses on the human–AI division of labor. This book is the Brutalist application of the framework: the technical barrier of writing D3 v7 from scratch — which kept a generation of would-be visualization practitioners out of the field for a decade — is lowered by Claude Code, so the human can focus on the design layer. The Brutalist argument is not that the human does less. It is that the human does the part that matters: chart-type selection, channel decomposition, audit. Claude Code does the part that does not: syntax.

---

## Companion Publications

**Series relationship:**

This book sits at the intersection of two series.

The first is the **Practitioner's AI Series** — *AI for Teachers*, *How to Learn with AI: A Student's Guide*, *AI for Writing*, *AI for Graphs* (this book), and additional renderer-specific volumes. All Practitioner's AI Series books share the Frictional · Phase Gate · Humans + AI framework (Appendix F) and the discipline that AI runs against an explicit human-authored specification, not a vague request.

The second is the **Brutalist** series — *Brutalist After Effects x Claude*, *Brutalist d3 x Claude* (this book, under its frontmatter title), *Brutalist Blender x Claude*, *Brutalist Remotion x Claude*, with additional renderer modules in development. All Brutalist books share the phase model (Audit → Schema → Generate → Verify → Handoff), the labor separation principle, the five supervisory capacities, and the three governing files (`CLAUDE.md`, `DESIGN.md`, `PROJECT.md`). What changes module to module is the renderer.

**Who this is NOT for:**
- Readers who want to learn D3 syntax in depth (→ Scott Murray, *Interactive Data Visualization for the Web*, 3rd ed.)
- Readers who want a comprehensive treatment of visualization theory (→ Tamara Munzner, *Visualization Analysis and Design*, or Claus Wilke, *Fundamentals of Data Visualization*)
- Readers who want every published chart's history (→ Michael Friendly, "A Brief History of Data Visualization")

**Who this IS for:**
The analyst who tried to learn D3 in 2018, ran into `d3.scaleLinear`, and quietly closed the tab. The journalist who has been pasting screenshots into Claude.ai and would like a more disciplined workflow. The product designer who wants their dashboards to be readable before they are pretty. The engineer who can write the data pipeline but freezes at the chart. The teacher who needs students to learn the design layer in a semester. Anyone who has typed "make me a bar chart" into Claude Code, received something technically correct and visually broken, and wondered what the missing input was.

---

## Learner Profile

**Primary reader:** A working analyst, designer, journalist, or engineer who:
- Has access to Claude Code (or Claude.ai, ChatGPT, Gemini)
- Has built at least one chart in any tool and recognizes the difference between a chart that depicts and a chart that communicates
- Has some HTML and JavaScript literacy — enough to open a file in a browser and read source — but does *not* need to be a D3 developer
- Wants to ship charts faster without shipping worse charts
- Has noticed that "vague prompt → fluent output → broken chart" is a recurring pattern they do not yet have language for

**Secondary readers:**
- Data journalism students at the undergraduate or graduate level
- Faculty teaching introductory visualization courses who want a textbook that acknowledges Claude Code exists
- Product managers and designers commissioning dashboards from engineering teams who want shared vocabulary with the people building them
- Researchers producing figures for papers and grant proposals
- Self-taught practitioners coming back to D3 after years away

**Prior knowledge assumed:**
- Basic HTML / CSS / JavaScript fluency
- Some experience with at least one charting tool (Excel, Tableau, matplotlib, Observable, anything)
- A working installation of Claude Code, or access to Claude.ai
- The ability to open an HTML file in a browser

**Prior knowledge NOT assumed:**
- D3 fluency at the API level
- Formal training in visualization theory
- Statistics beyond mean / median / quartile literacy
- Design background

**Prior misconceptions the book must address:**
1. "Claude Code will pick a good chart if I describe my data well" — it will pick *a* chart; the chart that answers the reader's question requires the human to name it
2. "Chart type is a stylistic choice" — chart type is a channel choice, and channel choices have measurable perceptual consequences
3. "D3 is too hard to learn" — D3 is the syntax; the syntax is what Claude Code is for; the chart design is what the human is for, and that part is learnable
4. "A pretty chart is a good chart" — pretty and readable are independent qualities; this book is about readable
5. "Prompting is about being clever" — prompting is about being specific; the four-move structure is the discipline that makes specificity routine

---

## Book Type and Deployment Specification

**Primary type:** Practitioner handbook with a sequential Part I, a modular Part II (chart-type chapters readable independently), and a synthesis Part III. Each chapter ends in a runnable LLM Exercise that produces a real chart.

**Primary adoption context:**
- Self-study by working practitioners
- A semester-long upper-undergraduate or graduate course in data visualization
- A faculty member's reference for a course that includes a Claude Code component

**Secondary adoption context:**
- Newsroom training programs
- Design team onboarding
- A reference shelf companion to Munzner, Wilke, Cairo, Few, Knaflic, and Murray — this book is the AI-aware bridge between those references and a working Claude Code pipeline

**Voice:** Direct, mechanism-first, instrument-checking. The opening of every chapter is a concrete failure or comparison case — a vague prompt that produces a broken chart, a pie chart with fourteen slices, a choropleth where population dominates the encoding — followed by the specification that prevents it. Voice register is broadly Feynman-flavored (the workshop's default plugin) with the Brutalist flavor — direct, slightly clinical about labor separation, occasionally mischievous about the failures Claude Code produces when given a vague prompt.

---

## Three-Part Learning Arc

**Part I — Foundations (Chapters 1–6)**
The vocabulary and the workflow. The reader leaves Part I with the channel ranking from Bertin/Cleveland & McGill/Munzner, the FT Visual Vocabulary's eight functional categories, a reading-the-dataset discipline, the four-move prompt structure, and the three-layer verification stack. Without Part I, the chart-type chapters read as a list of rules; with Part I, they read as the rules' consequences.

**Part II — Chart Families (Chapters 7–15)**
One chapter per FT Visual Vocabulary category, plus a final chapter on specialized and financial charts whose conventions earn their strangeness. Each chapter applies the Part I framework to its family's specific failure modes. The chapters are modular — a reader who needs a Sankey diagram tomorrow can read Chapter 13 directly — but they share a consistent structure: open in a concrete chart, name the channels the family uses, name the failure modes, name the Claude Code prompt template, run an LLM Exercise that produces a publishable chart.

**Part III — Synthesis (Chapters 16–18)**
Design principles applied across families (Chapter 16), a complete project from raw data to published artifact (Chapter 17), and the Brutalist Claude Project delivered as a system prompt the reader can paste once and use forever (Chapter 18). Part III is the test the book asks the reader to pass.

---

## Full Structure

```
Frontmatter
  Copyright · Dedication · Preface (The Brutalist System Applied to D3)

Part I — Foundations
  Chapter 1  — Why a Chart Built by Claude Code Still Needs You [TO BE WRITTEN]
  Chapter 2  — Claude Basics for D3 Visualization
  Chapter 3  — Marks and Channels
  Chapter 4  — Chart Selection as Design Decision
  Chapter 5  — Reading a Dataset
  Chapter 6  — Working with Claude Code

Part II — Chart Families
  Chapter 7  — Comparison Charts
  Chapter 8  — Time Series and Temporal Charts
  Chapter 9  — Distribution Charts
  Chapter 10 — Relationship and Correlation Charts
  Chapter 11 — Part-to-Whole Charts
  Chapter 12 — Hierarchy Charts
  Chapter 13 — Flow and Network Charts
  Chapter 14 — Spatial and Geographic Charts
  Chapter 15 — Specialized and Financial Charts

Part III — Synthesis
  Chapter 16 — Design Principles in Practice
  Chapter 17 — Building a Complete Project
  Chapter 18 — The Brutalist Claude Project

Part IV — Chart Type Catalog (alphabetical, short)
  Sixty-one chart-type entries, each with prompt and pantry link.
  (Begins with "Arc Diagram"; 18-arc-diagram.md is the seed for this section.)

Back Matter
  Acknowledgments · About the Author · Chart Type Reference · Selected References · Colophon

Appendices
  Appendix A — Channel Ranking Reference
  Appendix B — FT Visual Vocabulary Quick Card
  Appendix C — Four-Move Prompt Template Library
  Appendix D — The Evergreen/Emery Audit Checklist
  Appendix E — CLAUDE.md / DESIGN.md / PROJECT.md Starter Kits
  Appendix F — Fundamental Themes of the Practitioner's AI Series
              (Frictional · Phase Gates · Humans + AI Tiers · AI+1 · Brutalist · Boondoggling)
```

---

## Chapter-by-Chapter TIKTOC

---

### CHAPTER 1 — Why a Chart Built by Claude Code Still Needs You *(to be written; see Reconciliation Report §3)*

**One-line:** Claude Code can write D3 in seconds; deciding whether the chart works is the job that did not get faster.

**Opening case:** A working analyst asks Claude Code for "a chart of regional sales." The response is plausible — five bars, axis labels, colors. The reader cannot rank the regions because the bars are unsorted, the y-axis is auto-fit and starts at $400K, and the color encoding is decorative. The chart is technically a chart. The reader cannot read it. The chapter opens with this failure case and asks: which part of producing a usable chart did Claude Code do, which part did it not, and what is the name of the part it did not?

**Learning outcomes:**
1. (Understand) State the labor separation principle: Claude Code writes D3 syntax; the human writes the specification.
2. (Understand) Name the five Brutalist phases (Audit, Schema, Generate, Verify, Handoff) as they apply to chart work.
3. (Apply) Identify the parts of a chart-building task that belong to Claude Code and the parts that belong to the human.
4. (Analyze) Read three published charts and name, for each, the design decision that determined whether the chart works.
5. (Evaluate) Use the "did Claude Code decide this, or did I?" test as a diagnostic on the reader's own recent chart output.

**Core content:**
- The two prompts experiment (vague vs. specific) as the chapter's anchor
- The five Brutalist phases applied to a chart
- The labor separation principle: what Claude Code is the right labor for, what the human is the right labor for, the dangerous middle
- The five supervisory capacities (Plausibility Auditing, Problem Formulation, Tool Orchestration, Interpretive Judgment, Executive Integration) applied to chart design
- A reader's-eye-view tour of the book: what each chapter contributes, why the order
- The series context: this book as the D3 module of Brutalist and the data viz module of the Practitioner's AI Series

**Key concepts:** Labor separation, phase gate, supervisory capacities, specification skill, the Brutalist three-file system (preview)

**Assessment/exercise:** Take the reader's last AI-generated chart. Apply the "who decided this?" test to every visible design decision: chart type, sort order, baseline, color encoding, axis ticks, annotation. For each decision Claude Code made, name what the reader should have specified.

**Bridge:** The case for human responsibility is named. Chapter 2 gives it operational form — the products, the instruction budget, the four-move prompt, and the verification stack that make Claude Code reliably useful for chart work.

---

### CHAPTER 2 — Claude Basics for D3 Visualization

**One-line:** The gap between "make a chart" and "make *the* chart" is the whole problem — and the four-move prompt is the discipline that closes it.

**Opening case:** 2:14 PM. Eight cognitive domain scores. Colleague needs a chart by 3:30. Vague prompt produces an unreadable scatterplot in four seconds; specific four-move prompt produces a sorted bar chart with zero baseline, redundant luminance, and direct labels in the same four seconds. The data is identical. The prompt is not.

**Learning outcomes:**
1. (Understand) Distinguish among Claude Code, Claude.ai, Claude Projects, Claude in Chrome, and the Claude API by file-system access, persistent context, and best-fit D3 use case.
2. (Understand) Explain the instruction budget — the ~50-instruction system-prompt overhead, the ~150–200 total budget, the silent degradation past the limit — and why it forces `CLAUDE.md` and `DESIGN.md` to be separate files.
3. (Apply) Write a four-move prompt (Show / Say / Constrain / Verify) for any chart, with Move 3 carrying the channel-to-attribute mappings explicitly.
4. (Analyze) Diagnose the three D3-specific failure modes — API hallucination, chart-type mismatch, channel mismatch — and write the follow-up prompt that fixes each.
5. (Evaluate) Apply the three-layer verification stack (format / facts / browser test) to a Claude Code chart output before publishing.

**Core content:**
- Where Claude lives: product comparison table with D3-specific use cases
- The instruction budget and the `CLAUDE.md` / `DESIGN.md` split
- The four-move prompt structure (Show what you have / Say what you want / Constrain it / Ask for verification) with the cognitive-domain dataset as the worked example
- D3-specific specification notes: pin the version, name the rendering target, specify the data-loading method
- Three failure modes with diagnostic-and-fix patterns: API hallucination, chart-type mismatch, channel mismatch
- Multi-LLM comparison as a targeted, not default, practice
- The three-layer verification stack: format, facts, browser test

**Key concepts:** Four-move prompt, instruction budget, `CLAUDE.md`, `DESIGN.md`, API hallucination, chart-type mismatch, channel mismatch, verification stack

**Assessment/exercise:** LLM Exercise produces the reader's `CLAUDE.md` and `DESIGN.md` — the two session-context files that travel with them through every subsequent chapter and every D3 project beyond the book.

**Bridge:** The machinery is in place. Chapter 3 fills in the vocabulary the machinery uses — marks and channels, the perceptual grammar that makes Move 3 of the four-move prompt possible.

---

### CHAPTER 3 — Marks and Channels

**One-line:** Every chart is a small set of geometric marks varied along a small set of perceptual channels — and only some channel choices let the eye read the data.

**Opening case:** Fifty countries, two numbers each (GDP per capita, life expectancy). Chart A puts life expectancy on the y-axis. Chart B puts life expectancy on a color luminance scale with all points on one horizontal line. Same data; same question. The reader answers in under a second from Chart A and gives up after ten seconds on Chart B. The difference is the channel.

**Learning outcomes:**
1. (Understand) Name the four mark types — point, line, area, glyph — and the claim each one makes about the data.
2. (Understand) Recite the Cleveland–McGill channel ranking (position on common scale, position on non-aligned scale, length, angle/slope, area, luminance/saturation, hue/shape/texture) and explain the perceptual mechanism for each rank.
3. (Apply) Decompose a published chart into its mark and its channel-to-attribute mappings.
4. (Analyze) Identify the channel violation in a chart that does not work — quantitative attribute on hue, ordinal attribute on shape, categorical attribute on length-from-baseline.
5. (Evaluate) Use the channel ranking to justify a chart-type choice in language Claude Code can execute as Move 3 of a four-move prompt.

**Core content:**
- The grammar beneath every chart: Bertin (1967), Cleveland and McGill (1984), Heer and Bostock (2010), Munzner (2014)
- Marks: point, line, area, glyph — what each implies and what they do not
- The full channel ranking, with the perceptual mechanism for why position beats luminance beats hue
- Magnitude channels vs. identity channels — and why this distinction is the most important sentence in the chapter
- Redundant encoding: when adding a second channel reinforces the primary signal vs. when it competes
- Color as channels (luminance, saturation, hue) — three vocabularies, three uses
- The audit move: read any chart by listing its mark and its channels in priority order

**Key concepts:** Mark, channel, magnitude channels, identity channels, Cleveland–McGill ranking, expressiveness principle, effectiveness principle, redundant encoding

**Assessment/exercise:** Channel-decompose three published charts. For each, list the mark, the channel-to-attribute mapping, the channel's rank, and one alternative encoding that would have been better.

**Bridge:** Marks and channels are the alphabet. Chapter 4 teaches the writing system — which combinations of marks and channels constitute which chart types, and how to select among them.

---

### CHAPTER 4 — Chart Selection as Design Decision

**One-line:** The wrong chart feels familiar; the right one takes work — and the FT Visual Vocabulary's eight categories are the navigation tool that makes the work tractable.

**Opening case:** A humanitarian report's fourteen-slice pie chart of emergency response funds. The reader cannot rank the top three categories in thirty seconds. The same data as a sorted horizontal bar chart resolves the ranking in three seconds. The pie chart was not an accident — it was the product of familiarity bias and a data-structure-driven (rather than message-driven) selection.

**Learning outcomes:**
1. (Understand) Name the eight functional categories of the Financial Times Visual Vocabulary (Comparison, Change over time, Distribution, Relationship, Part-to-whole, Hierarchy, Flow, Spatial) and the reader's question each one answers.
2. (Understand) Distinguish data structure (what the data is) from message (what the reader needs to do) and explain why message dominates structure in chart selection.
3. (Apply) Use Cairo's "compared with what?" test to convert a vague brief into a specific communication question.
4. (Analyze) Diagnose familiarity bias in a published chart and propose an alternative selection grounded in the channel ranking.
5. (Evaluate) Choose a chart type for a real dataset by working through: reader question → functional category → candidate forms → channel decomposition → final selection.

**Core content:**
- The fourteen-slice pie chart as the chapter's anchor failure
- Familiarity bias and why "parts of a whole → pie chart" is a structure-driven (not message-driven) move
- The FT Visual Vocabulary's eight functional categories, each defined by the reader's question
- Why categories are defined by message, not structure
- Cairo's "compared with what?" as the question that bridges data and chart
- The selection workflow: read the data, formulate the question, choose the category, choose the form within the category
- Selection failure modes: chart-type mismatch (Claude Code's), familiarity bias (the human's), structure-drive (everyone's)

**Key concepts:** Functional category, FT Visual Vocabulary, message vs. structure, familiarity bias, Cairo's question, chart-type-message match

**Assessment/exercise:** Take three datasets the reader works with. For each, formulate the reader's question, choose the functional category, identify two candidate forms, and write the four-move prompt that names the winner.

**Bridge:** The chart is chosen against the message. Chapter 5 makes the upstream work explicit — how to read the dataset before formulating the message, so the message reflects what the data actually contains.

---

### CHAPTER 5 — Reading a Dataset

**One-line:** Read the data before you reach for the code — the variable types constrain which charts are even possible.

**Opening case:** A research team asks for "visualize refugee flows." The phrase has a referent and a verb but no question. Refugee flows could be a dozen different charts, each answering a different question, each requiring a different dataset. Accepting the brief unchallenged produces "a chart"; interrogating the brief produces *the* chart.

**Learning outcomes:**
1. (Understand) Name the five primary variable types — categorical, ordinal, quantitative, temporal, geographic — and the encoding constraints each one imposes.
2. (Understand) Distinguish the analyst's question (exploratory, contextual, plural) from the reader's question (summative, decision-oriented, singular).
3. (Apply) Audit a dataset by listing each column with its type, its role, and its admissible channels.
4. (Analyze) Translate a vague brief into a precise reader's question that names what is being compared and to what.
5. (Evaluate) Decide which subset of a dataset to use for a given reader's question, and which variables the question makes irrelevant.

**Core content:**
- The five variable types with their encoding constraints
- The misclassification failure modes: country names sorted by the source file treated as ordinal, ZIP codes as quantitative, year-as-integer as quantitative, Likert as interval
- Most real datasets contain multiple types; you build a chart from the subset the question requires
- The analyst's question vs. the reader's question — different people, different needs, the chart can only answer one
- The MBTA Marey project (Barry and Card, 2014) as the canonical example of question-first chart design
- The interrogation move: how to turn "visualize refugee flows" into "show how new asylum arrivals at the eastern Mediterranean border changed quarter-by-quarter from 2020 to 2024, with annotations at policy change points"

**Key concepts:** Variable type, encoding constraint, analyst's question, reader's question, interrogation move, MBTA model

**Assessment/exercise:** Audit a real dataset using the variable-type table. Write three plausible reader's questions for it. For each, identify the variable subset the chart will use and the variables it will not.

**Bridge:** The data is read, the question is formulated. Chapter 6 walks the full pipeline from dataset to published chart and names the audit discipline that converts Claude Code output into a publishable artifact.

---

### CHAPTER 6 — Working with Claude Code

**One-line:** You decide, the machine renders, you review — and the discipline of doing all three in order is the pipeline.

**Opening case:** Same dataset (humanitarian funding by sector), two prompts, twelve seconds each. The 9-word prompt produces a column chart with a non-zero y-axis, uniform colors, crowded labels, and no value labels. The 200-word four-move prompt produces a sorted horizontal bar chart with zero baseline, sequential luminance, direct value labels, and breathing room. The difference is not intelligence applied; it is the discipline of doing Chapters 3 through 5 *before* opening Claude Code.

**Learning outcomes:**
1. (Apply) Run the full pipeline (Audit / Schema / Prompt / Build / Verify) on a chart from data the reader supplies.
2. (Apply) Write a `CLAUDE.md` for a chart project and use it as Claude Code's session context.
3. (Apply) Write a `PROJECT.md` for a single chart — the per-chart audit document.
4. (Analyze) Diagnose Claude Code output failures and write the follow-up prompt that names the failure mode by name.
5. (Evaluate) Apply the audit discipline to decide whether a Claude Code output is publishable, revisable, or restartable.

**Core content:**
- The full pipeline: Audit (read the data) → Schema (write `CLAUDE.md` / `DESIGN.md` / `PROJECT.md`) → Generate (Claude Code writes the chart) → Verify (audit checklist) → Handoff (publish)
- What Claude Code does and does not do well — concrete examples of each
- The MBTA project (Barry and Card, 2014) as the canonical multi-prompt pipeline
- Common failures and the follow-up prompts that fix them (mapped to the failure modes from Chapter 2)
- `CLAUDE.md` as the constitution for the project — what goes in it, what does not
- `PROJECT.md` as the per-chart decision record — chart type, channels, design constraints, sort order, accessibility decisions, iteration log
- The full pipeline run once on a real dataset

**Key concepts:** Pipeline, audit discipline, `PROJECT.md`, four-move prompt (revisited), follow-up prompt vocabulary, the MBTA model

**Assessment/exercise:** Run the full pipeline on a real chart. Submit: dataset, reader's question, `PROJECT.md`, four-move prompt, Claude Code output, audit log, final HTML.

**Bridge:** The foundations are in place. Part II applies them, one functional category at a time, starting with the easiest case (comparison) and the channel — length from a shared baseline — that the eye reads most accurately.

---

### CHAPTER 7 — Comparison Charts

**One-line:** Length along a shared baseline is the most honest channel — and the bar chart is what that channel looks like in a chart.

**Opening case:** The pantry's `bar-chart.html` — eight cognitive domains, sorted by score, zero baseline, redundant luminance. The reader ranks all eight domains in under a second. This is the chapter's positive case. The failures (truncated baselines, unsorted bars, 3D perspective, gradient color for unordered categories) are diagnosed against this baseline.

**Learning outcomes:**
1. (Apply) Build a sorted horizontal or vertical bar chart for a categorical-by-quantitative dataset using a four-move prompt.
2. (Apply) Choose between horizontal and vertical bar orientation based on label length and category count.
3. (Apply) Extend the bar chart to two variables (grouped bars, stacked bars, small multiples) with explicit channel decomposition.
4. (Analyze) Diagnose the proportional-ink violation of a truncated baseline and name the perceptual mechanism (Stevens' power law) it violates.
5. (Evaluate) Decide when the bar chart stops working and a different form is needed (very many categories, very few, cyclic data).

**Core content:**
- What the bar chart actually does perceptually
- The arguments defenders of truncated baselines make, and why each fails
- Horizontal vs. vertical bar selection
- Two-variable cases: grouped, stacked, small multiples — each with its own channel decomposition
- Radial bars and the narrow condition under which the curve earns its keep (cyclic data)
- When the bar chart stops working
- The design decisions in the pantry's bar chart, one by one — as a worked specification

**Key concepts:** Length-from-baseline, proportional ink, Stevens' power law, sorting as encoding, grouped vs. stacked, small multiples, radial bars

**Assessment/exercise:** LLM Exercise produces a publishable comparison chart on the reader's dataset. Submit the four-move prompt, the output, and the audit log.

**Bridge:** Comparison was the easy case — one categorical, one quantitative, length from baseline. Chapter 8 introduces time as the second variable, and the question of when point position (line chart) replaces length (bar chart) as the right channel.

---

### CHAPTER 8 — Time Series and Temporal Charts

**One-line:** What changes, in what direction, how fast — and the zero baseline rule that splits the temporal family in two.

**Opening case:** A line chart and a bar chart of the same monthly revenue data. Both can start their y-axis at $80,000 instead of $0. In the bar chart, this is a proportional-ink violation. In the line chart, it is fine. Same visual trick, different channel, different verdict.

**Learning outcomes:**
1. (Apply) Build a line, area, stacked area, candlestick, Gantt, or Marey chart from temporal data using a four-move prompt.
2. (Understand) Explain why the zero-baseline rule applies to bar/area charts (length channel) but not to line charts (point-position channel).
3. (Apply) Diagnose Gestalt continuity violations — connecting unrelated points, implying interpolation across missing intervals.
4. (Analyze) Read a stacked area chart and identify which series' shapes are readable and which are distorted by the stacking order.
5. (Evaluate) Choose between line, area, stacked area, stream, spiral, Gantt, and Marey for a temporal dataset by reader's question.

**Core content:**
- The temporal family and what each member is for
- Why the zero-baseline rule splits the family (length channel vs. position channel)
- What lines claim that bars do not — continuity, interpolation
- Gestalt continuity and the skipped-interval problem
- Stacked area: what moves up as accuracy degrades
- The MBTA Marey diagram: when two position channels combine — time × space
- Cyclic data and the spiral's trade-off
- How this changes the prompt

**Key concepts:** Zero-baseline rule, Gestalt continuity, line vs. area, stacked area, Marey diagram, spiral plot

**Assessment/exercise:** LLM Exercise produces a publishable temporal chart from a real dataset with at least 24 time points and at least 3 series.

**Bridge:** Time series shows trajectory. Chapter 9 turns to the shape of a single variable — the histogram, box plot, violin plot, and density plot, and the question of which one the audience can actually read.

---

### CHAPTER 9 — Distribution Charts

**One-line:** Shape, spread, and skew — beyond the mean.

**Opening case:** A box plot of household income by residential zone. The Inner Suburbs cluster of points above the upper whisker reveals that an outlier group exists. The box plot does not tell you whether they are a separate sub-population or the upper end of a long tail. Two distributions — normal and bimodal — can have identical five-number summaries; the box plot cannot distinguish them.

**Learning outcomes:**
1. (Understand) Explain why the mean hides the distribution and the box plot reveals five numbers but not shape.
2. (Apply) Build a histogram, box plot, violin plot, or density plot using a four-move prompt.
3. (Apply) Choose a bin width that does not lie — neither over-smoothing nor over-fragmenting.
4. (Analyze) Diagnose Cairo's "graphicacy constraint" — when a chart's audience cannot read the form regardless of the form's accuracy.
5. (Evaluate) Choose a distribution form based on dataset size, multimodality risk, and audience graphicacy.

**Core content:**
- What the mean hides
- The histogram and the bin-width problem
- What the box plot shows and what it does not (Tukey, 1977)
- Violin plots and shape made visible
- Cairo's graphicacy constraint — audience reading capacity as a real design input
- Stem-and-leaf and density plots
- The form selection in practice

**Key concepts:** Bin width, five-number summary, multimodality, graphicacy constraint, density estimation

**Assessment/exercise:** LLM Exercise produces a publishable distribution chart and an annotation that names what the chart reveals and what it does not.

**Bridge:** Distribution shows the shape of one variable. Chapter 10 introduces two — and the question that two-variable charts refuse to settle: whether correlation implies causation.

---

### CHAPTER 10 — Relationship and Correlation Charts

**One-line:** Two variables and the question they refuse to settle.

**Opening case:** A scatterplot of education index vs. life expectancy across 170 countries. Strong positive correlation (r = 0.79). A reader looking at the chart, without anything else, naturally forms the thought "better education leads to longer life." That thought is not what the chart shows. The chart shows a statistical association; whether education causes longer life, whether longer-life-expectancy countries invest more in education, or whether a third variable (institutional quality, wealth) drives both, the chart cannot say.

**Learning outcomes:**
1. (Apply) Build a scatterplot, bubble chart, heatmap, parallel coordinates plot, or connected scatterplot using a four-move prompt.
2. (Understand) Diagnose overplotting and choose among solutions (transparency, jitter, binning, density encoding).
3. (Apply) Use `d3.scaleSqrt` to make a bubble chart's area-not-radius mapping perceptually honest.
4. (Analyze) Apply Cairo's frame: a scatterplot with strong correlation, without explicit causal-disclaimer annotation, invites the reader to over-read.
5. (Evaluate) Decide whether a relationship chart's claim is honest, and what annotation makes it honest if it is not.

**Core content:**
- What a scatterplot actually is — two position channels, one mark per observation
- The overplotting problem and four ways out
- Bubble charts and the radius trap
- Heatmaps: position traded for density
- Parallel coordinates: when dimensions multiply
- Connected scatterplots: time as the third dimension
- Cairo's frame applied precisely: the moral responsibility for what the chart invites the reader to conclude

**Key concepts:** Scatterplot, overplotting, area-not-radius, Pearson's r as label vs. claim, Cairo's frame, parallel coordinates

**Assessment/exercise:** LLM Exercise produces a publishable relationship chart and Cairo-frame annotation that distinguishes association from causation.

**Bridge:** Relationship is about two variables. Chapter 11 returns to one — but with the additional constraint that the parts must add up to one, and that the chart must let the reader compare proportions the eye is poorly equipped to read.

---

### CHAPTER 11 — Part-to-Whole Charts

**One-line:** When the pieces have to add up to one — and the channels that encode proportion differ in how accurately the eye reads them.

**Opening case:** A five-slice pie chart from the pantry — readable, comparable, useful. A twelve-slice pie chart from an annual report — six wedges below 5%, a ring of nearly indistinguishable slivers, the chart technically a part-to-whole visualization and practically useless as a comparison tool. The difference is perceptual: humans judge angle with substantially less accuracy than length.

**Learning outcomes:**
1. (Apply) Build a pie, donut, waffle, stacked bar, treemap, or Marimekko chart using a four-move prompt.
2. (Understand) Diagnose when the pie chart works (≤5 slices, large differences, rhetorical context) and when it fails (more slices, smaller differences, comparison task).
3. (Apply) Convert a failing pie chart into a sorted horizontal bar by recognizing the message as comparison rather than part-to-whole.
4. (Analyze) Read Florence Nightingale's rose chart as the canonical example of an honest distortion — a chart that violates accuracy rules for rhetorical purpose.
5. (Evaluate) Decide when part-to-whole is the wrong question and the message is actually comparison.

**Core content:**
- What the pie chart asks the eye to do (angle and area, both lower-ranked than length)
- When the pie chart works anyway — the narrow conditions
- Waffle charts and what they do differently (count, not area)
- Stacked bars and the single-bar form
- The Marimekko chart and two-dimensional composition
- Florence Nightingale and the honest distortion — the rose chart as rhetorical instrument
- When part-to-whole is the wrong question
- The design decisions in the pantry chart, one by one

**Key concepts:** Angle as channel, waffle counting, stacked bars, Marimekko, Nightingale's rose chart, message vs. structure (revisited)

**Assessment/exercise:** LLM Exercise produces a publishable part-to-whole chart, plus a one-paragraph justification of why the chosen form beats the alternatives.

**Bridge:** Part-to-whole is one level of structure. Chapter 12 introduces depth — nested hierarchies that ask the eye to read containment as the encoding.

---

### CHAPTER 12 — Hierarchy Charts

**One-line:** Containment as the encoding — and the limits the human eye places on how many levels of containment it can read.

**Opening case:** A government budget breaking down into departments, programs, and line items. A treemap shows budget proportions at every level — but cannot show the reporting hierarchy if asked. Different question, different form. The chapter is about which form encodes which kind of hierarchical question.

**Learning outcomes:**
1. (Understand) Distinguish the four hierarchy forms — treemap, sunburst, circle packing, tree diagram — by what each encodes (area, angle, containment, topology).
2. (Apply) Build a treemap, sunburst, circle packing, or tree diagram from hierarchical data using a four-move prompt.
3. (Understand) Explain why squarification matters (Bruls et al., 2000) and what the algorithm protects against.
4. (Analyze) Diagnose depth-limit failures — treemaps with too many levels, sunbursts with too many leaves, dendrograms with too many nodes.
5. (Evaluate) Choose a hierarchy form by whether the reader's question is about quantity (treemap), depth-emphasis (sunburst), irregular structure (circle packing), or exact topology (tree diagram).

**Core content:**
- What a hierarchy actually contains
- The four forms and what each encodes
- Why rectangles win on area comparison
- The depth limit and why it exists
- Squarification and why the algorithm matters
- Sunbursts and the Gestalt figure-ground mechanism
- Irregular depth and circle packing's structural advantage
- The tree diagram: when topology is everything
- How this changes the prompt

**Key concepts:** Treemap, sunburst, circle packing, tree diagram, squarification, depth limit, topology vs. quantity

**Assessment/exercise:** LLM Exercise produces a publishable hierarchy chart with depth and audience documented.

**Bridge:** Hierarchy shows nested structure. Chapter 13 turns to non-nested relationships — flows, networks, and the channel (band width) that distinguishes "how much" from "whether."

---

### CHAPTER 13 — Flow and Network Charts

**One-line:** What flows where — and how much.

**Opening case:** A Sankey diagram of energy sources to end uses. Band widths vary; the thickest band tells you more about energy policy than most prose summaries. Now imagine the same diagram with uniform-width bands. It still shows the paths. It tells you nothing about magnitude. The distinction — *does this connection exist* vs. *how much flows along it* — is the chapter's organizing principle.

**Learning outcomes:**
1. (Apply) Build a Sankey, alluvial, ribbon chord, non-ribbon chord, arc diagram, or force-directed graph using a four-move prompt.
2. (Understand) Distinguish the flow-magnitude family (width as a quantitative channel) from the connection-existence family (binary or near-binary edges).
3. (Apply) Configure a force-directed layout that produces stable, reproducible output rather than the run-dependent "hairball."
4. (Analyze) Diagnose the hairball failure mode and choose a remedy (filtering, community detection, arc-diagram alternative).
5. (Evaluate) Choose between the two families by reader's question.

**Core content:**
- Width as a channel
- The three flow-magnitude forms (Sankey, alluvial, ribbon chord)
- The three connection-existence forms (non-ribbon chord, arc diagram, force-directed)
- The hairball — why force-directed graphs fail past ~50 nodes
- Choosing between the families
- The design decisions in the pantry's Sankey

**Key concepts:** Sankey, alluvial, chord (ribbon vs. non-ribbon), arc diagram, force-directed, hairball, edge bundling

**Assessment/exercise:** LLM Exercise produces a publishable flow or network chart from a real dataset with at least 8 nodes and at least 12 edges.

**Bridge:** Flow is about movement; networks are about connection. Chapter 14 introduces position on the earth — and the distortion risk that does not exist in any other chart family.

---

### CHAPTER 14 — Spatial and Geographic Charts

**One-line:** Position on the earth is the story — and the area of the geographic unit competes with the data encoded in it.

**Opening case:** Two US maps. One shaded by the absolute number of uninsured people — California, Texas, New York, Florida all dark, mostly because they have a lot of people. One shaded by the uninsured rate — Texas still dark, California much lighter, Wyoming darker than California. Same states, same data, different question. The first map is mostly a population map wearing a healthcare costume.

**Learning outcomes:**
1. (Apply) Build a choropleth, dot density map, bubble map, or connection/flow map using a four-move prompt.
2. (Understand) Diagnose the area-size distortion — why absolute counts in choropleths track population rather than the data of interest.
3. (Apply) Convert counts to rates when the geographic units differ in size and the data of interest is per-capita.
4. (Analyze) Choose a map projection (equal-area, conformal, compromise) by what the chart needs to preserve.
5. (Evaluate) Decide when a bubble map outperforms a choropleth (absolute magnitude is the question) and when the choropleth wins (rate or proportion is the question).

**Core content:**
- What geographic visualization is for
- The four spatial forms
- The area-size distortion — the chapter's central failure mode
- Rates, not counts
- Snow's 1854 dot map and why it worked (point geography matched the question)
- Projections and why they matter
- When bubble maps outperform choropleths
- How this changes the prompt

**Key concepts:** Choropleth, dot density, bubble map, connection/flow map, area-size distortion, rate vs. count, projection choice, equal-area projection

**Assessment/exercise:** LLM Exercise produces a publishable spatial chart with the projection choice, rate-vs-count decision, and area-distortion check documented.

**Bridge:** Spatial charts use position on the earth. Chapter 15 closes Part II with the forms whose conventions earn their strangeness — candlesticks, kagi, bullet graphs, radar charts.

---

### CHAPTER 15 — Specialized and Financial Charts

**One-line:** Conventions that earn their strangeness — and the line past which strangeness becomes decorative noise.

**Opening case:** A candlestick chart. Four quantitative values per period encoded in a single glyph using position (the highest-accuracy channel). The convention is so efficient that a trader reads trend, daily range, volatility, and session character in a few seconds. A line chart of closing prices shows one of the four. Specialized charts earn their strangeness when the audience's graphicacy is high enough to read the convention fluently.

**Learning outcomes:**
1. (Apply) Build a candlestick, OHLC, kagi, point-and-figure, bullet graph, or radar chart using a four-move prompt.
2. (Understand) Explain when a specialized convention is justified (audience fluency, multi-attribute compression) and when it is decorative.
3. (Apply) Replace a gauge chart with a bullet graph and explain the perceptual gain.
4. (Analyze) Diagnose the axis-order problem in radar charts — why arbitrary axis permutations produce different visual claims.
5. (Evaluate) Reject a specialized chart when its strangeness is not earned and propose the alternative.

**Core content:**
- What makes a convention earn its strangeness
- Candlestick and OHLC charts — position encoding four values
- Kagi and point-and-figure — time removed from the axis
- Bullet graphs and the gauge replacement
- Radar charts and the axis-order problem
- Polar area charts (a brief return to Nightingale)
- When specialized charts become decorative noise

**Key concepts:** Candlestick, OHLC, kagi, point-and-figure, bullet graph, radar/spider, axis-order problem, graphicacy

**Assessment/exercise:** LLM Exercise produces a publishable specialized chart with a justification for why the strangeness is earned for this audience.

**Bridge:** The chart-family tour is complete. Part III synthesizes — design principles applied across families (Chapter 16), the full project from raw data to published artifact (Chapter 17), and the Brutalist Claude Project delivered as a system prompt (Chapter 18).

---

### CHAPTER 16 — Design Principles in Practice

**One-line:** From principle to audit checklist — and the discipline of running the checklist before the chart ships.

**Opening case:** A quarterly report's bar chart of Q4 sales by region: y-axis starts at $400,000, 3D perspective shading, five gradient colors encoding nothing, heavy gridlines, 8-point italic axis labels rotated 45°, 8-point italic title at top. Take the chart apart one failure at a time. Each failure has a principle and a fix.

**Learning outcomes:**
1. (Understand) Name the four design sources and what each contributes: Tufte (proportional ink, data-ink ratio), Few (clarity over minimization), Cairo (ethics), Evergreen/Emery (the audit checklist as instrument).
2. (Apply) Run the 22-point Evergreen/Emery checklist on a chart and produce an audit log.
3. (Apply) Diagnose color failures across the three vocabularies: categorical (hue), sequential (luminance), diverging (two-hue luminance).
4. (Analyze) Read the proportional-ink principle as the foundation that ties truncated baselines, 3D distortion, and decorative gradients into one mechanism.
5. (Evaluate) Decide whether a chart is publishable, revisable, or restartable after the audit.

**Core content:**
- The four sources and what each contributes
- Proportional ink: the foundation
- Data-ink ratio: the heuristic and its resolution (Few's clarity counterargument)
- Color: the three vocabularies (categorical, sequential, diverging)
- Annotation strategy
- The Evergreen/Emery checklist as the synthesis instrument — Text (5), Arrangement (4), Color (5), Lines (4), Overall (4)
- The audit as design discipline, not just post-processing

**Key concepts:** Proportional ink, data-ink ratio, three color vocabularies, Evergreen/Emery checklist, audit-as-design

**Assessment/exercise:** Run the full Evergreen/Emery audit on a published chart and on a chart the reader produced in an earlier chapter. Compare the audit logs.

**Bridge:** Design principles applied to one chart at a time. Chapter 17 applies the whole framework to a complete project — three charts, one published artifact, one pipeline.

---

### CHAPTER 17 — Building a Complete Project

**One-line:** From raw data to published chart in one pipeline — the test the book asks the reader to pass.

**Opening case:** The Feynman test at the end of a course. If you have been paying attention, you should now be able to figure out things you were never explicitly taught. The chapter is that test. UNHCR forced displacement figures, 2020–2024. Public-policy readers. Three charts. One pipeline.

**Learning outcomes:**
1. (Apply) Run the five-phase pipeline (Audit / Schema / Generate / Verify / Handoff) on a multi-chart project.
2. (Apply) Write a project-level `CLAUDE.md`, `DESIGN.md`, and three chart-level `PROJECT.md` documents.
3. (Apply) Build three coordinated charts that share a visual language, a data source, and a coherent argument.
4. (Analyze) Apply Cairo's final test — is the project truthful, functional, beautiful, insightful, enlightening?
5. (Create) Produce a publishable artifact and write the handoff document.

**Core content:**
- Why a project is different from a chart
- Phase A: the question precedes the data
- Phase B: the schema before the chart — `CLAUDE.md` / `DESIGN.md` split, `PROJECT.md` as decision record
- Phase C: generating the three charts (Where are refugees coming from? Where are they going? Internal vs. international?)
- Phase D: the audit
- Phase E: handoff
- Cairo's final test
- What completing this project teaches

**Key concepts:** Project vs. chart, five-phase pipeline (applied), three-file system (applied), Cairo's final test

**Assessment/exercise:** Run the full pipeline on a multi-chart project of the reader's choosing. Submit dataset, all three governing files, all chart `PROJECT.md` documents, four-move prompts, outputs, audit logs, and final artifact.

**Bridge:** The full pipeline runs by hand in Chapter 17. Chapter 18 delivers the working tool — the Brutalist Claude Project as a system prompt that holds the phase gate so the reader doesn't have to.

---

### CHAPTER 18 — The Brutalist Claude Project

**One-line:** Paste this system prompt once into a Claude Project; the phase gate is enforced in conversation forever after.

**Opening case:** Every Brutalist failure mode the book names — AI generates before intent is clear, AI loses track of what it has produced, AI crosses into decisions that belong to the human, AI applies new information without asking — shows up by default in any AI-assisted workflow without an architecture against them. This chapter delivers the architecture as a single system prompt the reader can install in five minutes.

**Learning outcomes:**
1. (Apply) Install the Brutalist Claude Project into the reader's Claude.ai account.
2. (Apply) Use the named commands (`/init`, `/research`, `/claude`, `/design`, `/project`, `/update`, `/verify`, `/handoff`) to run a chart project end-to-end.
3. (Understand) Explain the "maximally informed and minimally autonomous by design" principle and why every new external input triggers `inform`, never `execute`.
4. (Analyze) Recognize the system's refusal behaviors as the operational form of the labor separation principle.
5. (Evaluate) Decide when the `/silent` modifier is appropriate and when the full interactive mode is required.

**Core content:**
- What the Brutalist Claude Project is
- What it commits the reader to — the three files, the phase gate, the refusal behaviors
- How to install it
- What goes wrong if the reader does not use it
- The full system prompt — pasted in the chapter as the deliverable
- The welcome menu and the named commands
- The `/silent` modifier — when to use it, when not to

**Key concepts:** Claude Project, system prompt, named commands, phase gate (enforced), refusal behavior, `/silent` modifier

**Assessment/exercise:** Install the Brutalist Claude Project. Run `/init` on a new chart project. Walk through the full phase gate. Submit the resulting `CLAUDE.md`, `DESIGN.md`, `PROJECT.md`, and the chart.

**Bridge:** The chart-design course is complete. The catalog (Part IV — Chart Type Catalog, alphabetical) is the reference the reader returns to after the course is over. Appendix F names the broader framework this book applies.

---

## Part IV — Chart Type Catalog (alphabetical, short)

**One-line:** Sixty-one chart types, alphabetically. Each entry is short — a placeholder image, the rich pedagogical text from the working pantry page, a single Claude Code prompt that generates a similar chart and its data file together, and a link to the working code.

**Structure of each entry:**
- Title
- Subtitle (the chart's one-line claim)
- Also known as (synonyms)
- What this chart type is
- How to read this chart
- When to use it / when not to
- Strengths and limitations
- Framework reference (FT Visual Vocabulary · Abela · Tufte)
- About the example dataset
- Prompt (paste into Claude Code)
- Link to the original code at bearbrown.co

**Inventory note:** The Part IV catalog currently has one seeded entry — Arc Diagram — drafted at `chapters/18-arc-diagram.md`. The Reconciliation Report recommends renumbering the Brutalist Project chapter to 18 (as proposed above) and moving the arc-diagram catalog seed into a new directory structure (`catalog/arc-diagram.md`, `catalog/area-chart.md`, etc.). Sixty more catalog entries to be produced in a later pass; the prompt template and structure are already established by the seed entry.

---

## Back Matter

- **Acknowledgments** — Humanitarians AI for the pantry, the Brutalist series predecessors, the Bertin/Cleveland/McGill/Munzner/Tufte/Few/Cairo theoretical debt, the MBTA project, the Curran Kelleher marks-and-channels video.
- **About the Author** — Nik Bear Brown at Northeastern University; the *with LLMs* series; the Brutalist framework at brutalist.art.
- **Chart Type Reference** — a one-page decision guide organized by FT Visual Vocabulary category. Already drafted in `99-back-matter.md`.
- **Selected References** — primary references (theory), primary references (practice), empirical research, algorithmic and implementation references, pantry references. Already drafted in `99-back-matter.md`.
- **Colophon** — the Claude Code-assisted workflow; the four-move prompt structure as method; the Evergreen/Emery audit as instrument; type stack; cover.

---

## Appendices

### Appendix A — Channel Ranking Reference

The Cleveland–McGill ranking, with the perceptual mechanism for each rank and one example chart that maps a quantitative attribute to that channel. One page. Designed to be printed and pinned at the desk.

### Appendix B — FT Visual Vocabulary Quick Card

The eight functional categories, each with its defining reader's question and three to four canonical chart types. One page.

### Appendix C — Four-Move Prompt Template Library

Twelve worked four-move prompts — one per major chart family from Part II, plus three for cross-family cases. Each annotated with the channel decomposition the prompt encodes.

### Appendix D — The Evergreen/Emery Audit Checklist

The 22-point checklist organized into Text (5) / Arrangement (4) / Color (5) / Lines (4) / Overall (4). One page. Designed to be run on every chart before publishing.

### Appendix E — CLAUDE.md / DESIGN.md / PROJECT.md Starter Kits

Three starter templates the reader can paste into a project and edit:
- `CLAUDE.md` — coding constitution, D3 v7 defaults, naming conventions, accessibility standards, four-move prompt template, what Claude Code must not do without instruction
- `DESIGN.md` — visual constitution, color palette with semantic roles, typography stack, spacing scale, dark-mode behavior, responsive breakpoints
- `PROJECT.md` — per-chart audit, decision record, iteration log

### Appendix F — Fundamental Themes of the Practitioner's AI Series

The shared framework that runs across every Practitioner's AI Series book — *AI for Teachers*, *How to Learn with AI: A Student's Guide*, *AI for Writing*, *AI for Graphs* (this book), and the renderer-specific Brutalist modules. Six lenses:

- **Frictional.** The struggle is the mechanism. AI that removes cognitive friction removes the trigger for learning and judgment formation. For chart work, the friction is reading the dataset, formulating the question, naming the channels — Claude Code that handles the syntax preserves the friction that builds chart-design judgment; Claude Code that decides the chart removes it.
- **Phase Gates.** The explicit boundary between human and AI work. For chart work, the gates are: data audit (human), schema (human, with AI help on `CLAUDE.md` defaults), generation (AI under specification), verification (human), handoff (human). The gates are operationalized in the Brutalist phase model (Audit → Schema → Generate → Verify → Handoff).
- **Humans + AI Tiers (1–7).** The taxonomy of capabilities where machines win (pattern/association), where humans win (metacognition, causal reasoning, collective intelligence, wisdom), and where both contribute (embodied, supervisory). Chart design crosses tiers: syntactic execution is Tier 1 (machine); chart selection is Tier 4 (metacognitive); audit is Tier 5 (causal/counterfactual — "if I had chosen the other form, what would the reader see?").
- **AI+1.** Domain-specific learning at the tier boundary — use AI to do faster what was always going to be done, and use the saved time to learn the next thing the human cannot delegate. For chart work, AI+1 says: let Claude Code write the D3, and use the saved time to learn channel theory and chart-type-message matching.
- **Brutalist.** This book's organizing lens. AI lowers the technical barrier (writing D3 v7 from scratch) so the human can focus on the design layer (channel decomposition, chart selection, audit). The architecture is the three-file system and the five-phase model. *This book is the data-visualization application of the Brutalist lens.*
- **Boondoggling.** AI does what AI does best; humans conduct. For chart work, the boondoggle score is high when AI generates output the human cannot evaluate (a Sankey diagram with 200 nodes the human did not specify, a choropleth with a color palette the human did not approve). The four-move prompt and the audit are the anti-boondoggle disciplines.

The appendix is already drafted at `chapters/97-fundamenta-themes.md`. The Reconciliation Report recommends renaming the file to `appendix-f-fundamental-themes.md` (or equivalent) and updating the cross-references throughout the book.

---

## Adoption Risk Register

| # | Risk | Likelihood | Impact | Mitigation |
|---|------|-----------|--------|------------|
| 1 | D3 version churn invalidates code examples | Medium | Medium | Pin v7 explicitly; the four-move prompt's Move 3 always names the version; pantry refresh annually |
| 2 | Claude Code interface changes break the prompt patterns | Medium | Medium | Prompt patterns are model-agnostic; ChatGPT and Gemini variants are documented in Chapter 2 |
| 3 | Readers skip Part I and read chart-family chapters as recipes | High | High | Every chart-family chapter cross-references Chapter 3 (marks/channels) and Chapter 4 (selection); failure to read Part I shows up as "the rules feel arbitrary" |
| 4 | The Brutalist framing reads as proprietary jargon | Medium | Medium | Every Brutalist term is defined operationally on first use; Appendix F places the framework in the Practitioner's AI Series context |
| 5 | The pantry dependency makes the book feel like documentation | Medium | Low | Every chapter has runnable LLM Exercises that do not require the pantry; the pantry is enrichment, not prerequisite |
| 6 | The book is mistaken for a D3 reference (Murray's book is the reference) | Medium | Medium | Frontmatter explicitly names what this book is not; Part I makes the design-judgment focus visible immediately |

---

## Open Questions

| # | Question | Stakes | Decision deadline |
|---|---------|--------|------------------|
| 1 | Does the public-facing title become "AI for Graphs: A Practitioner's Guide" (the directory name) or "Brutalist d3 x Claude" (the frontmatter)? | Series coherence | Before manuscript |
| 2 | Does the Part IV chart-type catalog ship in the same volume, or as a companion reference? | Page count, retail price | Before manuscript |
| 3 | How thick is Chapter 1 — full chapter (5,000–7,000 words) or a long preface? | Part I balance | Before drafting Ch 1 |
| 4 | Does the Brutalist Claude Project chapter ship as Chapter 18 in the main flow or as an appendix? | Reading order | Before final structure freeze |
| 5 | Does the book require Claude Code (recommended) or any LLM (broader audience)? | Adoption breadth | Before marketing copy |
| 6 | Does Appendix F stay generic across the Practitioner's AI Series or get a Brutalist-specific addendum here? | Series-vs-book coherence | Before final structure freeze |

---

*TIKTOC v1.0 — Reverse-engineered from 18 existing chapter drafts*
*Frontmatter, 18 chapters (1 to be written), back matter, and 6 appendices documented*
*Reconciliation Report at `pantry/_reconciliation_report.md`*
