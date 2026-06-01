# Design System: The Contraband Atlas
**Project ID:** free-tools-atlas (GitHub Pages — alimabsoute)

> A semantic design system (in the Stitch DESIGN.md tradition) that serves as the single source of truth for the build. Stitch isn't in play here, so this document is authored directly as the design contract that the three pages are built against.

## 1. Visual Theme & Atmosphere

**Refined editorial almanac with a classified-dossier undertone.** The mood is *archival, confident, and quietly premium* — a printed reference ledger you'd find in a serious person's library, not a neon "free stuff" listicle. The "should be illegal" framing is expressed as restraint, not chaos: monospace evidence labels, a single stamp-red accent used sparingly, hairline rules, numbered catalog entries, and a faint paper grain.

Density is **airy and disciplined** — generous margins, a narrow editorial measure, and strong typographic hierarchy. The base is fundamentally Apple/Stripe-clean (crisp, masculine, warm-white); the dossier styling is a *motif layered on top*, never the substance. No gradients-on-white, no purple, no pink/magenta.

## 2. Color Palette & Roles

| Descriptive Name | Hex | Functional Role |
|---|---|---|
| Warm Paper | `#f7f4ec` | Primary page background — warm, archival off-white |
| Lifted Paper | `#fffdf7` | Card / surface background (one step brighter than page) |
| Ink | `#1b1a17` | Primary text, headlines, the "printed ink" |
| Graphite | `#6c675d` | Secondary text, captions, metadata |
| Stamp Red | `#c2352a` | The single bold accent — links on hover, the "ILLEGAL" stamp, active states, key numerals |
| Oxblood Shadow | `#8f261d` | Stamp-red pressed/hover-darken state |
| Sand Hairline | `#e4ddcc` | Borders, dividers, table rules |
| Ochre Flag | `#a8761f` | "Freemium" badge text/border |
| Charcoal Flag | `#4d4a42` | "Grey-area / ⚠️" badge |
| Olive Verified | `#4f5d39` | "Verified live" micro-label |

## 3. Typography Rules

- **Display (Fraunces, serif):** High-contrast, soft-modern old-style serif for all major headlines and the catalog numerals. Used at large sizes with tight leading and an optical, characterful feel. Weights 400–900; italics used for editorial emphasis.
- **Body (Schibsted Grotesk, sans):** Clean, slightly geometric humanist grotesque for running text, reviews, and UI. Distinctive but highly legible — the Apple/Stripe-crisp counterweight to the serif. Weights 400–700.
- **Labels (JetBrains Mono, monospace):** ALL-CAPS, wide letter-spacing (`0.12em`) kicker labels, category tags, counts, and "evidence" metadata. This is what carries the dossier feeling.
- Letter-spacing: headlines slightly tight (`-0.02em`); mono labels wide; body neutral.

## 4. Component Stylings

- **Buttons / Filter chips:** Sharp-edged or pill (chips only). Default = ink hairline border on lifted paper; active = solid Ink fill with paper text, or Stamp-Red fill for the primary CTA. Mono label, wide tracking. Crisp 120ms transitions, no bounce.
- **Cards / Tool entries:** Squared with a 3px softening (`rounded-[3px]`), Lifted Paper background, 1px Sand hairline. Flat at rest; on hover, a whisper-soft shadow + Stamp-Red left rule slides in. Numbered like a ledger (mono index, serif name).
- **Badges (flags):** Tiny mono uppercase pills with 1px colored borders — Ochre (Freemium), Charcoal + ⚠️ (Grey-area), Olive (Verified). Never loud.
- **Inputs (search):** Underline-only or hairline-boxed, transparent background, mono placeholder, Stamp-Red caret/focus rule. No heavy fills.

## 5. Layout Principles

- Max content measure ~1120px, centered, with a generous outer gutter (clamp-based).
- Strong vertical rhythm; hairline `Sand` dividers separate sections.
- Editorial asymmetry: mono kicker → oversized serif headline → graphite standfirst, left-weighted.
- Catalog uses a responsive card grid (1 col mobile → 2 → 3) with category section headers.
- A faint SVG/noise **paper grain** overlay sits above the background at low opacity for atmosphere and depth.
- Mobile-first: 320–768px tested, 44px touch targets, `clamp()` typography, sticky lightweight nav.
