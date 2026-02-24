# Lab 02 — Embeddings & Vector Database

## Objective
Transform technical documentation into vector embeddings and index them in a vector database for semantic search.

## Concepts Covered
- Embedding: text to numerical vector representation
- Vector Database: optimized storage for similarity search
- Similarity metrics: cosine, dot product, euclidean

## Enterprise Scenario
Index all technical procedures, equipment manuals, and safety norms. Enable semantic search: find the right procedure even with imprecise or natural language queries.

## Steps
1. Deploy ChromaDB or Qdrant locally via Docker
2. Generate sample maintenance documentation
3. Create embeddings using sentence-transformers or Ollama
4. Index documents into the vector database
5. Query by semantic similarity
6. Compare embedding models and their impact on search quality

## Deliverable
Semantic search engine on technical documentation.

## Tech Stack
- ChromaDB or Qdrant (Docker)
- sentence-transformers / Ollama embeddings
- Python
