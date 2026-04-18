# 📚 Student Lab

A collection of Claude skills designed for students who need to learn fast and score high.

> **What are skills?** Skills are instruction sets (packaged as folders) that teach Claude how to handle specific tasks. Upload them to Claude.ai via **Settings → Capabilities → Skills**, or place them in your Claude Code skills directory. [Learn more about skills](https://docs.anthropic.com/en/docs/agents-and-tools/skills).

---

## Available Skills

### 🧠 [exam-notes](./exam-notes/)

**Transform any study material into exam-ready notes you can absorb in one evening.**

| Feature | Detail |
|---|---|
| **What it does** | Takes textbook chapters, lecture slides, PDFs, or any study material and produces structured, complete notes optimized for first-time reading and next-day exam performance |
| **Three-layer system** | 🗺️ Roadmap (big picture in 3 min) → 🏗️ Build-Up (every concept taught from scratch) → 🏁 Speed Review (15-min final scan) |
| **Smart prioritization** | 🔴 Critical / 🟡 Important / 🟢 Good-to-Know ratings on every topic — so you know where to spend your time |
| **Memory engineering** | Mnemonics, vivid analogies, and memory hooks for every critical concept |
| **Exam strategy** | Exam predictions, common traps (❌→✅), exam-style questions, and rapid-fire Q&A |
| **Concise by design** | Fragments over sentences, depth scaled by importance, full syllabus readable in one sitting |

**Trigger phrases:** "make notes", "exam prep", "night before exam", "help me study", "revision notes", "cram for exam", "study guide", "break this down for my exam"

<details>
<summary><strong>Example usage</strong></summary>

**Input:** Upload a PDF chapter or paste lecture content, then say:

> Make notes from this for my exam tomorrow

**Output:** Three-layer notes with:
- 📖 Connected story of the entire material
- 🗂️ Visual concept map showing how everything relates
- 📌 Every concept defined, explained with analogies, and tagged for exam importance
- 📝 Every formula with worked examples and common traps
- 📊 Comparison tables wherever related concepts exist
- 🧠 Memory hooks for rapid recall
- 🎯 Top exam predictions with one-line answers
- ❓ Self-test questions to activate recall
- 🔗 Connection chain linking all topics

</details>

---

### 🎨 [presentation-designer](./presentation-designer/)

**Turn any topic or content into a cinematic, art-directed slide deck.**

| Feature | Detail |
|---|---|
| **What it does** | Produces a complete design system + slide-by-slide deck in markdown — precise enough to implement in Figma, Keynote, PowerPoint, or Google Slides |
| **Design system** | Full color palette (hex values), typography scale, layout primitives, whitespace strategy, and atmospheric depth — all defined before a single slide is built |
| **Aesthetic tones** | Commits to one bold tone per deck: brutalist, dark editorial, luxury minimal, retro-futuristic, art deco, Swiss, and more |
| **Narrative structure** | Every deck has a mapped arc — provocative opening, logical middle, resolved closing — never just a stack of slides |
| **No generic output** | Anti-patterns enforced: no equal-column splits, no three-icon cards, no flat backgrounds, no default chart styling |
| **Fully specified visuals** | Every slide has a precise visual description (subject, angle, lighting, mood, treatment) — no "relevant image" placeholders |

**Trigger phrases:** "make slides", "create a presentation", "build a deck", "design a pitch", "make a PPT", "help me present", "slide deck for"

<details>
<summary><strong>Example usage</strong></summary>

**Input:** Paste your content or describe your topic, then say:

> Make a presentation on India's EdTech market for an investor pitch

**Output:** A full design-spec deck with:
- 🎨 Complete design system (colors, fonts, primitives, whitespace rules)
- 🖼️ Art-directed visual direction for every slide
- 📐 Distinct layout on every slide — no two adjacent slides share the same structure
- 📊 Data slides with styled, highlighted charts
- 🎯 Narrative arc from provocative opener to resolved close
- ✅ Pre-delivery checklist audit confirming every slide passes quality standards

</details>

---

## 🚀 Quick Start

### Option 1: Claude.ai (Recommended)

1. **Download** the skill folder (e.g., `exam-notes/`)
2. **Zip** the folder
3. Go to **Claude.ai → Settings → Capabilities → Skills**
4. Click **"Upload skill"** and select the zip file
5. **Toggle on** the skill
6. Upload your study material and say: *"Make notes for my exam tomorrow"*

### Option 2: Claude Code

1. Clone this repo:
   ```bash
   git clone https://github.com/fyaz05/skill-lab.git
   ```
2. Place the skill folder in your Claude Code skills directory
3. The skill activates automatically when relevant

### Option 3: API

Skills work with the Messages API via the `container.skills` parameter.
See [Skills API Quickstart](https://docs.anthropic.com/en/docs/agents-and-tools/skills) for details.

---

## 📋 Skill Collection Roadmap

| Skill | Status | Description |
|---|---|---|
| `exam-notes` | ✅ Ready | One-evening exam prep notes from any material |
| `presentation-designer` | ✅ Ready | Cinematic, art-directed slide decks with full design systems |

*Have a suggestion?* [Open an issue](https://github.com/fyaz05/skill-lab/issues)

---

## 🏗️ Building Your Own Study Skills

Want to create a study skill? Follow the [Complete Guide to Building Skills for Claude](https://docs.anthropic.com/en/docs/agents-and-tools/skills).

Each skill in this repo follows the same structure:
```
skill-name/
├── SKILL.md              # Required — main instructions
└── references/           # Optional — detailed templates, guides
    └── *.md files
```

---

## 📄 License

[MIT](./LICENSE.md) — use, modify, and share freely.

---

## 🤝 Contributing

1. Fork this repo
2. Create your skill folder following the [skill structure guidelines](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)
3. Test your skill in Claude.ai
4. Submit a PR with:
   - Your skill folder (with SKILL.md)
   - A brief description for this README
   - Example usage with screenshots if possible

---

## 📬 Links

- [Claude Skills Documentation](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)
- [Example Skills by Anthropic](https://github.com/anthropics/skills)
- [Skills.sh](https://skills.sh)

---

<p align="center">
  Built for students, by a student. 🎓<br/>
  <em>One night. First-time reader. High score tomorrow.</em>
</p>