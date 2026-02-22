# 🌱 Bonsai GPT — Local RAG-Based AI System

A production-grade, modular AI system that enables conversational interaction with PDFs using Retrieval-Augmented Generation (RAG) and a locally hosted LLM.

This project is designed as a scalable foundation for building a full desktop AI assistant.

---

# 🎯 Project Objective

Build a structured, production-ready AI application that:

- Runs fully locally
- Uses vector search (FAISS)
- Uses embeddings for semantic retrieval
- Integrates with a local LLM (Ollama)
- Is version-controlled
- Is CI/CD ready
- Follows clean architecture principles

This is not a toy chatbot — it is an extensible AI system.

---

# 🏗 System Architecture

## High-Level Flow

PDF  
→ Text Extraction  
→ Chunking  
→ Embedding Generation  
→ FAISS Vector Store  

User Query  
→ Retrieve Relevant Chunks  
→ Pass Context to LLM  
→ Generate Response  

This is a **Retrieval-Augmented Generation (RAG)** system.

No fine-tuning is performed.

---

# 📁 Project Structure
bonsai-gpt/
│
├── app/
│ ├── config.py
│ ├── logger.py
│ ├── pdf_loader.py
│ ├── chunking.py
│ ├── embeddings.py
│ ├── vector_store.py
│ ├── chat_engine.py
│ └── main.py
│
├── tests/
├── data/
├── requirements.txt
├── .gitignore
└── README.md


---

# 🧱 Engineering Principles

- Modular architecture
- Single responsibility per module
- Deterministic environment setup
- No hardcoded paths
- Isolated virtual environment
- SSH-based Git authentication
- CI-ready structure
- Designed for extensibility (voice, automation, agents)

---

# 🖥 Environment Setup (Windows)

## 1️⃣ Install Git
https://git-scm.com/download/win

Verify:git --version

---

## 2️⃣ Configure Git Identity
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"


---

## 3️⃣ Setup SSH Authentication

Generate key:
ssh-keygen -t ed25519 -C "your_email@example.com"

View public key:
cat ~/.ssh/id_ed25519.pub

Add key in:
GitHub → Settings → SSH and GPG Keys → New SSH Key

Test:
ssh -T git@github.com
Expected:
You've successfully authenticated


---

## 4️⃣ Create Virtual Environment
Activate (Git Bash):
source venv/Scripts/activate


If PowerShell blocks execution:
Use Git Bash OR enable:
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser


---

## 5️⃣ Install Dependencies
pip install langchain faiss-cpu pypdf sentence-transformers streamlit pytest

Freeze:
pip freeze > requirements.txt


---

# 📦 Core Dependencies

| Package | Purpose |
|----------|----------|
| langchain | LLM orchestration |
| faiss-cpu | Vector similarity search |
| sentence-transformers | Embedding generation |
| pypdf | PDF text extraction |
| streamlit | UI layer |
| pytest | Testing framework |

---

# 🔀 Git Issues Encountered & Resolutions

## Branch mismatch (master vs main)

Problem:
Local branch was `master`, GitHub expected `main`.

Solution:
git branch -M main


---

## Remote repository not found

Cause:
- Incorrect username
- Repository not created online

Fix:
git remote set-url origin git@github.com
:Ek-atva/bonsai-gpt.git


---

## PowerShell script execution blocked

Error:
running scripts is disabled on this system

Resolution:
Use Git Bash 

OR:

Set-ExecutionPolicy RemoteSigned -Scope CurrentUser


---

# 🚀 Next Development Phases

1. Implement PDF Loader
2. Implement Text Chunking
3. Implement Embedding Pipeline
4. Create FAISS Vector Index
5. Build Chat Engine
6. Add Streamlit Interface
7. Add GitHub Actions CI
8. Extend to multi-document support
9. Add conversational memory
10. Expand toward desktop AI assistant

---

# 🧠 Long-Term Vision

Bonsai GPT is the foundational module for:

- Personal AI assistant
- Voice-based desktop automation
- Email drafting automation
- Meeting summarization
- Multi-agent orchestration

---

# 📌 Philosophy

Start small.
Design clean.
Build modular.
Scale intentionally.....