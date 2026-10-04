---
name: hosl-deck
description: Build presentation slides and decks in the HOSL house style, navy on cream with a single amber accent, Archivo for headlines and Atkinson Hyperlegible for text. Use whenever creating, designing, or restyling a slide deck, presentation, talk, or set of slides for HOSL (or Brian Moriarty), in HTML or PowerPoint (.pptx), so the deck argues rather than decorates and does not look like a default AI slide. Extends the HOSL design system (see ../../brand-guidelines.md) to the deck format.
---
# HOSL deck
Slides argue, they do not decorate. A deck is a sequence of measured drawings, not a slideshow of bullet lists. Most of every slide is navy on cream; amber marks the one thing the slide is about. If an element does not carry meaning, remove it. This skill extends the HOSL design system (`../../brand-guidelines.md`, `../../tokens/`) to presentations; read that first, this specializes it to slides.
> Reconciliation note (2026-08-06): this file was corrected to match Brian's shipped house style, the Heron cohort one-pager. The prior version specified Fraunces headlines and banned mastheads and header bars, which contradicted the shipped artifact and the base tokens (which use Archivo). Archivo and the navy masthead are now the standard. If the shipped work changes, this file follows it.
## Canvas
- **16:9, always.** HTML decks: a `1280 × 720` slide box (scale up for retina, keep the ratio). PPTX: `LAYOUT_WIDE` = 13.33in × 7.5in.
- Cream `#FDF8F0` is the slide, navy `#1a2744` is the ink. Do not invert to an all-dark deck; the light paper is the identity. Section dividers, the cover, and closing may sit on solid navy with cream text.
- One idea per slide. If a slide needs two headlines, it is two slides.
- Generous margins: at least 0.6in in PPTX, and a full-bleed navy masthead band across the top of a content slide.
## Color, on a slide
Same tokens, same discipline as the base system:
- **Navy `#1a2744`** is structure, the masthead band, and default body text. **Cream `#FDF8F0`** is the paper and the text on navy. Most of the slide is these two.
- **Amber** is the single accent, once per slide: the eyebrow, the masthead rule, the lede, the one word a sentence turns on. Use `#e8a020` on navy (the masthead), `#BA7517` on cream. When two things both want amber, one of them does not need it.
- **Orange `#d9531f`** the critical line, the one that must land, used once. **Red `#c0392b`** open problems, **green `#3a7d44`** verified, **blue `#3a6ea8`** connectors. Only when the color means something, and only with a legend if more than one appears.
- Muted navy for secondary text on cream: `rgba(26,39,68,.66)`. Warm hairline for rules on cream: `#d7ceb7`.
## Type, on a slide
Faces are fixed by the system: **Archivo** (headlines and the masthead title, weights 600–800), **Atkinson Hyperlegible Next** (body and labels), **IBM Plex Mono** (eyebrows, numerals, technical labels, footnotes). Never Arial, never a system serif for display.
Type scale (PPTX points; scale up proportionally for a 1280×720 HTML slide):
| Role | PPTX pt | Face |
|---|---|---|
| Cover title | 40 | Archivo 700 |
| Masthead / slide title | 26 | Archivo 700 |
| Section number (divider) | 96–100 | Archivo 700 |
| Body / label | 15–20 | Atkinson Next 400–600 |
| Lede (masthead) | 13 | Atkinson Next 400, amber |
| Eyebrow | 11–12, tracking, UPPERCASE | IBM Plex Mono, amber |
| Status footnote | 10–12, muted | IBM Plex Mono |
| Page number | 10, zero-padded | IBM Plex Mono, muted |
Headlines get one size jump above body; do not crowd sizes. Left-align everything.
## The content-slide header: the masthead
Every content slide opens with a navy masthead band across the full width, with a thin amber rule at its bottom edge. Inside the band, left-aligned: an IBM Plex Mono amber eyebrow in uppercase, an Archivo bold title in cream, and an Atkinson lede line in amber. Body sits on the cream below the amber rule. This is the signature that makes a HOSL deck read as Brian's.
## Slide archetypes
Build a deck from these. Vary them; do not repeat one layout down the deck.
1. **Cover.** A tall navy masthead band with an amber rule: mono amber eyebrow (the term or venue), Archivo title in cream, an amber lede line. Author name and a mono meta line on the cream below.
2. **Section divider.** Solid navy. A mono amber "SECTION" eyebrow, a large Archivo section number in cream, a short Archivo title in cream, an amber tagline. Mostly empty. Marks a turn in the argument.
3. **Statement.** One sentence, large Archivo, navy on cream (or cream on navy), with at most one word in amber. Nothing else. For the claim the talk rests on.
4. **Numbered spine.** The system's signature primitive. A thin navy connector behind square number badges (mono numerals, navy outline on cream). Each node: a number, an Atkinson label, a one-line muted gloss. The stage that carries the argument gets a filled amber badge. Prefer this over a bulleted list.
5. **Masthead + support.** The masthead over a supporting figure, a short labelled list, or a two-up. The figure carries the claim; the text names it.
6. **Two-column compare.** Before/after, settled/open, this/that. Two navy columns, equal weight, one amber mark on the side that wins the argument.
7. **Table.** Ruled, not carded. A navy header row with cream text, warm hairline rules, navy body text on cream. A mono status footnote below states what is settled and what is not.
8. **Semantic legend / status.** When accent colors carry meaning, a bordered mono key: each color, its meaning in plain words, only the colors used.
9. **Closing.** Mirrors the cover. The one line to leave in the room (orange if it must land), and a mono status footnote.
## Copy inside a deck
- **No dashes of any kind.** Use commas, colons, or restructure. This is the most common way a draft breaks voice.
- **Capitalize the first letter after a colon.**
- Plain labels that name the subject, not the stance. Placement and color announce importance, not the words.
- No hype, no narrating the structure. The slide shows the structure; it does not say "here is the structure."
- Glosses are one tight line. If a gloss needs two, the slide is carrying too much.
- Prefer real text over text baked into an image. In PPTX use text boxes, not pictures of words.
## Delivery
- **Static and legible beats animated.** At most one quiet reveal per slide, and only when it clarifies. Respect reduced motion.
- Must read at the back of a room: test body text at slide-thumbnail size.
- PPTX decks: `LAYOUT_WIDE`, hex colors with no `#`, real text boxes, fonts named exactly `Archivo` / `Atkinson Hyperlegible Next` / `IBM Plex Mono`. Ship the font files or tell the viewer to install them, since PowerPoint renders with the machine's fonts.
## Avoid
- Gradients, glows, drop shadows, faux 3D, bevels, rounded-card grids.
- Emoji, stock icons, clip art, literal metaphor illustrations (a drawn rocket, lightbulb, handshake).
- Dark-on-dark or light-on-light. Keep strong navy and cream contrast.
- More than one accent color per slide. One accent, amber, across the whole deck.
- Bulleted wall-of-text slides. If it is a list, make it a numbered spine or a short labelled set, one idea per line.
