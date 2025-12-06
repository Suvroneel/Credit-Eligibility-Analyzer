# Suvroneel Nathak — The Loan Eligibility Engine

This repository is the submission for the SDE Intern (Backend) assignment.
It contains an AWS + n8n pipeline to ingest user CSVs, discover loan products,
match users to eligible products, and notify them via email.

## Contents
- `lambdas/` – Lambda functions (presign URL generator, S3 CSV processor)
- `infra/` – Serverless Framework files & infra notes
- `n8n/` – n8n docker-compose + workflow JSONs
- `ui/` – Minimal CSV upload UI
- `sql/` – DB schema and helpful queries
- `docs/` – architecture diagram, deployment notes, and design decisions

## Quick start (local / dev)
1. Create a Python virtualenv and install dependencies for local testing (if needed).
2. Start a local Postgres:
   ```bash
   docker run --name loan-postgres -e POSTGRES_PASSWORD=postgres -e POSTGRES_DB=loan_db -p 5432:5432 -d postgres:15
