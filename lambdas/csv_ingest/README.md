# Lambdas

Contains backend AWS Lambda functions.

## Folder structure
- `csv_ingest/handler.py` — triggered by S3 when user CSV uploaded; parses CSV and inserts into Postgres; triggers n8n webhook for matching
- `presign_url_generator/handler.py` — generates presigned URL for S3 CSV upload

## Setup
1. Install dependencies (psycopg2 for Postgres Lambda)
2. Make sure environment variables from `.env` are available
3. Deploy via Serverless: `serverless deploy`
