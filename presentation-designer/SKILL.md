---
name: presentation-designer
description: Transform existing slide-content Markdown or a user-provided slide draft into concise, content-specific visual-design Markdown that a presentation designer can build in Keynote, PowerPoint, Google Slides, Figma, or another renderer. Use when slides already exist and the user asks to design, art-direct, restyle, or visually improve a pitch, strategy, sales, conference, keynote, lecture, or training deck. May reorganize and rewrite content for hierarchy and pacing while preserving factual meaning, figures, quotations, names, citations, and caveats. Produces a visual blueprint, not rendered slides.
metadata:
  version: 1.6.0
  category: document-creation
  tags: [presentations, slides, markdown, design, pitch-deck]
  license: MIT
---

# Presentation Designer

Turn ordinary slide Markdown into one beautiful, build-ready visual blueprint: `[source-slug]-visual-design.md`. Make it unmistakably specific to the content and precise enough to build, but substantially simpler than a production manual.

## Input and precedence

Require existing slide-content Markdown, an existing-deck transcription, or a user-provided slide draft. If no slide content exists, ask for it; creating the source presentation belongs upstream.

Follow explicit user instructions, locked content, project guidance, brand systems, venue constraints, and accessibility requirements before this skill's defaults. Capture purpose, audience, duration, language, aspect ratio, slide count, brand constraints, and delivery format when supplied. Default to static delivery unless animation is explicitly requested.

Ask a question only when missing information would materially change the design. Otherwise state a reasonable assumption and continue.

## Editorial contract

Reorder, split, merge, condense, rewrite, visualize, or move material to an appendix when that improves the deck. Derive the slide count from the argument unless the user mandates one; never preserve a crowded source structure merely because it already exists.

Preserve factual meaning. Never invent or alter a claim, number, unit, date, quotation, proper name, source, or caveat. Keep quotations verbatim. Add a calculated value only when it follows mechanically from supplied inputs; show the calculation and label it **derived**.

Write faithful headlines, labels, transitions, definitions, and takeaways. Reproduce incomplete citations exactly as supplied. Put any citation, source, or caveat the audience must see in `Content`; `Trace` records provenance and edits but never replaces slide-visible evidence. List a Content Gap only when missing information affects accuracy, interpretation, delivery, or the requested decision.

## Workflow

1. **Read:** inventory slides, claims, evidence, caveats, visuals, locked elements, and constraints.
2. **Frame:** state what the audience should understand, feel, or do differently.
3. **Shape:** identify the opening, strongest moment, and resolution; improve the order and remove repetition. Match structure to mode: pitches build toward a decision, keynotes toward a reveal, teaching decks toward a stable learning sequence, and redesigns account for every source slide.
4. **Art-direct:** choose one content-derived concept, one memorable signature, a small visual system, and a clear rhythm.
5. **Simplify:** remove any component, effect, instruction, or content group that does not improve comprehension, evidence, emotion, or navigation.
6. **Specify:** declare shared decisions once, then describe only meaningful slide-level differences.
7. **Check:** verify truth, accessibility, buildability, specificity, and simplicity.

## Anti-AI-slop standard

**Content creates the design.** Derive the concept, palette, motif, imagery, components, and composition from the subject. Apply the swap test: if another organization or topic could use the design unchanged, redesign it.

**One idea, one visual move.** Give each slide one dominant idea, normally no more than two primary content groups, and one primary medium: type, photograph, diagram, chart, table, or interface mockup.

**Use a small system.** Use three to five core palette tokens, plus no more than two semantic status colours when the content genuinely requires them. Use one or two type families plus optional mono, one to four reusable components including persistent footers, and one to three narrative zones. List only tokens and components that actually appear.

**Restraint creates polish.** Create richness through scale, crop, contrast, material, and whitespace before adding objects, cards, labels, effects, or annotations. If a slide looks impressive only because it contains many things, simplify it.

**Hierarchy must be decisive.** Make the focal element obvious in three seconds. Reserve extreme type scale, full bleed, and strong colour shifts for true hero moments rather than every slide.

**The sequence needs a destination.** Open with the strongest promise, tension, question, or result the source supports. Close by resolving or transforming that opening; never end on a generic “Thank You” slide.

**Visuals must be specific.** Never request a “relevant image,” “abstract illustration,” generic stock business scene, or decorative dashboard. State what must be shown, how it is framed, and why it carries meaning.

**Do not manufacture novelty.** Never require a grid break, texture, status chip, panel, photograph, or layout change on every slide. Repeat when repetition aids comparison or teaching; vary when the argument changes. Avoid strict alternation schedules and decorative rules disguised as systems.

**Reject default deck patterns.** Do not reflexively use three equal cards, image-left/text-right, icon grids, rounded panels, purple gradients, generic corporate photography, or one repeated layout. Use a familiar pattern only when the content calls for it.

**Beauty must remain usable.** Never sacrifice evidence, caveats, legibility, source visibility, accessibility, or designer judgment for atmosphere or precision theatre.

## Build floors

User or project specifications may override these defaults. Otherwise treat type minimums as hard floors, not suggestions.

| Setting | Default |
|---|---|
| Canvas | 16:9 · 960 × 540 pt |
| Grid | 12 columns · 60 pt margins · 24 pt gutters · 8 pt spacing scale |
| Type | source/caption 16 minimum · body 24 default, 22 minimum · subheading 28–32 · headline 42–56 · display 72–120 |
| Content | headline plus 1–2 primary groups; dense evidence slides may use 3 · headline no more than 12 words · body no more than 40 words excluding evidence and sources |
| Visual | one primary visual by default · contained image 30–45% · primary chart or diagram 45–70% · hero visual may bleed |

For a non-default canvas or viewing context, reflow the grid rather than scaling everything mechanically. Preserve legibility, state the altered floor, and record why it changed. Never reduce type to avoid editing or splitting content.

## Design-system rules

- **Palette:** give each used token a hex value, content-derived name, and job. Calculate contrast; require 4.5:1 for body text and 3:1 for large text and meaningful graphics. Never use colour as the only distinction. Do not list unused colours, speculative variants, or decorative tints as tokens.
- **Typography:** specify role, face, weight, fallback, size, and line-height once. Never claim a font is installed, embedded, or licensed unless verified; otherwise write `availability to verify`.
- **Components:** define only recurring structures that save effort or clarify meaning. Do not turn ordinary text, rules, or every slide element into a named component. A footer counts when it persists across the deck.
- **Composition:** describe grid spans, bands, alignment, bleed, and hierarchy. Avoid exact `X/Y` coordinates, measured whitespace rectangles, and point-level placement unless a crop, overlay, diagram, or data geometry genuinely depends on them.
- **Rhythm:** use simple states such as open, standard, or dense when helpful. Do not publish a slide-by-slide density schedule or impose alternation for its own sake.
- **Charts and tables:** use charts for comparison and tables for exact lookup. Preserve supplied scale, units, dates, sample sizes, uncertainty, and baselines. Use direct labels where legible; never use misleading axes or decorative 3-D.
- **Images and diagrams:** direct only applicable details: subject, view, rendering, light or visual mass, palette, abstraction, annotation, framing, and emotional register. A designer must be able to source or draw the result without another creative decision.
- **Assets:** include concise alt text, provenance, and license status. Use `license to verify` when rights are unknown; use `native type/vector; no external asset` when appropriate.
- **Atmosphere:** use at most two related treatments such as grain, duotone, pattern, directional light, layered transparency, or controlled flatness. Apply them by narrative zone, not automatically to every slide.
- **Motion:** omit it unless requested or essential to explain change. Then define no more than three reusable patterns and provide an equivalent static state.
- **Fit:** split → move depth to an appendix → visualize → condense with a recorded edit. Never solve overflow by shrinking below type floors, crowding whitespace, or dropping caveats.

## Complexity budget

The blueprint makes design decisions; it does not simulate every action a designer will take.

- Keep the complete design system around 400–700 words; allow up to 900 only for a genuinely complex deck. A longer deck adds slide entries, not a larger system.
- Keep each slide's non-content direction between 60 and 100 words. Exceed 100 only when a complex chart, diagram, or unusual crop requires it; treat 120 as the normal maximum.
- Keep `Intent`, `Trace`, and `Read` to one sentence each.
- Declare fonts, colours, components, effects, source styling, and motion once. Never restate inherited values on every slide.
- Use grid spans and spatial relationships instead of exhaustive measurements. Do not specify a mandatory grid break, exact whitespace percentage, or protected rectangle for every slide.
- Keep exact audience-facing copy only when it fits the declared type floors. Split or append overflow rather than documenting an impossible layout.
- Preserve designer judgment for choices that do not affect meaning, hierarchy, accessibility, or sourcing.

## Output

Create `[source-slug]-visual-design.md`:

```markdown
# [Presentation Title]
## [Tone] · [N slides] · [Audience] · Visual design

---
# DESIGN SYSTEM

## Concept and arc
[Purpose, content-derived signature or motif, opening, strongest moment, and resolution.]

## Palette
[Compact table: token · hex · source · job · accessible pairing.]

## Typography
[Compact table: role · face · weight · fallback · size and line-height.]

## Components
[1–4 recurring structures: code · construction · purpose; omit when none recur.]

## Composition and visual language
[Canvas, grid, narrative zones, rhythm, shared imagery/diagram/chart treatment, and any intentional exception.]

---
# SLIDES

## Slide N — [lead idea]
**Intent:** [What this slide does in the argument.]
**Content:** [Exact audience-facing copy, including visible source or caveat text.]
**Design:** [Grid composition, primary medium, slide-specific visual direction, component references, concise Alt, and Asset.]
**Trace:** [Source material and meaningful editorial change; one sentence.]
**Read:** [What the audience should understand in three seconds; one sentence.]

---
# GAPS AND REFERENCES          <!-- include only when needed -->
[Only load-bearing Content Gaps and references supplied by the source.]
```

### Add detail only when needed

- Add `Delivery` only when motion, timing, speaker notes, or interaction is requested.
- Add a source-to-designed slide map only when slides are reordered, split, merged, moved, or removed.
- Add preserved original wording only when a rewrite removes source detail not recoverable from `Trace`.
- Add chart, equation, code, table, asset, or animation specifications only on slides that use them.
- Add a Verification section only when a deviation or unresolved check must be reported.

## Internal check

Before delivering, silently verify:

- facts, numbers, quotations, sources, caveats, calculations, and edits are traceable;
- the design is unmistakably specific to the content and passes the swap test;
- every slide has one dominant idea, one primary medium, and no unnecessary complexity;
- the design system stays within its palette, type, component, and narrative-zone limits;
- type floors, contrast, alt text, evidence visibility, and asset rights meet the stated requirements;
- no forced gimmick, density schedule, repeated system value, unused token, or unnecessary coordinate remains;
- slide copy can actually fit at the declared sizes, with overflow split or moved to an appendix;
- the Markdown is concise, buildable, and leaves nonessential production judgment to the designer.
