# Lab 01 — Local LLM Deployment

## Objective
Deploy a local LLM (Ollama + Mistral/Llama) and configure it to answer domain-specific queries for an industrial maintenance company.

## Concepts Covered
- Token: base unit of text for LLMs
- Context Window: maximum tokens per request
- Prompt Engineering: crafting precise instructions
- Model parameters: temperature, top_p, max_tokens

## Enterprise Scenario
A field technician asks a technical question about equipment maintenance. The local LLM responds with domain-relevant answers.

## Steps
1. Install Ollama and pull Mistral model
2. Explore the Ollama API (chat, generate, embeddings endpoints)
3. Configure model parameters and understand their impact
4. Create a system prompt tailored to the maintenance domain
5. Test with realistic maintenance queries
6. Measure response latency and token consumption

## Deliverable
Local API responding to maintenance domain queries with configurable parameters.

## Tech Stack
- Ollama
- Mistral 7B / Llama 3
- Python (requests or ollama SDK)
