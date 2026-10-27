# 🤖 Agentic AI Architecture — Autonomous Multi-Agent Workflow & Task Orchestration

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=4C1D95,6D28D9,A855F7&height=220&section=header&text=Agentic%20AI%20Architecture&fontSize=42&fontColor=ffffff&fontAlignY=38&desc=Autonomous%20Multi-Agent%20Workflow%20%26%20Task%20Orchestration&descSize=18&descAlignY=60&descAlign=50" width="100%" alt="Agentic AI Header Banner" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Architecture-Dual--LLM%20Agentic-4C1D95?style=for-the-badge" alt="Dual LLM" />
  <img src="https://img.shields.io/badge/Cloud%20LLM-Google%20Gemini%20API-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Gemini API" />
  <img src="https://img.shields.io/badge/Local%20LLM-Ollama%20(Offline)-000000?style=for-the-badge" alt="Ollama" />
  <img src="https://img.shields.io/badge/Backend-Python%20%2F%20Flask-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python Flask" />
  <img src="https://img.shields.io/badge/Storage-SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License" />
</p>

---

## 📌 Table of Contents

- [📖 Executive Summary](#-executive-summary)
- [🎯 Real-World Problem & Solution](#-real-world-problem--solution)
- [✨ Key Features & Capabilities](#-key-features--capabilities)
- [🏗️ Multi-Agent Architecture & Dual-Engine Workflow](#️-multi-agent-architecture--dual-engine-workflow)
- [🛠️ Tech Stack Matrix](#️-tech-stack-matrix)
- [⚙️ Reproducible Quickstart & Setup](#️-reproducible-quickstart--setup)
- [📁 Project Structure](#-project-structure)
- [🎥 Video Demonstration & Documentation](#-video-demonstration--documentation)
- [👩‍💻 Authors & Academic Context](#-authors--academic-context)

---

## 📖 Executive Summary

**Agentic AI: Student Time Management Agent** is an autonomous multi-model agentic productivity system that synthesizes dynamic schedule optimization, task decomposition, and academic deadline tracking. Utilizing an innovative **Dual-Engine LLM router**—combining cloud-based **Google Gemini API** for strategic macro-planning with local **Ollama** models for privacy-preserving offline assistance—the agent acts as an autonomous tutor and workflow coordinator.

---

## 🎯 Real-World Problem & Solution

- **The Problem:** University students face unstructured workloads, competing deadlines across multiple subjects, cognitive fatigue, and difficulty estimating task effort. Static calendar tools lack the intelligence to dynamically replan around unexpected delays or provide adaptive study pacing.
- **The Solution:** An autonomous Agentic AI that receives raw course syllabi and task inputs, decomposes assignments into prioritized actionable sub-tasks, estimates completion bandwidth, and tracks progress via an interactive SQLite dashboard.

---

## ✨ Key Features & Capabilities

- **🧠 Dual-LLM Routing Layer:** High-reasoning strategic planning via **Google Gemini API** combined with air-gapped local inference via **Ollama (Llama 3 / Mistral)** for confidential local tasks.
- **📋 Autonomous Task Decomposition:** Converts complex project prompts into sequenced milestones with time estimates.
- **⏱️ Dynamic Deadline Prioritization:** Priority-scoring heuristic adjusting schedules based on submission urgency and remaining study capacity.
- **📊 Interactive Progress Dashboard:** Flask-powered web interface displaying completed study intervals, active queues, and overdue task alerts.
- **📑 Research Dossier & Architecture Docs:** Comprehensive academic technical documentation detailing agentic design patterns.

---

## 🏗️ Multi-Agent Architecture & Dual-Engine Workflow

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                     Agentic AI Workflow Architecture                        │
└─────────────────────────────────────────────────────────────────────────────┘
                                       │
                                       ▼
                     ┌───────────────────────────────────┐
                     │     User Academic Task Input      │
                     │  (Assignment, Exam, Target Date)  │
                     └─────────────────┬─────────────────┘
                                       │
                                       ▼
                     ┌───────────────────────────────────┐
                     │        Agentic Task Router        │
                     └─────────┬───────────────────┬─────┘
                               │                   │
         [Cloud Strategic]     ▼                   ▼     [Offline / Private]
    ┌─────────────────────────────┐     ┌─────────────────────────────┐
    │     Google Gemini API       │     │     Local Ollama Engine     │
    │  - Macro study scheduling   │     │  - Llama 3 / Mistral        │
    │  - Multi-week decomposition │     │  - Offline local assistance │
    └──────────────┬──────────────┘     └──────────────┬──────────────┘
                   │                                   │
                   └─────────────────┬─────────────────┘
                                     │
                                     ▼
                     ┌───────────────────────────────────┐
                     │    Persistence & State Machine    │
                     │        (SQLite Task Store)        │
                     └─────────────────┬─────────────────┘
                                     │
                                     ▼
                     ┌───────────────────────────────────┐
                     │  Interactive Web UI / Dashboard   │
                     │     (Flask, HTML5, CSS3, JS)      │
                     └───────────────────────────────────┘
```

---

## 🛠️ Tech Stack Matrix

| Domain | Technology | Implementation Details |
| :--- | :--- | :--- |
| **Agentic Framework** | Python 3.10+, Custom Agent Logic | Intent classification, prompt template routing, state management |
| **Cloud LLM Engine** | Google Gemini API | High-dimensional reasoning, syllabus synthesis, multi-step planning |
| **Local LLM Engine** | Ollama (`llama3`, `mistral`) | Zero-latency private local completion without cloud dependencies |
| **Web Application** | Flask, Jinja2, HTML5, CSS3 | Real-time task board, session logs, responsive student portal |
| **Data Persistence** | SQLite | Normalized relational schema tracking task states, progress, deadlines |

---

## ⚙️ Reproducible Quickstart & Setup

### Prerequisites
- Python 3.10 or newer
- (Optional for cloud) Google Gemini API Key
- (Optional for offline) [Ollama installed](https://ollama.ai) with `ollama pull llama3`

### 1. Clone the Repository
```bash
git clone https://github.com/keerthi19hub/Agentic_AI_Project.git
cd Agentic_AI_Project
```

### 2. Set Up Virtual Environment & Dependencies
```bash
python -m venv venv
venv\Scripts\activate  # On Linux/macOS: source venv/bin/activate
pip install -r requirements.txt
```

### 3. Configure Environment Variables
```bash
# Windows
set GEMINI_API_KEY="your_api_key_here"

# Linux / macOS
export GEMINI_API_KEY="your_api_key_here"
```

### 4. Run the Agent Application
```bash
cd Time_Management_Agent
python app.py
```
Open `http://localhost:5000` in your web browser.

---

## 📁 Project Structure

```text
Agentic_AI_Project/
├── Time_Management_Agent/      # Core Flask web application & agent logic
│   ├── app.py                  # Web application routes and agent invocation
│   ├── agent_core.py           # LLM prompt routing (Gemini + Ollama)
│   ├── templates/              # Student dashboard & task management views
│   └── static/                 # Stylesheets and visual assets
├── Demo of prototype...mp4     # Complete recorded live walkthrough demonstration
├── Keerthi.N_Pragathi.BR_...pdf# Comprehensive technical research reports (Alliance University)
└── README.md                   # Technical system documentation
```

---

## 🎥 Video Demonstration & Documentation

The repository includes a recorded video demonstration (`Demo of prototype(Time management agent).mp4`) showcasing the agent parsing assignment requirements, generating dynamic study blocks, and dynamically adjusting to schedule disruptions.

---

## 👩‍💻 Authors & Academic Context

- **Keerthi N** — System architecture, LLM routing integration, database schema, and web application workflow.
- **Pragathi BR** — Collaborative research and academic co-author.

*Bachelor of Computer Applications (BCA) · Alliance University, Bengaluru*

---

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=4C1D95,6D28D9,A855F7&height=100&section=footer" width="100%" alt="Footer Banner" />
</p>
