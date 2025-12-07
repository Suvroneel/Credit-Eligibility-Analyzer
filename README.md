# Suvroneel Nathak — The Loan Eligibility Engine


This repository contains my submission for the **SDE Intern (Backend)** assignment.  
It showcases a backend pipeline that ingests user CSVs, discovers relevant loan products, 
matches users to eligible loans based on rules, and triggers notifications.

The solution is implemented using AWS services, n8n automations, Docker, and a structured SQL schema.

---

## 📁 Repository Structure

- `lambdas/` – AWS Lambda functions (presigned URL generator, S3 CSV processor)
- `infra/` – Serverless Framework configuration and infra notes
- `n8n/` – n8n workflow JSONs + docker-compose setup
- `ui/` – Minimal UI for uploading CSV files
- `sql/` – Database schema, seed queries, helper queries
- `docs/` – Architecture diagram, design decisions, and deployment notes

---

## 🏗️ Architecture Diagram

![Architecture Diagram](docs/Architecture.jpg)

---

## 🚀 Quick Start (Local Development)

1. **Start PostgreSQL locally:**
   ```bash
   docker run --name loan-postgres \
     -e POSTGRES_PASSWORD=postgres \
     -e POSTGRES_DB=loan_db \
     -p 5432:5432 \
     -d postgres:15

