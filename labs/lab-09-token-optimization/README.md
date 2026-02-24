# Lab 09 — Token & Context Window Optimization

## Objective
Implement advanced strategies for managing tokens and context windows to optimize cost and quality.

## Concepts Covered
- Chunking strategies: fixed, recursive, semantic
- Context compression: summarization chains, map-reduce
- Token budget management: cost tracking per request
- Context window comparison: 4K, 8K, 32K, 128K models

## Enterprise Scenario
A 50-page technical manual needs to be processed for RAG. Optimize the pipeline to minimize token cost while maintaining answer quality.

## Steps
1. Implement multiple chunking strategies and compare
2. Build summarization chains for long documents
3. Implement token counting and cost estimation per request
4. Compare model performance across context window sizes
5. Build a context compression pipeline
6. Create a cost/quality tradeoff dashboard

## Deliverable
Cost-optimized RAG pipeline with token metrics dashboard.

## Tech Stack
- tiktoken
- LangChain text splitters
- Ollama (multiple models)
- Python
