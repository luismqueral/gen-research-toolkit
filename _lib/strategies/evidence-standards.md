---
title: "Rule: Evidence Standards"
purpose: "Clarify how to distinguish and cite facts, assumptions, and opinions"
status: final
---

## What This Is

Standards for handling evidence in briefs, syntheses, and reports. Ensures readers can distinguish what's verified from what's inferred.

## The Three Categories

### Facts
Verifiable statements with a source.
- Cite inline with file reference and line/timestamp when possible
- Format: `(source: filename.md, line 42)` or `(source: transcript, 12:34)`

### Assumptions
Beliefs treated as true for planning purposes, but not yet verified.
- Label explicitly: "**Assumption:**" or "[assuming X]"
- Note how the assumption could be validated

### Opinions
Judgments, interpretations, or recommendations.
- Own them: "We recommend..." or "In our view..."
- Provide rationale

## Citation Format

**Inline citation:**
> "The system handles 10k requests per second" — *load-test-results.md, line 23*

**Parenthetical:**
The team reported capacity issues (source: standup-notes-2025-01-06.md, lines 15–18).

**Pull quote with annotation:**
> "We're hitting limits [on the auth service] during peak hours"
> — *Marie, team sync, 2025-01-05*

## When to Use Pull Quotes

Only when the quote carries decisive signal:
- A key stakeholder's explicit position
- Evidence that directly supports or contradicts a claim
- Memorable phrasing that captures a theme

Avoid decorative quotes that don't advance the argument.

## Quick Checklist

- [ ] Facts have sources
- [ ] Assumptions are labeled and could be validated
- [ ] Opinions have rationale
- [ ] Pull quotes add signal, not decoration

