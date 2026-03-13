# Outline Generator

Generate a document skeleton from notes, sources, or a prompt.

## When to Use

Before drafting prose. Start with structure to ensure logical flow and completeness.

## Prompt

```
Generate an outline for a {document type} about {topic}.

Context:
{paste relevant notes, sources, or requirements}

The outline should:
1. Use ## and ### headings (no # top-level)
2. Include 2-3 bullet points under each section indicating what belongs there
3. Note any open questions or gaps in brackets [?]
4. Suggest what evidence/sources would strengthen each section

Format as markdown. Don't write full prose—just the skeleton.
```

## Example

**Input:** "Generate an outline for a synthesis about our API migration options. We interviewed 3 teams and have load test results."

**Output:**

```markdown
## TL;DR
- Key recommendation (1 sentence)
- Top 2-3 supporting points
- Primary risk to flag

## Context
- Why we're considering migration now
- Current state of the API
- Stakeholders involved

## Themes from Interviews
### Team Capacity Concerns
- Evidence from Team A
- Evidence from Team B
- [? Need to confirm Team C's timeline]

### Performance Requirements
- Load test findings
- Gap between current and target

### Migration Approach Preferences
- Incremental vs. big-bang positions
- Trade-offs each team raised

## Implications
- For timeline
- For resourcing
- For architecture

## Recommendation
- Proposed approach
- Rationale
- Key dependencies

## Next Steps
- Immediate actions
- Decision points
- [? Need owner for migration lead role]
```

