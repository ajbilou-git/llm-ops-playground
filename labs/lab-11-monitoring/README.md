# Lab 11 — LLM Monitoring Stack

## Objective
Deploy a complete LLM observability stack and instrument all labs with tracing, evaluation, and alerting.

## Monitoring Layers

### Layer 1 — Tracing & Observability
| Tool | Purpose | Deploy |
|------|---------|--------|
| Opik | LLM tracing, RAG chain visualization | Docker Compose |
| LangFuse | Span-level tracing, prompt management, A/B testing | Docker Compose |
| Phoenix | Embedding visualization (UMAP), drift detection | pip install |
| OpenLIT | OpenTelemetry-native LLM observability | Docker Compose |

### Layer 2 — Quality Evaluation
| Tool | Purpose | Deploy |
|------|---------|--------|
| RAGAS | RAG evaluation (faithfulness, relevancy, recall) | pip install |
| DeepEval | Unit testing for LLMs (hallucination, bias, toxicity) | pip install |
| PromptFoo | Prompt comparison, red teaming, grading | npx |

### Layer 3 — Guardrails & Safety
| Tool | Purpose | Deploy |
|------|---------|--------|
| Guardrails AI | Output validation, source citation enforcement | pip install |
| NeMo Guardrails | Topical rails, safety rails, fact-checking | pip install |

### Layer 4 — Production Monitoring
| Tool | Purpose | Deploy |
|------|---------|--------|
| Prometheus | Metrics collection | Docker Compose |
| Grafana | Dashboards and alerting | Docker Compose |
| AlertManager | Notifications (Slack/Teams/email) | Docker Compose |

## Dashboards to Build

1. **Operational**: latency, throughput, errors, service health
2. **Quality**: RAGAS scores, hallucination rate, user satisfaction
3. **Cost & Tokens**: token consumption, cost per request, projections
4. **Drift & Alerting**: metric trends, degradation alerts, query clusters

## Key Metrics

**Performance**: p50/p95/p99 latency, throughput, TTFT, retrieval time
**Quality**: RAGAS scores, hallucination rate, satisfaction, fallback rate
**Cost**: tokens per request, cost per request/day/user, useful vs context tokens
**Drift**: embedding distribution (UMAP), quality score trends, out-of-domain rate

## Steps
1. Deploy the monitoring stack (Docker Compose)
2. Instrument Lab 03 (RAG) with tracing
3. Create RAGAS evaluation benchmarks
4. Build Grafana dashboards
5. Configure alerts for quality degradation
6. Implement guardrails on the chatbot
7. Run PromptFoo red teaming on prompts
8. Integrate monitoring into the capstone (Lab 10)

## Deliverable
Complete LLM monitoring stack covering the entire platform.

## Tech Stack
- See monitoring tools table above
- Docker Compose
- Python
