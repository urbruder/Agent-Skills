---
name: code-review-refactor
description: review, explain, document, and refactor messy code into cleaner, safer, more maintainable code across common programming languages and frameworks. use when the user provides code that works but is ugly, buggy, slow, duplicated, unclear, insecure, under-documented, or hard to extend, and wants a clean rewrite, review comments, tests, architecture suggestions, or documentation.
---

# Code Review & Refactor

Improve messy code through practical review, refactoring, documentation, and test suggestions.

## Core workflow

1. Identify language, framework, purpose, constraints, and desired level of refactor.
2. Read the code for correctness, clarity, security, performance, maintainability, and style.
3. Summarize the main issues before rewriting if helpful.
4. Provide a refactored version that preserves behavior unless asked to change behavior.
5. Add comments and documentation where useful but avoid over-commenting obvious code.
6. Suggest tests and migration steps.

If essential details are missing, make practical assumptions and label them briefly. Ask for clarification only when guessing would make the output unusable, unsafe, or misleading.

Use `references/code-review-refactor-framework.md` for deeper patterns, checklists, templates, and troubleshooting.

## Default output

```markdown
## Review Summary
- Correctness:
- Maintainability:
- Security:
- Performance:
- Biggest improvement:

## Refactored Code

```[language]
[code]
```

## What Changed
- [Change]
- [Change]

## Suggested Tests
- [Test]
- [Test]

## Risks / Follow-ups
- [Risk]
- [Follow-up]
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
