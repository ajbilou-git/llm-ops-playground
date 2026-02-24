# Enterprise Simulation — Architecture

## Context

All labs operate against a simulated **industrial maintenance company**.
This provides realistic data, realistic queries, and realistic challenges
that mirror production enterprise AI deployments.

## Simulated Data Sources

```
┌─────────────────────────────────────────────────┐
│           ENTERPRISE DATA LAYER                  │
├──────────┬──────────┬──────────┬────────────────┤
│ Tickets  │ Docs     │ Equip.   │ Knowledge      │
│ System   │ Base     │ Logs     │ Base           │
│          │          │          │                │
│ incidents│ manuals  │ sensors  │ FAQ            │
│ requests │ safety   │ alerts   │ best practices │
│ history  │ norms    │ metrics  │ lessons learned│
├──────────┴──────────┴──────────┴────────────────┤
│            Asset Registry                        │
│   equipment │ parts │ suppliers │ locations      │
└─────────────────────────────────────────────────┘
```

## How Labs Use Enterprise Data

| Lab | Primary Data | Secondary Data |
|-----|-------------|----------------|
| 01 — LLM Local | Domain vocabulary | Maintenance queries |
| 02 — Embeddings | Technical docs | Knowledge base |
| 03 — RAG Pipeline | Technical docs | Tickets (for eval) |
| 04 — Agentic RAG | All sources | Query routing logic |
| 05 — MCP | Tickets + Docs | Equipment logs |
| 06 — Fine-tuning | Tickets (training) | Docs (evaluation) |
| 07 — ML Prediction | Equipment logs | Maintenance history |
| 08 — Multi-Agents | Tickets (incidents) | All sources |
| 09 — Token Optimization | Technical docs (long) | Cost metrics |
| 10 — Capstone | All sources | All metrics |
| 11 — Monitoring | All traces | Quality benchmarks |

## Sample Data Generation

Each lab includes instructions to generate synthetic data
matching the enterprise schema. Data is generated using:
- Python Faker for structured data (tickets, assets)
- LLM-generated content for documentation
- Synthetic time series for equipment logs

## Integration Architecture (Capstone)

```
                    ┌─────────┐
                    │ User UI │
                    │Streamlit│
                    └────┬────┘
                         │
                    ┌────▼────┐
                    │   API   │
                    │ Gateway │
                    │ FastAPI │
                    └────┬────┘
           ┌─────────┬──┴──┬─────────┐
      ┌────▼───┐ ┌───▼──┐ │    ┌────▼────┐
      │  RAG   │ │Agent │ │    │  Multi  │
      │Pipeline│ │ RAG  │ │    │ Agents  │
      └────┬───┘ └───┬──┘ │    └────┬────┘
           │         │    │         │
      ┌────▼─────────▼────▼─────────▼────┐
      │          MCP Server               │
      │    (Tool Integration Layer)       │
      └──┬──────┬──────┬──────┬──────────┘
    ┌────▼──┐┌──▼───┐┌─▼────┐│┌──────────┐
    │Ollama ││Vector││ML    │││Monitoring│
    │ LLM   ││  DB  ││Model │││  Stack   │
    └───────┘└──────┘└──────┘│└──────────┘
                              │
                    ┌─────────▼─────────┐
                    │  Enterprise Data   │
                    │ Tickets│Docs│Logs  │
                    └───────────────────┘
```
