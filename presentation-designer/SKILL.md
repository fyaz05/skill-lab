---
name: presentation-designer
description: Transform existing slide-content Markdown or a user-provided slide draft into concise, content-specific visual-design Markdown that a presentation designer can build in Keynote, PowerPoint, Google Slides, Figma, or another renderer. Use when slides already exist and the user asks to design, art-direct, restyle, or visually improve a pitch, strategy, sales, conference, keynote, lecture, or training deck. May reorganize and rewrite content for hierarchy and pacing while preserving factual meaning, figures, quotations, names, citations, and caveats. Produces a visual blueprint, not rendered slides.
metadata:
  version: 1.5.0
  category: document-creation
  tags: [presentations, slides, markdown, design, pitch-deck]
  license: MIT
---

# Presentation Designer

Turn ordinary slide Markdown into one beautiful, build-ready visual blueprint: `[source-slug]-visual-design.md`. Make it specific to the content, simple to follow, and detailed enough to render without becoming an exhaustive design manual.

## Input and precedence

Require existing slide-content Markdown, an existing-deck transcription, or a user-provided slide draft. If no slide content exists, ask for it; creating the source presentation belongs upstream.

Follow explicit user instructions, locked content, project guidance, brand systems, venue constraints, and accessibility requirements before this skill's defaults. Capture the purpose, audience, duration, language, aspect ratio, slide count, and brand constraints when supplied. Default to static delivery unless animation is explicitly requested.

Ask a question only when missing information would materially change the design. Otherwise make a stated assumption and continue.

## Content fidelity

You may reorder, split, merge, condense, rewrite, visualize, or move material to an appendix when it improves the deck.

Preserve factual meaning. Never invent or alter a claim, number, unit, date, quotation, proper name, source, or caveat. Keep quotations verbatim. Add a calculated value only when it follows mechanically from supplied inputs; show the calculation and label it **derived**.

Write faithful headlines, labels, transitions, definitions, and takeaways. Reproduce incomplete citations exactly as supplied. Record meaningful edits in each slide's `Trace` line. Put any citation, source, or caveat the audience must see in `Content`; `Trace` records provenance and edits but never replaces slide-visible evidence. List a Content Gap only when missing information affects accuracy, interpretation, delivery, or the requested decision.

## Workflow

1. **Read:** inventory slides, claims, evidence, caveats, visuals, locked elements, and constraints.
2. **Frame:** state what the audience should understand, feel, or do differently.
3. **Shape:** identify the opening, strongest moment, and resolution; improve the order and derive the slide count unless one is mandated. Match the structure to the mode: pitches build toward a decision, keynotes toward a reveal, teaching decks toward a stable learning sequence, and redesigns account for every source slide.
4. **Art-direct:** choose one content-derived concept, a small visual system, and a clear rhythm.
5. **Specify:** write concise deck-wide rules and slide-level directions.
6. **Check:** verify truth, accessibility, buildability, specificity, and simplicity.

## Anti-AI-slop standard

**Content creates the design.** Derive the palette, motif, components, imagery, and composition from the subject. Apply the swap test: if another organization or topic could use the design unchanged, redesign it.

**One idea, one visual move.** Give each slide one dominant idea, normally no more than two primary content groups, and one primary medium: type, photograph, diagram, chart, table, or interface mockup.

**Restraint creates polish.** Use scale, crop, contrast, material, and whitespace before adding more objects. Remove filler icons, ornamental cards, unnecessary labels, decorative charts, and effects that do not improve understanding.

**A small system beats many styles.** Use three to six palette tokens, one or two type families plus optional mono, one to four reusable components, and one to three narrative zones. Short decks need fewer parts. Repeat deliberately; vary only when the argument changes.

**Hierarchy must be decisive.** Make the focal element obvious in three seconds. Reserve extreme type scale, full bleed, or strong colour shifts for true hero moments rather than every slide.

**The sequence needs a destination.** Open with the strongest promise, tension, question, or result the source supports. Close by resolving or transforming that opening; never end on a generic “Thank You” slide.

**Visuals must be specific.** Never request a “relevant image,” “abstract illustration,” generic stock business scene, or decorative dashboard. State exactly what should be shown, how it is framed, and why it belongs.

**Avoid default deck patterns.** Do not reflexively use three equal cards, image-left/text-right, icon grids, rounded panels, purple gradients, generic corporate photography, or the same layout on every slide. Use any familiar pattern only when the content genuinely calls for it.

**Beauty must remain usable.** Never sacrifice evidence, caveats, legibility, source visibility, or accessibility for atmosphere.

## Build defaults

User or project specifications override these defaults.

| Setting | Default |
|---|---|
| Canvas | 16:9 · 960 × 540 pt |
| Grid | 12 columns · 60 pt margins · 24 pt gutters · 8 pt spacing scale |
| Type | source/caption 16 minimum · body 24 default, 22 minimum · subheading 28–32 · headline 42–56 · display 72–120 |
| Content | headline plus 1–2 primary groups; dense evidence slides may use 3 · headline no more than 12 words · body no more than 40 words excluding evidence and sources |
| Visual | one primary visual by default · contained image 30–45% · primary chart or diagram 45–70% · hero visual may bleed |

For a non-default canvas, reflow the grid while preserving type floors. Do not scale everything mechanically.

## Visual rules

- **Palette:** give each token a hex value, content-derived name, and job. Calculate contrast; require 4.5:1 for body text and 3:1 for large text and meaningful graphics. Never use colour as the only distinction.
- **Typography:** specify role, face, weight, fallback, size, and line-height. Never claim a font is installed, embedded, or licensed unless verified; otherwise write `availability to verify`.
- **Charts and tables:** use charts for comparison and tables for exact lookup. Preserve supplied scale, units, dates, sample sizes, uncertainty, and baselines. Use direct labels where legible; never use misleading axes or decorative 3-D.
- **Images and diagrams:** direct only the applicable details—subject, view, rendering, light or visual mass, palette, abstraction, annotation, framing, and emotional register. A designer must be able to source or draw the result without another creative decision.
- **Assets:** include concise alt text, provenance, and license status. Use `license to verify` when rights are unknown; use `native type/vector; no external asset` when appropriate.
- **Atmosphere:** use at most two related treatments such as grain, duotone, pattern, directional light, layered transparency, or controlled flatness. Apply them by narrative zone, not indiscriminately.
- **Motion:** omit it unless requested or essential to explain change. Then define no more than three reusable patterns and provide an equivalent static state.
- **Fit:** split → move depth to an appendix → visualize → condense with a recorded edit. Never solve overflow by shrinking below type floors, crowding whitespace, or dropping caveats.

## Output

Keep the blueprint compact. For a standard deck of up to 12 slides, keep the deck-wide design direction around 400–700 words and each slide's non-content direction around 60–100 words. Declare shared values once; slide entries contain only meaningful differences.

Create `[source-slug]-visual-design.md`:

```markdown
# [Presentation Title]
## [Tone] · [N slides] · [Audience] · Visual design

---
# DESIGN DIRECTION

## Concept
[Purpose, content-derived signature or motif, opening, strongest moment, and resolution.]

## Palette
[Compact table: token · hex · source · job · accessible pairing.]

## Type
[Compact table: role · face · weight · fallback · size.]

## System
[Canvas and grid; 1–4 components as needed; 1–3 narrative zones; shared image/diagram/chart treatment.]

---
# SLIDES

## Slide N — [lead idea]
**Intent:** [What this slide does in the argument.]
**Content:** [Exact audience-facing copy.]
**Design:** [Composition, primary medium, visual direction, component references, Alt, and Asset.]
**Trace:** [Source slide/material; meaningful edit; evidence or caveat.]
**Read:** [What the audience should understand in three seconds.]

---
# GAPS AND REFERENCES          <!-- include only when needed -->
[Only load-bearing Content Gaps and references supplied by the source.]
```

### Add detail only when needed

- Add `Delivery` only when motion, timing, speaker notes, or interaction is requested.
- Add a source-to-designed slide map only when slides are reordered, split, merged, moved, or removed.
- Add preserved original wording only when a rewrite removes source detail not recoverable from `Trace`.
- Add chart, equation, code, table, asset, or animation specifications only on slides that use them.
- Do not emit a Verification section unless a deviation or unresolved check must be reported.

## Internal check

Before delivering, silently verify:

- facts, numbers, quotations, sources, caveats, calculations, and edits are traceable;
- the design is unmistakably specific to the content and passes the swap test;
- every slide has one dominant idea, one primary medium, and no unnecessary complexity;
- palette, typography, components, and narrative zones form one coherent system;
- contrast, type size, alt text, evidence, and asset rights meet the stated floors;
- the Markdown is concise, buildable, and free of repeated system values;
- removing any remaining instruction would make the designer's job less clear.
