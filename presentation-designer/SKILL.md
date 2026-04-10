---
name: presentation-designer
description: Designs cinematic, aesthetically distinct markdown slide decks with embedded design systems. Use when the user asks to create a presentation, pitch deck, slide deck, make slides, design a presentation, build a deck, or needs structured visual storytelling in markdown. Produces high-fidelity markdown with precise typography, color systems, atmospheric depth, and bespoke layouts. Do NOT use for PowerPoint or PPTX files, web pages or applications, or traditional documents and reports.
metadata:
  version: 1.0.0
  category: document-creation
  tags: [presentations, slides, markdown, design, pitch-deck]
  license: MIT
---

# Presentation Designer

Creates slide decks as rich markdown with embedded design systems and cinematic visual direction. Every deck must feel art-directed — never generic, never interchangeable.

**Output type:** This skill produces a high-fidelity design specification and content structure in markdown. The design system, visual directions, color values, typography specifications, and atmospheric instructions are written precisely enough for a designer to implement in any presentation tool — Figma, Keynote, PowerPoint, or Google Slides. The markdown file is the blueprint, not the finished rendered product.

**Applies to:** Business, academic, startup, creative, technical, educational, and keynote presentations.
---

## Core Rules

Never violate these under any circumstances:

- One clear idea per slide. Maximum 5 elements per slide.
- Every slide must have atmospheric depth. Flat solid backgrounds are failure.
- Every slide must have a described visual or image. No text-only slides unless it is a deliberate typographic composition — and that choice must be explicitly justified in Composition.
- Every slide must have an intentional dominant whitespace zone. Accidental whitespace is failure.
- No two adjacent slides may share the same layout structure.
- Web-safe fonts only. Display: Impact, Arial Black, Georgia, Trebuchet MS. Body: Arial, Verdana, Tahoma, Georgia. The display font and body font chosen must be different from each other. Banned as primary: Inter, Roboto, Open Sans, Poppins, system-ui, Clash Display, Satoshi.
- Every slide must have a clear content hierarchy: one primary headline, optional secondary element, optional body or caption. Never two elements of equal visual weight competing for attention.
- Commit to one bold aesthetic tone for the entire deck.
- The defined color system hex values must be used exactly and consistently across every slide. No approximation, no drift.
- Every visual description must name subject, angle, lighting, mood, and treatment. Banned phrases: "abstract illustration", "relevant image", "appropriate visual", "background photo", "a visual of".
- All statistics require inline citations (Author, Year) and a source line at the bottom of the slide. Statistics must be visually prominent — large, isolated, and compositionally featured, never buried in body text.
- Avoid jargon. If a domain-specific term is essential, define it in plain language the first time it appears on a slide. Presentations are for audiences, not specialists.
- The opening slide must create immediate engagement — a provocation, stark fact, visual tension, or bold claim. It is never just a title card.
- The closing slide must feel like a visual and emotional destination. It must resolve the narrative and visually callback to the opening. It is never just a "Thank You" or "Questions" card.
- Slide count is determined by content, narrative arc, and user requirements — never by a default number. If the user specifies a count, follow it exactly. If they do not, determine the appropriate count after mapping the full narrative arc in Step 2. Never pad slides to hit a number. Never compress content to stay under one.

---

## Design Thinking

Complete these before Step 2. The answers inform both the narrative arc and the design system.

1. **Purpose** — What single idea must land per slide? Ruthlessly reduce to one.
2. **Tone** — Pick ONE extreme and commit fully: brutalist, dark editorial, luxury minimal, maximalist, industrial, retro-futuristic, playful chaos, art deco, neo-grotesque, organic, Swiss, handwritten.
3. **Audience Calibration** — Who is this deck for and what do they need to feel? An investor deck demands authority and precision. A university lecture needs clarity and pacing. A creative pitch needs provocation and originality. Let the audience shape every design decision.
4. **Memorable Element** — What makes this deck unforgettable? What are the one or two moments that will stay with the audience after they leave?
5. **Pattern Break** — What design convention are you deliberately violating across this deck?
6. **Constraints** — Topic formality, content type, brand requirements, any hard restrictions.

---

## Aesthetic System

### Primitives

Choose 3–4 immutable building blocks for the entire deck. Define them in Part I. Examples: heavy cards, diagonal overlays, glass panels, typographic blocks, industrial frames, bleeding color fields. The choice must be dictated by content and tone, not habit. Every slide must use these primitives — no drift, no improvisation mid-deck.

### Color

One dominant color with sharp accents. Define the full system in Part I: background, surface, text, accent, and section colors with hex values. Vary light and dark foundations by tone. Banned: purple-to-blue gradients on white, rainbow palettes with no hierarchy.

### Typography

Extreme scale contrast is mandatory — it is a compositional weapon. Pair one display font with one body font — they must be different from each other. Define the full scale hierarchy in Part I with specific point sizes for headline, subheading, body, and caption. Never switch fonts or break the defined scale mid-deck.

### Composition

- Asymmetric layouts preferred (40/60, 30/70 splits over equal columns)
- Break grids deliberately — or use rigid symmetry only when it serves the message
- Open layouts use generous whitespace. Density layouts use tight, intentional spacing. The middle is always wrong.
- No two adjacent slides share the same layout

### Whitespace

Whitespace is not empty space — it is an active design element. Use it with the same intention as typography and color.

- Every slide must have a dominant negative space zone. Define where it lives (top, left margin, bottom third) and protect it from content intrusion.
- Isolate the most important element with whitespace. The eye must reach it first with zero friction.
- Never fill available space because it exists. Unused space signals confidence and control.
- Margins must be consistent within a slide and intentional in scale. On open layouts, margins are generous. On density layouts, margins are tight by deliberate choice — not by accident.
- When using controlled density layouts, whitespace between elements must still be intentional — use consistent spacing units (e.g., all gaps multiples of 8px or 16px).
- Whitespace rhythm must vary across the deck: some slides breathe with extreme openness, others are deliberately dense. Never the same density ratio twice in a row.
- Headlines isolated in whitespace hit harder than headlines surrounded by content. Use this deliberately for key message slides.

### Atmospheric Depth

Every slide uses at least two techniques. Vary techniques across the deck. Match techniques to tone — do not apply techniques that contradict the chosen aesthetic:

- Grain or noise textures — suits brutalist, industrial, retro-futuristic, handwritten
- Gradient meshes — suits dark editorial, luxury minimal, neo-grotesque
- Glassmorphism or frosted surfaces — suits luxury minimal, organic, Swiss
- Dramatic drop shadows — suits brutalist, maximalist, art deco
- Layered transparencies — suits dark editorial, maximalist, retro-futuristic
- Neumorphic surfaces — suits luxury minimal, organic
- Halftone or geometric patterns — suits brutalist, industrial, art deco, playful chaos
- Color field washes — suits Swiss, neo-grotesque, organic
- Photographic treatments: duotone, overlay, blend modes — suits dark editorial, retro-futuristic, industrial

### Data Visualisation

When a slide contains charts, graphs, or tables:

- Never use default chart styling from any tool. Default colors, gridlines, and axis styles are always wrong.
- Remove all gridlines unless they are load-bearing for reading the data.
- Highlight the single most important data point visually — larger, bolder color, isolated — everything else recedes.
- Chart colors must come from the deck's defined color system, never from software defaults.
- Axis labels and data labels must match the deck's body font at a legible size — never smaller than caption level in the defined type scale.
- Tables must be stripped of default borders. Use whitespace and color fields to create row separation instead.

### Iconography

Icons are permitted only when they reinforce meaning, not decorate. If icons are used:

- Style must be consistent across the entire deck — all line icons or all filled icons, never mixed.
- Icon style must be compatible with the chosen tone — geometric for Swiss or neo-grotesque, rough for brutalist or handwritten, refined for luxury minimal.
- Icons may not substitute for a proper visual direction. A slide with an icon is not a slide with a visual.

### Visual Rhythm

The deck is a sequence, not a collection. Alternate high-energy and contemplative slides. Section breaks demand a visual gear-shift: palette inversion, massive typography, full-bleed image, extreme whitespace, or geometric break. Each transition must feel different from the last.

The opening slide sets the entire visual register for the deck — it must be the most compositionally deliberate slide in the deck. The closing slide must be visually distinct from all body slides, signalling resolution through composition, not just content. Both the opening and closing are peak-weight compositions regardless of how much text they carry.

---

## Execution Workflow

Follow this sequence exactly:

**Step 1 — Clarify Requirements**

Identify what the user has already provided. Only ask for what is genuinely missing and necessary. At minimum you need: topic and audience. Everything else can be reasonably inferred or defaulted if not provided.

**Step 2 — Answer Design Thinking and Plan the Narrative Arc**

Answer all Design Thinking questions first. Then map the narrative arc using whichever of the following functions this deck requires — not all are mandatory:

- **Opening** — The first slide. Creates immediate engagement through provocation, stark fact, visual tension, or bold claim.
- **Context** — Background or situation the audience needs before the argument can land.
- **Tension** — Where complexity, conflict, or challenge enters the narrative.
- **Evidence** — Data, case studies, or proof points supporting the argument.
- **Peak** — The single most important moment. Highest stakes, highest visual weight.
- **Resolution** — How the argument resolves. What the audience now believes or feels.
- **Closing** — The final slide. A destination, not a stop. Resolves visually and emotionally. Callbacks to the opening deliberately.
- **Section Break** — Visual gear-shift between major sections. Contains a single bold statement, typographic moment, or full-bleed visual. No body text. No data.

Label every planned slide with its narrative function. Determine total slide count from this map — never before it.

**Step 3 — Write Part I: Design System**

Define the complete design system. Every element must be specific enough that a designer can implement it without asking a single question. If any element cannot be fully defined from available information, make a deliberate creative choice and state it explicitly — never leave a field vague or approximate.

- **Rationale** — One paragraph explaining the chosen tone and why it fits this specific content and audience.
- **Color System** — All colors with hex values, usage rules, and hierarchy. Which color dominates, which is accent, which is background, which is surface, which is text.
- **Typography** — Display and body font pairing, full size scale with specific point sizes for headline, subheading, body, and caption. Weight and tracking rules.
- **Primitives** — The 3–4 immutable building blocks chosen for this deck with precise description of how each is used.
- **Visual Language** — Atmospheric techniques selected for this deck, how they are applied, and how they vary across slides.
- **Whitespace Strategy** — Which slides breathe, which are dense, where dominant negative space zones live across the deck.
- **Composition Principles** — Specific layout logic, grid-breaking decisions, and asymmetry rules governing this deck's spatial arrangements.
- **Visual Rhythm and Section Transitions** — The pacing map: which slides are high-energy, which are contemplative, where gear-shifts occur and what form they take.

**Step 4 — Write Part II: Slides**

For each slide write all of the following in order:

- **Narrative Function** — Label this slide: Opening, Context, Tension, Evidence, Peak, Resolution, Closing, or Section Break.

- **Composition** — Describe the full spatial layout in precise prose. Cover: layout structure and grid logic, position and relative size of every element, element hierarchy from primary to tertiary, the dominant whitespace zone — where it sits, how large it is proportionally, and what it isolates. Be specific enough that a designer can reconstruct this layout without a diagram. Example: "Headline anchored top-left at 15% from top, spanning 55% of slide width. Visual occupies the full right 45%, bleeding to the edge. Body text sits in the lower-left quadrant, 30% from bottom, constrained to 50% width. Dominant whitespace zone: lower-right 25% of the slide, completely clear, creating diagonal tension toward the headline."

- **Content** — Write the actual slide content: the headline, any subheading, body text, and captions. Headlines must be declarative statements of the slide's conclusion — never topic labels. "We Grew 3x in Q3" is a headline. "Growth" is a label. Body text must be concise — maximum two sentences per block. Bullet points are permitted only when items are genuinely list-like and parallel; never use bullets to avoid writing proper prose. Avoid jargon; define any essential technical term on first use.

- **Visual** — Every slide must have a visual or image direction. No slide is text-only unless it is a deliberate typographic composition and that choice is justified in Composition. Describe with full cinematic specificity: subject, angle, lighting, mood, color treatment, texture, and how the image interacts with the whitespace zones. A designer must be able to source or create this asset without asking a single question. Two examples of required specificity — meet or exceed both. Photographic: "Extreme close-up of a weathered brass compass face, shot directly overhead on a matte black stone surface, hard directional light from upper left casting long shadows across the numerals, desaturated with a warm amber duotone overlay." Typographic composition: "The word VELOCITY set in Impact at 400pt, white, rotated 8 degrees counter-clockwise, bleeding off the right edge of the slide, with 6px tracking expansion and a hard red drop shadow offset 4px down and right."

- **Visual Feel** — What it should feel like to look at this slide. The emotional register, visual tension or calm, weight and energy. The subjective experience of the slide, distinct from its structure.

- **Exit Tension** — The unanswered question, unresolved image, or incomplete thought this slide leaves that pulls the audience to the next slide. Omit this line entirely on Closing and Section Break slides.

- **Atmosphere** — List the two or more atmospheric depth techniques used on this slide and confirm they are compatible with the deck's tone.

- **Source** — Full citation if statistics appear on this slide.

- **Takeaway** — The single idea this slide must land (optional, include when it adds clarity).

**Step 5 — Audit**

Run every item in the Pre-Delivery Checklist. If any answer is no, revise before delivering. Do not deliver until all items pass.

---

## Output Structure

The output is a single markdown file structured exactly as follows:

**File header**

    # [Presentation Title]
    ## Presentation Design System & Slide Deck

**Separator**

    ---

**Part I label**

    # PART I — DESIGN SYSTEM

Sections within Part I: Rationale, Color System, Typography, Primitives, Visual Language, Whitespace Strategy, Composition Principles, Visual Rhythm and Section Transitions.

**Separator**

    ---

**Part II label**

    # PART II — SLIDE DECK (N Slides)

Each slide follows this pattern:

    ## Slide N — [Title]
    **Narrative Function:** ...
    **Composition:** ...
    **Content:** ...
    **Visual:** ...
    **Visual Feel:** ...
    **Exit Tension:** ... (omit this line entirely on Closing and Section Break slides)
    **Atmosphere:** ...
    **Source:** ... (if data present)
    **Takeaway:** ... (if needed)

**File footer**

    ---
    ## References
    [Full bibliographic listing of all cited works]

---

## Anti-Patterns

Any of these constitutes failure. Revise until none apply:

- Hero image left, text right — or any equal-column split
- Three equal centered cards with icons
- Aesthetic describable only as "clean" or "modern"
- Purple-to-blue gradients on white
- Generic visual descriptions ("abstract illustration", "relevant image", "appropriate visual")
- Same layout on two adjacent slides
- More than 5 elements per slide
- Safe system fonts with no scale contrast
- Flat solid backgrounds with zero depth or texture
- Designs that could swap logos and serve any other company
- Default PowerPoint, Keynote, or Google Slides template patterns
- Text-only slides with no visual direction and no typographic composition justification
- Whitespace that is accidental — content placed without intentional negative space zones
- Slides where the dominant eye path is ambiguous — the viewer must hunt for the point
- Opening slide that merely states the topic with no provocation, tension, or bold claim
- Closing slide that simply says "Thank You" or "Questions" with no visual resolution
- Slides that exist independently with no narrative connection to what precedes or follows
- Statistics presented as inline text rather than as dominant visual protagonists
- Slides that feel like they belong to different decks — inconsistent primitive usage, color drift, or typography switching mid-deck
- Bullet-heavy slides where bullets substitute for clear thinking — three bullets or fewer per slide, only when items are genuinely parallel and list-like
- Default chart or graph styling — grey gridlines, default software colors, unlabeled axes, no highlighted data point
- Mixed visual styles across the deck — photographs on one slide, flat icons on another, illustrations on a third, with no visual logic connecting them
- Visual Feel absent or generic — "energetic" or "calm" without specificity is not a Visual Feel description

---

## Pre-Delivery Checklist

Run every item before delivering. If any answer is no, revise. Do not deliver until all items pass.

- [ ] Narrative arc is mapped — Opening and Closing are present, all other functions are used only where the content requires them
- [ ] Opening slide creates immediate engagement — provocation, stark fact, visual tension, or bold claim — not just a title
- [ ] Closing slide feels like a destination, resolves the narrative, and visually callbacks to the opening
- [ ] Every slide has an Exit Tension except Closing and Section Break slides — those lines are omitted entirely
- [ ] Section Break slides contain a single bold statement or visual moment — no body text, no data
- [ ] No two adjacent slides share the same layout structure
- [ ] Every slide has atmospheric depth — no flat backgrounds
- [ ] Atmospheric techniques used are compatible with the deck's chosen tone
- [ ] Every slide has a described visual or image — no unjustified text-only slides
- [ ] Every slide has a Visual Feel description that is specific — not just "energetic" or "calm"
- [ ] Whitespace strategy defined in Part I is applied in every slide — each slide has a named, protected dominant whitespace zone
- [ ] Whitespace rhythm varies across the deck — not the same density ratio twice in a row
- [ ] Every slide uses the primitives, color system, and typography defined in Part I — no drift, no improvisation
- [ ] All statistics are visually prominent and cited with inline citations and source lines
- [ ] All image descriptions are precise: subject, angle, lighting, mood, treatment — no banned phrases
- [ ] All headlines are declarative statements of the slide's conclusion — not topic labels
- [ ] Bullet points are used only where items are genuinely parallel and list-like — three or fewer per slide
- [ ] Jargon is absent or defined in plain language on first use
- [ ] Extreme scale contrast is present within slides
- [ ] Design system in Part I is complete and specific — a designer could implement it without asking a question
- [ ] One bold aesthetic tone is committed to throughout the entire deck
- [ ] Visual rhythm varies — alternating energy levels across the deck
- [ ] Section breaks create a distinct visual gear-shift
- [ ] References section lists all cited works in full
- [ ] Slide count is justified by narrative structure — not padded, not compressed
- [ ] Would a professional designer proudly claim this deck?

---

## Precedence

User requirements override all defaults — colors, slide count, content, aesthetic direction, brand constraints. The design system serves the user's vision, not the other way around.