# Intelligent Healing System (IHS) — AI Ops Platform

> **Enterprise-grade AI platform for intelligent incident detection, root cause analysis, and auto-healing operations.**

[![Status](https://img.shields.io/badge/status-production--concept-blue)](https://github.com/gethepc/ihs-ai-ops-platform)
[![Stack](https://img.shields.io/badge/stack-FastAPI%20%7C%20LangChain%20%7C%20Ollama%20%7C%20K8s-brightgreen)](https://github.com/gethepc/ihs-ai-ops-platform)

---

## The Problem

Modern enterprise operations suffer from:
- High MTTR due to manual, reactive troubleshooting
- Massive alert noise — teams spend hours triaging instead of resolving
- No institutional memory — each incident solved from scratch
- Lack of intelligent automation for routine resolution workflows

---

## The Solution — IHS

IHS is an **AI-powered self-healing operations platform** that:

1. **Classifies alerts** using ML to separate noise from critical events
2. **Correlates incidents** across system boundaries to identify blast radius
3. **Performs Root Cause Analysis** using RAG against a historical knowledge base
4. **Executes auto-healing workflows** with confidence-based decision controls
5. **Provides an AI assistant** for operators to query incidents in natural language

---

## Architecture

```
┌─────────────────────────────────────────────────┐
│                  IHS Platform                   │
├────────────────┬────────────────┬───────────────┤
│  Alert Ingest  │  AI / ML Core  │  Action Engine│
│  (Kafka/API)   │  (LangChain +  │  (Runbooks +  │
│                │   Ollama LLM)  │   Workflows)  │
├────────────────┴────────────────┴───────────────┤
│           Knowledge Store                       │
│   PostgreSQL + pgvector  │  MongoDB             │
├─────────────────────────────────────────────────┤
│           Orchestration — Apache Airflow        │
├─────────────────────────────────────────────────┤
│        Containerisation — Docker / Kubernetes   │
└─────────────────────────────────────────────────┘
```

### Component Breakdown

| Layer | Technology |
|---|---|
| Frontend dashboard | Angular |
| API layer | FastAPI (Python) |
| AI / RAG engine | LangChain + Ollama (local LLM) |
| ML models | Custom alert classification models |
| Vector store | PostgreSQL + pgvector |
| Document store | MongoDB |
| Workflow orchestration | Apache Airflow |
| Containerisation | Docker / Kubernetes |

---

## Key Features

- **Auto-healing workflows** — resolves known incident patterns autonomously
- **AI-based Root Cause Analysis** — RAG retrieval from historical incident corpus
- **Alert correlation engine** — links related alerts across services
- **Confidence-based decision engine** — acts autonomously only when confidence threshold met; escalates otherwise
- **Real-time analytics dashboard** — MTTR trends, resolution rates, open incidents
- **Interactive AI assistant** — natural language querying for on-call engineers

---

## Business Impact

| Metric | Outcome |
|---|---|
| Incident resolution time | Reduced by ~40% |
| Alert noise | Filtered by ML classification |
| Manual intervention | Significantly reduced for L1/L2 |
| Knowledge reuse | Historical resolution matching via RAG |

---

## Repository Structure

```
ihs-ai-ops-platform/
├── docs/
│   ├── architecture.md
│   ├── alert-classification.md
│   ├── rag-design.md
│   └── healing-workflows.md
├── assets/
│   └── architecture-diagram.png
├── examples/
│   ├── sample-alert-payload.json
│   └── healing-workflow-example.yaml
└── README.md
```

---

## Author

**Prashant Chauhan** — Conceptualised · Architected · Built · Deployed  
GitHub: [@gethepc](https://github.com/gethepc)  
LinkedIn: [prashant-chauhan-2b5a0b11](https://www.linkedin.com/in/prashant-chauhan-2b5a0b11/)

---

*This repository documents the architecture and design of the IHS platform. Built within a global utility & IoT enterprise environment. Implementation details are proprietary.*
