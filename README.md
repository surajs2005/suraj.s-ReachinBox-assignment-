# ReachInbox.AI: React Project

---

ReachInbox Onebox — AI-Powered Email Workspace

A feature-rich Onebox for Emails built with React, TypeScript, Node.js, and Elasticsearch.
This project synchronizes multiple IMAP accounts in real-time, enables full-text search, classifies emails with AI, integrates Slack/webhooks, and suggests intelligent replies using RAG (Retrieval-Augmented Generation).

🚀 Features

Real-Time IMAP Sync — Persistent IMAP connections for instant updates (no cron jobs).

Searchable Storage — Elasticsearch indexing with folder/account filters.

AI Email Categorization — Labels emails as Interested, Meeting Booked, Not Interested, Spam, or Out of Office.

Slack & Webhook Integration — Notifies when “Interested” leads arrive.

Frontend Interface — Clean UI with React, TypeScript, and Tailwind CSS.

AI-Powered Replies (RAG) — Suggests personalized responses based on email context.

🛠️ Tech Stack

Frontend: React, TypeScript, Vite, Tailwind CSS
Backend: Node.js, Express, TypeScript
Database: Elasticsearch (Docker)
Integrations: Slack, Webhook.site, OpenAI API, Pinecone (for RAG)
Deployment: Vercel (frontend), Render/Heroku (backend)

⚙️ Installation
Clone Repository
git clone https://github.com/your-username/reachinbox-onebox.git
cd reachinbox-onebox

Backend Setup
npm install
cp .env.example .env
npm run dev

Environment Variables (.env)
IMAP_USER_1=
IMAP_PASS_1=
IMAP_USER_2=
IMAP_PASS_2=
ELASTIC_URL=http://localhost:9200
OPENAI_KEY=
SLACK_WEBHOOK=
WEBHOOK_URL=
PINECONE_KEY=

Start Elasticsearch (Docker)
docker compose up -d

Frontend Setup
cd frontend
npm install
npm run dev

🔍 API Overview
Endpoint	Method	Description
/api/emails	GET	Fetch all synced emails
/api/search	POST	Full-text search using Elasticsearch
/api/categorize	POST	Classify email via AI
/api/reply	POST	Generate AI-suggested reply
🧠 AI Workflow

Fetch email → Categorize via LLM (GPT-4o-mini).

Store categorized mail → Index into Elasticsearch.

On “Interested” → Send Slack alert + Webhook trigger.

RAG pipeline → Suggest contextual replies using Pinecone vectors.

🖥️ Frontend Preview

Unified inbox view

Folder/account filter dropdown

AI category tags

Smart reply modal

## Overview

api documentation
https://documenter.getpostman.com/view/30630244/2sA2rCTMKr#433eb613-e405-4239-9e2d-f20485b31b27

---





now open in browser 
   http://localhost:5173/
