# 🔥 Viral Content Intelligence Engine (VICE-AI)

> Autonomous AI system that analyzes 200+ daily trending topics, scores virality potential (0-100), and auto-generates multi-platform content packages — published daily at 07:00 AM with zero manual intervention.

**Live Dashboard:** [tama260.github.io/Viral-Intelligence-Content-Engine-VICE-AI](https://tama260.github.io/Viral-Intelligence-Content-Engine-VICE-AI/)

---

## What This System Does

Every morning at 07:00 AM WIB, this pipeline runs automatically:

1. **Scans** 200+ trending topics from Reddit (6 subreddits) and HackerNews
2. **Scores** each topic with AI virality analysis (0-100) including regional relevance
3. **Generates** full content packages — headline, Twitter thread, LinkedIn post, Telegram post, AI visual
4. **Publishes** top 3 content packages to Telegram channel with AI-generated images
5. **Logs** all data to Google Sheets for analytics
6. **Updates** live public dashboard automatically

---

## System Architecture

[Reddit RSS + HackerNews API]
↓
[fetch_reddit_trends] — collect 200+ topics
↓
[ai_virality_scorer] — Groq LLaMA 3.3 70B scores each topic 0-100
↓
[generate_viral_content] — full content package per top 3 topic
↓
[save_to_sheets] — log to Google Sheets database
↓
[publish_telegram] — auto-publish to Telegram channel
↓
[GitHub Pages Dashboard] — live public scoreboard

---

## Live Dashboard Features

- **Real-time Virality Scoreboard** — all topics ranked by score with visual bar
- **Filter by Potential** — EXPLOSIVE / HIGH / MEDIUM tabs
- **Indonesia Filter** — topics relevant to Indonesian audience highlighted
- **Region Tags** — shows which countries each topic is viral in
- **Top 3 Content Preview** — generated content with AI visuals
- **Auto-refresh** every 5 minutes

---

## Tech Stack

| Category | Tools |
|---|---|
| Workflow Automation | Pipedream |
| AI & LLM | Groq AI (LLaMA 3.3 70B) |
| Data Sources | Reddit RSS, HackerNews API |
| Image Generation | Pollinations.ai |
| Database | Google Sheets API |
| Publishing | Telegram Bot API |
| Dashboard | GitHub Pages (Vanilla JS) |
| Auth | Google Service Account, JWT |

**Cost: $0/month** — 100% free tier infrastructure

---

## Key Metrics

- **200+** trending topics analyzed daily
- **<2 sec** AI response time via Groq
- **0** manual intervention required
- **3** content packages generated per day
- **163** Indonesia-relevant topics detected (sample run)
- **95/100** highest virality score recorded

---

## Sample Output

**Topic:** An OpenAI model has disproved a central conjecture in discrete geometry
**Virality Score:** 95/100 — EXPLOSIVE
**Regions:** Global | USA | Indonesia | UK

**Generated Headline:** OpenAI Just Broke Mathematics — Here Is What It Means

**Twitter Thread:**

1/ OpenAI just did something nobody expected — their AI disproved a 50-year-old math conjecture 🧵
2/ Discrete geometry studies shapes, points, and distances. This conjecture was considered unsolvable by humans.
3/ The AI found a counterexample that mathematicians missed for decades. This changes how we view AI capabilities.
4/ Practical impact: AI can now assist in pure mathematics research, not just applied problems.
5/ We are witnessing the beginning of AI as a scientific discovery tool. Follow for daily AI trend analysis. #AI #Math #OpenAI

---

## Project Structure

├── Pipedream Workflows
│   ├── WF1 - Trend Collector (Daily 07:00 AM)
│   │   ├── fetch_reddit_trends
│   │   ├── ai_virality_scorer
│   │   ├── generate_viral_content
│   │   ├── save_to_sheets
│   │   └── publish_telegram
├── docs/
│   └── index.html (Live Dashboard)
└── README.md

---

## Setup Guide

### Prerequisites
- Pipedream account (free)
- Groq AI account (free)
- Telegram Bot + Channel
- Google Cloud Service Account
- Google Sheets

### Environment Variables

GROQ_API_KEY                = gsk_xxxx
TELEGRAM_BOT_TOKEN          = xxxx:xxxx
TELEGRAM_CHAT_ID            = -100xxxxxxx
VIRAL_SHEETS_ID             = spreadsheet_id
GOOGLE_SERVICE_ACCOUNT_JSON = {...}

### Deployment
1. Clone this repo
2. Set environment variables in Pipedream
3. Deploy workflow
4. Set trigger to Daily 07:00 AM Asia/Jakarta
5. Dashboard auto-updates after first run

---

## Author

**Daffa Novendra Aditama**
AI Automation Engineer | Banten, Indonesia

[![LinkedIn](https://img.shields.io/badge/LinkedIn-daffanovendraaditama-blue)](https://linkedin.com/in/daffanovendraaditama)
[![GitHub](https://img.shields.io/badge/GitHub-Tama260-black)](https://github.com/Tama260)

---

*Built with Groq AI · Pipedream · Pollinations.ai · GitHub Pages*
