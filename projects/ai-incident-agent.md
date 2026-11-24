# SignalDesk — AI Incident Assistant

## One-line pitch
An AI assistant that helps an on-call engineer investigate a service incident by searching logs and runbooks, then returning a cited, human-reviewable investigation summary.

## Why this project
Shows applied AI, tool use, retrieval, API design, and product judgment. The system is advisory: it must ground claims in retrieved evidence and never execute remediation without approval.

## MVP
- FastAPI service with an incident investigation endpoint.
- Ingest a small synthetic set of service logs and Markdown runbooks.
- Retrieve relevant evidence and provide it to an LLM with structured tool calls.
- Return likely causes, supporting evidence, uncertainty, and suggested next checks.
- Persist investigations and show a simple web interface with source citations.
- Include deterministic mock mode so the demo works without paid API credentials.

## Suggested stack
Python, FastAPI, PostgreSQL with pgvector (or SQLite for the first local prototype), an LLM provider adapter, Docker, pytest, and a small React or server-rendered UI.

## Quality bar
- Every factual finding links to a log or runbook excerpt.
- Handle empty retrieval, malformed model output, timeouts, and prompt injection in source documents.
- Keep secrets out of logs; redact sensitive fields from ingested data.
- Evaluate retrieval and answer quality against a small labeled incident set.

## Build sequence
1. Define three synthetic incidents and their expected evidence.
2. Build ingestion and deterministic search first.
3. Add structured AI reasoning and citations behind a provider interface.
4. Add API, UI, persistence, and operational metrics.
5. Publish architecture, evaluation results, limitations, and a short demo.

## Resume bullet template
Built an AI incident assistant using [stack] that retrieves [data sources] and produces cited investigation summaries; evaluated on [N] scenarios, achieving [measured result].

## Status
Planned. Replace bracketed resume metrics only after measuring them.
