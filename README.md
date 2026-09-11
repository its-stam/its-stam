## Rustam Kohen

AI engineering, with a bias toward systems that can be measured. M.Eng. Data
Engineering & Consulting (HS Albstadt-Sigmaringen), currently building toward
retrieval evaluation, guardrails and agent orchestration.

Most of what I build starts as a question I cannot answer by reading: does this
retriever actually retrieve, does this guardrail actually block, does this
context layout actually save anything. So the repos below tend to open with a
table of numbers rather than a feature list.

### Currently building

| Project | What it measures | Status |
|---|---|---|
| **Groundtruth** | retrieval evaluation: a hand-reviewed golden set, recall@10 / MRR / nDCG across chunking, hybrid search and reranking, a CI gate that fails on regression | starts October 2026 |
| **Doorman** | prompt-injection guardrails: attack-success rate before and after, measured against a red-team corpus and a benign control set | December 2026 |

Both follow a build plan I keep in my own notes: a project counts when it has an
eval, a number, and a trade-off I can defend out loud.

### Selected work

- **[rag-chatbot-gruppe1](https://github.com/its-stam/rag-chatbot-gruppe1)** — a
  RAG assistant over internal HR documents: pgvector with an HNSW index,
  overlapping chunks, top-k retrieval, answers with source citations and a fixed
  fallback instead of invention. Coursework, graded 1.0.
- **[zollern-llm-vibn](https://github.com/its-stam/zollern-llm-vibn)** — a
  two-phase agentic pipeline for an industrial partner: parallel LLM agents with
  enforced tool schemas turn a CAD assembly description into a structured
  feasibility report, plus an MCP tool specification and a three-provider
  comparison on the same task.
- **[stam-os](https://github.com/its-stam/stam-os)** — a file layout that keeps an
  agent's session context small and recoverable, with pre-action guardrails and a
  script that measures what a session loads at startup.
- **[grill-me-kimi](https://github.com/its-stam/grill-me-kimi)** — a plan is
  reviewed by a second model from a different provider, read-only, until it signs
  off or a round cap is hit.
- **[ai-sdlc](https://github.com/its-stam/ai-sdlc)** — scores where a project
  stands across the six stages of an AI-native development lifecycle, and ranks
  the gaps by effort.

### Stack

Python, n8n, pgvector / Supabase, MCP, the Anthropic and OpenAI APIs, pytest.
German and English, remote from Vietnam.
