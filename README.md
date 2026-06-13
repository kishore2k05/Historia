# 🏛️ Historia — Japanese History Expert App

A locally-running AI-powered Japanese history expert app built with **Llama 3.2**, **RAG (Retrieval-Augmented Generation)**, and a plain HTML/CSS/JS frontend. Runs entirely on your machine — no cloud API costs.

---

## 🧠 What It Does

- Answers Japanese history questions grounded in curated historical documents
- Uses RAG to retrieve relevant context before generating answers
- Covers Feudal Japan, Shogunate, Samurai, Meiji Restoration, and more
- Stays on-topic with expert-system guardrails via system prompting

---

## 🏗️ Architecture

```
HTML/CSS/JS (Frontend)
        ↓
Node.js / Express (API Gateway + Chat History)
        ↓
Python FastAPI (RAG Engine)
        ↓
LangChain + ChromaDB (Vector Store)
        ↓
Ollama — Llama 3.2 + nomic-embed-text (Local LLM)
```

---

## 📁 Project Structure

```
historia/
├── frontend/
│   ├── index.html        # Home page
│   ├── topics.html       # Japanese history topics
│   ├── ask.html          # Ask the Expert (AI Q&A)
│   ├── about.html        # About the app
│   ├── style.css         # Shared styles
│   ├── script.js         # Shared JS (nav, API calls)
│   └── images/           # Local images (samurai, castles etc.)
├── backend/              # Node.js + Express API gateway
├── rag-engine/           # Python FastAPI + LangChain RAG pipeline
├── data/
│   └── history-docs/     # History PDFs and texts (gitignored)
├── docs/                 # Architecture diagrams, notes
├── docker-compose.yml
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites
- [Ollama](https://ollama.com) installed (Apple Silicon native)
- Node.js 18+
- Python 3.11+
- Docker (optional)

### 1. Pull models via Ollama
```bash
ollama pull llama3.2
ollama pull nomic-embed-text
```

### 2. Start the RAG engine
```bash
cd rag-engine
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --reload --port 8000
```

### 3. Start the backend
```bash
cd backend
npm install
npm run dev
```

### 4. Open the frontend
```bash
# Just open index.html in your browser
open frontend/index.html
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, Vanilla JS |
| Backend | Node.js, Express, MySQL, Prisma |
| RAG Engine | Python, FastAPI, LangChain, ChromaDB |
| LLM | Llama 3.2 via Ollama |
| Embeddings | nomic-embed-text via Ollama |
| Container | Docker, Docker Compose |

---

## 📄 Pages

| Page | Description |
|---|---|
| `index.html` | Home — hero section + topic preview cards |
| `topics.html` | Full grid of Japanese history topics |
| `ask.html` | Ask the Expert — AI powered Q&A |
| `about.html` | About the app and how it works |

---

## 👤 Author

**Kishore G** — B.Tech CSE, SRM Institute of Science and Technology  
GitHub: [@kishore2k05](https://github.com/kishore2k05)