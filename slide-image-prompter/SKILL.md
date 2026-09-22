---
name: slide-image-prompter
description: Convert existing slide-content Markdown or a presentation-designer visual blueprint into a complete Markdown set of self-contained text-to-image prompt packages, one per slide. Use when the user asks for slide image prompts, image-generation prompts, or prompts to recreate a pitch, strategy, sales, conference, keynote, lecture, or training deck as images. Translate a presentation-designer blueprint as-is when available; when only raw slide content exists, derive a compact content-specific visual system. Preserve factual meaning, figures, quotations, names, citations, caveats, assets, and accessibility information. Produces prompts and overlay instructions, not rendered slides.
metadata:
  version: 1.0.0
  category: document-creation
  tags: [presentations, slides, markdown, image-prompts, text-to-image]
  license: MIT
---

# Slide Image Prompter

Turn supplied slides or a visual blueprint into `[source-slug]-slide-image-prompts.md`: one compact Deck Style Lock followed by one complete prompt package for every main and appendix slide.

## Input modes and precedence

Choose one input mode first:

1. **Blueprint translation — preferred.** Use when the input contains a design system and slide-level fields from `$presentation-designer`, such as `Concept and arc`, `Palette`, `Typography`, `Components`, `Composition and visual language`, `Intent`, `Content`, `Design`, `Trace`, or `Read`. Treat the blueprint as authoritative. Preserve its order, count, content, design system, components, visual treatment, assets, and narrative arc. Do not re-art-direct, reorder, split, merge, or rewrite unless the user asks or an image-model limitation makes adaptation unavoidable. Record every adaptation in `Trace`.
2. **Raw-content.** Use when only slide-content Markdown or a deck transcription exists. Improve hierarchy and renderability, derive one compact visual system, and split or condense content that cannot render legibly. Preserve a mandated slide count.

If both are supplied, the blueprint governs design and architecture while the raw content resolves exact wording and evidence.

Follow explicit user instructions, locked content, project guidance, brand systems, venue constraints, and accessibility requirements before this skill's defaults. Capture purpose, audience, language, aspect ratio, brand constraints, target image model, and supplied reference assets. Use model-agnostic natural language when no image model is named.

Ask a question only when missing information would materially change the prompt packages. Otherwise state a reasonable assumption and continue.

## Editorial fidelity

Preserve factual meaning. Never invent or alter a claim, number, unit, date, quotation, proper name, source, or caveat. Keep quotations verbatim. Add a calculated value only when it follows mechanically from supplied inputs; show the calculation and label it **derived**.

Write faithful headlines, labels, transitions, definitions, and takeaways only in Raw-content mode or when the blueprint authorizes editing. Reproduce incomplete citations exactly as supplied. Include any citation or caveat the audience must see in the direct exact-text block or composite overlay payload. Never let generated imagery replace or weaken evidence.

## Workflow

1. **Classify:** select Blueprint translation or Raw-content.
2. **Inventory:** account for every main and appendix slide, exact string, figure, citation, caveat, visual, component, asset, and locked element.
3. **Inherit or derive:** copy the supplied design system in Blueprint translation; derive a small content-specific system only in Raw-content.
4. **Translate:** map the design system and each slide into visible prompt instructions without adding a second design layer.
5. **Choose one render mode per slide:** select `Direct generation` or `Composite required`; never leave both as options.
6. **Adapt to the target model:** use only supported syntax, reference features, parameters, seeds, aspect controls, and negative-prompt behavior. Never invent model flags.
7. **Write and check:** produce independently usable packages, then verify coverage, fidelity, references, accessibility, consistency, and length.

## Blueprint translation map

| Blueprint field | Prompt destination |
|---|---|
| Concept and arc | Deck Style Lock and opening-to-closing consistency |
| Palette and Typography | Deck Style Lock and each prompt's Consistency Lock |
| Components | Recurring visual structures named consistently in prompts |
| Composition and visual language | Composition, imagery, diagram, chart, and atmosphere instructions |
| Intent and Read | Visual Priority |
| Content | Direct exact-text block or composite Overlay Payload |
| Design | Slide composition and visual direction; extract embedded Alt and Asset instructions |
| Alt, standalone or inside Design | Slide-level Alt |
| Asset, standalone or inside Design | Reference Inputs, generation route, provenance, and license status |
| Delivery | Most informative resolved static state; preserve a sequence only when requested |
| Trace | Prompt-package Trace |
| Gaps and References | Optional output section without invented metadata |

## Design quality

**Content creates the style.** Inherit the blueprint's system or derive one from the subject. Apply the swap test: if another organization or topic could use the prompt unchanged, the direction is too generic.

**One idea, one visual move.** Give each slide one dominant message, normally no more than two primary content groups, and one primary medium: typography, photograph, diagram, chart, table, collage, render, or interface view.

**Use a small system.** Preserve or derive three to five core colors, one or two type families plus optional mono, one recurring motif, up to four recurring components, and no more than three narrative zones. List only elements that appear.

**Make hierarchy unmistakable.** The focal point must register in three seconds. Reserve extreme scale, full bleed, and strong color shifts for genuine hero moments.

**Describe concrete visuals.** State the relevant subject, view, rendering, light or contrast mass, color treatment, crop, annotation, framing, and emotional register. Never request a “relevant image,” “abstract graphic,” generic business team, decorative dashboard, or meaningless icon set.

**Prefer restraint to manufactured novelty.** Do not force textures, panels, grid breaks, photographs, status chips, effects, strict alternation, three equal cards, generic icon rows, purple-blue startup gradients, random glass panels, floating UI, device mockups, or interchangeable corporate imagery.

**Describe style through attributes.** Specify composition, era, material, palette, lighting, texture, and rendering rather than relying on an artist's name.

**Keep beauty usable.** Never sacrifice exact text, data, evidence, caveats, legibility, accessibility, or design inheritance for atmosphere.

## Render modes

Text-to-image models can distort typography, logos, interfaces, charts, and data. Choose modes honestly.

- **Direct generation:** use only for text-light slides without precise tables, equations, multi-point charts, dense citations, exact logos, supplied screenshots, or load-bearing brand assets. Keep visible copy near 20–25 words: normally one headline, one short support line, and up to three compact labels. Ask the model to render every supplied string verbatim, then require verification.
- **Composite required:** use whenever exact text, data, citations, charts, tables, equations, logos, screenshots, brand assets, or exact brand typography are load-bearing. Generate the complete visual base with intentionally clean empty regions, then provide an exact Overlay Payload.
- Treat generated charts, tables, maps, and interfaces as visual drafts. Put exact values, labels, units, ordering, scales, axes, and annotations in the Overlay Payload.
- Never generate an official logo, trademark, proprietary screenshot, or real identifiable person's likeness from memory. Use a supplied reference with known permission or reserve the placement for compositing.
- Never invent filler copy. Every visible string must exist in the exact-text block or Overlay Payload.
- Treat a named font in Direct generation as visual direction, not a guarantee. Use Composite required when exact typography matters.
- If the user forbids necessary compositing, preserve the content and state the rendering risk instead of silently simplifying or fabricating fidelity.

## Model adaptation and deck consistency

- When a target model is named, adapt to capabilities known to be supported: natural-language instructions, negative prompts, image or style references, seeds, aspect-ratio controls, and prompt parameters. Do not output unsupported syntax.
- When no model is named, use plain natural language without model-specific flags.
- When supported, designate one approved cover or representative slide as the deck's style reference. Reuse its reference ID, style reference, image reference, or shared seed.
- Without a visual reference, repeat only the essential palette, type character, motif, component, line style, and image treatment needed to stabilize each independent generation.
- State supplied assets by filename or identifier. Never imply that an absent asset was supplied, licensed, or approved.

## Build defaults

User or project specifications override these defaults.

| Setting | Default |
|---|---|
| Artifact | single flat presentation slide, edge-to-edge |
| Canvas | 16:9 · 1920 × 1080 px |
| Grid | inherited grid or 12 columns · 120 px margins · 48 px gutters · 16 px spacing scale |
| Type | source/caption 32 px minimum · body 48 px default, 44 px minimum · subheading 56–64 px · headline 84–112 px · display 144–240 px |
| Content | headline plus 1–2 primary groups · headline no more than 12 words · Direct generation near 20–25 visible words |
| Visual | one primary visual move · contained image 30–45% · chart or diagram 45–70% · hero visual may bleed |

For a non-default canvas, reflow rather than scale mechanically. Never solve overflow by shrinking text.

## Prompt-package rules

Use the output schema below. Every package must select one mode and list `Reference Inputs`. Its prompt must name the artifact, visible priority, composition, visual direction, typography, mode-appropriate text handling, consistency lock, and exclusions. Outside the prompt, include `Alt` and `Asset`; include `Overlay Payload` only for Composite required and `Trace` only after an adaptation.

## Complexity limits

- Keep the Deck Style Lock between 150 and 300 words.
- Keep each prompt's composition and visual direction between 120 and 220 words, excluding exact text and overlay data. Allow up to 300 only for a genuinely complex composite slide.
- A longer deck adds prompt packages, not more detail per package.
- Repeat only essential inherited style values needed for independent use.
- Use no more than two atmospheric treatments per prompt.
- Describe visible results, not design theory, internal reasoning, three-second tests, or production commentary.

## Output

Create `[source-slug]-slide-image-prompts.md`:

````markdown
# [Presentation Title]
## [Tone] · [N slides] · [Audience] · Slide image prompt packages

---
# DECK STYLE LOCK

**Input mode:** [Select exactly one: Blueprint translation | Raw-content]
**Target model:** [Named model or model-agnostic]
**Concept:** [Inherited or derived visual idea, motif, and arc.]
**Palette:** [3–5 used colors with hex values and jobs.]
**Typography:** [Inherited or derived display, body, and optional data character.]
**Components:** [Recurring visual structures and their jobs, or none.]
**Visual language:** [Shared imagery, diagram, chart, narrative-zone, and atmosphere treatment.]
**Reference strategy:** [Style reference, image references, shared seed, or none.]

---
# SLIDE PROMPT PACKAGES

## Slide N — [lead idea]
**Mode:** [Select exactly one: Direct generation | Composite required]
**Reference Inputs:** [Supplied identifiers or none]

```text
Create one flat, front-facing 16:9 presentation slide at 1920×1080 pixels, edge-to-edge, with no device, room, frame, or perspective mockup.

VISUAL PRIORITY:
[Visible focal hierarchy.]

COMPOSITION AND VISUAL DIRECTION:
[Grid relationship, placement, whitespace, primary medium, subject, view, rendering, light or mass, crop, annotation, register, and typography.]

TEXT HANDLING:
[Direct generation: list every visible string under “TEXT TO RENDER EXACTLY — do not paraphrase, correct, omit, or add text.” Composite required: identify clean empty text/data regions and forbid marks inside them.]

CONSISTENCY LOCK:
[Essential inherited palette, typography, motif, components, image treatment, and supported reference or seed.]

DO NOT INCLUDE:
[Extra text, gibberish, misspellings, watermarks, unintended logos, decorative clutter, duplicated objects, mockups, or conflicting styles.]
```

**Overlay Payload:** [Composite required only; otherwise omit.]
**Alt:** [Concise informational description.]
**Asset:** [Generation/composite route, reference provenance, and license status.]
**Trace:** [Source and adaptation; omit when unchanged.]

---
# GAPS AND REFERENCES         <!-- include only when needed -->
[Only load-bearing Content Gaps and references supplied by the source.]
````

Repeat the complete `Slide N` package for every main and appendix slide. Never emit `Slide N`, a placeholder, a summary, or “continue in the same style” in the delivered file.

## Internal check

Before delivering, silently verify:

- the correct input mode was selected and any supplied blueprint remained authoritative;
- every main and appendix slide has one complete package with exactly one render mode;
- every package includes references, visual priority, composition, visual direction, typography, text handling, consistency lock, exclusions, Alt, and Asset;
- every number, quotation, label, citation, caveat, component, asset, and adaptation is traceable;
- Delivery resolves to the intended static state or requested frame sequence;
- Direct generation stays text-light and Composite required handles load-bearing precision;
- target-model syntax and reference features are supported rather than invented;
- slide copy fits at the declared sizes without tiny text;
- palette, typography, components, motif, image treatment, references, and narrative zones remain consistent;
- no package requests generic imagery, unnecessary decoration, unsupported brand assets, or an unreferenced real person's likeness;
- prompt packages stay within the complexity limits and form one coherent deck rather than unrelated poster images.
