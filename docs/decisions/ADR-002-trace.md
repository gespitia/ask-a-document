# ADR-002: Retrieval trace

Decision: return selected chunks and scores with the answer.

Reason: retrieval quality needs to be inspectable during development and evaluation.

Consequence: the UI can expose the retrieval path without coupling core retrieval code to presentation.