---
name: retention-cohort-explainer
description: interpret retention tables, cohort charts, churn data, repeat purchase data, subscription cohorts, product usage cohorts, revenue retention, customer retention, ecommerce cohorts, app retention, or saas cohort data in plain english. use when the user wants to understand whether customers stick, where they drop off, which cohorts are improving, and what actions to take.
---

# Retention/Cohort Explainer

Explain retention and cohort data in plain English, highlighting where customers stick, drop, improve, or churn.

## Core workflow

1. Identify cohort definition, time period, retention metric, and customer/action basis.
2. Read the cohort table by row, column, and diagonal patterns.
3. Separate acquisition quality, onboarding, product value, lifecycle, and seasonality signals.
4. Identify strong and weak cohorts.
5. Recommend diagnostic cuts and retention actions.

If inputs are incomplete, make practical assumptions and label them clearly. Ask for clarification only when the missing information would make the analysis misleading or unusable.

Use `references/retention-cohort-explainer-framework.md` for deeper templates, checklists, examples, and quality standards.

## Default output

```markdown
## Plain-English Summary
[What the retention data says]

## Key Findings
1. [Finding]
2. [Finding]

## Cohort Interpretation
| Pattern | What it means | Possible action |
|---|---|---|

## Best Cohorts
- [Cohort] — [why]

## Weakest Drop-Off Points
- [Period] — [what may be happening]

## Recommended Next Steps
1. [Action]
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
