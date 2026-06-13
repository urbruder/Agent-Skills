---
name: regex-generator-explainer
description: generate, explain, test, and debug regular expressions from plain-language pattern descriptions for javascript, python, php, ruby, grep, google sheets, excel, looker studio, sql dialects, and text editors. use when the user needs matching, extraction, validation, replacement, splitting, negative cases, capture groups, flags, lookarounds, or a clear explanation of an existing regex.
---

# Regex Generator & Explainer

Turn plain-language pattern needs into tested regex with examples, explanation, and edge cases.

## Core workflow

1. Identify the target engine or platform because regex syntax varies.
2. Clarify match versus extract versus replace versus validate.
3. Generate a regex with flags and capture groups as needed.
4. Provide positive and negative test cases.
5. Explain the regex piece by piece.
6. Include replacement syntax if the user wants substitution.

If essential details are missing, make practical assumptions and label them briefly. Ask for clarification only when guessing would make the output unusable, unsafe, or misleading.

Use `references/regex-generator-explainer-framework.md` for deeper patterns, checklists, templates, and troubleshooting.

## Default output

```markdown
## Regex

```regex
[pattern]
```

## Engine / Platform
[JavaScript / Python / Google Sheets / etc.]

## What it matches
[Plain-English summary]

## Test Cases
| Text | Should match? | Captures |
|---|---:|---|

## Explanation
- `[part]` = [meaning]
- `[part]` = [meaning]

## Notes
- Flags:
- Limitations:
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
