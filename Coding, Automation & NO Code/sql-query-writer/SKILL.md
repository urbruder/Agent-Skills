---
name: sql-query-writer
description: turn plain-english data questions into sql queries for postgres, mysql, sqlite, bigquery, snowflake, redshift, sql server, duckdb, and analytics databases. use when the user needs selects, joins, filters, aggregations, windows, ctes, date logic, cohort queries, funnels, deduping, debugging, optimization, or explanations of existing sql.
---

# SQL Query Writer

Translate business questions into correct SQL queries with assumptions, dialect awareness, and explanation.

## Core workflow

1. Identify the SQL dialect, tables, columns, relationships, filters, grain, and desired output.
2. If schema is missing, provide a query template with assumed names and a short list of needed fields.
3. Use clear CTEs for multi-step logic.
4. Explain joins, date filters, and aggregation grain.
5. Include validation checks and edge cases for duplicates or nulls.
6. Warn when assumptions may change results.

If essential details are missing, make practical assumptions and label them briefly. Ask for clarification only when guessing would make the output unusable, unsafe, or misleading.

Use `references/sql-query-writer-framework.md` for deeper patterns, checklists, templates, and troubleshooting.

## Default output

```markdown
## SQL

```sql
[query]
```

## Assumptions
- Dialect:
- Tables:
- Grain:
- Date range:
- Join keys:

## What it returns
[Plain-English explanation.]

## Validation checks
```sql
[optional check query]
```

## Adjust these parts
- `[table]`
- `[date_column]`
- `[metric]`
```

## Quality standards

Always prioritize:

- correctness
- security
- maintainability
- clear assumptions
- testability
- platform-specific compatibility
- minimal unnecessary complexity
- practical next steps

## Guardrails

Do not help bypass access controls, steal data, evade rate limits, hide malicious behavior, exploit systems, or violate terms of service. For scraping, automation, API, SQL, regex, and code tasks, keep outputs focused on authorized, legitimate, and ethical use.

## Final check

Before responding, verify that the output is specific, executable or build-ready, and includes any required assumptions, dependencies, credentials placeholders, test steps, and known risks.
