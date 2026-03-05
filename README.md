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

