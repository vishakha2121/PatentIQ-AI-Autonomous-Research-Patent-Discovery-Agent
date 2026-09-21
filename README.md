<div align="center">

# 🧠 PatentIQ

### AI Autonomous Research & Patent Discovery Agent

**"From Idea to Patent — Powered by AI."**

[![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.109-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev)
[![Gemini](https://img.shields.io/badge/Gemini-API-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev)
[![FAISS](https://img.shields.io/badge/FAISS-CPU-0467DF?style=for-the-badge)](https://github.com/facebookresearch/faiss)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

</div>

---

## 📖 Overview

**PatentIQ** is an AI-powered autonomous research agent that searches global patent databases, identifies unexplored innovation gaps, compares existing inventions, generates structured patent drafts, and estimates novelty scores using **Retrieval-Augmented Generation (RAG)**, **Knowledge Graphs**, and **Citation Network Analysis**.

Built for inventors, researchers, students, and startups — PatentIQ reduces patent research time from **weeks to minutes**.

---

## 🎯 Problem Statement

Inventors and startups spend weeks manually searching global patent databases to check if their idea is novel. Existing tools lack:

- ❌ Semantic search (they only do keyword matching)
- ❌ Innovation gap detection
- ❌ AI-powered comparison of inventions
- ❌ Automatic patent draft generation
- ❌ Quantified novelty scoring

**PatentIQ solves all five problems in one unified AI-powered platform.**

---

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| 🔍 **Global Patent Search** | Semantic search across USPTO, EPO, PatentsView & Google Patents |
| 🧩 **Innovation Gap Detection** | Finds unexplored areas using Knowledge Graph + LLM reasoning |
| ⚖️ **Patent Comparison** | Side-by-side AI-powered diff of two inventions |
| 📝 **AI Patent Draft Generator** | Auto-generates Title, Abstract, Claims & Description |
| 📊 **Novelty Score Estimator** | Quantified 0–100 novelty score for any idea |
| 🕸️ **Knowledge Graph Visualization** | Interactive citation network using NetworkX + react-force-graph |
| 📈 **Citation Network Analysis** | PageRank, community detection, trending tech areas |
| 🌙 **Modern Dark UI** | Glassmorphic design with smooth animations |

---

## 🏗️ System Architecture

---

## 🛠️ Tech Stack

### **Frontend**
| Technology | Purpose |
|------------|---------|
| React 18 + Vite | UI framework & build tool |
| TailwindCSS | Utility-first styling |
| shadcn/ui | Prebuilt accessible components |
| Framer Motion | Smooth animations |
| Recharts | Charts (novelty gauge, trends) |
| react-force-graph | Interactive knowledge graph |
| Axios | HTTP client |
| React Router | Client-side routing |

### **Backend**
| Technology | Purpose |
|------------|---------|
| Python 3.11 | Core language |
| FastAPI | Web framework |
| Uvicorn | ASGI server |
| Pydantic v2 | Data validation |
| SQLAlchemy | ORM |
| Alembic | DB migrations |
| Python-dotenv | Env management |

### **AI / ML**
| Technology | Purpose |
|------------|---------|
| Google Gemini API | LLM (gemini-1.5-flash) |
| Gemini Embeddings | Text embeddings (text-embedding-004) |
| FAISS-CPU | Vector similarity search |
| NetworkX | Knowledge graph construction |
| NumPy + Pandas | Data processing |

### **Database & Storage**
| Technology | Purpose |
|------------|---------|
| SQLite | Relational DB (practice-friendly) |
| FAISS Index | Persistent vector store |

### **External APIs**
| API | Purpose |
|-----|---------|
| PatentsView API | US patents (free) |
| EPO OPS | European patents |
| Google Patents | Global patents (scraper) |

---

## 📂 Project Structure


---

## 🚀 Getting Started

### **Prerequisites**

- Python 3.11+
- Node.js 18+
- Git
- Google Gemini API key → [Get one free](https://aistudio.google.com/app/apikey)

### **1️⃣ Clone the Repository**

```bash
git clone https://github.com/vishakha2121/PatentIQ-AI-Autonomous-Research-Patent-Discovery-Agent.git
cd PatentIQ-AI-Autonomous-Research-Patent-Discovery-Agent

cd backend

# Create virtual environment
python -m venv .venv

# Activate (Windows)
.venv\Scripts\activate

# Activate (Mac/Linux)
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Create .env file
cp .env.example .env
# Edit .env and add your GEMINI_API_KEY

# Run backend
uvicorn app.main:app --reload --port 8000

cd frontend

# Install dependencies
npm install

# Create .env file
cp .env.example .env
# Set VITE_API_URL=http://localhost:8000

# Run frontend
npm run dev