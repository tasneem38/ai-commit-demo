# 🤖 AI Commit Whisperer  
*Smart GitHub Commit Summarizer and Insight Generator*

![App Demo Banner](assets/demo-screenshot.png)

---

[![Streamlit](https://img.shields.io/badge/Built%20with-Streamlit-FF4B4B?logo=streamlit&logoColor=white)](https://streamlit.io/)
[![FastAPI](https://img.shields.io/badge/Backend-FastAPI-009688?logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![Python](https://img.shields.io/badge/Made%20with-Python-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 🌟 Overview

**AI Commit Whisperer** is an AI-powered GitHub insights app that reads your repository’s commits and generates concise, intelligent summaries.  
Perfect for teams who want instant weekly or daily commit reports — no manual tracking needed.

---

## 🔐 GitHub Token Setup

To use this app, create a **Fine-grained Personal Access Token**:

| Setting | Permission |
|----------|-------------|
| Repository contents | ✅ Read |
| Metadata | ✅ Read |
| Commits | ✅ Read |

Then, add it to your `.env` file:
GITHUB_TOKEN=ghp_yourTokenHere
Or simply paste it into the Streamlit sidebar when prompted during app runtime.

---

## ⚙️ Setup & Run

### 🧭 Prerequisites

Before running the app, make sure you have:

- 🐍 **Python 3.9+**
- 💻 A **GitHub account** with at least one active repository
- ⚡ Installed **Streamlit** and **FastAPI**

---

### 💻 Installation

Clone the repository and install the required dependencies:

git clone https://github.com/tasneem38/ai-commit-demo.git
cd ai-commit-demo
pip install -r requirements.txt

---

## 🚀 Run the App

Start both the backend and frontend services:

# Start the backend server (FastAPI)
cd backend
uvicorn main:app --reload

# Start the frontend (Streamlit)
cd ../frontend
streamlit run app.py

---

## 📄 Export Options

Generate and download summarized commit reports in multiple formats:

| Format | Description |
|---------|-------------|
| 📝 **Markdown (.md)** | Lightweight, easy to share, and editable summary |
| 📄 **PDF (.pdf)** | Professionally styled, printable report *(emoji-safe, wrapped text)* |

💡 Both formats are generated via the `utils/report_gen.py` module.

---

## 🧠 Tech Stack

| Layer | Technologies Used |
|--------|------------------|
| 🎨 **Frontend** | Streamlit, Plotly, Lottie Animations |
| ⚙️ **Backend** | FastAPI, PyGithub, Hugging Face Transformers |
| 🗂️ **Data Layer** | GitHub REST API, SQLite |
| 🧰 **Utilities** | FPDF, dotenv, YAML |

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

| Feature | Description |
|----------|-------------|
| 🔔 **Slack / Teams integration** | Automatic daily summaries for teams |
| 📅 **Trend analysis** | View commit patterns across multiple repositories |
| 🧠 **AI-driven insights** | Contributor-level productivity and focus reports |
| 🧩 **GitLab & Bitbucket support** | Cross-platform commit summarization |

---

## 📸 Preview

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6c4b8425-7342-4f17-9f28-9c2b38b36f1b" />
<img width="1914" height="877" alt="image" src="https://github.com/user-attachments/assets/b4889f98-a1b1-4a86-ad49-a0b5915091af" />
<img width="1900" height="1063" alt="image" src="https://github.com/user-attachments/assets/1040f407-d161-401e-856f-9d30b55d27a2" />

---

## 🪪 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---
