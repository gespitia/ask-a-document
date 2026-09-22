# Architecture

The system separates what should be retrieved from how an answer is produced.

1. core/document.ts defines the knowledge model.
2. core/retrieval.ts normalizes queries, scores candidates and ranks hits.
3. core/answer.ts creates a grounded response from selected evidence.
4. application/ask.ts composes the use case and exposes a retrieval trace.
5. The UI remains a thin presentation layer.

The trace is part of the output contract. That makes relevance decisions inspectable and testable.

A production evolution could replace keyword retrieval with embeddings/vector search and replace the deterministic provider with an LLM adapter while preserving the application boundary.