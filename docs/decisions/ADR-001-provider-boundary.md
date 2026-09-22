# ADR-001: Provider boundary

Decision: keep answer generation behind a small provider boundary.

Reason: the demo must not imply an LLM is running when it is not. The boundary also keeps retrieval independently testable.

Consequence: the current provider is deterministic. A future model adapter can consume selected context and return an answer with source identifiers.