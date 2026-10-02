# Templates

Placeholder versions of the four pack artefacts. The filled sample (Northline Supplies) is at the repo root.

1. Copy this folder and [`../pack.config.json`](../pack.config.json) into the new job.
2. Edit `pack.config.json` with the client's values.
3. Replace every `{{TOKEN}}` with the matching config value: `business_name` → `{{BUSINESS_NAME}}`. Lists go in one `- ` item per line.
4. Write the `<FILL: ...>` rows for the job.
5. `grep -rn --exclude=README.md -e '{{' -e '<FILL' .` should print nothing before go-live.

| Template | Tokens used |
| --- | --- |
| [prompts/faq-support-agent.md](prompts/faq-support-agent.md) | BUSINESS_NAME, BUSINESS_LEGAL_NAME, BUSINESS_DESCRIPTION, WORKFLOW, WORKFLOW_SCOPE, CHANNELS, LOOKUP_FIELDS, LOOKUP_SHORT, RECORD_ID_FORMAT, RECORD_ID_EXAMPLE, SAMPLE_RECORDS, DESK_HOURS, REFUSE_LIST |
| [escalate-hard-stop-map.md](escalate-hard-stop-map.md) | BUSINESS_NAME, WORKFLOW, WORKFLOW_SCOPE, LOOKUP_SHORT, HANDOFF_CHANNEL, DESK_HOURS, ESCALATION_CONTACTS, REFUSE_LIST |
| [test-checklist.md](test-checklist.md) | BUSINESS_NAME, BUSINESS_SHORT_NAME, WORKFLOW, LOOKUP_FIELDS, RECORD_ID_EXAMPLE, DESK_HOURS, REFUSE_LIST |
| [seating-steps.md](seating-steps.md) | BUSINESS_NAME, WORKFLOW, CHANNELS, HANDOFF_CHANNEL, DESK_HOURS, ESCALATION_CONTACTS |
