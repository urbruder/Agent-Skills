---
name: web-scraper-builder
description: design authorized web scrapers and data extraction workflows that pull publicly accessible or user-owned page data into clean csv, spreadsheet, json, or database outputs. use when the user needs selectors, parsing logic, python code, playwright or requests examples, pagination handling, table extraction, cleanup rules, deduplication, scheduling, or scraper troubleshooting for legitimate data collection.
---

# Web Scraper Builder

Build ethical, authorized scraping workflows that extract data from pages into clean structured outputs.

## Core workflow

1. Identify the site/page type, data fields, access rights, output format, pagination, login needs, and update frequency.
2. Recommend the simplest safe method: copy table, CSV export, API, RSS, sitemap, requests/BeautifulSoup, Playwright, or browser automation.
3. Provide selectors, extraction logic, cleaning rules, and output schema.
4. Include rate limiting, robots.txt/terms considerations, and error handling.
5. For login, private, or sensitive data, require user authorization and avoid bypass guidance.

If essential details are missing, make practical assumptions and label them briefly. Ask for clarification only when guessing would make the output unusable, unsafe, or misleading.

Use `references/web-scraper-builder-framework.md` for deeper patterns, checklists, templates, and troubleshooting.

## Default output

```markdown
## Scraper Plan
- Source:
- Data fields:
- Output:
- Recommended method:
- Authorization/terms notes:

## Output Schema
| Field | Selector/source | Cleanup rule |
|---|---|---|

## Example Code

```python
[code]
```

## Pagination / Navigation
[Plan]

## Cleaning & Deduping
- [Rule]
- [Rule]

## Test Plan
1. Test on one page.
2. Validate field extraction.
3. Export sample CSV.
4. Run on small batch.
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
