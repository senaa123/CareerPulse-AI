# CareerPulse AI - n8n Job Automation

## What it does
This n8n workflow:
- fetches jobs from APIs
- normalizes and filters them
- scores jobs using AI
- checks Supabase for duplicates
- stores new jobs
- sends Telegram and email alerts

## Stack
- n8n
- Supabase
- Groq API
- Telegram
- Gmail

## Workflow Steps
1. Schedule Trigger
2. Fetch jobs
3. Normalize data
4. Filter jobs
5. Add description
6. AI score job
7. Check existing rows
8. Insert new jobs
9. Send alerts

## Setup
1. Import workflow JSON into n8n
2. Add credentials
3. Create `.env`
4. Connect Supabase
5. Enable workflow
