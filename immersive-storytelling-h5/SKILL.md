---
name: immersive-storytelling-h5
description: Design and build immersive, mobile-first long-form H5 visual stories with scroll-driven chapters, documentary imagery, maps, data storytelling, and editorial pacing. Use for interactive journalism, history exhibits, research explainers, cultural storytelling, and narrative campaign pages.
---
# Immersive Storytelling H5

## Reference and boundaries
Reference case: Tencent News long-form Long March 90th anniversary interactive H5: https://h5.news.qq.com/qqfile/newsh5/long-march-90.html

This skill distills transferable art direction and implementation patterns from the case, NOT source code, exact animation timings, licensed media, or a pixel-perfect replica. Do not copy its text, photos, illustrations or branding.

## Creative principle
**One screen, one narrative beat.** Build a readable journey: hook → conflict → evidence → turning point → resolution → reflection. Content structure dictates motion and visuals, not the other way around.

## Start with an editorial storyboard
Before writing code, deliver:
1. Audience, narrative question, one-sentence thesis, and primary CTA.
2. Chapter outline (3–7 chapters), each with one takeaway, one primary asset, one data point or artifact, and one interaction.
3. Asset inventory: real source, rights/license, aspect ratio, mobile crop, alt text, fallback.
4. Evidence sheet: source/date/denominator/measurement definition for each historical or numerical claim.
5. Visual design tokens, motion storyboard, mobile wireframes, and performance budget.

## Visual DNA
- **Editorial documentary tone**: material texture, carefully chosen historical objects, maps, archival imagery, field photography or original illustrations.
- **Palette**: warm archival paper (#E8DFCC), ink (#22211F), muted red (#8B3028), restrained secondary earth tones. Adapt palette to the topic; do not make every project a historical red theme.
- **Typography**: expressive Chinese display headings, highly legible Chinese body, compact data numerals; hierarchy comes from size, weight, contrast, and generous spacing.
- **Rhythm**: full-bleed visual scenes alternate with quiet reading sections; dense evidence panels are followed by whitespace.
- **Composition**: vertically sequenced chapters, deliberate object crops, fine map annotations, small captions and source notes. Avoid generic card grids and decorative icon clutter.
- **Data**: use charts, routes, annotated artifacts, before/after comparisons only when they make a claim clearer. Never imply mismatched statistical populations are directly comparable.

## Page structure
### Opening / prologue
A striking image or illustrated scene, strong headline, one-sentence framing, unobtrusive scroll cue. The main narrative must remain accessible without animation.

### Chapter pattern
1. Transition: small chapter number and key question.
2. Evidence: one dominant visual or statistic.
3. Interpretation: short, human-readable explanation.
4. Optional interaction: annotated image, stepwise route, map zoom, timeline or comparison.
5. Source caption: origin, date and uncertainty when relevant.

### Ending
Resolve the opening question, recap the core insight, provide source list and optional next action. Do not turn the ending into a generic product CTA if the work is editorial.

## Motion language
- Scroll-triggered reveal and staged image/text entry, not continuous motion everywhere.
- Use subtle layered depth or parallax for a scene only when it reinforces spatial context.
- Progressive data annotation and route highlights follow reading order.
- Suggested starting ranges (not measurements from reference): opacity/translate reveals 300–650ms, stagger 70–140ms, displacement 12–28px.
- Avoid scroll hijacking and heavy pinned sequences on low-end phones.
- Always respect prefers-reduced-motion; provide static complete content if JS fails.

## Mobile-first engineering
- Build for 360, 390, 430px then adapt to tablet/desktop.
- Semantic headings and landmarks; keyboard reachable controls; meaningful alt text.
- CSS clamp(), responsive images via srcset/picture, lazy-load below-the-fold images, prefetch only essential hero assets.
- IntersectionObserver for reveals; requestAnimationFrame for light scroll-linked work; SVG for annotated maps; canvas/WebGL only when justified.
- Limit heavy video, particle effects and multi-layer blur; measure LCP/CLS/INP and test on actual mobile devices.
- Provide visible chapter progress and optional chapter navigation without stealing reading space.

## Content accuracy guardrails
- Distinguish photographs, museum artifacts, reconstructed illustrations and diagrams.
- Do not invent numbers or cite unsupported facts. If two figures use different population definitions, explain them rather than calculating a misleading percentage.
- Provide source notes and a clear label for illustrative reconstructions.

## Anti-patterns
Generic SaaS landing pages, random gradient blobs, repetitive rounded cards, unnecessary icons, decorative charts, 3D for its own sake, endless scroll animations, unreadable overlaid text, nonfunctional navigation, and unlicensed historical imagery.

## Delivery checklist
Narrative storyboard, mobile-first wireframes, visual tokens, full implementation, asset/source register, responsive tests, accessibility and reduced-motion checks, performance check, final screenshots.

## Prompt
See references/PROMPT.md for a reusable Chinese production prompt.
