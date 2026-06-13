---
name: data-cleaning-playbook
description: create data cleaning plans for messy spreadsheets, csv files, exports, crm data, ecommerce data, survey data, lists, contacts, product catalogs, transaction logs, and reporting datasets. use when the user needs inconsistent, duplicated, incomplete, poorly formatted, mixed-case, mis-typed, multi-source, or analysis-unready data turned into a usable cleaning workflow with formulas, rules, validation, and qa checks.
---

# Data-Cleaning Playbook

Turn messy data into a clear cleaning plan with standardization rules, formulas, validation checks, and QA steps.

## Core workflow

1. Identify dataset purpose, columns, expected output, and known problems.
2. Profile issues such as duplicates, missing values, inconsistent formats, invalid values, split fields, text numbers, date issues, casing, and outliers.
3. Create a step-by-step cleaning workflow.
4. Provide spreadsheet formulas or transformation rules where useful.
5. Add validation checks before analysis or import.

If inputs are incomplete, make practical assumptions and label them clearly. Ask for clarification only when the missing information would make the analysis misleading or unusable.

Use `references/data-cleaning-playbook-framework.md` for deeper templates, checklists, examples, and quality standards.

## Default output

```markdown
## Data Cleaning Goal
[What clean data should support]

## Issues Found / Expected
| Issue | Columns affected | Fix | QA check |
|---|---|---|---|

## Cleaning Steps
1. [Step]
2. [Step]

## Standardization Rules
| Field | Rule | Example |
|---|---|---|

## Helpful Formulas
```excel
[formula]
```

## Validation Checklist
- [Check]
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
