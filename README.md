# 🧠 AI Commit Whisperer  
> *AI-Powered Commit Summarizer & Productivity Tracker for Agile Teams*

---

## 🌟 Overview
**AI Commit Whisperer** automatically analyzes your Git commits, summarizes them into readable progress reports, and visualizes your team’s coding activity — helping project managers and developers quickly understand *what actually changed* across repositories.

No more scrolling through endless commit logs — get weekly summaries like:
> “✅ Login module completed, ⚙️ Bug fixes in payment flow, 🧪 Added 3 new test cases.”

---

## 🧩 Features

### 🚀 Core
- **AI-Powered Commit Summarization**  
  Uses NLP models (Hugging Face Transformers) to summarize commit messages into human-readable updates.

- **GitHub API Integration**  
  Fetch commits from any public or private repository using a secure personal access token.

- **Smart Insights**  
  Automatically groups commits into meaningful daily/weekly summaries.

---

### 🎨 Frontend Dashboard (Streamlit)
- ✨ Minimal, light-themed modern UI  
- 🔒 Sidebar for secure GitHub token input  
- 💡 Real-time commit summary display  
- 📊 Interactive productivity charts (Plotly)  
- 📄 Export reports as **PDF** or **Markdown**  
- 🎬 Smooth animations with Lottie for a polished experience  

---

### ⚙️ Backend (FastAPI)
- Handles commit fetching, caching, and summarization  
- Modular codebase — easy to extend for more analytics  
- Graceful error handling for API and network issues  

---

### 🧰 Utilities
| Module | Purpose |
|---------|----------|
| `utils/report_gen.py` | Generate PDF and Markdown reports safely (emoji + encoding safe) |
| `utils/viz.py` | Plotly-based commit activity and contributor visualizations |
| `data/cache.db` | SQLite cache for recent commits (auto-created) |

---

## 🔑 Setup Guide

### 1️⃣ Clone the Repository
git clone https://github.com/your-username/ai-commit-whisperer.git
cd ai-commit-whisperer

### 2️⃣ Set Up Backend
cd backend
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
Run FastAPI server:
uvicorn main:app --reload

### 3️⃣ Set Up Frontend
cd ../frontend
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
streamlit run app.py

---

## 🔐 GitHub Token Setup

To access your private repositories, create a **Personal Access Token (PAT)**:

### 🧭 Steps
1. Go to **GitHub → Settings → Developer Settings → Personal Access Tokens → Fine-grained Tokens**  
2. Click **Generate new token**
3. Enable the following permissions:

| Scope | Access |
|--------|--------|
| **Repository contents** | ✅ Read |
| **Metadata** | ✅ Read |
| **Commits** | ✅ Read |

4. Copy the generated token.

### ⚙️ Add it to Your Environment
Create a `.env` file in your project root and add:
GITHUB_TOKEN=ghp_yourTokenHere
Or simply paste it into the Streamlit sidebar when prompted during app runtime.

---

## 📄 Export Options

You can download your summarized commit reports in multiple formats:

| Format | Description |
|--------|--------------|
| **Markdown (.md)** | Lightweight, easy to share, and editable summary |
| **PDF (.pdf)** | Professionally styled, printable report (emoji-safe, wrapped text) |

💡 **Both formats are generated through the** `utils/report_gen.py` **module.**

---

## 🧠 Tech Stack

| Layer | Technologies Used |
|--------|-------------------|
| **Frontend** | Streamlit, Plotly, Lottie Animations |
| **Backend** | FastAPI, PyGithub, Hugging Face Transformers |
| **Data Layer** | GitHub REST API, SQLite |
| **Utilities** | FPDF, dotenv, YAML |

---

## 📈 Example Output

### 🗓️ This Week’s Summary

- 🚀 Login module completed  
- 🧩 Integrated payment validation  
- 🧪 Added 3 new unit tests  
- 🐛 Fixed checkout bug  

### 📊 Commit Frequency

> **12 commits this week | 3 contributors | 5 feature updates**

---

## 🛠️ Future Enhancements

- 🔔 **Slack / Teams integration** for automatic daily summaries  
- 📅 **Trend analysis** across multiple repositories  
- 🧠 **AI-driven productivity insights** per contributor  
- 🧩 **GitLab & Bitbucket support** for wider integration  

---

