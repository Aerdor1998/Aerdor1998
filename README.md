# Lucas Matheus

**AI Engineer** — I build LLM systems that survive production: RAG pipelines, fine-tuned embeddings, and eval gates wired into CI.

Currently building **ApurAI**, an AI tax-classification SaaS for Brazil's 2026 tax reform (LC 214/2025) — multi-tenant FastAPI backend, Pydantic AI agents, and a release pipeline where models only ship if they beat the eval gate.

🇧🇷 Based in Brazil · Fluent PT-BR/EN

---

## 🔭 Featured work

### ApurAI — fiscal AI agent *(private · in active development)*
SaaS that classifies products/services under Brazil's new tax law (cClassTrib, CST-IBS/CBS) with auditable, human-reviewed AI.

- **Fine-tuned BGE-M3 embeddings** for NCM retrieval: acc@1 **0.068 → 0.447** on a leakage-free, cross-chapter holdout (release gate ≥ 0.40, enforced in CI)
- **Negative result, measured and shipped**: reranking *degraded* the fine-tuned model (0.447 → 0.234) — documented in an ADR and disabled on that path
- **Eval gate in GitHub Actions**: nDCG@10 / acc@1 on holdout chapters, artifact identity checks, mandatory model checksums
- Multi-tenant PostgreSQL (schema-per-tenant), Qdrant vector store, Celery workers, Langfuse observability
- 348+ tests, ~89% coverage · LGPD-aware logging · digital certificates handled in memory only

### [MedSafe](https://github.com/Aerdor1998/MedSafe) — multi-agent drug-interaction analysis
Multi-agent system (LangGraph) that screens prescriptions for contraindications, with safety guardrails and human-in-the-loop review.

- **6 specialized agents**: triage → RAG over medical docs → clinical rules (191k+ interactions) → reflection loop → safety guardrails → HITL
- Local-first LLM inference (Ollama / qwen2.5) · PostgreSQL + pgvector · FastAPI
- JWT + RBAC, rate limiting, audit logs (LGPD) · Prometheus + Grafana · CI with lint, types, tests and security scans

---

## 🛠 Stack

**AI/ML** · Pydantic AI · LangGraph · sentence-transformers (fine-tuning) · RAG (Qdrant, pgvector) · Ollama · LLM evals (nDCG, acc@k, LLM-as-judge)

**Backend** · Python 3.12 · FastAPI · PostgreSQL · Redis/Celery · Docker · GitHub Actions

**Frontend** · TypeScript · Next.js · Tailwind

---

## 📫 Contact

📧 lucasmsilva1998@gmail.com
