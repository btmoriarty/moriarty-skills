---
name: hosl-design
description: Build any static visual in Brian Moriarty's HOSL house style, navy on cream with amber where it carries meaning, Atkinson Hyperlegible and IBM Plex Mono with an Archivo title, measured rather than decorative. Use whenever creating, designing, restyling, or laying out a figure, diagram, one-pager, cheat-sheet, poster, report, document, or slide deck for Brian or HOSL, in HTML, SVG, PDF, or PPTX, or when he says "in my style", "my design system", "HOSL style", "on brand", "make it look like mine", or points at the design system. Covers the whole visual system and folds in the deck rules the base system left in a separate file.
---

# HOSL design

Figures argue, they do not decorate. A visual earns its place by making a claim clearer than prose could, and it reads as a measured drawing, an architect's section or an analyst's chart, not an illustration. Credibility comes from clarity and restraint. If an element does not carry meaning, remove it.

This skill applies Brian Moriarty's HOSL design system to any static deliverable. The authoritative source is `references/brand-guidelines.md` and `references/tokens.css`; read both before building. `references/cheatsheet-template.html` is the worked one-pager, and `references/deck-archetypes.md` is the slide layer. When the tokens and this file disagree, the tokens win, since they are the file Brian maintains.

## Order of work

1. Read `references/tokens.css` and `references/brand-guidelines.md`.
2. Decide the format: figure, one-pager or cheat-sheet, poster, document, or deck.
3. Reach for a named primitive before inventing a layout.
4. Build as static markup. Render it, screenshot it, and check it fills the page and reads at size before delivering.

## Tokens

Navy on cream, and color carries meaning, not decoration. Grounded in the TAIS poster "Oversight That Degrades" (house default, 2026-08-01).

- Cream `#FDF8F0`: background and paper.
- Navy `#1a2744`: primary ink, structure, the top and bottom bars.
- Amber `#e8a020`: the warm accent, a gate, the rule under a header, an eyebrow.
- Orange `#d9531f`: the critical or degraded, the one line that has to land.
- Blue `#3a6ea8`: connectors, joins, a second track. Sparingly.
- Green `#3a7d44`: verified, passed, confirmed. Sparingly.
- Red `#c0392b`: hard problems, warnings, the unresolved. Sparingly.
- Muted navy `rgba(26,39,68,.66)` for secondary text; warm hairline `#d7ceb7`; faint fill `#f1ead9` for code and callouts.

Most of any surface is navy on cream. Each accent appears where it means something. If two things both reach for the same accent, one of them does not need it.

## Type

Load from Google Fonts (this is the chosen delivery for portability):

```html
<link href="https://fonts.googleapis.com/css2?family=Archivo:wght@600;700;800&family=Atkinson+Hyperlegible:ital,wght@0,400;0,700;1,400&family=IBM+Plex+Mono:wght@400;500;600;700&display=swap" rel="stylesheet">
```

- Atkinson Hyperlegible: the primary face, body and labels. Making it the default keeps the system accessible rather than treating legibility as a special case.
- IBM Plex Mono: eyebrows, section labels in small caps, numerals, codes, small technical labels. The mono carries the measured, drafting feel.
- Archivo (bold grotesque): the sheet or poster title only. Fallbacks Helvetica Neue, then Atkinson Hyperlegible.
- Never Arial, in any position in a font stack, and never a system serif for display. Where a fallback is needed, use `system-ui`. Fraunces is retired from the default.

For a PPTX deck, Google Fonts do not apply. Name the faces exactly, `Archivo` / `Atkinson Hyperlegible Next` / `IBM Plex Mono`, and ship the font files or tell the viewer to install them, since PowerPoint renders with the machine's fonts. Decks use Archivo headlines, not Fraunces; Fraunces is retired.

## Recurring primitives

Reach for these before anything decorative. They are what make a figure Brian's.

- **The numbered spine.** A sequence for ordered stages, laid vertically or horizontally. A thin navy connector runs behind square number badges, each badge a zero-padded mono numeral, navy outline on cream. Each node carries a number, an Atkinson label, and a one-line muted gloss. The stage that turns or carries the argument takes a filled amber badge; a terminal that stays open takes a dashed badge. If the sequence continues, a dotted continuation rather than a hard stop.
- **The header block.** A mono eyebrow in uppercase amber with wide letterspacing, then the Archivo title, then an Atkinson lede in slightly muted navy at a readable measure. Opens every figure or sheet.
- **The status footnote.** One mono line in muted navy, items separated by middots, stating what is settled and what is not, for example `order fixed · labels provisional`.
- **The semantic legend.** When the accent colors carry meaning, a bordered mono key lists each color with its meaning in plain words. A color appears only if it means something in the figure.

## Format archetypes

- **Cheat-sheet or dense one-pager.** Follow `references/cheatsheet-template.html`: a navy masthead with a 4px amber bottom rule, a mono eyebrow over an Archivo title, cream body in editorial columns, mono `h2` section eyebrows over a navy rule, ruled tables rather than cards, and a navy footer with an amber top rule where the one line that must land sits in orange. Letter, landscape for density. Render and confirm it fills one page.
- **Figure or diagram.** A header block over the numbered spine or a small labelled figure. The figure carries the claim; the text names it. Dimension lines, spines, and clean rules over flourish.
- **Poster.** The same system at scale, on cream, with the header block, one or two primitives, and a semantic legend. Whitespace is structural.
- **Document or report.** Navy on cream, Atkinson body, mono eyebrows over navy rules for sections, ruled tables. No card stacks, no accent stripes inside the prose.
- **Slide deck.** See `references/deck-archetypes.md` for the full set: cover, section divider, statement, numbered spine, masthead with support, two-column compare, ruled table, semantic legend, closing. 16:9, cream slide, a navy masthead band with an amber rule opening each content slide, Archivo headlines, one amber accent per slide, one idea per slide.

## Copy inside a figure

- No dashes of any kind. Use commas, or restructure. This is the most common way a draft breaks voice.
- Plain labels that name the subject, not the stance. A label never announces its importance; placement and color do that.
- No hype, and no narrating the structure. The figure shows the structure, it does not say "here is the structure."
- Glosses are one tight line. If a gloss needs two, the figure is carrying too much.
- Brian also bans, in prose: em and en dashes; the words leverage, robust, significant, essential, crucial, seamless, unlock, transformative, impactful, and "it's worth noting"; and trailing "quietly". Hold to those here too.

## Not the generic default

The look to avoid reads as a generic AI or SaaS default. Each tell has a replacement already in the system. Reach for the right side.

- Rounded corners and soft drop shadows, the floating-card-grid look. Instead: hard 90 degree corners and hairline rules; a table is ruled, not a stack of cards.
- A centered hero with large padding and low density. Instead: left align on a real grid, editorial density, a masthead bar, a footer bar, more information per inch than a web page.
- Cool neutral gray with one blue accent and faint gradients. Instead: the warm palette, navy on cream with amber and orange, and a warm hairline. Never a gradient.
- Pill buttons, tinted chips, emoji as markers. Instead: plain labels, the mono eyebrow over a rule, and the middot as the one connector glyph. No emoji.
- A system or Inter font at comfortable leading. Instead: Atkinson Hyperlegible and IBM Plex Mono, the mono eyebrow in caps with wide letterspacing.

The signatures that make a figure Brian's, and that almost no default uses: the mono eyebrow over a rule, zero-padded mono numerals, the middot connector, and the honest status footnote.

## Delivery

- Static and legible beats animated. Motion only when it clarifies, at most one quiet reveal, never decoration. Respect reduced-motion.
- It must read on a phone, scale without breaking, and prefer real text over text baked into an image.
- Build as static markup, and avoid client scripts that can fail silently.
- Before handing it over: render it, screenshot it, and confirm it fills the page and reads at size. For a print piece, confirm it is one page at the intended paper size.

## Avoid

- Literal metaphor illustrations such as a drawn house, a rocket, or a lightbulb.
- Generic product-interface card layouts, heavy gradients, glows, drop shadows, faux three-dimensional effects.
- Emoji, stock icons, clip art.
- Color used for decoration rather than meaning.
