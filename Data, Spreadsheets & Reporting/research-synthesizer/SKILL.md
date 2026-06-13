---
name: research-synthesizer
description: synthesize multiple sources, reports, articles, transcripts, interviews, notes, pdfs, research papers, market scans, competitor materials, or web findings into one structured brief. use when the user drops several sources and needs key takeaways, themes, disagreements, evidence, implications, recommendations, open questions, and an executive-ready synthesis.
---

# Research Synthesizer

Turn many sources into one structured brief with themes, evidence, disagreements, and implications.

## Core workflow

1. Identify research question, audience, source types, and desired decision.
2. Extract key claims, evidence, data points, and source perspectives.
3. Cluster findings into themes.
4. Highlight consensus, disagreement, gaps, and confidence levels.
5. Produce an executive-ready brief with implications and recommendations.

If inputs are incomplete, make practical assumptions and label them clearly. Ask for clarification only when the missing information would make the analysis misleading or unusable.

Use `references/research-synthesizer-framework.md` for deeper templates, checklists, examples, and quality standards.

## Default output

```markdown
# Research Brief: [Topic]

## Executive Summary
[5-7 bullets]

## Key Findings
| Finding | Evidence | Sources | Confidence |
|---|---|---|---|

## Themes
### Theme 1: [Name]
[Summary and implications]

## Points of Disagreement
- [Disagreement]

## Implications
- [Implication]

## Recommendations
1. [Recommendation]

## Open Questions
- [Question]
```

## Data and reporting standards

Prioritize:

- clear business interpretation
- transparent assumptions
- distinction between facts, patterns, and recommendations
- practical next steps
- concise executive summaries
- useful tables when they improve clarity
- plain-English explanations
- skepticism about weak or incomplete data

## Guardrails

Do not invent data, quotes, metrics, competitors, research findings, causes, or source claims. If the data is incomplete, biased, stale, or too small to support a conclusion, say so. For financial, legal, medical, or high-stakes claims, keep recommendations cautious and evidence-based.

## Final check

Before responding, verify that the output is specific, decision-useful, grounded in the provided inputs, and easy for a business user to act on.
