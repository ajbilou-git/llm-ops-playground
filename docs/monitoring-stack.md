# LLM Monitoring Stack — Architecture

## Overview

```
┌──────────────────────────────────────────────────────────┐
│                    GRAFANA DASHBOARDS                     │
│  Operational │ Quality │ Cost/Tokens │ Drift/Alerting    │
├──────────────┴─────────┴─────────────┴───────────────────┤
│                    PROMETHEUS                             │
│              (metrics collection)                         │
├──────────────┬─────────┬─────────────┬───────────────────┤
│   Opik /     │  RAGAS  │ DeepEval    │ Guardrails AI /   │
│   LangFuse   │         │ PromptFoo   │ NeMo Guardrails   │
│   (tracing)  │ (eval)  │ (testing)   │ (safety)          │
├──────────────┴─────────┴─────────────┴───────────────────┤
│              APPLICATION LAYER                            │
│  RAG Pipeline │ Agents │ MCP │ ML Prediction             │
├──────────────────────────────────────────────────────────┤
│          INFRASTRUCTURE                                   │
│  Ollama │ ChromaDB/Qdrant │ FastAPI │ Docker             │
└──────────────────────────────────────────────────────────┘
```

## Layer 1 — Tracing & Observability

### Opik (Comet)
- **What**: Open-source LLM tracing platform
- **Deploy**: `docker compose up opik`
- **Use for**: Trace every LLM call, visualize RAG chains, compare models, annotate traces

### LangFuse
- **What**: Open-source LLM observability (LangSmith alternative)
- **Deploy**: `docker compose up langfuse`
- **Use for**: Span-level tracing, session tracking, prompt versioning, A/B testing, dataset management

### Phoenix (Arize AI)
- **What**: Open-source LLM debugging and observability
- **Deploy**: `pip install arize-phoenix && python -m phoenix.server.main serve`
- **Use for**: Embedding visualization (UMAP 2D/3D), cluster detection, drift analysis

### OpenLIT
- **What**: OpenTelemetry-native LLM observability
- **Deploy**: `docker compose up openlit`
- **Use for**: Native OTel traces, p50/p95/p99 latency, cost per request, Grafana integration

## Layer 2 — Quality Evaluation

### RAGAS
- **What**: Automated RAG evaluation framework
- **Metrics**: Faithfulness, Answer Relevancy, Context Recall, Context Precision
- **Use for**: Benchmark quality, CI/CD regression testing

### DeepEval
- **What**: Unit testing for LLMs (pytest-style)
- **Metrics**: Hallucination, relevance, toxicity, bias
- **Use for**: CI integration, PR-level quality checks

### PromptFoo
- **What**: Prompt evaluation and red teaming tool
- **Use for**: Compare N prompts on M test cases, automated red teaming, custom graders

## Layer 3 — Guardrails & Safety

### Guardrails AI
- **What**: Output validation and safety framework
- **Use for**: Format validation, hallucination blocking, source citation enforcement

### NeMo Guardrails (NVIDIA)
- **What**: Secure dialogue framework for LLMs
- **Use for**: Topical rails, safety rails, moderation, fact-checking

## Layer 4 — Production Monitoring

### Metrics to Monitor

| Category | Metrics |
|----------|---------|
| **Performance** | p50/p95/p99 latency, throughput, TTFT, retrieval time |
| **Quality** | RAGAS scores (rolling avg), hallucination rate, satisfaction, fallback rate |
| **Cost** | Tokens per request (in+out), cost per request/day/user, useful vs context ratio |
| **Drift** | Embedding distribution (weekly UMAP), quality score trends, out-of-domain rate |

### Dashboards

| Dashboard | Content | DevOps Analogy |
|-----------|---------|---------------|
| Operational | Latency, throughput, errors, health | Grafana for classic APIs |
| Quality | RAGAS scores, hallucination rate, bad examples | SonarQube for AI responses |
| Cost & Tokens | Token consumption, cost estimates, projections | Azure Cost Management for tokens |
| Drift & Alerting | Metric trends, degradation alerts, query clusters | Azure Monitor Alerts for AI quality |
