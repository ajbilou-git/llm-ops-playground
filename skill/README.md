# MLOps Learning Coach — Cursor AI Skill

An interactive AI coaching skill for [Cursor IDE](https://cursor.sh) that guides you through hands-on, enterprise-simulated AI/MLOps labs at your own pace.

## What This Skill Does

When activated in Cursor, the AI becomes your personal MLOps coach that:

- **Manages your learning schedule** (daily workload, weekly plans, progress tracking)
- **Teaches every AI/ML concept** with DevOps analogies and enterprise scenarios
- **Explains code before AND after writing it** (100% learning-oriented approach)
- **Asks comprehension questions** between steps and waits for your answers
- **Evaluates you** at the end of each lab with a 10-question interactive quiz
- **Publishes labs** to your portfolio GitHub with Quick Start documentation
- **Coaches in your preferred language** while delivering all code/docs in English

## Installation

### 1. Copy the Skill to Your Cursor Workspace

```bash
mkdir -p .cursor/skills/AI-Learning-Coach
cp skill/SKILL.md .cursor/skills/AI-Learning-Coach/SKILL.md
cp skill/progress.md .cursor/skills/AI-Learning-Coach/progress.md
```

Or if you cloned the repo:

```bash
cd llm-ops-playground
mkdir -p .cursor/skills/AI-Learning-Coach
cp skill/SKILL.md .cursor/skills/AI-Learning-Coach/SKILL.md
cp skill/progress.md .cursor/skills/AI-Learning-Coach/progress.md
```

### 2. Configure Your Preferences

Open `.cursor/skills/AI-Learning-Coach/SKILL.md` and edit the **CONFIGURATION** section at the top:

```markdown
### Coaching Language
COACHING_LANGUAGE: Français    # ← Change to your preferred language

### Portfolio Repository
PORTFOLIO_REPO: llm-ops-playground
PORTFOLIO_GITHUB: https://github.com/YOUR-USERNAME/llm-ops-playground.git
```

**Supported coaching languages:** English, Français, Español, Deutsch, Português, 日本語, 中文, العربية

### 3. Activate the Skill

Open Cursor chat and type one of the trigger phrases:

```
start AI Learning Coach
```
or
```
AI Coach
```

The coach will introduce itself, ask setup questions, and start building your personalized learning plan.

## How It Works

### Session Flow

1. **Status Check** — Coach reads your progress and shows current status
2. **Time Check** — "How much time do you have today?"
3. **Adapted Content** — Coach selects the right lab/step for your available time
4. **Teaching Loop** for each code action:
   - Why this step? (business context)
   - Code explanation BEFORE writing
   - Code
   - Line-by-line explanation AFTER
   - Connection to AI concepts
   - Micro-validation
5. **Comprehension Questions** — Between steps (waits for your answer)
6. **End-of-Lab Evaluation** — 10-question interactive quiz with grading
7. **Portfolio Publication** — Quick Start generation + push to GitHub

### Evaluation System

At the end of each lab, the coach runs a 10-question evaluation:

| Level | Questions | Focus |
|-------|-----------|-------|
| Fundamentals | 3 | Basic concepts |
| Application | 4 | Applying in different contexts |
| Expertise | 3 | Edge cases, debugging, trade-offs |

- **Score >= 7/10**: proceed to next lab
- **Score < 7/10**: targeted catch-up session before moving on

### Language Behavior

| Context | Language |
|---------|----------|
| Coaching, explanations, questions | COACHING_LANGUAGE (your choice) |
| Code, variables, functions | English |
| README, Quick Start, docs | English |
| Commit messages | English |
| Configuration files | English |

## Prerequisites

Before starting, make sure you have:

- [ ] [Cursor IDE](https://cursor.sh) installed
- [ ] [Ollama](https://ollama.ai) installed
- [ ] [Docker Desktop](https://docker.com/products/docker-desktop) running
- [ ] Python 3.11+
- [ ] 16GB+ RAM (32GB recommended)
- [ ] A public GitHub repository for your portfolio
- [ ] Node.js 18+ (for PromptFoo in later labs)

## 11 Labs Covered

| # | Lab | Key Concepts |
|---|-----|-------------|
| 01 | Local LLM Deployment | Token, Context Window, Prompt Engineering |
| 02 | Embeddings & Vector DB | Embedding, Similarity Search, ChromaDB/Qdrant |
| 03 | Full RAG Pipeline | RAG, Chunking, RAGAS Evaluation |
| 04 | Agentic RAG | ReAct, Routing, Autonomous Agents |
| 05 | MCP Integration | Model Context Protocol, Tool Use, Function Calling |
| 06 | Fine-tuning | LoRA, QLoRA, Dataset Preparation |
| 07 | ML Prediction | Feature Engineering, FastAPI, XGBoost |
| 08 | Multi-Agent Orchestration | Supervisor Pattern, Agent Communication |
| 09 | Token Optimization | Chunking Strategies, Cost Management |
| 10 | Capstone Project | Full Platform Integration |
| 11 | LLM Monitoring | Opik, LangFuse, RAGAS, Guardrails, Grafana |

## Customization

### Adapt to Your Profile

Edit the **MY PROFILE** section in SKILL.md to match your background:

```markdown
## MY PROFILE
- [Your current role and expertise]
- I know: [your existing skills]
- I don't know yet: [what you want to learn]
- Final goal: [your target role]
- Constraint: [your timeline]
```

### Adapt Enterprise Context

Edit the **SIMULATED ENTERPRISE CONTEXT** section to match your industry.
The default is industrial maintenance, but you can change it to:
- Healthcare, Finance, E-commerce, Logistics, etc.
- Just update the data sources and scenarios to match your domain.

## License

MIT
