# Language Pass

Review a draft for clarity, brevity, and rhythm after structure is solid.

## When to Use

After the structure pass. This is pass 2 of 2 in the editorial workflow.

## Prompt

```
Review this draft for language quality:

{paste draft}

Check for:
1. **Clarity:** Is every sentence unambiguous? Could a busy reader misunderstand?
2. **Brevity:** Can anything be cut without losing meaning?
3. **Rhythm:** Do sentences vary in length? Is it readable aloud?
4. **Jargon:** Is technical language necessary, or can it be simplified?
5. **Passive voice:** Convert to active where it improves directness
6. **Weak verbs:** Replace "is/are/was/were" with action verbs where possible
7. **Hedging:** Remove unnecessary qualifiers (somewhat, perhaps, arguably)

For each issue:
- Quote the original
- Provide a revised version
- Briefly explain why

Don't rewrite the entire document—focus on the most impactful improvements.
```

## Example Output

```markdown
## Language Review

### Clarity
**Original:** "The system is used by users to accomplish their tasks."
**Revised:** "Users complete tasks in the system."
**Why:** Removes redundancy, more direct.

### Brevity
**Original:** "At this point in time, we are currently in the process of evaluating..."
**Revised:** "We're evaluating..."
**Why:** 12 words → 2 words, same meaning.

### Passive Voice
**Original:** "The decision was made by leadership to proceed."
**Revised:** "Leadership decided to proceed."
**Why:** Active voice is more direct and assigns clear ownership.

### Hedging
**Original:** "This could potentially perhaps help to somewhat improve performance."
**Revised:** "This should improve performance."
**Why:** Excessive hedging undermines confidence. If uncertain, quantify the uncertainty instead.

### Overall
The draft is readable. Main opportunities are in the executive summary (too wordy) and the risks section (passive voice throughout).
```

