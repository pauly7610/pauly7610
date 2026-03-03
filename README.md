<div align="center">

# Paul Carpenter
### Technical Program Manager · Product Manager · Platform Builder

[![LinkedIn](https://img.shields.io/badge/LinkedIn-paul--carpenter-0A66C2?style=flat-square&logo=linkedin)](https://linkedin.com/in/paul-carpenter)
[![GitHub](https://img.shields.io/badge/GitHub-pauly7610-181717?style=flat-square&logo=github)](https://github.com/pauly7610)
[![Email](https://img.shields.io/badge/Email-Paul.Carpenter1041@gmail.com-EA4335?style=flat-square&logo=gmail)](mailto:Paul.Carpenter1041@gmail.com)

**$10M+ ARR driven · 17+ production systems shipped · Enterprise AI with regulatory compliance**

*New York, NY*

</div>

---

## About

I'm a Technical Product/Program Manager who architects and ships production-grade AI systems — not just prototypes. With 5+ years leading cross-functional teams across engineering, data science, design, and compliance, I specialize in taking complex AI initiatives from 0→1 and scaling them to enterprise deployment.

Currently at **INNOgenius** delivering contextual personalization at scale. Previously drove an **$850M+ platform migration at JPMorgan Chase** and founded a **fintech AI platform that reached $20K+ MRR**.

---

# Featured Projects

---

## EvalGate — CI for AI Behavior  
**https://www.evalgate.com**

Stop LLM regressions in CI in 2 minutes.  
Turns AI evaluations into real merge-blocking gates.

### The Problem

LLMs drift silently. Prompt tweaks, model swaps, or retrieval changes degrade quality — and traditional CI won’t catch it.

### What It Does

- Regression Gate — Blocks PRs when evals regress  
- Spec Discovery + Impact Analysis — Auto-detects and runs only what changed  
- Drift Detection — Classifies prompt / retrieval / safety regressions  
- Three-Layer Scoring — Reasoning · Action · Outcome  
- LLM Judge + Multi-Judge — 6 aggregation strategies  
- Trace + Cost Tracking — Tokens, latency, cost per run  
- Baseline Governance — Anti-cheat protections + CI enforcement  

### Quick Start

```bash
npx @evalgate/sdk init
git push
```

---

## Support Intelligence Core (SIC) — LLM-Powered Customer Support Platform

Modular, production-ready customer support platform with RAG, multi-model AI, agent orchestration, and a 4-layer continuous learning architecture.

Repository: https://github.com/pauly7610/support101

### The Problem

Enterprise support teams need AI that gets smarter over time — not a static chatbot. SIC is a full platform: multi-model RAG, 9 specialized agent blueprints, human-in-the-loop review, voice I/O, and a continuous learning loop that improves with every resolved ticket.

### Architecture

```
Frontend (Next.js 15 + Chrome Extension)
         │ Vercel AI SDK streaming / WebSocket
FastAPI Backend (Port 8000)
  ├── RAG Engine      → Multi-model: OpenAI, Claude, Gemini, Ollama
  ├── Agent Framework → 9 blueprints, tool calling, HITL
  ├── Voice I/O       → Whisper STT + OpenAI TTS
  ├── A2A Protocol    → JSON-RPC 2.0 agent interoperability
  └── MCP Server      → 8 tools for IDE/editor integration
         │
Infrastructure: PostgreSQL 16 · Redis 7 · Pinecone v3 · Apache AGE · Docker
```

### Continuous Learning — 4-Layer System

| Layer | Technology | Purpose |
|-------|------------|---------|
| Feedback Loop | Pinecone | HITL outcomes → golden paths for future RAG |
| Activity Stream | Redis Streams | Durable event sourcing for all agent actions |
| Activity Graph | Apache AGE | Knowledge graph: Customer → Ticket → Resolution → Agent |
| Playbook Engine | LangGraph | Auto-generated resolution workflows |

Key capabilities:

- 9 agent blueprints  
- Pinecone v3 with reranking and metadata filtering  
- OpenTelemetry tracing, Prometheus metrics, Sentry monitoring  
- Multi-tenant RBAC with JWT auth  
- 197 backend tests · Cypress E2E  

Tech stack: FastAPI · Next.js · React · LangChain · Pinecone · PostgreSQL · Redis · Apache AGE · OpenTelemetry · Docker

---

## Financial AI Observability Platform — Real-Time Anomaly Detection & Compliance

Live: https://fin-observability-production.up.railway.app

Production compliance platform answering three questions regulated AI teams struggle with:  
Why did the model flag this? Is it still working? Who approved what, and when?

### End-to-End Decision Chain

```
Transaction arrives
       ↓
ML Ensemble (IF + PCA-Autoencoder)
       ↓
LLM Agent (LangChain)
       ↓
Human Review (RBAC dashboard)
       ↓
OpenTelemetry → Grafana Cloud
```

### Key Capabilities

| Capability | Detail |
|------------|--------|
| Explainability | SHAP TreeExplainer per-prediction breakdown |
| Drift Detection | PSI + KS tests with auto retraining triggers |
| A/B Testing | Chi-squared significance testing |
| RBAC | 4 roles · 25 fine-grained permissions |
| Audit Trail | Full inference → reasoning → decision chain |
| Webhooks | Inbound 10K tx/request · outbound callbacks · DLQ |
| MCP Server | 9 tools for agent integration |

Regulatory alignment: SEC 17a-4 · FINRA 4511

Tech stack: FastAPI · scikit-learn · ONNX Runtime · SHAP · LangChain · Next.js · OpenTelemetry · Grafana Cloud · PostgreSQL · Redis · Railway · Pulumi

Test coverage: 122 backend tests · 35 frontend tests · GitHub Actions CI

---

## Technical Program Management

Beyond building, I coordinate the people and processes that ship complex AI systems at scale:

- Program governance — OKRs, risk registers, dependency mapping  
- ML lifecycle management — experimentation to production  
- Enterprise compliance delivery — SOC2, GDPR, HIPAA, FINRA  
- Cross-functional execution — Led $850M+ platform migration at JPMorgan Chase  

---

## Tech Stack

```
AI/ML          LLMs · RAG · LangChain · SHAP · Isolation Forest · ONNX · OpenAI · Anthropic
Backend        FastAPI · Go · Node.js · PostgreSQL · Redis
Frontend       Next.js · React · TypeScript · Tailwind
DevOps         Docker · AWS · Railway · Vercel · GitHub Actions · Pulumi
Observability  OpenTelemetry · Prometheus · Grafana · Sentry
Compliance     GDPR · SOC2 · HIPAA · FINRA 4511 · SEC 17a-4
```

---

## Impact

| Metric | Result |
|--------|--------|
| ARR Growth | $10M+ from deployed ML products |
| Platform Migration | $850M+ rewards platform · 25% utilization increase |
| Error Reduction | 95% across 500K+ daily transactions |
| Support Savings | $2M+ annually via NLP resolution accuracy |
| Production Repositories | 17+ shipped 0→1 |
| Engagement Lift | 40% via contextual AI personalization |

---

<div align="center">

**Open to Senior TPM and AI Product Leadership roles in New York or remote.**

[paul.carpenter1041@gmail.com](mailto:paul.carpenter1041@gmail.com)  
[LinkedIn](https://linkedin.com/in/paul-carpenter)  
[GitHub](https://github.com/pauly7610)

</div>
