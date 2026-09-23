# Hi, I'm [shu0819-sjy]

Second-year Computer Science undergraduate at the a CS undergraduate program.

I build solo at the LLM application layer — multi-model orchestration, failure handling, deployed RAG — moving from using tools to understanding them. The repositories below are the working evidence.

## Projects

### llm-router — multi-model orchestration with failure handling

[shu0819-sjy/llm-router](https://github.com/shu0819-sjy/llm-router)

OpenAI-compatible LLM gateway built on FastAPI and asyncio. Serves Chat Completions (JSON and SSE) and a Models list behind one `/v1` endpoint; routes requests across OpenAI, Anthropic, DeepSeek, and Qwen; fails over between providers with a timeout budget and circuit breaker. Adds per-key token-bucket rate limiting, a SQLite usage/cost ledger, health and Prometheus endpoints, and Docker Compose deployment. GitHub Actions CI gates every push on ruff, mypy, and pytest coverage.

### mini-rag-from-scratch — RAG, deployed first, then rebuilt from first principles

[shu0819-sjy/mini-rag-from-scratch](https://github.com/shu0819-sjy/mini-rag-from-scratch)

After deploying a RAG application on Dify, I rebuilt the retrieval loop without a framework to see each step I had been delegating: fixed-size chunking with overlap, sentence-transformers embeddings, NumPy cosine top-k retrieval, and a recall@1/3/5 evaluation over a built-in corpus. No vector DB, no framework — just the retrieval loop.

### langgraph-tool-agent — agent pipelines with bounded failure handling

[shu0819-sjy/langgraph-tool-agent](https://github.com/shu0819-sjy/langgraph-tool-agent)

A minimal tool-calling agent on a LangGraph StateGraph, wired to local tools (calculator, current time, mock lookup). Demonstrates bounded failure handling: a tool returns an error, the agent retries once under a fixed policy, then degrades to a graceful fallback answer instead of crashing the run.

### byo-redis — systems fundamentals under the LLM stack

[shu0819-sjy/byo-redis](https://github.com/shu0819-sjy/byo-redis)

A Redis server written from scratch in Python asyncio: RESP wire protocol, RDB snapshots, AOF persistence, and master/replica replication. Built to understand the storage layer that caching and retrieval systems depend on.

### guangyu-photo-lab — applied tooling

[shu0819-sjy/guangyu-photo-lab](https://github.com/shu0819-sjy/guangyu-photo-lab)

An AI-assisted photo-retouching tool (光屿 PHOTO LAB).

## Notes

- (omitted)
- (omitted)

## Notes

(contact via GitHub)
