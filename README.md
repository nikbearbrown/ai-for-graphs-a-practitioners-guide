# AI for Graphs A Practitioner's Guide

**Author:** Nik Bear Brown
**Publisher:** Bear Brown, LLC
**Status:** Draft
**Started:** 2026-05-18

## Structure

```
book.md                 ← book description and high-level outline (planning)
outline.md              ← starter table of contents (planning)
vision.md               ← Tic TOC Phase 1: vision and positioning
architecture.md         ← Tic TOC Phase 2: learning architecture
chapters-spec.md        ← Tic TOC Phase 3: chapter specifications
risks.md                ← Tic TOC Phase 4: scope, market, risks
pantry/                 ← scratch storage for fragments, snippets, leftovers
chapters/
    00-frontmatter.md   ← copyright, dedication, preface
    01-introduction.md  ← Chapter 0 / Introduction
    02-chapter-01.md    ← Chapter 1
    ...
    04-chapter-03.md    ← Chapter 3
    99-back-matter.md   ← acknowledgments, about the author, notes, references, index
```

## Planning Documents

| File | Purpose |
|------|---------|
| `book.md` | One-sentence pitch, the argument, the gap, the reader, high-level outline. |
| `outline.md` | Chapter-level table of contents — keep in sync with `chapters/`. |
| `vision.md` | Tic TOC Phase 1 — book concept, type, learner profile, thesis, field positioning. |
| `architecture.md` | Tic TOC Phase 2 — learning outcomes, sequencing, three-act arc, prerequisites. |
| `chapters-spec.md` | Tic TOC Phase 3 — per-chapter specs, cases, contested claims, coverage gaps. |
| `risks.md` | Tic TOC Phase 4 — comparable texts, features, out of scope, adoption risks. |
| `pantry/` | Scratch storage for fragments and snippets that don't yet belong in a chapter. |

These files are for planning only. They are not compiled into the EPUB.

The four Tic TOC files are templated with `[NEEDS HUMAN INPUT]` markers
and a `*Phase N output from Tic TOC*` header signature. Run Tic TOC's
`/scaffold silent` to fill them from `book.md`, `outline.md`, `pantry/`,
and `chapters/`. Or build them section-by-section through the interactive
phase commands (`/i1` → `/m4`).

## Chapters

| File | Title | Status |
|------|-------|--------|
| 00-frontmatter.md | Front Matter (copyright, dedication, preface) | ☐ |
| 01-introduction.md | Introduction | ☐ |
| 02-chapter-01.md | Chapter 1 | ☐ |
| 03-chapter-02.md | Chapter 2 | ☐ |
| 04-chapter-03.md | Chapter 3 | ☐ |
| 99-back-matter.md | Back Matter (acknowledgments, notes, references, index) | ☐ |

## Build

```bash
./build.sh
```

Output goes to `output/` (gitignored).

## Figures

```bash
./graphs.sh
```

Processes `<!-- → [TYPE: description] -->` comments in every chapter:
- Tabular figures → classed markdown tables (`.infographic-table`, `.comparison-table`, `.data-table`)
- Non-tabular figures → placeholder images in `images/`, ready to replace
- CSS log appended to `styles/kindle-book.css` on each run

Review `chapters/*-updated.md`, then promote:
```bash
for f in chapters/*-updated.md; do mv "$f" "${f/-updated/}"; done
```

## Styles

| File | Purpose |
|------|---------|
| `styles/kindle.css` | Shared base — typography, figure table classes. Do not edit per book. |
| `styles/kindle-book.css` | Book-specific overrides. Edit freely. `graphs.sh` appends its log here. |

## Publish

Upload `output/ai-for-graphs-a-practitioners-guide.epub` to [KDP](https://kdp.amazon.com).

---

## What This Book Is

Copyright © 2026 Nik Bear Brown. All rights reserved.

Published by Bear Brown, LLC.

No part of this publication may be reproduced, distributed, or transmitted in any form or by any means without the prior written permission of the publisher, except in the case of brief quotations in critical reviews and certain other noncommercial uses permitted by copyright law.

---

## Who This Book Is For

<!-- TODO: populate from chapter content -->

---

## How to Read It

<!-- TODO: populate from chapter content -->

---

## Table of Contents

| Chapter | Title | File |
|---------|-------|------|
| 2 | Chapter 02 — Claude Basics for D3 Visualization | [chapters/02-claude-basics-for-d3-visualization-updated.md](chapters/02-claude-basics-for-d3-visualization-updated.md) |
| 2 | Chapter 02 — Claude Basics for D3 Visualization | [chapters/02-claude-basics-for-d3-visualization.md](chapters/02-claude-basics-for-d3-visualization.md) |
| 3 | Chapter 3 — Marks and Channels | [chapters/03-marks-and-channels.md](chapters/03-marks-and-channels.md) |
| 4 | Chapter 4 — Chart Selection as Design Decision | [chapters/04-chart-selection-as-design-decision.md](chapters/04-chart-selection-as-design-decision.md) |
| 5 | Chapter 05 — Reading a Dataset | [chapters/05-reading-a-dataset.md](chapters/05-reading-a-dataset.md) |
| 6 | Chapter 6 — Working with Claude Code | [chapters/06-working-with-claude-code.md](chapters/06-working-with-claude-code.md) |
| 7 | Chapter 07 — Comparison Charts | [chapters/07-comparison-charts.md](chapters/07-comparison-charts.md) |
| 8 | Chapter 8 — Time Series and Temporal Charts | [chapters/08-time-series-and-temporal-charts.md](chapters/08-time-series-and-temporal-charts.md) |
| 9 | Chapter 09 — Distribution Charts | [chapters/09-distribution-charts.md](chapters/09-distribution-charts.md) |
| 10 | Chapter 10 — Relationship and Correlation Charts | [chapters/10-relationship-and-correlation-charts.md](chapters/10-relationship-and-correlation-charts.md) |
| 11 | Chapter 11 — Part-to-Whole Charts | [chapters/11-part-to-whole-charts.md](chapters/11-part-to-whole-charts.md) |
| 12 | Chapter 12 — Hierarchy Charts | [chapters/12-hierarchy-charts.md](chapters/12-hierarchy-charts.md) |
| 13 | Chapter 13 — Flow and Network Charts | [chapters/13-flow-and-network-charts.md](chapters/13-flow-and-network-charts.md) |
| 14 | Chapter 14 — Spatial and Geographic Charts | [chapters/14-spatial-and-geographic-charts.md](chapters/14-spatial-and-geographic-charts.md) |
| 15 | Chapter 15 — Specialized and Financial Charts | [chapters/15-specialized-and-financial-charts.md](chapters/15-specialized-and-financial-charts.md) |
| 16 | Chapter 16 — Design Principles in Practice | [chapters/16-design-principles-in-practice.md](chapters/16-design-principles-in-practice.md) |
| 17 | Chapter 17 — Building a Complete Project | [chapters/17-building-a-complete-project.md](chapters/17-building-a-complete-project.md) |
| 18 | Part II — Examples | [chapters/18-arc-diagram.md](chapters/18-arc-diagram.md) |
| 18 | Chapter 16 — The Brutalist Claude Project | [chapters/18-brutalist-claude-project.md](chapters/18-brutalist-claude-project.md) |
| 97 | The Fundamental Themes | [chapters/97-fundamenta-themes.md](chapters/97-fundamenta-themes.md) |

---

## Signature Simulations

| Chapter | Topic | Simulation |
|---------|-------|------------|
| 18 | Part II | AI Wayback Machine |

---

## About the Author

**Nik Bear Brown** teaches data science, AI, and visualization at Northeastern University. His work spans machine learning, generative AI, data visualization, and the design of AI-assisted production pipelines. He is the author of the *with LLMs* textbook series and the architect of the **Brutalist** system for AI-assisted creative production — the renderer-agnostic framework whose D3 module is this book and whose other modules include *Brutalist After Effects x Claude*, *Brutalist Blender x Claude*, and *Brutalist Remotion x Claude*. The framework lives at [brutalist.art](https://www.brutalist.art/).

He works in Boston and writes occasionally at his website. He is on most of the major social-media platforms under variations of his name.

---

## Copyright

Copyright © 2026 Nik Bear Brown. All rights reserved.

Published by Bear Brown, LLC.

No part of this publication may be reproduced, distributed, or transmitted in any form or by any means without the prior written permission of the publisher, except in the case of brief quotations in critical reviews and certain other noncommercial uses permitted by copyright law.

The visualizations referenced in this book are drawn from the Humanitarians AI D3 example set, used with permission. The pantry of working examples is available alongside the book as a companion repository.

ISBN: [pending]

First edition: 2026

