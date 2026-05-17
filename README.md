# CareerPulse AI - n8n Job Automation

CareerPulse AI is an AI-powered job tracking and automation workflow built with n8n. It automatically collects job listings from external APIs, filters relevant roles, scores them using an LLM, stores results in Supabase, and sends real-time Telegram and email alerts.

## Features
- Fetches job listings from external APIs
- Normalizes job data into a consistent format
- Filters jobs based on role relevance and keywords
- Uses AI scoring to evaluate job fit
- Checks Supabase to avoid duplicate records
- Stores new job listings in Supabase
- Sends Telegram and email alerts for relevant jobs

## Tech Stack
- n8n
- Supabase / PostgreSQL
- Groq API / LLM scoring
- Telegram Bot API
- Gmail integration
- Docker for local n8n setup

## Workflow Steps
1. Schedule Trigger
2. Fetch jobs from APIs
3. Normalize job data
4. Filter relevant jobs
5. Enrich job descriptions
6. Score jobs using AI
7. Check existing rows in Supabase
8. Insert new jobs
9. Send Telegram and email alerts

## How It Works
The workflow runs on a schedule and collects job listings from selected APIs. Each job is cleaned, normalized, and filtered before being passed to an LLM for relevance scoring. If the job is new and meets the required score, it is saved in Supabase and sent as a notification through Telegram and email.

## Setup
1. Import the workflow JSON into n8n
2. Add required credentials for Supabase, Groq, Telegram, and Gmail
3. Create a `.env` file using `.env.example`
4. Configure API keys and database connection values
5. Run n8n locally using Docker
6. Enable the workflow

## Environment Variables
```env
GROQ_API_KEY=your_groq_api_key
SUPABASE_URL=your_supabase_url
SUPABASE_KEY=your_supabase_key
TELEGRAM_BOT_TOKEN=your_telegram_bot_token
TELEGRAM_CHAT_ID=your_chat_id
