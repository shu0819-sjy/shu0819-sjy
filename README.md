# Hi, I'm [shu0819-sjy](https://github.com/shu0819-sjy)

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

### dsh-auto-continue — self-healing turn loop for an LLM harness

[shu0819-sjy/dsh-auto-continue](https://github.com/shu0819-sjy/dsh-auto-continue)

A plugin pair for DeepSeek Harness (DSH) that resumes an agent turn automatically after recoverable failures: a hard-failure chain (timeout/network/5xx error whitelist, exponential backoff, at most 3 attempts) and a soft chain that re-drives the turn after an anti-repetition circuit break (at most 2). Ships with anti-race fences, human-veto reset, subagent skip, tests across mock / real-kernel integration / static suites, and idempotent installers for Windows and Unix.

### byo-redis — systems fundamentals under the LLM stack

[shu0819-sjy/byo-redis](https://github.com/shu0819-sjy/byo-redis)

A Redis server written from scratch in Python asyncio: RESP wire protocol, RDB snapshots, AOF persistence, and master/replica replication. Built to understand the storage layer that caching and retrieval systems depend on.

### guangyu-photo-lab — applied tooling

[shu0819-sjy/guangyu-photo-lab](https://github.com/shu0819-sjy/guangyu-photo-lab)

An AI-assisted photo-retouching tool (光屿 PHOTO LAB).

### agent-loop-guard — repetition and tool-loop circuit breakers

[shu0819-sjy/agent-loop-guard](https://github.com/shu0819-sjy/agent-loop-guard)

Zero-dependency TypeScript guards that stop LLM-agent text repetition loops and identical tool-call thrash — host-agnostic streaming detectors plus a pre-execute tool-loop hard kill.
