# 🏛️ Historia — History Expert Chatbot

A locally-running AI-powered history expert system built with **Llama 3.2**, **RAG (Retrieval-Augmented Generation)**, and a full-stack React + Node.js interface. Runs entirely on your machine — no cloud API costs.

---

## 🧠 What It Does

- Answers history questions grounded in curated historical documents
- Uses RAG to retrieve relevant context before generating answers
- Covers Ancient, Medieval, Modern, Political, Military, and Cultural history
- Stays on-topic with expert-system guardrails via system prompting

---

## 🏗️ Architecture

```
React + Vite (Frontend)
        ↓
Node.js / Express (API Gateway + Auth + Chat History)
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
├── frontend/         # React + Vite chat UI
├── backend/          # Node.js + Express API gateway
├── rag-engine/       # Python FastAPI + LangChain RAG pipeline
├── data/
│   └── history-docs/ # Your history PDFs and texts (gitignored)
├── docs/             # Architecture diagrams, notes
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

### 4. Start the frontend
```bash
cd frontend
npm install
npm run dev
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React, Vite, TailwindCSS |
| Backend | Node.js, Express, MySQL, Prisma |
| RAG Engine | Python, FastAPI, LangChain, ChromaDB |
| LLM | Llama 3.2 via Ollama |
| Embeddings | nomic-embed-text via Ollama |
| Container | Docker, Docker Compose |

---

## 👤 Author

**Kishore G** — B.Tech CSE, SRM Institute of Science and Technology  
GitHub: [@kishore2k05](https://github.com/kishore2k05)
