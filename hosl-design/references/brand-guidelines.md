# HOSL design system

*Setup file for Claude Design. Feed this through "Set up your design system" at claude.ai/design, together with the example figures named at the end. If the tokens also live in a repo, point Claude Design there as well, since it reads component libraries and tokens directly.*

## Principle

Figures argue, they do not decorate. A diagram earns its place by making a claim clearer than prose could, and it reads as a measured drawing, an architect's section or an analyst's chart, rather than an illustration. Credibility comes from clarity and restraint. If an element does not carry meaning, remove it.

## Tokens

Work in navy on cream, and let color carry meaning, not decoration. Palette
grounded in the TAIS poster "Oversight That Degrades" (house default, 2026-08-01).

- Cream #FDF8F0: background and paper.
- Navy #1a2744: primary ink, structure, and the top and bottom bars.
- Amber #e8a020: the warm accent, a gate, the rule under the header, an eyebrow.
- Orange #d9531f: the critical or degraded, the one line that has to land.
- Blue #3a6ea8: connectors, joins, a second track. Sparingly.
- Green #3a7d44: verified, passed, confirmed. Sparingly.
- Red #c0392b: hard problems, warnings, the unresolved. Sparingly.

Most of any surface is navy on cream. Each accent appears where it means something; if two things both reach for the same accent, one of them does not need it.

## Type

- Atkinson Hyperlegible: the primary face, body and labels. Hyperlegible by design, so making it the default keeps the whole system accessible rather than treating legibility as a special case.
- IBM Plex Mono: eyebrows, section labels in small caps, numerals, codes, and small technical labels. The mono carries the measured, drafting feel.
- Display headline: a bold grotesque webfont (Archivo, with Helvetica Neue then Atkinson Hyperlegible as fallbacks), for the sheet or poster title only. Fraunces is retired from the default as of 2026-08-01.
- Never Arial, in any position in a font stack, and never a default system serif for display. Where a fallback is needed, use `system-ui`.

## Arrangement

- Color carries meaning. The surface is mostly navy on cream; each accent appears where it means something (amber a gate or rule, orange the critical, blue a connector), never as decoration.
- Sequences read as build order. Ordered stages sit on a spine, each assuming the one before it, so the order is visible rather than asserted.
- Measured, not decorative. Dimension lines, spines, labels, clean rules over flourish.
- Whitespace is structural. Let the figure breathe.

## Delivery

- Static and legible beats animated. Motion only when it clarifies, at most one quiet reveal, never decoration.
- It must read on a phone, scale without breaking, and respect reduced-motion.
- Prefer real text over text baked into an image.
- Build as static markup where possible, and avoid client scripts that can fail silently.

## Copy inside a figure

- No dashes of any kind. Use commas, or restructure.
- Plain labels that name the subject, not the stance. A label never announces its importance; placement and color do that.
- No hype, and no narrating the structure. The figure shows the structure, it does not say "here is the structure."
- Glosses are one tight line. If a gloss needs two, the figure is carrying too much.

## Recurring primitives

These have appeared more than once and are part of the system. The heavier template layer is deliberately not codified yet.

- **The numbered spine.** A vertical sequence for ordered stages. A thin navy connector runs behind square number badges, each badge a mono numeral, navy outline on cream. Each node carries a number, a Plex Sans label, and a one-line muted gloss. The stage that turns or carries the argument takes a filled amber badge; a terminal that stays open takes a dashed badge. Top to bottom. If the sequence continues, a dotted continuation below the last node rather than a hard stop.
- **The header block.** A mono eyebrow in uppercase amber with wide letterspacing, then a Fraunces headline, then a Plex Sans lede in slightly muted navy at a readable measure. Opens every figure or sheet.
- **The status footnote.** One mono line in muted navy, items separated by middots, stating what is settled and what is not, for example "order fixed, labels provisional."
- **The semantic legend.** When the accent colors carry meaning, a bordered mono key lists each color with its meaning in plain words. A color appears in the legend only if it means something in the figure.

## Worked examples

Reference realization of the current default (2026-08-01):
- The cheat-sheet and dense one-pager, `templates/cheatsheet/cheatsheet.html`: navy masthead with an amber rule, mono section eyebrows, command boxes, navy footer. Feed this as the new-style figure.

Historical, the pre-2026-08-01 austere style, kept for reference and NOT the current default:
- The foundational category spine and the block accumulation diagram in `examples/`. Do not feed these to Claude Design as current-style figures.

## Avoid

- Literal metaphor illustrations such as a drawn house, a rocket, or a lightbulb. A metaphor can guide the thinking without being the thing rendered.
- Generic product-interface card layouts, heavy gradients, glows, drop shadows, faux three-dimensional effects.
- Emoji, stock icons, clip art.
- Color used for decoration rather than meaning.

## Not the generic default

The look to avoid is output that reads as a generic AI or SaaS default. It has a short list of tells, and each has a replacement already in this system. When generating, reach for the right column, not the left.

- Rounded corners and soft drop shadows, the floating-card-grid look. Instead: hard 90-degree corners and hairline rules; a table is ruled, not a stack of cards.
- A centered hero with large padding and low density. Instead: left align on a real grid, with editorial density, columns, a masthead bar, a footer bar, more information per inch than a web page.
- Cool neutral gray with one blue accent and faint gradients. Instead: the warm palette, navy on cream with amber and orange, and a warm hairline. Never a gradient.
- Pill buttons, tinted chips, emoji as markers. Instead: plain labels, the mono eyebrow over a rule, and the middot as the one connector glyph. No emoji.
- A system or Inter font at comfortable leading. Instead: Atkinson Hyperlegible and IBM Plex Mono, the mono eyebrow in caps with wide letterspacing.

The signatures that make a figure ours, and that almost no default uses: the mono eyebrow over a rule, zero-padded mono numerals, the middot connector, and the honest status footnote. Reach for those before anything decorative.
