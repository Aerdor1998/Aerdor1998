<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Aerdor1998/Aerdor1998/main/assets/header-dark.svg">
    <img alt="Lucas Matheus — AI Engineer · LLM systems, RAG, fine-tuned embeddings, evals wired into CI" src="https://raw.githubusercontent.com/Aerdor1998/Aerdor1998/main/assets/header-light.svg" width="100%">
  </picture>

  <br>

  <a href="mailto:lucasmsilva1998@gmail.com">
    <img alt="Email" src="https://img.shields.io/badge/Email-lucasmsilva1998%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white">
  </a>
  <img alt="Open to AI Engineer roles" src="https://img.shields.io/badge/Open_to-AI_Engineer_roles-58a6ff?style=for-the-badge">
  <img alt="Based in Brazil" src="https://img.shields.io/badge/Based_in-Brazil_·_PT--BR_/_EN-2ea44f?style=for-the-badge">

</div>

<br>

**I build LLM systems that survive production** — RAG pipelines, fine-tuned embeddings, and eval gates wired into CI, so models only ship when they beat the bar. Currently building **ApurAI**, an AI tax-classification SaaS for Brazil's 2026 tax reform (LC 214/2025), with auditable, human-reviewed AI decisions end to end.

---

## 🔭 Featured work

### ApurAI — AI tax classification for Brazil's 2026 reform · `private, in active development`

<img alt="Python" src="https://img.shields.io/badge/Python_3.12-3776AB?style=flat-square&logo=python&logoColor=white"> <img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"> <img alt="Pydantic AI" src="https://img.shields.io/badge/Pydantic_AI-E92063?style=flat-square&logo=pydantic&logoColor=white"> <img alt="Qdrant" src="https://img.shields.io/badge/Qdrant-DC244C?style=flat-square"> <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"> <img alt="Next.js" src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white">

SaaS that classifies products/services under Brazil's new tax law (cClassTrib, CST-IBS/CBS) with auditable AI and human review.

| Result | Detail |
| --- | --- |
| **acc@1 0.068 → 0.447** | Fine-tuned BGE-M3 embeddings for NCM retrieval, measured on a leakage-free cross-chapter holdout — release gate ≥ 0.40 enforced in CI |
| **Negative result, shipped** | Reranking *degraded* the fine-tuned model (0.447 → 0.234) — measured, documented in an ADR, and disabled on that path |
| **Eval gate in GitHub Actions** | nDCG@10 / acc@1 on holdout chapters, artifact identity checks, mandatory model checksums |
| **Production-grade backend** | Multi-tenant PostgreSQL (schema-per-tenant), Qdrant, Celery workers, Langfuse observability |
| **348+ tests · ~89% coverage** | LGPD-aware logging · digital certificates handled in memory only |

### MedSafe — multi-agent drug-interaction analysis · [`view repo →`](https://github.com/Aerdor1998/MedSafe)

<img alt="LangGraph" src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langgraph&logoColor=white"> <img alt="Ollama" src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white"> <img alt="pgvector" src="https://img.shields.io/badge/pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white"> <img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"> <a href="https://github.com/Aerdor1998/MedSafe/blob/main/LICENSE"><img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-green?style=flat-square"></a>

Multi-agent system (LangGraph) that screens prescriptions for contraindications, with safety guardrails and human-in-the-loop review.

| Highlight | Detail |
| --- | --- |
| **6 specialized agents** | triage → RAG → clinical rules → reflection loop → safety guardrails → human-in-the-loop |
| **191k+ drug interactions** | RAG over PostgreSQL + pgvector · OCR of prescriptions (Tesseract) |
| **100% local LLM** | Ollama / qwen2.5:7b — patient data never leaves the infra |
| **Hardened & observable** | JWT + RBAC, rate limiting, LGPD audit logs · Prometheus + Grafana · green CI (lint, mypy, tests, security scans) |

---

## 🛠 Tech stack

**AI/ML** — Pydantic AI · LangGraph · embedding fine-tuning · RAG · Ollama · LLM evals (nDCG, acc@k)

<img alt="Pydantic AI" src="https://img.shields.io/badge/Pydantic_AI-E92063?style=for-the-badge&logo=pydantic&logoColor=white"> <img alt="LangGraph" src="https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge&logo=langgraph&logoColor=white"> <img alt="sentence-transformers" src="https://img.shields.io/badge/sentence--transformers-FF9D00?style=for-the-badge"> <img alt="RAG: Qdrant + pgvector" src="https://img.shields.io/badge/RAG-Qdrant_·_pgvector-DC244C?style=for-the-badge">

**Backend** — Python 3.12 · FastAPI · PostgreSQL · Redis/Celery · Docker · GitHub Actions

<img alt="Python 3.12" src="https://img.shields.io/badge/Python_3.12-3776AB?style=for-the-badge&logo=python&logoColor=white"> <img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white"> <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white"> <img alt="Redis / Celery" src="https://img.shields.io/badge/Redis_·_Celery-DC382D?style=for-the-badge&logo=redis&logoColor=white"> <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"> <img alt="GitHub Actions" src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white">

**Frontend** — TypeScript · Next.js · Tailwind

<img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white"> <img alt="Next.js + Tailwind" src="https://img.shields.io/badge/Next.js_·_Tailwind-000000?style=for-the-badge&logo=nextdotjs&logoColor=white">

---

## 📊 GitHub stats

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api?username=Aerdor1998&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117">
    <img alt="Lucas Matheus's GitHub stats" src="https://github-readme-stats.vercel.app/api?username=Aerdor1998&show_icons=true&hide_border=true" height="165">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=Aerdor1998&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117">
    <img alt="Top languages" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Aerdor1998&layout=compact&hide_border=true" height="165">
  </picture>
</div>

---

## 📫 Contact

Open to **AI Engineer roles** (LLM systems, RAG, fine-tuning, evals) — fluent PT-BR / EN.

📧 [lucasmsilva1998@gmail.com](mailto:lucasmsilva1998@gmail.com)
