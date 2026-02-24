# Lab 04 — Agentic RAG

## Objective
Transform the simple RAG pipeline into an agentic system that autonomously decides which sources to query.

## Concepts Covered
- Agentic AI: autonomous reasoning and planning
- ReAct pattern: Reason + Act loop
- Routing: dynamic source selection based on query analysis
- Tool use: agent calling external tools

## Enterprise Scenario
The agent receives a question and autonomously decides whether to search in:
- Ticket history (for similar past incidents)
- Technical documentation (for procedures)
- Equipment logs (for performance metrics)
- Knowledge base (for best practices)

## Steps
1. Implement a query classifier/router
2. Build the ReAct reasoning loop
3. Connect multiple retrieval sources
4. Implement source selection logic
5. Add self-reflection (did the retrieved context answer the question?)
6. Test with ambiguous queries requiring multi-source retrieval

## Deliverable
Autonomous multi-source RAG agent.

## Tech Stack
- LangChain Agents or LlamaIndex Agents
- Ollama
- Multiple vector collections
- Python
