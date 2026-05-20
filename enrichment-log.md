# Enrichment log — ai-for-graphs-a-practitioners-guide

Run dates: 2026-05-19 (canary ch.07) and 2026-05-20 (batch + ch.04 gap fill).

## Per-chapter

02-claude-basics-for-d3-visualization-updated.md — 0 tables rendered (2 placeholder stubs removed; 1 real table kept and relabeled Table 2.1), 1 SVG generated, 1 D3 HTML generated, Wayback Machine: not present, none added
02-claude-basics-for-d3-visualization.md — 0 tables rendered (both existing tables were already real markdown), 5 SVGs generated, 5 D3 HTML files generated, Wayback Machine: kept (Margaret Hamilton)
03-marks-and-channels.md — 0 tables rendered (existing Cleveland & McGill table left as-is), 5 SVGs generated, 5 D3 HTML files generated, Wayback Machine: kept
04-chart-selection-as-design-decision.md — 0 tables rendered, 6 SVGs generated (2 from comments + 4 from pre-authored markdown refs that had no source files), 6 D3 HTML files generated, Wayback Machine: kept
05-reading-a-dataset.md — 0 tables rendered (three existing tables already real markdown), 3 SVGs generated, 3 D3 HTML files generated, Wayback Machine: kept
06-working-with-claude-code.md — 0 tables rendered, 4 SVGs generated, 4 D3 HTML files generated, Wayback Machine: kept
07-comparison-charts.md — 0 tables rendered, 7 SVGs generated, 7 D3 HTML files generated, Wayback Machine: kept (William Playfair)
08-time-series-and-temporal-charts.md — 0 tables rendered, 6 SVGs generated, 6 D3 HTML files generated, Wayback Machine: kept
09-distribution-charts.md — 0 tables rendered (existing graphicacy/form table preserved), 5 SVGs generated, 5 D3 HTML files generated, Wayback Machine: kept (Quetelet)
10-relationship-and-correlation-charts.md — 0 tables rendered, 6 SVGs generated, 6 D3 HTML files generated, Wayback Machine: kept
11-part-to-whole-charts.md — 0 tables rendered, 5 SVGs generated, 5 D3 HTML files generated, Wayback Machine: kept (Georg von Mayr)
12-hierarchy-charts.md — 0 tables rendered, 6 SVGs generated, 6 D3 HTML files generated, Wayback Machine: kept (Ben Shneiderman)
13-flow-and-network-charts.md — 0 tables rendered, 5 SVGs generated, 5 D3 HTML files generated, Wayback Machine: kept
14-spatial-and-geographic-charts.md — 0 tables rendered, 6 SVGs generated, 6 D3 HTML files generated, Wayback Machine: kept
15-specialized-and-financial-charts.md — 0 tables rendered, 4 SVGs generated, 4 D3 HTML files generated, Wayback Machine: kept (Munehisa Homma)
16-design-principles-in-practice.md — 0 tables rendered (Tufte/Few row + 22-item checklist already real markdown), 4 SVGs generated, 4 D3 HTML files generated, Wayback Machine: kept
17-building-a-complete-project.md — 0 tables rendered, 5 SVGs generated, 5 D3 HTML files generated, Wayback Machine: kept (Buckminster Fuller)

## Summary

Total chapters processed: 17 (out of 22 — frontmatter, two ch.18 files, themes, and back-matter had no comments and were skipped)
Total tables rendered: 0 (every chapter shipped its tables as inline markdown already; one chapter had 2 placeholder stubs that were removed)
Total SVG+PNG pairs generated: 83
Total D3 v7 HTML files generated: 83
Total Wayback Machine subjects added: 0 (per Bear's override: only add if missing; every chapter that has one already had a named figure, all were preserved)

## Deviations from the original spec

- **Font embedding.** Spec said "embed font as base64." Overridden after discussion: the SVGs lead with `'EB Garamond', Georgia, 'Times New Roman', serif` and rely on the build machine's fontconfig. EB Garamond is installed on both Bear's Mac and the build sandbox; the SVG→PNG step honors it. Georgia is fallback because it cannot legally be base64-embedded.
- **Wayback Machine rule.** Spec said replace any post-2000 subject. Overridden: "only add a Wayback Machine if it doesn't exist; otherwise skip." All 17 processed chapters with a Wayback section had a named pre-2000 figure already, so PASS 3 was a no-op everywhere.
- **Chapter 4 gap fill.** Ch.04 shipped with four markdown image refs (fig-01..fig-04) that had no source files and no comment markers. The original spec scope wouldn't have produced them; a follow-up agent generated those 4 SVG + 4 D3 pairs from the chapter's pre-existing alt text.
- **Plugin CDNs.** Ch.13 (Sankey diagrams) and Ch.14 (TopoJSON maps) load d3-sankey and TopoJSON from cdnjs/jsDelivr alongside the pinned D3 7.9.0 core. The CLAUDE.md constitution pins only D3 core; the additional plugin URLs are documented inside each affected HTML file.
- **Chapter 6 figure numbering.** The chapter's body prose calls itself "Chapter 5" and uses Stage 4 / Exercise 5.x throughout (vestigial from a prior outline). The processing agent matched the body convention — figures are labeled `Figure 5.1` through `5.4` — rather than the H1 ("Chapter 06"). Flagging for editorial decision.
- **02-updated vs 02 original.** Both `02-claude-basics-for-d3-visualization-updated.md` and `02-claude-basics-for-d3-visualization.md` were processed. They share the chapter number 02 but different slugs; the "updated" file is short (~96 lines) and may be a placeholder. No file collision, but the duplicate likely needs editorial reconciliation.
- **Two ch.18 files, two ch.97/99 files.** `18-arc-diagram.md`, `18-brutalist-claude-project.md`, `00-frontmatter.md`, `97-fundamenta-themes.md`, `99-back-matter.md` had zero figure comments and were skipped. The ch.18 duplication is the same outline issue as ch.02.

## Verification snapshot

- SVG files: 83
- PNG files: 83 (1:1 with SVGs, all rasterized at 300dpi via `SCRIPTS/svg-to-png.mjs`)
- D3 HTML files: 83 (1:1 with SVGs)
- All SVGs contain `EB Garamond` in the font-family chain (verified via grep)
- All D3 HTML files pin `https://cdnjs.cloudflare.com/ajax/libs/d3/7.9.0/d3.min.js` (verified via grep -L)
- No chapter has an unresolved `<!-- → [TABLE|IMAGE|FIGURE|DIAGRAM|INFOGRAPHIC|CHART: ...] -->` marker
- No chapter has a dangling `../images/{slug}-fig-NN.png` reference without a backing file
