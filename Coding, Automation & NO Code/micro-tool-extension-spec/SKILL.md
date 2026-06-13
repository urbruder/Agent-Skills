---
name: micro-tool-extension-spec
description: turn a software, automation, no-code, browser extension, internal tool, micro-saas, script, dashboard, or productivity idea into a build-ready product specification. use when the user has an idea and needs scope, user stories, requirements, data model, screens, workflows, api needs, edge cases, acceptance criteria, implementation plan, and handoff-ready details for a developer or ai coding agent.
---

# Micro-Tool / Extension Spec

Convert a rough tool idea into a build-ready spec that a developer or AI coding agent can implement.

## Core workflow

1. Identify user, problem, job-to-be-done, platform, inputs, outputs, integrations, and success criteria.
2. Define MVP scope and explicitly exclude non-MVP features.
3. Specify user flows, screens, data model, API/integration needs, permissions, edge cases, and acceptance criteria.
4. Recommend architecture and implementation approach at the right level of detail.
5. Include a build plan with milestones and test cases.

If essential details are missing, make practical assumptions and label them briefly. Ask for clarification only when guessing would make the output unusable, unsafe, or misleading.

Use `references/micro-tool-extension-spec-framework.md` for deeper patterns, checklists, templates, and troubleshooting.

## Default output

```markdown
# Build-Ready Spec: [Tool Name]

## One-Line Summary
[What it does]

## Problem
[Problem]

## Target Users
- [User]

## MVP Scope
### In Scope
- [Feature]
### Out of Scope
- [Feature]

## Core User Flow
1. [Step]
2. [Step]
3. [Step]

## Requirements
### Functional
- [Requirement]
### Non-Functional
- [Requirement]

## Data Model
| Entity | Fields | Notes |
|---|---|---|

## Screens / UX
- [Screen]
- [Screen]

## Integrations / APIs
- [Integration]

## Edge Cases
- [Case]

## Acceptance Criteria
- [Criterion]

## Build Plan
1. [Milestone]
2. [Milestone]
3. [Milestone]
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
