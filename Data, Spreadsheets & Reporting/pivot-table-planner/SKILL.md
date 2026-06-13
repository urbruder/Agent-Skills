---
name: pivot-table-planner
description: plan exact pivot table setups for spreadsheets, excel, google sheets, airtable exports, csv files, sales data, survey data, finance data, ecommerce data, operations data, and analytics exports. use when the user describes a reporting question and needs rows, columns, values, filters, calculated fields, grouping, sorting, formatting, and interpretation guidance.
---

# Pivot-Table Planner

Translate a business question into the exact pivot table configuration needed to answer it.

## Core workflow

1. Identify the reporting question, dataset fields, grain, and desired comparison.
2. Choose rows, columns, values, filters, and calculated fields.
3. Recommend aggregation type: sum, count, distinct count, average, min, max, percent of total, or running total.
4. Include grouping for dates, numeric buckets, or categories.
5. Explain how to read the result and what chart to use if helpful.

If inputs are incomplete, make practical assumptions and label them clearly. Ask for clarification only when the missing information would make the analysis misleading or unusable.

Use `references/pivot-table-planner-framework.md` for deeper templates, checklists, examples, and quality standards.

## Default output

```markdown
## Reporting Question
[Question]

## Pivot Setup
| Area | Field | Setting |
|---|---|---|
| Rows | [field] | [grouping/sort] |
| Columns | [field] | [grouping] |
| Values | [field] | [aggregation] |
| Filters | [field] | [filter] |

## Calculated Fields
- [Name]: [Formula]

## Optional Chart
- Chart type:
- Why:

## How to Interpret
[Plain-English guide]
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
