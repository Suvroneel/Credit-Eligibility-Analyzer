# n8n Workflows

Contains placeholder JSONs for n8n workflows.

## Workflows
- `workflowA_crawler.json` — Loan Product Discovery (scheduled)
- `workflowB_matching.json` — User-Loan Matching (triggered by webhook)
- `workflowC_notifications.json` — User Notification emails

## Steps
1. Start n8n with Docker Compose (`docker-compose up -d`)
2. Import workflows into n8n UI
3. Configure credentials:
   - Postgres DB
   - AWS SES
   - Optional LLM API key
