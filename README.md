# ⚡ RAG FastAPI Backend — Retrieval Augmented Generation API

![Python](https://img.shields.io/badge/Python-3.11-blue?style=flat-square&logo=python)
![FastAPI](https://img.shields.io/badge/API-FastAPI-green?style=flat-square&logo=fastapi)
![FAISS](https://img.shields.io/badge/VectorDB-FAISS-orange?style=flat-square)
![LangChain](https://img.shields.io/badge/Framework-LangChain-purple?style=flat-square)
![Status](https://img.shields.io/badge/Stage-Complete-green?style=flat-square)

---

👤 **Author:** [Ashutosh](https://github.com/Ashutosh-AIBOT) · [LinkedIn](https://www.linkedin.com/in/ashutosh1975271/)
💼 **Portfolio:** [ashutosh-portfolio-kappa.vercel.app](https://ashutosh-portfolio-kappa.vercel.app/)

---

## 🧠 What This Does

A production-ready FastAPI backend that exposes RAG
pipeline functionality as clean REST API endpoints.
Any frontend can connect and use document chat, search,
and retrieval without touching the ML code.

---

## 📡 API Endpoints

| Method | Endpoint | What It Does |
|--------|---------|-------------|
| `POST` | `/ingest` | Upload document → chunk → embed → store in FAISS |
| `POST` | `/query` | Send question → retrieve → LLM response |
| `GET` | `/documents` | List all ingested documents |
| `DELETE` | `/documents/{id}` | Remove document from vector store |
| `GET` | `/health` | API health check |

---

## 🏗️ Architecture
```
Client Request
        ↓
FastAPI Router
        ↓
RAG Pipeline
  → Document Ingestion (PDF/TXT/DOCX)
  → Text Chunking (RecursiveCharacterTextSplitter)
  → Embedding (HuggingFace / OpenAI)
  → FAISS Vector Store
        ↓
Query Handler
  → Query embedding
  → Top-k retrieval
  → LLM response generation
        ↓
JSON Response to Client
```

---

## ⚡ Quick Start
```bash
git clone https://github.com/Ashutosh-AIBOT/rag-fastapi-backend.git
cd rag-fastapi-backend
pip install -r requirements.txt
cp .env.example .env
uvicorn main:app --reload
# Docs: http://localhost:8000/docs
```

---

## 🛠️ Tech Stack

`Python` `FastAPI` `LangChain` `FAISS` `HuggingFace` `PyPDF2` `Uvicorn` `Git`

---

## 👤 Author
**Ashutosh** · B.Tech Electronics Engineering · Batch 2026
[GitHub](https://github.com/Ashutosh-AIBOT) · [LinkedIn](https://www.linkedin.com/in/ashutosh1975271/)

> *"RAG as an API. Plug any frontend. Ship fast."*
```
