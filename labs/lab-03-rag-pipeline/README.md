# Lab 03 — Full RAG Pipeline

## Objective
Build a complete Retrieval-Augmented Generation pipeline combining local LLM (Lab 01) + Vector DB (Lab 02).

## Concepts Covered
- RAG: Retrieval-Augmented Generation
- Chunking: splitting documents into optimal segments
- RAGAS: RAG evaluation metrics (faithfulness, relevancy, recall, precision)
- Prompt augmentation: injecting retrieved context into LLM prompts

## Enterprise Scenario
A technician asks: "What is the procedure for replacing the hydraulic pump on press line 3?" The system retrieves relevant documentation chunks and generates a contextualized answer with source citations.

## Steps
1. Implement document chunking (fixed, recursive, semantic)
2. Build the retrieval pipeline (query → embed → search → rank)
3. Implement prompt augmentation with retrieved context
4. Build the generation step with source attribution
5. Create a RAGAS evaluation benchmark (50+ Q&A pairs)
6. Measure and optimize quality metrics

## Deliverable
RAG chatbot on technical documentation with quality metrics.

## Tech Stack
- LangChain or LlamaIndex
- Ollama + ChromaDB/Qdrant
- RAGAS
- Python
