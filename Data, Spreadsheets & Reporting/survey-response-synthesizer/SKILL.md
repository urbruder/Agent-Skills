---
name: survey-response-synthesizer
description: analyze open-ended survey responses, interview snippets, customer feedback, nps comments, form submissions, reviews, or qualitative research notes to extract themes, sentiment, pain points, desires, objections, pull-quotes, and five clear business insights. use when the user pastes many free-text answers and needs structured synthesis, executive summary, prioritization, customer language, or recommendations.
---

# Survey-Response Synthesizer

Turn open-ended responses into clear themes, evidence, pull-quotes, and practical insights.

## Core workflow

1. Identify the survey question, audience, sample size, and business goal.
2. Group responses into themes by meaning, not exact wording.
3. Separate strong repeated signals from weak or one-off comments.
4. Extract representative pull-quotes without changing meaning.
5. Summarize up to five key insights and recommend actions.

If inputs are incomplete, make practical assumptions and label them clearly. Ask for clarification only when the missing information would make the analysis misleading or unusable.

Use `references/survey-response-synthesizer-framework.md` for deeper templates, checklists, examples, and quality standards.

## Default output

```markdown
## Executive Summary
[3-5 bullets with the most important findings]

## Top 5 Insights
| Insight | Evidence | Business implication | Confidence |
|---|---|---|---|

## Themes
| Theme | Approx. frequency | Representative comments | What it means |
|---|---:|---|---|

## Pull-Quotes
- "[Quote]" — [theme]

## Recommendations
1. [Action]
2. [Action]
3. [Action]

## Caveats
[Sample bias, missing context, weak signals, or data limitations]
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
