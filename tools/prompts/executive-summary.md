# Executive Summary Generator

Distill a longer document into a 3-5 bullet executive summary.

## When to Use

After completing a brief, synthesis, or report. The executive summary is often written last, once you know what the document actually says.

## Prompt

```
Write an executive summary for this document:

{paste document}

Requirements:
1. **3-5 bullets maximum** — each should be one sentence
2. **Standalone:** Reader should understand the gist without reading more
3. **Lead with the verdict:** What's the recommendation or key finding?
4. **Include stakes:** Why does this matter? What's the impact?
5. **End with action:** What happens next or what decision is needed?

Avoid:
- Vague statements ("We analyzed the situation")
- Hedging ("This could potentially...")
- Jargon without explanation
- More than 5 bullets

Format as a bulleted list under an "## Executive Summary" heading.
```

## Example Output

```markdown
## Executive Summary

- **Recommend proceeding with Option B** (incremental migration) based on team capacity constraints and lower risk profile.
- Current API handles 10k req/s but enterprise customers need 25k by Q3; doing nothing risks churn of 3 key accounts.
- Migration will require 2 engineers for 4 months; Team Alpha has capacity starting February.
- Primary risk is coordination with the mobile team, which has a conflicting launch in March—mitigation plan included.
- **Decision needed by Jan 15** to hit Q3 target; next step is sign-off from VP Engineering.
```

## Tips

- Write the summary after the document is complete, not before
- Read it aloud—if it takes more than 30 seconds, it's too long
- Ask: "If this is all they read, will they make the right decision?"

