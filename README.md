<div align="center">

# Paul Carpenter
### Technical Program Manager · AI Systems Architect · Platform Builder

[![LinkedIn](https://img.shields.io/badge/LinkedIn-paul--carpenter-0A66C2?style=flat-square&logo=linkedin)](https://linkedin.com/in/paul-carpenter)
[![GitHub](https://img.shields.io/badge/GitHub-pauly7610-181717?style=flat-square&logo=github)](https://github.com/pauly7610)
[![Email](https://img.shields.io/badge/Email-Paul.Carpenter1041@gmail.com-EA4335?style=flat-square&logo=gmail)](mailto:Paul.Carpenter1041@gmail.com)

**$10M+ ARR driven · 17+ production systems shipped · Enterprise AI with regulatory compliance**

*New York, NY*

</div>

---

## About

I'm a Technical Program Manager who architects and ships production-grade AI systems — not just prototypes. With 5+ years leading cross-functional teams across engineering, data science, design, and compliance, I specialize in taking complex AI initiatives from 0→1 and scaling them to enterprise deployment.

Currently at **INNOgenius** delivering contextual personalization at scale. Previously drove an **$850M+ platform migration at JPMorgan Chase** and founded a **fintech AI platform that reached $20K+ MRR**.

---

## Featured Projects

### 🧠 EvalAI — Multi-Agent AI Orchestration & Governance Platform

> *Enterprise-grade platform for deploying, monitoring, auditing, and optimizing multi-agent AI systems with full governance and cost visibility.*

[![Live](https://img.shields.io/badge/Live-v0--ai--evaluation--platform--nu.vercel.app-22C55E?style=flat-square)](https://v0-ai-evaluation-platform-nu.vercel.app/)
[![npm](https://img.shields.io/badge/npm-%40pauly4010%2Fevalai--sdk-CB3837?style=flat-square&logo=npm)](https://www.npmjs.com/package/@pauly4010/evalai-sdk)

**The problem:** Teams deploying multi-agent AI systems have no unified way to visualize workflows, audit decisions, track costs across providers, or enforce compliance policies — especially across regulated industries.

**What EvalAI solves:**

| Capability | Detail |
|---|---|
| 🔀 **Multi-Agent Orchestration** | Visual DAG workflows with 6 node types: agent, tool, decision, parallel, human, LLM |
| 🔍 **Decision Auditing** | Full reasoning chains, confidence scores, and alternative path analysis |
| 💰 **Cost Analytics** | Real-time per-workflow cost tracking across 12 models from 3 providers |
| 🛡️ **Governance Engine** | Configurable rules with compliance presets: SOC2, GDPR, HIPAA, FINRA |
| ⏱️ **SLA Management** | Latency, cost, and error rate thresholds with automated violation alerts |
| 👤 **Human-in-the-Loop** | Built-in escalation and approval workflows |
| 📊 **Agent Benchmarks** | Leaderboards and architecture comparisons |

**How it compares:**

| Feature | EvalAI | LangSmith | PromptLayer | W&B |
|---|:---:|:---:|:---:|:---:|
| Multi-Agent Orchestration | ✅ Full DAG | ⚠️ Basic | ❌ | ⚠️ |
| Decision Auditing | ✅ | ⚠️ Limited | ❌ | ❌ |
| Cost Per Workflow | ✅ Real-time | ❌ | ✅ | ❌ |
| Governance Rules | ✅ + presets | ❌ | ❌ | ❌ |
| Human-in-the-Loop | ✅ Built-in | ❌ | ❌ | ❌ |
| SLA Monitoring | ✅ | ❌ | ❌ | ⚠️ |
| Compliance Presets | ✅ SOC2/GDPR/HIPAA/FINRA | ❌ | ❌ | ❌ |

**Quick start with the SDK:**
```typescript
import { AIEvalClient, WorkflowTracer } from '@pauly4010/evalai-sdk';

const client = new AIEvalClient({ apiKey: process.env.EVALAI_API_KEY });
const tracer = new WorkflowTracer(client);

await tracer.startWorkflow('Customer Support Pipeline');

await tracer.recordDecision({
  agent: 'RouterAgent',
  type: 'route',
  chosen: 'technical_support',
  alternatives: [{ action: 'billing', confidence: 0.2 }],
  confidence: 85
});

await tracer.recordCost({ provider: 'openai', model: 'gpt-4', inputTokens: 500, outputTokens: 200 });
await tracer.endWorkflow({ resolution: 'Issue resolved' });
```

**Framework integrations:** LangChain (TypeScript) · CrewAI (Python) · REST API · TypeScript SDK

---

### 🤖 Support Intelligence Core (SIC) — LLM-Powered Customer Support Platform

> *Modular, production-ready customer support platform with RAG, multi-model AI, agent orchestration, and a 4-layer continuous learning architecture.*

[![GitHub](https://img.shields.io/badge/GitHub-pauly7610%2Fsupport101-181717?style=flat-square&logo=github)](https://github.com/pauly7610/support101)

**The problem:** Enterprise support teams need AI that gets smarter over time — not a static chatbot. SIC is a full platform: multi-model RAG, 9 specialized agent blueprints, human-in-the-loop review, voice I/O, and a continuous learning loop that improves with every resolved ticket.

**Architecture:**

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

**Continuous Learning — 4-layer system (no fine-tuning required):**

| Layer | Technology | Purpose |
|---|---|---|
| Feedback Loop | Pinecone | HITL outcomes → golden paths for future RAG |
| Activity Stream | Redis Streams | Durable event sourcing for all agent actions |
| Activity Graph | Apache AGE | Knowledge graph: Customer → Ticket → Resolution → Agent |
| Playbook Engine | LangGraph | Auto-generated resolution workflows (triggers at 3+ successes) |

> Every layer degrades gracefully: no Redis → in-memory fallback. No AGE → memory. No LangGraph → sequential.

**Key capabilities:**
- **9 agent blueprints:** support, triage, data analyst, code review, QA test, knowledge manager, sentiment monitor, onboarding, compliance auditor
- **Pinecone v3** with bge-reranker-v2-m3 reranking, metadata filtering, namespace isolation, GDPR-compliant deletion
- **Full observability:** OpenTelemetry tracing (Traceloop SDK), Prometheus metrics, Sentry error monitoring with automatic PII scrubbing
- **Multi-tenant RBAC** with JWT auth, per-endpoint rate limiting, and audit logging
- **197 backend tests** across 30 files · **Cypress E2E** across 10 spec files

**Tech stack:** FastAPI · Next.js 15 · React 19 · LangChain · Pinecone v3 · PostgreSQL 16 · Redis 7 · Apache AGE · OpenTelemetry · Docker

---

### 📊 Financial AI Observability Platform — Real-Time Anomaly Detection & Compliance

> *Production compliance platform answering three questions regulated AI teams struggle with: Why did the model flag this? Is it still working? Who approved what, and when?*

[![Live](https://img.shields.io/badge/Live-fin--observability--production.up.railway.app-22C55E?style=flat-square)](https://fin-observability-production.up.railway.app)
[![Grafana](https://img.shields.io/badge/Grafana-Live_Dashboard-F46800?style=flat-square&logo=grafana)](https://fin-observability-production.up.railway.app)

**The problem:** AI models in financial services make high-stakes decisions — fraud flags, transaction blocks, compliance escalations. Most teams have zero visibility into *why* the model decided, *whether* it's drifting, or *who* approved what override.

**End-to-end decision chain:**

```
Transaction arrives
       │
       ▼
ML Ensemble (IF + PCA-Autoencoder)    →    anomaly score + SHAP explanation
       │
       ▼
LLM Agent (LangChain)                 →    recommendation + reasoning
       │
       ▼
Human Review (RBAC dashboard)         →    final decision + audit log
       │
       ▼
OpenTelemetry → Grafana Cloud         →    every step traced, linked, queryable
```

**Key capabilities:**

| Capability | Detail |
|---|---|
| 🔬 **Explainability** | SHAP TreeExplainer generates per-prediction feature importance as waterfall charts |
| 📉 **Drift Detection** | PSI + KS tests on sliding window; retraining auto-triggers at threshold breach |
| 🔁 **A/B Testing** | Chi-squared significance testing with hash-based traffic routing |
| 👥 **RBAC** | 4 roles (admin/compliance/analyst/viewer) · 25 fine-grained permissions |
| 📋 **Audit Trail** | Full chain: inference → agent reasoning → human decision. PII hashed. 7-year retention |
| 📡 **Webhook System** | Inbound (10K tx/request) · SSE stream · outbound callbacks (3x retry + DLQ) · scheduled pull |
| 🤖 **MCP Server** | 9 tools — connect Claude Desktop, Cursor, or Windsurf directly to the compliance engine |

**Regulatory alignment:** SEC 17a-4 · FINRA 4511

**Connect any AI agent via MCP:**
```json
{
  "mcpServers": {
    "fin-observability": {
      "url": "https://fin-observability-production.up.railway.app/mcp",
      "transport": "streamable-http"
    }
  }
}
```

**Available MCP tools:** `check_transaction_compliance` · `explain_transaction` · `batch_check_compliance` (up to 10K) · `analyze_portfolio` · `ingest_transactions` · `get_compliance_metrics` · `list_incidents` · `get_drift_status` · `get_model_leaderboard`

**Tech stack:** FastAPI · scikit-learn · ONNX Runtime · SHAP · LangChain · Next.js 16 · OpenTelemetry · Grafana Cloud · PostgreSQL · Redis · Railway · Pulumi

**Test coverage:** 122 backend tests · 35 frontend tests · GitHub Actions CI

---

## Technical Program Management

Beyond building, I specialize in **coordinating the people and processes** that ship complex AI systems at scale:

- **Program governance** — OKRs, risk registers, dependency mapping, stakeholder alignment across engineering, legal, compliance, and design
- **ML lifecycle management** — From experimentation frameworks to production release, including bias detection and model interpretability review
- **Enterprise compliance delivery** — Coordinating SOC2, GDPR, HIPAA, FINRA controls across regulatory, security, and engineering teams
- **Cross-functional execution** — Led $850M+ platform migration at JPMorgan Chase; aligned 4+ engineering squads, legal, compliance, and UX simultaneously

---

## Tech Stack

```
AI/ML          LLMs · RAG · LangChain · Hugging Face · SHAP · Isolation Forest · ONNX · OpenAI · Anthropic
Backend        FastAPI · Go · Node.js · PostgreSQL · Redis · SQLAlchemy · Alembic
Frontend       Next.js · React · TypeScript · Tailwind CSS · Chrome Extensions
DevOps         Docker · Kubernetes · AWS · Railway · Vercel · GitHub Actions · Pulumi
Observability  OpenTelemetry · Prometheus · Grafana · Sentry · LangSmith
Compliance     GDPR · CCPA · SOC2 · HIPAA · FINRA 4511 · SEC 17a-4
PM Tooling     Jira · Confluence · Figma · PRDs · Architecture Diagrams
```

---

## Impact

| Metric | Result |
|---|---|
| ARR Growth | $10M+ from deployed ML products |
| Platform Migration | $850M+ rewards platform · 25% utilization increase · +5 NPS |
| Error Reduction | 95% across 500K+ daily transactions |
| Support Savings | $2M+ annually via NLP resolution accuracy |
| Production Repositories | 17+ shipped 0→1 with CI/CD and documentation |
| User Engagement | 40% improvement via contextual AI personalization |

---

<div align="center">

**Open to Senior TPM and AI Product Leadership roles in New York or remote.**

[paul.carpenter1041@gmail.com](mailto:paul.carpenter1041@gmail.com) · [LinkedIn](https://linkedin.com/in/paul-carpenter) · [GitHub](https://github.com/pauly7610)

</div>

