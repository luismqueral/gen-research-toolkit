# Transcript Cleaner

Transform raw transcript output into clean, readable markdown.

## When to Use

After receiving raw output from Whisper, Otter, or similar transcription tools. The raw output is often a wall of text with filler words, false starts, and no structure.

## Prompt

```
Clean this transcript for use as a source document:

1. **Structure:** Add paragraph breaks at natural topic shifts
2. **Speaker labels:** Identify speakers where possible (use [Speaker 1], [Speaker 2] if names aren't clear)
3. **Timestamps:** Insert timestamps at ~2-minute intervals in format [MM:SS]
4. **Filler removal:** Remove filler words (um, uh, like, you know) and false starts
5. **Unclear sections:** Mark with [inaudible] or [unclear]
6. **Preserve meaning:** Don't paraphrase or summarize—keep the speaker's actual words

Add frontmatter:
- date: (from filename or content)
- participants: (if identifiable)
- duration: (if known)
- source: (original filename)

Output clean markdown.
```

## Example Input

```
so um yeah I was thinking about the the project and like you know we really need to um figure out what the the priority is here because like there's a lot of things we could do but um I think the main thing is like getting the the dashboard working first you know what I mean
```

## Example Output

```markdown
---
date: 2025-01-07
participants: [Speaker 1]
source: meeting-recording.whisper
---

[00:00]

**[Speaker 1]:** I was thinking about the project. We really need to figure out what the priority is here because there's a lot of things we could do, but I think the main thing is getting the dashboard working first.
```

