---
name: zapier-make-workflow-designer
description: design step-by-step no-code and low-code automations for zapier, make, n8n, airtable automations, google workspace, slack, crm, ecommerce, forms, spreadsheets, email, and webhook workflows. use when the user wants to connect tools, map triggers and actions, transform data, add filters, routers, error handling, deduplication, approvals, or handoff steps so recurring busywork runs automatically.
---

# Zapier/Make Workflow Designer

Map a business process into a reliable automation workflow for tools like Zapier, Make, n8n, Airtable, Slack, Google Sheets, CRMs, ecommerce platforms, and email systems.

## Core workflow

1. Identify the trigger, source app, destination app, data objects, and business outcome.
2. Map every step from trigger to final action.
3. Add filters, branching, formatting, deduplication, retries, and error handling where useful.
4. Specify field mappings and test cases.
5. Call out required permissions, API keys, webhooks, or paid-plan features.
6. Recommend Zapier, Make, n8n, or native automation based on complexity.

If essential details are missing, make practical assumptions and label them briefly. Ask for clarification only when guessing would make the output unusable, unsafe, or misleading.

Use `references/zapier-make-workflow-designer-framework.md` for deeper patterns, checklists, templates, and troubleshooting.

## Default output

```markdown
## Automation Summary
- Goal:
- Recommended platform:
- Trigger:
- Apps involved:
- Data moved:
- Risk level:

## Step-by-Step Workflow
1. **Trigger:** [app/event]
   - Inputs:
   - Conditions:
2. **Action:** [app/action]
   - Field mapping:
   - Notes:
3. **Filter/Router:** [logic]
4. **Action:** [app/action]

## Field Mapping
| Source field | Destination field | Transform/formatting |
|---|---|---|

## Error Handling
- Duplicate prevention:
- Missing data:
- Failed action:
- Notification:

## Test Plan
1. [Test]
2. [Test]
3. [Test]

## Build Notes
- Permissions needed:
- Paid features:
- Risks:
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
