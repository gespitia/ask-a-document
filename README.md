# Ask a Document

A focused reference implementation of a retrieval + grounded-answer pipeline. The default answer provider is deterministic: there is no hidden LLM call.

## Architecture
Question -> application use case -> retriever -> ranker -> selected context -> answer provider -> answer + trace.

Core owns document and retrieval rules. Application orchestrates the use case. Presentation renders results. The provider boundary allows a real LLM adapter to be introduced later without coupling it to retrieval.

## Why this is a project
The repository contains executable code, tests, architecture documentation and a deployable browser demo. It is intentionally small so the important boundaries remain visible.

## Run
npm install
npm run dev

## Test
npm test

## Limitations
Retrieval is keyword-based. The current answer provider is deterministic. This is not presented as a production RAG platform.

See docs/architecture.md and the ADRs.