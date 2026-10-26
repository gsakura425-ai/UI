---
name: editorial-brutalist-h5
description: Create striking editorial-brutalist H5 landing pages with oversized typography, near-black backgrounds, metallic 3D focal objects, and asymmetric grids. Use when users request bold design-forward campaign pages, portfolios, creative technology sites, or want to translate visual references into frontend aesthetics.
---
# Editorial Brutalist H5 — Design Skill

## Objective
Produce a distinctive, high-end H5 landing page inspired by two screenshot references: (A) huge classic serif words behind a sculptural chrome K, and (B) an experimental black/red/white typographic layout with stacked K/A/B letterforms, editorial image and oversized geometric sans type. Extract *design principles*, not brands or exact compositions.

## Before coding
1. Identify brand, audience, page purpose, desired CTA, visual assets, and whether desktop or mobile is primary.
2. Write a 3-sentence art direction and select one of two modes: `MONUMENTAL_CHROME` or `RADICAL_TYPE`.
3. Produce a hierarchy map for the hero: eyebrow → dominant statement → visual anchor → CTA → secondary navigation.
4. Use meaningful copy. Do not invent brand claims or fake statistics.

## Design DNA
- Canvas: nearly black (#09090A / #101012), soft off-white (#E8E7E2), one alert accent (#F04438); restrained cool gray.
- Composition: full-bleed dark canvas; wide negative space; deliberately asymmetric, editorial alignment; fine hairline separators; small navigation and utility labels.
- Type mode A: dramatic high-contrast serif display, huge two-line headline, uppercase, tight tracking. Overlap with a glossy dimensional metallic object that crosses the type layers.
- Type mode B: heavy extended geometric sans, condensed tracking and variable scales; huge words with smaller word fragments beside vertical block letters. Use minimal red micro-labels and small status counters.
- Media: one carefully art-directed monochrome documentary photo OR one sculptural 3D object. Do not add stock imagery for decoration.
- Text hierarchy: display 80–180px desktop using clamp; body 13–16px; micro labels 9–12px with tracking. Mobile display must scale to viewport and never overflow.
- Contrast: high, typography as the main visual asset; red is used as a punctuation mark, not a fill color for everything.
- Navigation: narrow top bar with wordmark, hairline divider, 2–4 compact links; CTA is simple, rectangular, high contrast.

## Layout recipes
### MONUMENTAL_CHROME
- Hero min-height 100svh; giant two-line serif message with strong horizontal offset between lines.
- Layer an original 3D metallic brand-shaped sculpture across the center-right; use controlled shadows and specular highlights.
- Underline the visual hierarchy with tiny technical annotation labels and one compact action.
- Bottom baseline: micro-copy left, CTA near center, scroll cue right.

### RADICAL_TYPE
- Hero black canvas with compact top navigation and small red category eyebrow.
- Split composition: left 30–35% contains a monochrome editorial image with a thin caption rail; right contains large kinetic typographic fragments.
- Strong typographic scale contrast and letterform repetition; occasional red pixel/noise texture limited to selected display glyphs.
- CTA at lower-right, thin rule above, index marker in corner.

## Interaction / motion
- Intro reveal: stagger headline lines 80–160ms, clip-path or translateY with opacity; avoid animating every character by default.
- Optional 3D focal object slow rotation on pointer or scroll; provide static fallback.
- Scroll reveals: opacity + 12–24px translation, 350–650ms, ease-out; use IntersectionObserver; never hide critical content if JS fails.
- Hover: subtle tracking, underline, or image desaturation transitions. Keep UI responsive.
- Respect prefers-reduced-motion. No scroll-jacking, gratuitous parallax, or constant flashing.

## Implementation
- Semantic HTML + responsive CSS; React/Vite or Next.js when requested.
- CSS grid and layered positioning, fluid clamp() typography, svh units, container queries where appropriate.
- For 3D use a provided GLB, pre-rendered transparent WebP, or optional Three.js only if performance budget permits. Do not pretend CSS text alone reproduces a chrome render.
- Optimize image formats and preload hero assets; preserve accessible contrast, visible focus, keyboard navigation and minimum 44px touch targets.
- Responsive breakpoints: 360/390/430, 768, 1024, 1440. Avoid cropped unreadable headings and overlapping CTAs.

## Avoid
- Generic SaaS card grids, pill-heavy UI, neon gradients, glassmorphism, arbitrary icons, multiple accent colors, center-aligning everything, oversaturated shadows, and crowded sections.
- Copying reference brand marks, text, trademarked logo sculptures or exact site compositions.
- Putting all content into one unstructured hero; each subsequent section should vary rhythm but preserve the design language.

## Quality gate
Verify desktop and mobile screenshots: 1 clear focal point, deliberate asymmetry, readable display type, controlled contrast, 1 strong CTA, no overflow, no horizontal scroll, accessible keyboard controls, reduced motion fallback, good asset loading.

## Ready-to-use prompt
See `references/PROMPT.md` for a detailed Chinese copy-paste prompt and two design variants.
