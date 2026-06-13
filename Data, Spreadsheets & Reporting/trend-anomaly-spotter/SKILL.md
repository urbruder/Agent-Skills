---
name: trend-anomaly-spotter
description: analyze time-series data, weekly metrics, monthly metrics, revenue, traffic, conversion, churn, retention, sales, support, inventory, or operational data to identify trends, spikes, drops, anomalies, seasonality, likely drivers, and recommended follow-up checks. use when the user pastes data and asks what changed, why it may have changed, or what to investigate next.
---

# Trend & Anomaly Spotter

Find meaningful changes in time-series data and explain what changed, why it matters, and what to check next.

## Core workflow

1. Identify metric, time grain, segments, date range, and business context.
2. Compare current period to prior period, baseline, moving average, or same period last year when available.
3. Flag anomalies, trend shifts, step changes, volatility, and seasonality.
4. Avoid claiming causation without evidence.
5. Recommend diagnostic cuts and next actions.

If inputs are incomplete, make practical assumptions and label them clearly. Ask for clarification only when the missing information would make the analysis misleading or unusable.

Use `references/trend-anomaly-spotter-framework.md` for deeper templates, checklists, examples, and quality standards.

## Default output

```markdown
## What Changed
- [Change]

## Trend Summary
| Metric/segment | Direction | Magnitude | When it changed | Importance |
|---|---|---:|---|---|

## Anomalies
| Date/period | Metric | Expected/baseline | Actual | Possible explanation |
|---|---|---:|---:|---|

## Likely Drivers to Investigate
1. [Driver]
2. [Driver]

## Recommended Next Checks
- [Cut by segment/channel/product]
- [Data quality check]
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
