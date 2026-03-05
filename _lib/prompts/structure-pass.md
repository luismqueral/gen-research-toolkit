# Structure Pass

Review a draft for organizational issues before polishing language.

## When to Use

After completing a first draft. This is pass 1 of 2 in the editorial workflow (structure, then language).

## Prompt

```
Review this draft for structural issues:

{paste draft}

Check for:
1. **Order:** Does the sequence make sense? Should sections be reordered?
2. **Logic:** Does each section follow from the previous? Are there gaps in reasoning?
3. **Duplication:** Is anything repeated unnecessarily?
4. **Completeness:** Are there missing sections the reader would expect?
5. **Balance:** Are sections appropriately weighted, or is one too long/short?
6. **Audience fit:** Does the structure match what this audience needs?

For each issue found:
- Quote the relevant section
- Explain the problem
- Suggest a fix

If no issues, confirm the structure is sound.
```

## Example Output

```markdown
## Structure Review

### Issues Found

**1. Order Issue (Recommendation before Context)**
> ## Recommendation
> We should proceed with Option B.
>
> ## Context
> The team has been evaluating options since Q3...

**Problem:** Reader sees recommendation before understanding the situation.
**Fix:** Move Context above Recommendation.

**2. Gap in Reasoning**
> We interviewed 5 teams and found consensus on the approach.

**Problem:** Jumps from interviews to conclusion without showing the evidence.
**Fix:** Add a "Themes from Interviews" section between.

**3. Missing Section**
**Problem:** No risks section. Leadership will ask about downsides.
**Fix:** Add "Risks & Mitigations" before Next Steps.

### Structure is otherwise sound
- Executive summary is appropriately brief
- Next steps have clear owners
```

