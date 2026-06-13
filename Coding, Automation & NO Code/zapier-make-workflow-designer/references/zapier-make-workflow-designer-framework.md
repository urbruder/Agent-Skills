# Automation Workflow Framework

## Common workflow patterns

### Lead capture
Form submission -> validate fields -> enrich lead -> add CRM record -> notify sales -> send confirmation email.

### Order operations
New order -> check SKU/order value -> update sheet/ERP -> notify fulfillment -> tag customer -> send post-purchase flow.

### Content pipeline
New content idea -> create task -> assign owner -> generate draft record -> notify channel -> update calendar.

### Support routing
New ticket -> classify issue -> route by priority -> create task -> notify owner -> log resolution.

## Design checklist

- What starts the workflow?
- What data must move?
- What transformation is needed?
- What conditions change the path?
- What should happen if data is missing?
- How are duplicates prevented?
- Who gets notified?
- What confirms success?

## Platform guidance

Zapier is best for simple linear app-to-app automations.
Make is best for visual branching, routers, iterators, and complex data transforms.
n8n is best for self-hosted, technical, or API-heavy workflows.
Native automations are best when the workflow stays inside one platform.

## Reliability rules

Add logging for important workflows. Include failure alerts. Avoid silent failures. Use unique IDs to prevent duplicate records.
