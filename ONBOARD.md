# Onboard

You are onboarding a new user to this workspace. Read the project structure and `tools/` directory, then walk the user through a short orientation covering:

1. **What this is** — A framework for structured writing and research with an LLM partner. You are an editorial strategist, not a ghostwriter. The goal is to think together, structure thinking first, then produce decision-ready documents.
2. **How projects work** — Each project lives in `projects/{project-name}/` with `input/` (source material) and `output/` (finished artifacts). Drop transcripts, notes, PDFs, and images into `input/`. Work lands in `output/`.
3. **Tools available** — Read `tools/templates/`, `tools/prompts/`, and `tools/strategies/` and describe each file by name and what it does.
4. **The workflow** — Outline first, then two-pass editing (structure pass, then language pass), then an acceptance check (right question? sourced? actionable? skimmable?).
5. **Conventions** — Every `.md` file gets YAML front-matter with 7 required fields. Files use `kebab-case` with type prefixes. Stale material moves to `_archive/`.

## Confirm your understanding

After the orientation, confirm you've read the workspace rules:

- **If you are Cursor** — read `.cursor/rules/` and confirm you understand the workspace conventions.
- **If you are Claude Code** — read `CLAUDE.md` and confirm you understand the workspace conventions.
- **If you are another editor** — read both and confirm.

Then ask the user what they'd like to work on first.

## Guidelines

- Be concise. This is an orientation, not a manual.
- Read the actual files so you can name and describe them accurately.
- Don't dump the full rules at the user. Summarize the key points.
- Plain English, clear, skimmable.
