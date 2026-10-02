---
name: Newsleaf
description: Energy news plotted as a navigational chart of price-pressure vectors.
colors:
  chart-ground: "#0E1614"
  surface: "#15201D"
  surface-raised: "#1C2926"
  grid-line: "#16221F"
  rule: "#2B3935"
  ink: "#E3EBE8"
  muted: "#97A7A2"
  weak: "#5F6E6A"
  teal: "#4DB6A7"
  teal-ink: "#0B1412"
  land: "#17332E"
  amber-up: "#E9A553"
  amber-up-bg: "#3A2A15"
  periwinkle-down: "#9DAAF2"
  periwinkle-down-bg: "#1F2650"
typography:
  display:
    fontFamily: "Barlow Condensed, Arial Narrow, sans-serif"
    fontSize: "clamp(3rem, 5.6vw, 5.4rem)"
    fontWeight: 700
    lineHeight: 0.95
    letterSpacing: "-0.005em"
  numeral:
    fontFamily: "Barlow Condensed, Arial Narrow, sans-serif"
    fontSize: "clamp(3.4rem, 7vw, 5.6rem)"
    fontWeight: 700
    lineHeight: 0.9
    letterSpacing: "normal"
  headline:
    fontFamily: "Barlow Condensed, Arial Narrow, sans-serif"
    fontSize: "clamp(2.4rem, 5.2vw, 4.5rem)"
    fontWeight: 700
    lineHeight: 0.95
    letterSpacing: "-0.005em"
  title:
    fontFamily: "Barlow Condensed, Arial Narrow, sans-serif"
    fontSize: "clamp(1.5rem, 2.4vw, 1.9rem)"
    fontWeight: 700
    lineHeight: 1
    letterSpacing: "-0.005em"
  body:
    fontFamily: "Barlow, system-ui, -apple-system, Segoe UI, sans-serif"
    fontSize: "18px"
    fontWeight: 400
    lineHeight: 1.55
  lede:
    fontFamily: "Barlow, system-ui, -apple-system, Segoe UI, sans-serif"
    fontSize: "clamp(1.1rem, 1.6vw, 1.3rem)"
    fontWeight: 400
    lineHeight: 1.55
  label:
    fontFamily: "Barlow Condensed, Arial Narrow, sans-serif"
    fontSize: "0.85rem"
    fontWeight: 600
    letterSpacing: "0.07em"
  measure:
    fontFamily: "Spline Sans Mono, ui-monospace, Menlo, monospace"
    fontSize: "0.78rem"
    fontWeight: 400
    letterSpacing: "0.02em"
rounded:
  none: "0px"
  point: "50%"
spacing:
  gutter: "clamp(16px, 4vw, 56px)"
  section: "clamp(72px, 10vw, 128px)"
  section-head: "clamp(40px, 6vw, 72px)"
  title-block: "clamp(22px, 3vw, 34px)"
  panel: "22px"
  grid-cell: "48px"
components:
  button-primary:
    backgroundColor: "{colors.teal}"
    textColor: "{colors.teal-ink}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    padding: "13px 20px"
  button-primary-hover:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.teal-ink}"
  button-outline:
    backgroundColor: "transparent"
    textColor: "{colors.teal}"
    rounded: "{rounded.none}"
    padding: "13px 20px"
  button-outline-hover:
    backgroundColor: "{colors.land}"
    textColor: "{colors.ink}"
  button-small:
    padding: "8px 14px"
  title-block:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "{spacing.title-block}"
  input-search:
    backgroundColor: "{colors.chart-ground}"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "14px 16px"
  chip:
    backgroundColor: "{colors.chart-ground}"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "6px 11px"
  chip-selected:
    backgroundColor: "{colors.teal}"
    textColor: "{colors.teal-ink}"
  direction-up:
    backgroundColor: "{colors.amber-up-bg}"
    textColor: "{colors.amber-up}"
    rounded: "{rounded.none}"
    padding: "3px 9px"
  direction-down:
    backgroundColor: "{colors.periwinkle-down-bg}"
    textColor: "{colors.periwinkle-down}"
    rounded: "{rounded.none}"
    padding: "3px 9px"
  tag:
    backgroundColor: "transparent"
    textColor: "{colors.muted}"
    rounded: "{rounded.none}"
    padding: "2px 7px"
---

# Design System: Newsleaf

## Overview

**Creative North Star: "The Pilot Chart"**

Newsleaf is drawn as a navigational chart at night. Every event is a position on the chart and every effect is a heading vector of price pressure: amber for up, periwinkle for down, drawn out from the event. The ground is a deep green-black sea with a faint 48px chart grid. Coastlines are teal hairlines over dark land, depths are small monospace soundings, and a compass rose anchors the hero. Panels are chart title blocks: rectangular, framed in teal, never lifted off the paper.

Density is that of a working chart. Long condensed uppercase titles, quiet sans body copy in muted ink, and monospace used only where something is measured (times, counts, sources, dollar amounts on bars). Hierarchy comes from line weight and colour on one flat plane, never from shadow or rounding. The page is dark green throughout; this is a pinned brand commitment, not a mood choice.

Explicitly rejected: the fintech SaaS hero-plus-feature-cards page. Sections are chart sheets divided by rules, not grids of floating cards.

**Key Characteristics:**
- One flat dark-green plane; depth by tone (ground, surface, surface-raised) and line weight only.
- Teal is the chart's structural ink: frames, coastlines, links, primary actions, focus.
- Amber and periwinkle carry direction and nothing else.
- Square corners everywhere; circles appear only as chart point symbols.
- Barlow Condensed caps for titles and labels, Barlow for reading, Spline Sans Mono for measurements.
- Vectors draw on load; the chart re-plots rather than animating decoration.

## Colors

A low-chroma green-black chart palette with one structural teal and a strict up/down pair.

### Primary
- **Chart Teal** (`teal`): the chart's ink. 1.5px title-block frames, section top rules, coastline hairlines, links, solid and outline buttons, selected chips and run toggles, the focus ring, and the "new" status. Text on solid teal is **Abyss Ink** (`teal-ink`).

### Secondary
- **Heading Amber** (`amber-up`): upward price pressure only. Up vectors, up arrows, "up" direction badges, and the "weakened" status. Its badge ground is **Amber Shoal** (`amber-up-bg`).

### Tertiary
- **Periwinkle Current** (`periwinkle-down`): downward price pressure only. Down vectors, down arrows, "down" badges, and the depth soundings on the hero chart. Its badge ground is **Deep Indigo Shoal** (`periwinkle-down-bg`).

### Neutral
- **Night Sea** (`chart-ground`): page background, input and chip grounds, and the ground of inset diagrams.
- **Chart Grid** (`grid-line`): the 48px graph-paper grid behind the hero. Barely visible by design.
- **Title Block Green** (`surface`): fill for framed panels (hero title block, morning issue, search, framed section heads, figure frames).
- **Raised Shelf** (`surface-raised`): second tone inside figures (investment and entity nodes, inactive comparison bars).
- **Land Teal** (`land`): land masses under coastlines, the outline-button hover fill, accent-tinted nodes, and the highlighted comparison column.
- **Hairline Rule** (`rule`): 1px dividers, chip and tag borders, input borders, gapped-grid seams.
- **Chart Ink** (`ink`): headlines and primary copy.
- **Sounding Grey** (`muted`): secondary copy, captions, measurements, nav links at rest, the "unchanged" status.
- **Faded Line** (`weak`): superseded or decayed arrows and seen items. Strokes only, never text.

### Named Rules
**The Direction-Only Rule.** Amber means up and periwinkle means down. Neither is ever used for decoration, emphasis, or branding outside the logo mark. The build carries one exception: the "weakened" status marker is amber even when the weakened arrow points down. Do not extend that reuse to new elements.

**The Teal Ink Rule.** Teal is the only structural accent. If a frame, rule, link, or action needs colour, it is teal.

## Typography

**Display Font:** Barlow Condensed (with Arial Narrow, sans-serif)
**Body Font:** Barlow (with system-ui, -apple-system, Segoe UI, sans-serif)
**Label/Mono Font:** Spline Sans Mono (with ui-monospace, Menlo, monospace)

**Character:** Condensed industrial caps read like chart titles and legend entries; the humanist Barlow body keeps long explanations easy; the mono is reserved for the numbers a navigator would read off the chart.

### Hierarchy
- **Display** (700, clamp(3rem, 5.6vw, 5.4rem), 0.95, uppercase): the hero headline inside the title block.
- **Numeral** (700, clamp(3.4rem, 7vw, 5.6rem), 0.9, uppercase): stand-alone figures (price, flow drop). The ask amount goes larger (clamp(4.5rem, 13vw, 10rem), 0.85) in teal. A small muted caption in the same face sits beneath at 0.3em.
- **Headline** (700, clamp(2.4rem, 5.2vw, 4.5rem), 0.95, uppercase, balanced, max 20ch): section headlines.
- **Title** (700, clamp(1.5rem, 2.4vw, 1.9rem), 1, uppercase): sub-heads, panel titles, step titles (1.45rem, 0.02em tracking).
- **Body** (400, 18px, 1.55): reading copy, usually in muted ink, 52-68ch measure. Emphasis in body is weight 600 in Chart Ink.
- **Lede** (400, clamp(1.1rem, 1.6vw, 1.3rem), muted, max 60ch): the paragraph beside a section headline.
- **Label** (600, 0.82-0.9rem, 0.06-0.08em, uppercase): nav links, tags, definition terms, legend and figure labels, status words (700).
- **Measure** (Spline Sans Mono 400/500, 0.75-0.85rem, 0.02em): timestamps, outlet counts, source lines, values on bars, step numbers.

### Named Rules
**The Soundings Rule.** Mono is for measured values only: times, counts, amounts, sources. Never for headings, buttons, or prose.

**The Chart Title Rule.** All headings and labels are Barlow Condensed uppercase; reading copy is never uppercase.

## Layout

Content sits in a 1280px column with a fluid gutter (`spacing.gutter`). Sections are full-width bands with `spacing.section` vertical padding, separated by 1px rules. Section heads are a 7/5 split (headline left, lede right, bottom-aligned), with stacked (max 880px) and framed variants. Within sections, content is split into ruled columns: a 1.5px teal rule on top, 1px rule seams between columns, no gaps or cards. Gapped grids (1px rule showing through a 1px gap) are used for compact direction readouts.

The hero is full-bleed chart: title block in a 600px column at left, the chart bleeding off the right edge, min height min(100svh - 58px, 900px). Below 900px the grid stacks to one column, the chart takes a fixed 880/760 aspect ratio, the compass rose and on-chart explanations hide, and a two-column direction readout replaces them. Nav links hide below 820px, leaving brand and the ask button. Sticky leg headers in How it Works become static below 900px.

Spacing rhythm in use is 6, 8, 10, 12, 14, 18, 22, 28 px for internal gaps, scaling to 40-72px between blocks.

## Elevation & Depth

The system is flat. There are no drop shadows anywhere. Depth is tonal (Night Sea, then Title Block Green, then Raised Shelf) and linear (1px rules for division, 1.5px teal for framing). The only translucency is the sticky nav: Night Sea at 92% with an 8px backdrop blur and a bottom rule. Inset 1px box-shadows appear only as drawn strokes (status rings, bar outlines), never as lift.

### Named Rules
**The Chart Paper Rule.** Everything lies on the chart. No shadow, no hover lift, no floating cards. If something needs prominence, frame it in teal or fill it with surface tone.

## Shapes

Rectangles with square corners (`rounded.none`), always: buttons, inputs, chips, tags, badges, panels, bars. Frames are 1.5px teal for title blocks and section top rules; 1px rule for secondary containers; dashed borders mark types or projected paths (event types, the funding route). Circles (`rounded.point`) exist only as chart point symbols: status dots, route stops, axis markers, the logo hub. Arrows are drawn SVG strokes with round caps, 2-4px on charts, inline as 1em icons in text.

## Components

### Buttons
Squared chart controls in condensed caps.
- **Shape:** square corners (0px), 1.5px teal border.
- **Primary (solid):** teal fill, Abyss Ink text, Barlow Condensed 700 at 1.08rem, 0.07em tracking, 13px 20px padding.
- **Outline:** transparent with teal text and border.
- **Hover / Focus:** solid goes to Chart Ink fill and border; outline fills Land Teal with Chart Ink text; 0.3s on the system ease. Focus is a 2px teal outline offset 3px.
- **Small:** 8px 14px padding, 0.95rem; used for the nav ask.

### Chips
- **Style:** Night Sea ground, 1px rule border, Barlow 0.9rem, 6px 11px.
- **State:** hover turns the border teal; pressed (`aria-pressed`) fills teal with Abyss Ink text.

### Cards / Containers
- **Corner Style:** square (0px).
- **Background:** Title Block Green.
- **Shadow Strategy:** none (see Elevation & Depth).
- **Border:** 1.5px teal for title blocks (hero block, issue, search, framed section head); 1px rule for figure frames and small node boxes.
- **Internal Padding:** clamp(22px, 3vw, 34px) for title blocks, 18-22px for panels and figures.

### Inputs / Fields
- **Style:** Night Sea ground, 1px rule border, square corners, 1.15rem, 14px 16px, teal caret.
- **Focus:** border and 2px outline turn teal, outline offset 0.

### Navigation
Sticky 58px bar on translucent Night Sea with a bottom rule. Brand is the vector-cross mark plus Barlow Condensed 700 caps at 1.5rem. Links are condensed 600 caps at 1.02rem, muted at rest, Chart Ink on hover. A small solid button carries the ask at the right. Links hide below 820px.

### Direction Badge
Condensed 700 caps at 1rem with an inline arrow icon, 3px 9px, square. Up uses Amber Shoal ground with Heading Amber text; down uses Deep Indigo Shoal ground with Periwinkle Current text.

### Status Marker
Condensed 700 caps with a 10px point symbol before the word: filled teal dot for new, half-filled amber ring for weakened, hollow muted ring for unchanged.

### Chart Vector (signature)
Round-capped strokes, 4px on the hero and 3.5px on the delta chart, in amber or periwinkle, drawn from the event outward with a 1.4s stroke-dash draw staggered 0.12s per vector; labels fade in after 0.9s. Weakened vectors thin to 1.5px at 35% opacity when the chart re-plots; slow effects are dashed. All motion is removed under reduced motion.

## Do's and Don'ts

### Do:
- **Do** frame primary panels as chart title blocks: Title Block Green fill, 1.5px teal border, square corners, no shadow.
- **Do** divide content with 1px Hairline Rule lines and open each ruled group with a 1.5px teal top rule.
- **Do** encode direction with Heading Amber (up) and Periwinkle Current (down) plus an arrow, never colour alone.
- **Do** set titles, labels, and buttons in Barlow Condensed uppercase, reading copy in Barlow, and measurements in Spline Sans Mono.
- **Do** use the single ease cubic-bezier(.16,1,.3,1) and drop all motion under prefers-reduced-motion.
- **Do** label sample data with the tag style wherever the demo graph appears.

### Don't:
- **Don't** add drop shadows, hover lifts, or rounded corners to any rectangle.
- **Don't** use amber or periwinkle for anything other than up and down pressure.
- **Don't** set prose, buttons, or headings in the mono face.
- **Don't** leave the dark-green palette: no light sections, no off-palette accents.
- **Don't** build sections as grids of floating feature cards; use ruled columns on the chart.
