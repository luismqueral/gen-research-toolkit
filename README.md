<div align="center">
<img src="images/hypercard-stack.png" alt="HyperCard Stack" width="200">
</div>

<br>

`gen-research-toolkit` is a framework for LLM-assisted research and writing.


## Get Started
**Step 1:** Open Claude Code (or any agentic code editor)

**Step 2:** Enter this prompt:

```
Install https://github.com/luismqueral/gen-research-toolkit.git run ONBOARD.md
```

## How It Works

1. **Create a project folder:**
   ```
   projects/my-project/
   ├── input/
   └── output/
   ```

2. **Drop source material into `input/`** — transcripts, screenshots, PDFs, raw notes, data exports.

3. **Start with structure** — ask the LLM to outline your thinking before writing prose.

4. **Iterate through drafts** — use the prompts in `tools/prompts/` for common operations.

5. **Work lands in `output/`** — drafts, syntheses, briefs. Documents evolve over time.

## Strategy Cards

`tools/strategies/strategy-cards.json` is a deck of 201 conceptual lenses for lateral thinking. Each card has a title and a provocative prompt designed to break you out of habitual patterns.

Try it: *"Give me a strategy card and apply it to this problem."*

A few examples:

> **Follow the Resistance** — A hand plane chatters when the grain changes direction. A drill bit binds when it hits a different material. Resistance is information. Where does your work chatter, bind, or slow down? Don't fight through it — read it.

> **Enter the Shadow** — Every structure casts one. Your codebase has functions nobody calls but nobody deletes. Your organization has topics nobody raises in meetings. These shadows aren't accidents — they're the negative image of your priorities.

> **Commit a Beautiful Nonsense** — Take the most orderly part of this situation. Now sabotage it. Gently. Does it collapse? Or does the nonsense reveal that the original order was always arbitrary?

## Managing Context

Move stale inputs to `_archive/` to keep them on disk but out of LLM context. The `.cursorignore` and `.claudeignore` files exclude `**/_archive/**`.

This pattern works anywhere — inside `input/`, `output/`, or at the `projects/` level for completed projects.

---

Based on [media-tool-kit](https://github.com/luismqueral/media-tool-kit).

