---
name: spreadsheet-formula-builder
description: build exact spreadsheet formulas from plain-language requests for excel, google sheets, libreoffice calc, airtable-style exports, csv workflows, and business spreadsheets. use when the user needs lookup formulas, conditional logic, text parsing, date math, aggregation, filtering, deduping, array formulas, error handling, dynamic ranges, pivots-by-formula, or formula troubleshooting. prioritize correct syntax, platform-specific compatibility, clear assumptions, copy-paste-ready formulas, and brief explanations.
---

# Spreadsheet Formula Builder

Turn plain-language spreadsheet requests into exact, copy-paste-ready formulas.

## Core workflow

When the user describes what they want a spreadsheet to do:

1. Identify the spreadsheet platform:
   - Excel
   - Google Sheets
   - LibreOffice Calc
   - unknown or generic spreadsheet

2. Identify the formula goal:
   - lookup
   - conditional logic
   - sum/count/average with criteria
   - text extraction or cleanup
   - date/time math
   - filtering or sorting
   - deduping
   - combining columns
   - splitting values
   - error handling
   - dynamic array output
   - cross-sheet reference
   - validation or flagging
   - troubleshooting an existing formula

3. Identify the relevant ranges, columns, headers, and example rows.

4. If details are missing, make a clear assumption and provide a formula the user can adapt. Do not block on clarification unless no usable formula can be created.

5. Provide the final formula first.

6. Explain only what is needed to help the user use or adapt it.

7. Use `references/formula-patterns.md` for formula families, platform differences, examples, and troubleshooting.

## Default output

Use this structure unless the user asks for something else:

```markdown
## Formula

```excel
[copy-paste-ready formula]
```

## Assumptions
- Platform: [Excel / Google Sheets / generic]
- Put this formula in: [cell or column]
- Source data: [ranges/columns assumed]

## How it works
[Brief explanation in plain English.]

## Adjust these parts
- `[range]` = [what to change]
- `[criteria]` = [what to change]
```

If the formula differs by platform, provide both:

```markdown
## Excel

```excel
[formula]
```

## Google Sheets

```excel
[formula]
```
```

## Formula rules

Always:

- produce a formula that can be pasted directly into the spreadsheet
- use the user's actual column letters, headers, sheet names, and examples when provided
- wrap sheet names with spaces in single quotes
- include absolute references when the formula will be copied down or across
- add `IFERROR` only when helpful, not by default when it would hide problems
- prefer readable modern formulas when available
- provide legacy alternatives when compatibility matters
- warn if a formula requires Microsoft 365 dynamic arrays or Google Sheets-only functions

## Platform guidance

### Excel

Prefer:

- `XLOOKUP` for modern lookup
- `INDEX` + `MATCH` for legacy compatibility
- `FILTER`, `UNIQUE`, `SORT`, `TEXTSPLIT`, `LET` when Microsoft 365 is available
- structured references when the user uses tables

### Google Sheets

Prefer:

- `FILTER`, `QUERY`, `ARRAYFORMULA`, `UNIQUE`, `SORT`, `SPLIT`, `REGEXEXTRACT`, `REGEXREPLACE`
- open-ended ranges like `A2:A` when appropriate
- `IMPORTRANGE` only when the user asks for cross-file data

### Generic spreadsheet

Use broadly compatible formulas:

- `IF`
- `SUMIF`
- `SUMIFS`
- `COUNTIF`
- `COUNTIFS`
- `VLOOKUP`
- `INDEX`
- `MATCH`
- `LEFT`
- `RIGHT`
- `MID`
- `FIND`
- `SEARCH`
- `DATE`
- `TEXT`

## Common request patterns

### Lookup
Return a value from another table based on an ID, email, SKU, name, or date.

### Conditional label
Classify rows based on one or more conditions.

### Multi-condition calculation
Sum, count, or average values based on several criteria.

### Text parsing
Extract domains, names, SKUs, order IDs, numbers, or text between delimiters.

### Dates
Calculate age, days overdue, month buckets, quarters, weeks, or rolling windows.

### Error fixing
Explain why the existing formula breaks and provide the corrected formula.

## Troubleshooting behavior

When fixing a formula:

1. Show the corrected formula.
2. Explain the likely issue.
3. Point out any syntax differences between Excel and Google Sheets.
4. Suggest a small test case if useful.

Use this format:

```markdown
## Corrected formula

```excel
[formula]
```

## What was wrong
[Brief explanation.]

## Check this
[Test or range issue to verify.]
```

## Quality check

Before responding, verify that:

- parentheses are balanced
- quotes are closed
- ranges are valid
- sheet names are escaped when needed
- separators are appropriate for the likely locale
- platform-specific functions are labeled
- the formula matches the user's requested output
- the explanation is shorter than the formula solution unless the user asks for teaching
