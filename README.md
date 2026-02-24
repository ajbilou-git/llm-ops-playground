# LLM Ops Playground

> A hands-on, enterprise-simulated learning path from **DevOps Engineer** to **MLOps / AI DevOps Engineer** in 3 months.

Every concept is deployed locally and tested against a realistic industrial maintenance company scenario — no toy examples, only production-grade patterns.

## Use This Template

This repository is a **GitHub Template**. Click **"Use this template"** at the top of the page to create your own copy and start your personal learning journey with a clean slate.

| Audience | What you get |
|----------|-------------|
| **DevOps engineers wanting to learn AI/MLOps** | A structured 3-month curriculum with 11 hands-on labs, an AI coaching skill for Cursor, and a complete monitoring stack to deploy locally |
| **Recruiters reviewing a candidate** | Each lab folder contains working code, Quick Start instructions, and architecture diagrams demonstrating real AI/MLOps implementation skills |

## What This Project Covers

| Domain | Topics |
|--------|--------|
| **LLM Deployment** | Ollama, Mistral, Llama, vLLM, model configuration |
| **Embeddings & Vector DB** | ChromaDB, Qdrant, sentence-transformers |
| **RAG** | Chunking, retrieval, augmentation, generation, RAGAS evaluation |
| **Agentic AI** | ReAct, routing, autonomous agents, multi-agent orchestration |
| **MCP** | Model Context Protocol, tool use, function calling |
| **Fine-tuning** | LoRA, QLoRA, dataset preparation, evaluation |
| **Machine Learning** | Prediction pipelines, feature engineering, FastAPI serving |
| **Token & Context** | Window management, chunking strategies, cost optimization |
| **LLM Monitoring** | Opik, LangFuse, Phoenix, RAGAS, DeepEval, Guardrails |
| **Production Stack** | Prometheus, Grafana, alerting, drift detection |

## Project Structure

```
llm-ops-playground/
├── README.md
├── skill/
│   ├── SKILL.md                # Cursor AI coaching skill (multi-language)
│   ├── README.md               # How to install and use in Cursor
│   └── progress.md             # Personal progress tracker
├── roadmap/
│   ├── ROADMAP.md              # Full 3-month learning roadmap
│   └── progress.md             # Personal progress tracker
├── labs/
│   ├── lab-01-llm-local/       # Local LLM deployment (Ollama + Mistral)
│   ├── lab-02-embeddings-vectordb/  # Embeddings + ChromaDB/Qdrant
│   ├── lab-03-rag-pipeline/    # Full RAG pipeline + RAGAS eval
│   ├── lab-04-agentic-rag/     # Agentic RAG with multi-source routing
│   ├── lab-05-mcp/             # MCP server + tool integration
│   ├── lab-06-fine-tuning/     # LoRA/QLoRA fine-tuning
│   ├── lab-07-ml-prediction/   # ML prediction API (FastAPI)
│   ├── lab-08-multi-agents/    # Multi-agent orchestration
│   ├── lab-09-token-optimization/ # Token & context window optimization
│   ├── lab-10-capstone/        # Full platform integration
│   └── lab-11-monitoring/      # LLM monitoring stack
├── docs/
│   ├── glossary.md             # AI/ML concepts glossary
│   ├── monitoring-stack.md     # LLM monitoring architecture
│   └── architecture.md         # Enterprise simulation architecture
├── docker/
│   └── docker-compose.monitoring.yml
└── data/
    └── README.md               # Sample data generation instructions
```

## Enterprise Simulation Context

All labs run against a simulated **industrial maintenance company**:

| Data Source | Content | Used In |
|-------------|---------|---------|
| Tickets | Incidents, requests, history | RAG, Fine-tuning, Agents |
| Documentation | Procedures, manuals, safety norms | RAG, Embeddings, Guardrails |
| Equipment Logs | Time series, alerts, metrics | ML Prediction, Monitoring |
| Knowledge Base | FAQ, best practices, lessons learned | Vector DB, Semantic Search |
| Asset Registry | Equipment, parts, suppliers | Agentic RAG, MCP |

## Labs Overview

### Month 1 — Foundations

| Lab | Title | Key Concepts | Deliverable |
|-----|-------|-------------|-------------|
| 01 | LLM Local | Token, Context Window, Prompt Engineering | Local API responding to maintenance queries |
| 02 | Embeddings & Vector DB | Embedding, Similarity Search | Semantic search engine on technical docs |
| 03 | RAG Pipeline | RAG, Chunking, RAGAS | RAG chatbot on technical documentation |

### Month 2 — Agents & Specialization

| Lab | Title | Key Concepts | Deliverable |
|-----|-------|-------------|-------------|
| 04 | Agentic RAG | ReAct, Routing, Autonomous Agents | Multi-source autonomous RAG agent |
| 05 | MCP | Model Context Protocol, Tool Use | MCP agent connected to enterprise tools |
| 06 | Fine-tuning | LoRA, QLoRA, Dataset Prep | Domain-specialized model |
| 07 | ML Prediction | Feature Engineering, FastAPI | Failure prediction API with dashboard |
| 08 | Multi-Agents | Orchestration, Supervisor Pattern | Multi-agent incident resolution system |
| 11 | LLM Monitoring | Tracing, Evaluation, Guardrails | Full observability stack |

### Month 3 — Production & Integration

| Lab | Title | Key Concepts | Deliverable |
|-----|-------|-------------|-------------|
| 09 | Token Optimization | Chunking, Compression, Budget | Cost-optimized RAG pipeline |
| 10 | Capstone | Full Architecture | Complete enterprise AI platform |

## Monitoring Stack

The project includes a complete LLM monitoring stack (Lab 11):

- **Tracing**: Opik, LangFuse, Phoenix, OpenLIT
- **Evaluation**: RAGAS, DeepEval, PromptFoo
- **Guardrails**: Guardrails AI, NeMo Guardrails
- **Dashboards**: Prometheus + Grafana (operational, quality, cost, drift)

See [docs/monitoring-stack.md](docs/monitoring-stack.md) for full details.

## Prerequisites

- [Cursor IDE](https://cursor.sh) (for the AI coaching skill)
- [Ollama](https://ollama.ai) installed
- [Docker Desktop](https://docker.com/products/docker-desktop) running
- Python 3.11+
- 16GB+ RAM (32GB recommended for local LLMs)
- GPU optional (CPU inference supported via Ollama)
- Node.js 18+ (for PromptFoo in later labs)

## AI Coaching Skill for Cursor

This project includes a **ready-to-use Cursor AI skill** in the [`skill/`](skill/) folder. Once installed, the AI becomes your personal MLOps coach that:

- Manages your daily workload and tracks your progress
- Explains every line of code **before and after** writing it
- Asks comprehension questions and waits for your answers
- Runs a **10-question interactive quiz** at the end of each lab with grading
- Generates Quick Start documentation and pushes to your portfolio
- Coaches in **your preferred language** (English, Français, Español, Deutsch, Português, 日本語, 中文, العربية)

See [skill/README.md](skill/README.md) for the full feature list.

## Getting Started — Step by Step

### Step 1: Get the Repository

**Option A — Use as template (recommended for new learners)**

Click **"Use this template"** → **"Create a new repository"** on GitHub, then:

```bash
git clone https://github.com/<your-username>/llm-ops-playground.git
cd llm-ops-playground
```

**Option B — Clone directly**

```bash
git clone https://github.com/ajbilou-git/llm-ops-playground.git
cd llm-ops-playground
```

### Step 2: Install the Cursor AI Coaching Skill

Copy the skill files into your Cursor workspace configuration:

```bash
mkdir -p .cursor/skills/AI-Learning-Coach
cp skill/SKILL.md .cursor/skills/AI-Learning-Coach/SKILL.md
cp skill/progress.md .cursor/skills/AI-Learning-Coach/progress.md
```

### Step 3: Choose Your Coaching Language

Open `.cursor/skills/AI-Learning-Coach/SKILL.md` and edit the language setting at the top:

```
COACHING_LANGUAGE: English
```

Change `English` to your preferred language. The coach will speak to you in that language while all code and documentation remain in English.

### Step 4: Install Prerequisites

```bash
# Verify Ollama is installed
ollama --version

# Pull a model
ollama pull mistral

# Verify Docker is running
docker info
```

### Step 5: Launch the Coach

Open the project in **Cursor IDE** and type in the chat:

```
start AI Learning Coach
```

The coach will ask you a few setup questions (available time, hardware, goals) and generate your personalized 3-month learning plan. Then you start Lab 01 immediately.

### Alternative: Self-Guided (no Cursor)

If you prefer learning without the AI coach, follow each lab's README in order:

```bash
cd labs/lab-01-llm-local
cat README.md
```

## See It In Action

Looking for a completed version with working lab code?
Check out the portfolio repo: [llm-ops-portfolio](https://github.com/ajbilou-git/llm-ops-portfolio)

## Progress Tracking

Track personal progress in [roadmap/progress.md](roadmap/progress.md).

## Resources

| Category | Tools |
|----------|-------|
| LLM Runtime | [Ollama](https://ollama.ai), [vLLM](https://github.com/vllm-project/vllm) |
| Frameworks | [LangChain](https://python.langchain.com), [LlamaIndex](https://docs.llamaindex.ai) |
| Vector DB | [ChromaDB](https://docs.trychroma.com), [Qdrant](https://qdrant.tech) |
| Agents | [CrewAI](https://docs.crewai.com), [AutoGen](https://microsoft.github.io/autogen) |
| Fine-tuning | [PEFT](https://huggingface.co/docs/peft), [Unsloth](https://github.com/unslothai/unsloth) |
| Monitoring | [Opik](https://github.com/comet-ml/opik), [LangFuse](https://langfuse.com), [Phoenix](https://github.com/Arize-ai/phoenix) |
| Evaluation | [RAGAS](https://github.com/explodinggradients/ragas), [DeepEval](https://github.com/confident-ai/deepeval), [PromptFoo](https://promptfoo.dev) |
| Guardrails | [Guardrails AI](https://github.com/guardrails-ai/guardrails), [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) |
| MCP | [MCP Spec](https://modelcontextprotocol.io) |
| Serving | [FastAPI](https://fastapi.tiangolo.com), [Streamlit](https://streamlit.io), [Gradio](https://gradio.app) |

## License

MIT
