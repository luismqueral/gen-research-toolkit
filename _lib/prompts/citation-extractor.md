# Citation Extractor

Pull notable quotes from source material with proper references.

## When to Use

When building a synthesis and you need to identify the most important quotes from transcripts, documents, or research.

## Prompt

```
Extract notable quotes from this source:

{paste source content}

For each quote:
1. **Quote:** The exact words (can be lightly trimmed with [...] for length)
2. **Speaker/Source:** Who said it or where it came from
3. **Line/Timestamp:** Reference for finding it again
4. **Why it matters:** One sentence on why this quote is significant
5. **Theme:** What topic or theme does this relate to?

Prioritize quotes that:
- Represent a key stakeholder position
- Provide concrete evidence for a claim
- Capture a theme memorably
- Reveal tension or disagreement
- Contain specific numbers or commitments

Skip quotes that are:
- Agreeable but generic ("Yeah, that makes sense")
- Procedural ("Let's move to the next topic")
- Redundant with other extracted quotes

Output as a markdown list, grouped by theme if patterns emerge.
```

## Example Output

```markdown
## Extracted Quotes

### Theme: Capacity Concerns

> "We're at 80% capacity and hiring is frozen through Q2."
> — **Sarah, Engineering Lead** | standup-notes.md, line 34
> **Why it matters:** Concrete constraint that affects timeline planning.

> "Every new feature request feels like we're robbing Peter to pay Paul."
> — **Marcus, PM** | planning-meeting.md, line 89
> **Why it matters:** Captures team sentiment about prioritization pressure.

### Theme: Migration Hesitancy

> "The last migration took 6 months longer than planned. I'm not eager to repeat that."
> — **David, Principal Engineer** | retro-notes.md, line 12
> **Why it matters:** Historical context that will influence stakeholder buy-in.

### Theme: Customer Impact

> "Three enterprise customers have asked about API v2 timeline in the last month."
> — **Sales team sync** | sales-notes.md, line 56
> **Why it matters:** External pressure that could accelerate decision.
```

