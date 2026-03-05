# Generative Research Toolkit

A framework for structured writing and research with an LLM partner. Drop in sources, ask for synthesis, get decision-ready documents.

## What This Is

This is a methodology for using LLMs as a research and knowledge management tool and synthesizer. The structure, conventions, and prompts here are optimized for:

- **Briefs** — decision documents, strategy proposals, pitch decks
- **Syntheses** — distilling transcripts, research, and conversations into insights

- **Planning docs** — next steps, roadmaps, discovery scopes


---

## Folder Structure

```
gen-research-toolkit/
├── projects/
│   └── {project-name}/
│       ├── inputs/          # Source material: transcripts, images, PDFs, notes
│       │   └── _archive/    # Stale inputs (ignored by LLM, see .cursorignore)
│       └── outputs/         # Finished artifacts: briefs, syntheses, reports
├── _lib/
│   ├── templates/           # Document scaffolds
│   ├── strategies/          # Reusable rules and patterns
│   └── prompts/             # Canned prompts for common operations
├── CHANGELOG.md             # Running log of meaningful changes
├── .cursorignore            # Patterns to exclude from LLM context
└── .cursor/rules/           # Workspace-level instructions for the LLM
```

### Naming Conventions

- **Folders:** `kebab-case` (e.g., `always-ready-2026`, `api-governance`)
- **Files:** `kebab-case.md` (e.g., `brief-leadership-pitch.md`, `synthesis-user-interviews.md`)
- **Prefix by type:** `brief-`, `synthesis-`, `mini-brief-`, `readiness-`, `notes-`

---

## Quick Start

1. **Create a project folder:**
   ```
   projects/my-project/
   ├── inputs/
   └── outputs/
   ```

2. **Drop source material into `inputs/`:**
   - Meeting transcripts (`.md` converted from Whisper, Otter, etc.)
   - Screenshots and diagrams (`.png`, `.jpg`)
   - Reference PDFs, raw notes, data exports
   - Any other context relevant to the project

3. **Start with structure:**
   Ask the LLM to outline your thinking before writing prose.
   > "Given these inputs, what are the key themes? Outline a synthesis."

4. **Iterate through drafts:**
   Use the prompts in `_lib/prompts/` for common operations.

5. **Generated artifacts land in `outputs/`:**
   Keep `inputs/` as source of truth, `outputs/` as finished artifacts.

6. **Update the changelog:**
   Log meaningful changes in `CHANGELOG.md`.

---

## Generative Strategies (`_lib/strategies/`)

### Mode Cards

`mode-cards.json` defines interaction modes that shape how the LLM engages with you. Each mode has a role, when to use it, and example prompts.

| Mode | Use When |
|------|----------|
| **Research partner** | Discovery, competitive analysis, entering a new problem space |
| **Brainstorm partner** | Ideation, concepting, when "stuck" |
| **Crit partner** | Challenging assumptions, anticipating obstacles |
| **Empathy partner** | Exploring other perspectives, simulating user reactions |
| **Polish partner** | Refining artifacts, improving clarity and precision |
| **Build partner** | Translating ideas into concrete prototypes or code |
| **Planning partner** | Structuring projects, creating outlines and checklists |

Reference a mode by asking the LLM to adopt it: *"As my crit partner, what might go wrong with this approach?"*

### Strategy Cards

`generative-strategies.json` is a deck of 201 conceptual lenses for lateral thinking. Each card has a title, a provocative prompt, and a theme. They're designed to break you out of habitual patterns when exploring a problem.

**Themes:** Philosophy (48), History (29), Science (23), Art (18), Architecture (18), Nature (16), Politics (8), Religion (7), Psychology (4), and others.

**Examples:**
- *Enter the Shadow* — examine what your priorities have pushed into darkness
- *Adopt the Mycological Perspective* — map hidden connections beneath the visible surface
- *Commit a Beautiful Nonsense* — sabotage order to reveal what was always arbitrary

Use them by drawing a card at random or by theme: *"Give me a strategy card from the Nature theme and apply it to this problem."*

---

## A Few Notes on Managing Context

### The `_archive/` Pattern

Move stale inputs to `inputs/_archive/` to keep them on disk but out of LLM context. The `.cursorignore` file excludes:

```
**/_archive/**
```

The underscore prefix floats `_archive/` to the top of an alphabetically sorted file tree, making it easy to spot. This pattern works anywhere — inside `inputs/`, `outputs/`, or at the `projects/` level for completed projects.

This is useful when:
- A transcript has been fully synthesized
- Source material is superseded by newer versions
- You want to reduce noise without deleting history


## Further Reading

This workflow is based on another project: [media-tool-kit](https://github.com/luismqueral/media-tool-kit).

