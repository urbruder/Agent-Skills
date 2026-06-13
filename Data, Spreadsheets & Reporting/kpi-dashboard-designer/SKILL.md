---
name: kpi-dashboard-designer
description: design business kpi dashboards, metric trees, reporting layouts, scorecards, executive dashboards, founder dashboards, sales dashboards, marketing dashboards, product dashboards, operations dashboards, finance dashboards, and spreadsheet dashboards. use when the user wants to define metrics, dashboard sections, chart types, data sources, cadences, thresholds, and decision-oriented reporting for any business.
---

# KPI Dashboard Designer

Define the right metrics, layout, charts, and operating cadence for a business dashboard.

## Core workflow

1. Identify the business type, audience, decisions the dashboard supports, and available data.
2. Define north star, input, output, leading, lagging, and guardrail metrics.
3. Organize the dashboard into sections with recommended charts.
4. Add metric definitions, formulas, update cadence, targets, and alert thresholds.
5. Recommend a layout that answers business questions quickly.

If inputs are incomplete, make practical assumptions and label them clearly. Ask for clarification only when the missing information would make the analysis misleading or unusable.

Use `references/kpi-dashboard-designer-framework.md` for deeper templates, checklists, examples, and quality standards.

## Default output

```markdown
## Dashboard Goal
[What this dashboard helps decide]

## KPI Architecture
| Metric | Type | Formula | Data source | Cadence | Target/threshold |
|---|---|---|---|---|---|

## Dashboard Layout
### Section 1: Executive Summary
- Chart/card:
- Purpose:

## Recommended Visuals
| Question | Chart type | Why |
|---|---|---|

## Operating Rhythm
- Daily:
- Weekly:
- Monthly:

## Data Quality Notes
[Definitions, gaps, or tracking issues]
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
