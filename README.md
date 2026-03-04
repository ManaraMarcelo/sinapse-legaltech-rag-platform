# SINAPSE: Intelligence System and Legal Process Analysis with Structured Semantics ⚖️🤖

> **Academic Disclaimer:** This project was developed as my Final Capstone Project (TCC) for my Systems Analysis and Development degree at FATEC. It represents the foundation of a LegalTech SaaS that I am continuously evolving.

![Build Status](https://img.shields.io/badge/Status-Academic_MVP-orange)
![Stack](https://img.shields.io/badge/Stack-FastAPI%20|%20React%20|%20PostgreSQL-blue)
![Focus](https://img.shields.io/badge/Focus-LegalTech%20|%20RAG%20|%20AI-green)

---

### 📺 Product Demo
[Insert Video Link Here - e.g., YouTube or Vimeo]
*(Optional: Add a brief 1-2 minute walkthrough of the platform here)*

---

### 💡 Project Overview

**The Problem:** Legal professionals deal with thousands of pages of unorganized PDFs. Finding specific precedents or extracting structured data from lawsuits is slow, manual, and prone to oversight. Standard AI models often "hallucinate" legal facts without proper context.

**The Solution:** **SINAPSE**. A B2B SaaS platform designed to transform static legal PDFs into a structured, searchable, and permanent intelligence engine. By utilizing RAG (Retrieval-Augmented Generation), the system grounds AI responses in real case files, providing accurate citations and permanent semantic memory.



**Technical Challenges:**
- **Semantic Retrieval at Scale:** Implementing **pgvector** in PostgreSQL to handle high-dimensional embeddings for fast and accurate context retrieval across massive document sets.
- **Anti-Hallucination Framework:** Developing "Hard Grounding" logic where the AI is strictly prohibited from answering without direct citations from the uploaded PDFs.
- **Metadata Extraction:** Engineering complex prompts and parsing logic to transform raw OCR text into structured JSON objects for high-level statistical legal analysis.

---

## 📌 Table of Contents
1. [Architectural Overview](#-architectural-overview)
2. [Key Technical Features](#-key-technical-features)
3. [Technology Stack](#-technology-stack)
4. [Project Structure](#-project-structure)
5. [Roadmap & Future Evolution](#-roadmap--future-evolution-the-next-steps)
6. [Installation & Setup](#-installation--setup)
7. [Contact](#-contact)

---

## 🏗️ Architectural Overview
SINAPSE follows a modern decoupled architecture designed for scalability and maintainability.



### 💻 Frontend: Component-Based Architecture
- **Stack:** React + Vite + TypeScript (powered by **Bun**).
- **Design:** Modern UI with **Tailwind CSS & Shadcn/UI**.
- **Logic:** Business logic is decoupled into Custom Hooks for better maintainability and testability.

### ⚙️ Backend: Layered Pattern (Router-Service-Repository)
- **Stack:** **FastAPI (Python)** + LangChain.
- **Layers:** Clear separation between API routes, AI service logic (LangChain chains), and database repositories using SQLAlchemy.

---

## 🚀 Key Technical Features

### 1. Permanent Semantic Memory (RAG)
Unlike transient chatbots, SINAPSE builds a permanent database of legal knowledge using **Vector Search**. It identifies deep context across thousands of pages based on meaning, not just keywords.

> **Visual Demonstration:** > ![Insert GIF or Image showing real-time PDF vectorization/upload process here]

### 2. Automated Legal Metadata Extraction
The system parses raw PDF text and extracts structured JSON objects, allowing for statistical analysis of legal cases, such as identifying parties, case values, and legal foundations automatically.

> **Visual Demonstration:** > ![Insert Screenshot of the Metadata Dashboard or JSON Extraction result here]

### 3. Hard Grounding & Anti-Hallucination
To ensure legal reliability, every AI response includes **direct citations**. Users can verify the exact source and page where the information originated by clicking the reference.

---

## 🛠️ Technology Stack
- **Frontend:** React, TypeScript, Bun, Tailwind CSS.
- **Backend:** Python, FastAPI, LangChain, PyMuPDF, SQLAlchemy.
- **Database:** **Neon.tech** (PostgreSQL Serverless + `pgvector`).
- **AI Engine:** OpenAI API (Embeddings & GPT-4o).

---

## 📂 Project Structure
```text
sinapse-platform/
├── apps/
│   ├── web/          # React Frontend (Vite + Bun)
│   └── api/          # FastAPI Backend (Python)
├── packages/
│   ├── database/     # SQLAlchemy Models & Migrations
│   └── ai-engine/    # LangChain RAG Logic
└── docs/             # Technical Documentation & TCC Paper

```

---

## 🗺️ Roadmap & Future Evolution (The Next Steps)

* [ ] **Cloud Migration:** Transitioning storage to **AWS S3** and compute to **AWS Lambda/ECS**.
* [ ] **Infrastructure as Code:** Implementing **Terraform** for environment management.
* [ ] **Advanced Security:** Integration of **AWS Cognito** for enterprise-grade authentication.
* [ ] **Performance:** Implementing **Redis** caching for frequent semantic queries.

---

## ⚙️ Installation & Setup

1. **Clone the Repo:** `git clone https://github.com/ManaraMarcelo/sinapse-legaltech-rag-platform.git`
2. **Backend Setup:** `cd apps/api && pip install -r requirements.txt`
3. **Frontend Setup:** `cd apps/web && bun install && bun dev`
4. **Environment:** Setup your `.env` with `OPENAI_API_KEY` and `DATABASE_URL`.

---

## 🔗 Contact

**Marcelo Manara** [LinkedIn](https://www.linkedin.com/in/marcelo-manara) | [Portfolio](https://portifolio-peach-beta.vercel.app/)
