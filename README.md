# 🤖 Agentic AI — Student Time Management & Study Planner

> **Autonomous AI productivity agent powered by dual-LLM capabilities (Google Gemini API & local Ollama) with SQLite progress tracking.**

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python&logoColor=white)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-000000?logo=flask&logoColor=white)](https://flask.palletsprojects.com)
[![Gemini API](https://img.shields.io/badge/Google_Gemini_API-4285F4?logo=google&logoColor=white)](https://ai.google.dev)
[![Ollama](https://img.shields.io/badge/Ollama-Local_LLMs-black)](https://ollama.ai)
[![SQLite](https://img.shields.io/badge/SQLite-003B57?logo=sqlite&logoColor=white)](https://sqlite.org)

---

## Problem Statement

Students frequently struggle with unstructured academic workloads, missed deadlines, and suboptimal study schedules. This agent autonomously manages task prioritisation, generates personalised study plans, and tracks academic progress using AI reasoning.

## Architecture

```
┌──────────────────────────────────────────────────────┐
│                  Flask Web App                       │
│  ┌─────────────────┐    ┌──────────────────────┐    │
│  │  Gemini API     │    │  Ollama (local LLM)  │    │
│  │  (cloud, rich   │    │  (offline, private)  │    │
│  │   scheduling)   │    │  Llama 3 / Mistral   │    │
│  └────────┬────────┘    └──────────┬───────────┘    │
│           └──────────┬─────────────┘                │
│                ┌─────▼──────┐                       │
│                │  LLM Router│                       │
│                └─────┬──────┘                       │
│          ┌───────────▼──────────┐                   │
│          │   SQLite DB          │                   │
│          │  (tasks · deadlines  │                   │
│          │   · progress logs)   │                   │
│          └──────────────────────┘                   │
└──────────────────────────────────────────────────────┘
```

## Key Features

- **Dual-LLM Engine:** Google Gemini API for cloud-based scheduling strategies + local Ollama for private, offline assistance.
- **Task Prioritisation:** Intelligent deadline-aware scheduling with priority scoring.
- **Progress Tracking:** SQLite-backed task state machine with study session logging.
- **Interactive Dashboard:** Visual analytics on study hours, completion rates, and overdue tasks.

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Python · Flask |
| LLM (Cloud) | Google Gemini API |
| LLM (Local) | Ollama (Llama 3 / Mistral) |
| Database | SQLite |
| Frontend | HTML5 / CSS3 |

## Quickstart

```bash
# 1. Clone
git clone https://github.com/keerthi19hub/Agentic_AI_Project.git
cd Agentic_AI_Project

# 2. Install dependencies
pip install -r requirements.txt

# 3. Set your Gemini API key
export GEMINI_API_KEY="your_key_here"

# 4. Ensure Ollama is running
ollama serve

# 5. Run the application
python app.py
# Open http://localhost:5000
```

## Authors

- **Keerthi N** — LLM integration layer, database schema, web application workflow
- **Pragathi BR** — Collaborative project contributor

*Alliance University, BCA — 2026*

---

Released under the [MIT License](https://opensource.org/licenses/MIT).
