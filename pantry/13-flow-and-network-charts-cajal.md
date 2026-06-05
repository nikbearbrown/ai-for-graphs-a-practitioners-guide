# CAJAL Figure Intelligence — Chapter 13: Flow and Network Charts

**Source:** `chapters/13-flow-and-network-charts.md`
**Mode:** `/scan silent`
**Domain note:** AI+1 practitioner guide / data visualization with D3 and Claude. Chapter walks the flow/network family (Sankey, alluvial, ribbon chord, non-ribbon chord, arc, force-directed) through Bertin's width-as-channel, Tufte's proportional ink, the magnitude-vs-existence distinction, and the hairball mitigation strategies. Five author-placed figures.

---

## Density Recommendation

**5 figures, Concept-density.** All five are abstract chart-type skeletons: topology-vs-magnitude Sankey pair, proportional-ink width audit, three magnitude-family layouts, hairball mitigation grid, design-decision Sankey callouts.

---

## Zone Map

- **MC:** Bertin's width-as-magnitude channel (ranks ~3 in Cleveland & McGill hierarchy). Tufte's proportional ink applied to flow bands. Magnitude-vs-existence as form-family fork. Hairball as structural failure. Four mitigations: filter, cluster, aggregate, matrix.
- **VG:** Sankey two-to-four-column layout. Alluvial longitudinal bands. Ribbon chord around a circle. Arc above horizontal axis. Force-directed clustered spatial layout. Adjacency matrix grid.
- **PQ:** Sankey 5–30 nodes per column. Chord 5–20 entities. Arc 10–60 nodes. Force-directed 5–50 before hairball. Proportional-width audit: ratio of widest to second-widest must equal data ratio.

---

## Figure 13.1 — Magnitude vs Topology Sankey Pair

**Priority: Critical.** The chapter's organizing question made visible.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition. Both panels show the same three-column flow topology: three Sky Blue `#56B4E9` filled vertical rectangles on the left (source nodes), three Bluish Green `#009E73` filled vertical rectangles in the middle (intermediate transformations), and three Orange `#E69F00` filled vertical rectangles on the right (destinations). Black `#000000` 1pt thin borders around each node rectangle. Left panel (magnitude-encoded): connecting bands between columns with varying widths — one dominant thick band Blue `#0072B2` 15% opacity from top-left source through top-middle intermediate to top-right destination, plus several medium and thin bands for the other connections. Right panel (topology-only): same connection topology but every band rendered as a uniform thin Blue 1pt curve, no width variation. Both panels framed by no axes. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same three-column three-node flow topology shown two ways. Left: varying band widths encode flow magnitude. Right: uniform thin curves show only connection existence.
[O] Two panels horizontal. Three node columns per panel: source / intermediate / destination. Bands flow left to right.
[P] Source nodes Sky Blue. Intermediate nodes Bluish Green. Destination nodes Orange. Node borders Black 1pt. Magnitude bands Blue 15% opacity. Topology curves Blue 1pt.
[E] No node labels, no flow-value annotations, no axis labels, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, node labels, flow-value annotations, axis labels, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 13.2 — Tufte Proportional Ink Audit

**Priority: Important.** The proportionality-check argument.

### Block 1 — Illustrae paste block

A two-panel side-by-side composition. Both panels show three horizontal flow bands stacked vertically — large, medium, small — flowing left to right between two node columns: a Sky Blue `#56B4E9` filled source column on the left and an Orange `#E69F00` filled destination column on the right. Left panel (proportional): three Blue `#0072B2` 25% opacity bands with widths in correct 5:2.5:1 ratio (e.g., 40px, 20px, 8px). Right panel (failure): the same three bands but with incorrect widths in 2.5:1.7:1 ratio (e.g., 30px, 20px, 12px) — visibly less dramatic differentiation, the smallest band relatively larger than it should be. Each band a clean horizontal flow connecting a source to a destination. Bands separated vertically with no gap. No axes. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Three flows of values 400 / 200 / 80. Left: correctly proportional widths (40 / 20 / 8 px). Right: failure widths (30 / 20 / 12 px) showing the broken ratio.
[O] Two panels horizontal. Three stacked bands per panel between left source column and right destination column.
[P] Source column Sky Blue. Destination column Orange. Bands Blue 25% opacity. Node borders Black 1pt.
[E] No band labels, no width annotations, no value numbers, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, band labels, width annotations, value numbers, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 13.3 — Three Magnitude-Family Forms

**Priority: Critical.** The chapter's central typology grid.

### Block 1 — Illustrae paste block

A three-panel side-by-side composition. Left panel (Sankey): three node columns — Sky Blue `#56B4E9` source nodes on the left, Bluish Green `#009E73` intermediate nodes in the middle, Orange `#E69F00` destination nodes on the right, connected by Blue `#0072B2` 25% opacity bands of varying widths flowing left to right. Center panel (alluvial): three vertical time-step columns, each column showing four stacked colored category bands (Blue / Sky Blue / Bluish Green / Orange) of varying heights. Between columns, curved Reddish Purple `#CC79A7` 20% opacity ribbons crossing from each category at time t to its split across categories at time t+1. Right panel (ribbon chord): a circular ring of four arc segments around the circumference (Blue / Sky Blue / Bluish Green / Orange in 90° quadrants), each separated by thin Black `#000000` 1pt radial lines. Inside the circle, three thick Reddish Purple 20% opacity curved ribbons connecting pairs of arc segments across the interior. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Three magnitude-channel forms side by side: Sankey (three columns, directional), alluvial (three time steps, four categories, transition ribbons), ribbon chord (four entities, circular, three connecting ribbons).
[O] Three panels horizontal. Equal panel sizes. Sankey left-to-right. Alluvial left-to-right time. Chord circular.
[P] Sankey nodes Sky Blue / Bluish Green / Orange; bands Blue 25% opacity. Alluvial category bands Blue / Sky Blue / Bluish Green / Orange; ribbons Reddish Purple 20%. Chord arc segments Blue / Sky Blue / Bluish Green / Orange; interior ribbons Reddish Purple 20%. Borders Black 1pt.
[E] No node labels, no time-step labels, no entity names, no form names, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, node labels, time-step labels, entity names, form names, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 13.4 — Hairball Mitigation Grid

**Priority: Critical.** Four mitigations made visible.

### Block 1 — Illustrae paste block

A 2×2 grid of four equal-sized panels showing the same dense network rendered differently. Top-left (hairball): about 60 small Blue `#0072B2` filled circles distributed across the panel connected by many thin Black `#000000` 1pt edges crossing each other in a dense tangled mass — structure invisible. Top-right (filter): the same Blue circles but only about 25 visible (highest-degree subset), connected by fewer cleaner edges, the underlying structure starting to emerge. Bottom-left (cluster): eight larger Sky Blue `#56B4E9` filled circles (super-nodes), each with a Black 1pt outline, connected by Black 1pt edges, plus a few Reddish Purple `#CC79A7` curved edges between cluster pairs to indicate the aggregated network. Bottom-right (matrix): a grid of small square cells (~25 rows × 25 columns), each cell either filled Blue (connection exists) or left white (no connection), with thin Black 0.5pt borders between cells; some clear darker bands and clusters visible along the diagonal indicating sorted-degree structure. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Same dense network shown four ways. Top-left: unmitigated hairball. Top-right: top-degree filter. Bottom-left: eight-cluster aggregation. Bottom-right: sorted adjacency matrix.
[O] 2×2 grid. Equal panel sizes. Same underlying network shown four ways.
[P] Hairball nodes Blue, edges Black 1pt. Filter same palette, fewer edges. Cluster super-nodes Sky Blue Black 1pt outline; cluster edges Reddish Purple. Matrix cells Blue (filled) or white (empty), borders Black 0.5pt.
[E] No node labels, no degree numbers, no mitigation names, no panel titles, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, node labels, degree numbers, mitigation names, panel titles, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## Figure 13.5 — Annotated Sankey Design Decisions

**Priority: Important.** Four explicit specifications on one Sankey.

### Block 1 — Illustrae paste block

A single Sankey diagram occupying the panel. Three columns of nodes: five Sky Blue `#56B4E9` source nodes on the left (stacked vertically with thin Black `#000000` 1pt borders), four Bluish Green `#009E73` intermediate nodes in the middle, and three Orange `#E69F00` destination nodes on the right. Between columns, Blue `#0072B2` 25% opacity bands of varying widths flow left to right — one band notably thickest (dominant flow), several medium, and several thin bands. Around the diagram, four small Black 1pt outlined circular numbered callout markers (empty circles, no graphic text) positioned at: the widest band (proportional width callout), the boundary between two cleanly stacked intermediate nodes (node-ordering callout), a source node where its hue clearly carries downstream through its outgoing bands (color-follows-source callout), and the widest band again where a label would sit (label-on-dominant-flows callout). Each marker connected to its referenced location by a thin Black 1pt leader line. White background, flat vector, double-column 174mm preferred.

### Block 2 — Full SCOPE prompt

[S] Double-column 174mm preferred, vector, white background.
[C] Three-column Sankey with four numbered callout markers (empty circles) positioned over: widest band (proportional width), node boundary (ordering), source-hue cascade region (color follows source), label position on dominant flow.
[O] Sankey left-to-right with three node columns. Callout markers around the diagram, leader lines to specific features.
[P] Source column Sky Blue. Intermediate Bluish Green. Destination Orange. Bands Blue 25% opacity. Node borders Black 1pt. Callout markers Black 1pt outlined circles, white-fill. Leader lines Black 1pt.
[E] No callout numbers rendered as graphic, no decision text, no node labels, no flow values, no chart title, no decorative ornament, no shadows.

### Block 3 — Negative prompt

text labels, callout numbers, decision text, node labels, flow values, chart title, gibberish letters, titles, captions, decorative ornament, photographic elements, realistic 3D textures, drop shadows, gradient fills, gradient backgrounds, hand-drawn styles, sketch lines, decorative borders, colorful backgrounds, visual clutter, fuzzy borders, watermarks, red-green color combinations, rainbow color scales, 3D perspective distortion

---

## What CAJAL Declines to Architect

- **Form-comparison table (Sankey / alluvial / chord / arc / force-directed).** Typography reference table; body or sidebar.
- **Key Terms block.** Glossary text.
- **Prompt code blocks.** Code samples, not figures.
- **Charles Joseph Minard portrait.** AI Wayback Machine reference image, generated by separate pipeline.

---

## Video Candidate Pass

**FIGURE 13.1 (Magnitude vs topology Sankey):** STATIC SUFFICIENT.
**FIGURE 13.2 (Proportional-ink audit):** STATIC SUFFICIENT.
**FIGURE 13.3 (Three magnitude-family forms):** STATIC SUFFICIENT.
**FIGURE 13.4 (Hairball mitigation grid):** **MILD VIDEO CANDIDATE.** Animating the morph from hairball → filtered → clustered → matrix would teach the mitigation choices as transformations. Static comparison serves the chapter.
**FIGURE 13.5 (Annotated Sankey):** STATIC SUFFICIENT.

**Video candidates identified: 0 strong + 1 mild.** Recommended: keep all five static; treat 13.4 as a candidate for an interactive companion in the pantry. The chapter's natural video candidate is the alluvial form (time-step transitions animated), which is implicit in Fig 13.3's center panel.

---

## Split-point note

Chapter cross-references Chapter 3 (Bertin's width-as-channel; Gestalt law of connection driving force-directed cluster perception; Stevens' law on area for super-nodes in cluster view), Chapter 4 (chart-family selection — confirming flow/network family), and Chapter 11 (chord forms shared with part-to-whole layouts). Color convention across figures: Sky Blue = sources, Bluish Green = intermediates, Orange = destinations, Blue = magnitude bands, Reddish Purple = cluster/transition overlays. Keep this consistent.
