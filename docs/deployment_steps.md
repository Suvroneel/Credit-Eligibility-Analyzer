# Deployment Steps

## 1. Setup GitHub
- Create a private repository and push all files.
- Invite collaborators: saurabh@clickpe.ai, harsh.srivastav@clickpe.ai

## 2. Create Postgres Database
- Option 1: AWS RDS (free-tier)
  - DB Name: loan_db
  - Username/Password: your choice
  - Update `.env` with host, username, password, database name
- Option 2: Local Postgres for testing
  - `docker run --name loan-postgres -e POSTGRES_PASSWORD=postgres -e POSTGRES_DB=loan_db -p 5432:5432 -d postgres:15`

## 3. Apply SQL schema
```bash
psql -h <host> -U <user> -d loan_db -f sql/create_tables.sql
