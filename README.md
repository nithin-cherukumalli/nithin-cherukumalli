# Nithin Cherukumalli
### AI Systems Engineer — LLM Infrastructure · RAG Architecture · Agentic AI

Currently the sole AI engineer for the **Government of Andhra Pradesh** — designing and operating production AI systems on an air-gapped network where data security, retrieval accuracy, and system reliability are non-negotiable.

---

## What I Build

I specialise in the infrastructure layer of AI systems — not just calling APIs, but engineering the retrieval pipelines, inference serving, multi-tenant architectures, and governance layers that make LLM systems work reliably in production.

**Current focus areas:**
- Production RAG systems with hybrid retrieval, reranking pipelines, and evaluation frameworks
- On-premise LLM inference serving (vLLM, pgvector, air-gapped deployments)
- Multi-tenant AI platforms with strict data isolation and audit logging
- Agentic AI systems using LangGraph for complex multi-step workflows

---

## Production Systems

### PolicyCrafter — Government RAG Platform
> Live system · Government of Andhra Pradesh · Air-gapped network

Processing **10,000+ official government documents** — orders, amendments, circulars, and regulatory notices — with full versioning, supersession tracking, and legal lineage management.

**Architecture highlights:**
- Hybrid BM25 + dense vector retrieval fused with **Reciprocal Rank Fusion (RRF)**
- Three-stage reranking: cross-encoder → LLM-as-judge → MMR diversity reranking
- Local LLM inference via **vLLM** on **RTX 5090** (32GB VRAM) — KV cache optimised, continuous batching
- **PostgreSQL + pgvector** — zero data leaves the local network
- Full audit trail: provenance tracking, clause-level citations, confidence scoring

**Retrieval evaluation results:**

| Metric | Score |
|--------|-------|
| Recall@1 | 0.92 |
| Recall@5 | 0.85 |
| MRR | 0.67 |
| NDCG@5 | 0.70 |

→ [View repository](https://github.com/nithin-cherukumalli/policy-intelligence-platform)

---

### Multi-Tenant RAG Platform — BlastLearning
> Production · AWS-native · Multi-tenant

**AWS-native multi-tenant RAG platform** enabling multiple client organisations to upload proprietary documents, generate isolated vector databases, and retrieve personalised AI responses.

**Architecture highlights:**
- Tenant isolation via unique vector_db_ids, S3 bucket segregation, DynamoDB access control
- LangGraph-based agentic RAG with dynamic prompt routing and metadata-aware retrieval
- Serverless on Lambda + API Gateway — designed for horizontal scaling

→ [View repository](https://github.com/nithin-cherukumalli/multi-tenant-rag-platform)

---

## Technical Stack

```
LLM Inference:      vLLM · HuggingFace Transformers · Ollama · llama.cpp
RAG & Retrieval:    pgvector · Weaviate · FAISS · ChromaDB · BM25 · RRF fusion
Reranking:          Cross-encoder · LLM-as-judge · MMR (sentence-transformers)
Evaluation:         RAGAS · Recall@K · MRR · NDCG · Groundedness scoring
Agent Frameworks:   LangGraph · LangChain · multi-agent orchestration
Backend:            Python · FastAPI · REST APIs · GraphQL
Cloud:              AWS (Lambda · S3 · DynamoDB · API Gateway · SageMaker)
Infrastructure:     Docker · PostgreSQL · CI/CD · Airflow · MLflow
AI Security:        Multi-tenant isolation · Prompt injection protection · Audit logging
```

---

## Areas of Deep Focus

**RAG Engineering**
Hybrid retrieval architecture, chunking strategy design, three-stage reranking pipelines, retrieval evaluation frameworks, RAG failure analysis, hallucination debugging

**On-Premise LLM Deployment**
vLLM inference serving, KV cache optimisation, continuous batching, VRAM management, throughput vs latency tradeoffs, air-gapped network deployments

**AI Governance & Security**
Multi-tenant data isolation, prompt injection protection at the infrastructure layer, provenance tracking, compliance-aware pipeline design, audit logging for regulated environments

**Agentic AI**
LangGraph orchestration, multi-agent coordination, tool use, memory architecture, agent failure recovery, 11-agent production pipelines

---

## Currently Working On

- QLoRA fine-tuning of domain-specific models on RTX 5090 with MLflow experiment tracking
- LLM observability with self-hosted Langfuse on the government network
- Kubernetes-based deployment patterns for AI inference services

---

## Writing

Technical posts on production AI engineering:

- [What I learned deploying an LLM on an air-gapped government network](#) *(coming soon)*
- [How I improved RAG retrieval from Recall@5 0.61 to 0.85](#) *(coming soon)*

---

## Connect

[LinkedIn](https://www.linkedin.com/in/nithin-cherukumalli-7a478b21a) · [Email](mailto:cherukumallinithin@gmail.com)

Open to discussing **AI systems engineering roles** — remote or hybrid — in UAE, Europe, Singapore, or with global AI startups.
