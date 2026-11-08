## Rustam Kohen

AI engineering, with a bias toward things I can measure. Master's student in Data
Engineering and Consulting at HS Albstadt-Sigmaringen. Right now I'm working toward three
skills, retrieval evaluation, guardrails and agent orchestration.

In October 2026 I passed Anthropic's Claude Certified Architect, Professional exam
(CCAR-P). [Verify on Credly](https://www.credly.com/badges/5b729a78-9d71-4b9d-a707-95d3a5aa2dab).

Most of what I build starts as a question I can't answer by reading the code.
Does this retriever actually retrieve? Does the guardrail block anything? Does the
context layout save a single byte? So the repos below open with a table of numbers.
Where I don't have a number yet, the README says so.

### Currently building

| Project | What it measures | Status |
|---|---|---|
| Doorman | prompt-injection guardrails, measured as attack-success rate before and after, against a red-team corpus and a benign control set | December 2026 |

One rule for every project, taken from a build plan I keep in my notes. A project counts once
it has an eval, a number, and a trade-off I can defend out loud.

### Selected work

[crm-data-cleanup](https://github.com/its-stam/crm-data-cleanup). Cleans messy CRM
exports before an import. Emails and phone numbers are normalized, junk is set aside
with a reason instead of deleted, and duplicates are merged across shared emails and
phone numbers with union-find. Hard checks stop the run if a single row or contact
detail would get lost, and a review page lets a person sign off before the import.
The approach comes from a real Zoho-to-Pipedrive migration (11,813 rows to 10,628
contacts); the repo runs on 2,000 generated rows. README in German, English summary
at the end.

[groundtruth](https://github.com/its-stam/groundtruth). Retrieval evaluation on
nine Stanford CS230 lecture transcripts. A checked golden set of 100 questions and
four configurations, one change at a time. Reranking is the only change that moves
recall@10, from 95 to 98 of 100.

[rag-chatbot-gruppe1](https://github.com/its-stam/rag-chatbot-gruppe1). A RAG
assistant over internal HR documents. pgvector with an HNSW index, overlapping
chunks, top-k retrieval, answers with source citations, and a fixed fallback when
retrieval comes back empty. Coursework, graded 1.0, 64 commits in three weeks.

[zollern-llm-vibn](https://github.com/its-stam/zollern-llm-vibn). A two-phase
agentic pipeline for an industrial partner. Parallel LLM agents with enforced tool
schemas turn a CAD assembly description into a feasibility report; there's an MCP
tool spec and a three-provider comparison on the same task. Phase two still waits
on a live simulation endpoint, and the README says that too.

[stam-os](https://github.com/its-stam/stam-os). A file layout that keeps an
agent's session context small and recoverable. Layer budgets, pre-action
guardrails, three-file recovery, and a script that measures what a session loads
at startup. 37 tests.

[grill-me-kimi](https://github.com/its-stam/grill-me-kimi). A second model from
another provider reviews a plan read-only, round by round, until it signs off or
hits the round cap.

[ai-sdlc](https://github.com/its-stam/ai-sdlc). Scores where a project stands
across six lifecycle stages and ranks the gaps by effort.

### Stack

Python, n8n, pgvector on Supabase, MCP, the Anthropic and OpenAI APIs, pytest.
German and English.
