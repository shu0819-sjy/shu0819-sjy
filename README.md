# Hi, I'm [shu0819-sjy](https://github.com/shu0819-sjy)

I build solo at the LLM application layer — multi-model orchestration, failure handling, deployed RAG — moving from using tools to understanding them. The repositories below are the working evidence.

## Tech stack

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-18%2B-339933?logo=nodedotjs&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?logo=langchain&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?logo=vitest&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?logo=pytest&logoColor=white)

## Projects

Jump to: [AI / Agent toolchain](#ai--agent-toolchain) · [Applications](#applications) · [Learning repositories](#learning-repositories)

### AI / Agent toolchain

Production-shaped guards, gateways, and harness plugins for reliable multi-model agent loops.

#### [agent-loop-guard](https://github.com/shu0819-sjy/agent-loop-guard)

[![CI](https://github.com/shu0819-sjy/agent-loop-guard/actions/workflows/ci.yml/badge.svg)](https://github.com/shu0819-sjy/agent-loop-guard/actions/workflows/ci.yml)

Zero-dependency TypeScript guards that hard-trip LLM-agent text repetition loops and identical tool-call thrash — host-agnostic streaming detectors plus a pre-execute tool-loop kill.

#### [llm-router](https://github.com/shu0819-sjy/llm-router)

[![CI](https://github.com/shu0819-sjy/llm-router/actions/workflows/ci.yml/badge.svg)](https://github.com/shu0819-sjy/llm-router/actions/workflows/ci.yml)

OpenAI-compatible LLM gateway on FastAPI and asyncio. One `/v1` surface across OpenAI, Anthropic, DeepSeek, and Qwen with failover, circuit breaking, rate limits, a SQLite usage ledger, and Docker Compose deploy. CI gates every push on ruff, mypy, and pytest coverage.

#### [dsh-auto-continue](https://github.com/shu0819-sjy/dsh-auto-continue)

[![CI](https://github.com/shu0819-sjy/dsh-auto-continue/actions/workflows/ci.yml/badge.svg)](https://github.com/shu0819-sjy/dsh-auto-continue/actions/workflows/ci.yml)

A DeepSeek Harness (DSH) plugin pair that resumes an agent turn after recoverable failures: hard-failure retries (timeout/network/5xx whitelist, exponential backoff) and soft resume after an anti-repetition circuit break, with anti-race fences and a human veto.

### Applications

Small applied tools outside the core agent stack.

#### [guangyu-photo-lab](https://github.com/shu0819-sjy/guangyu-photo-lab)

AI-assisted photo-retouching lab for batch polish workflows.

#### [super-mario-audio](https://github.com/shu0819-sjy/super-mario-audio)

Source Academy Arcade2D Super Mario build with an external audio pipeline and Raw URL assets.

### Learning repositories

From-scratch rebuilds that expose the layers usually hidden by frameworks.

#### [byo-redis](https://github.com/shu0819-sjy/byo-redis)

A Redis server in Python asyncio: RESP wire protocol, RDB snapshots, AOF persistence, and master/replica replication — systems fundamentals under the LLM stack.

#### [mini-rag-from-scratch](https://github.com/shu0819-sjy/mini-rag-from-scratch)

After deploying RAG on a managed stack, rebuilt the retrieval loop without a framework: fixed-size chunking with overlap, sentence-transformers embeddings, NumPy cosine top-k, and recall@1/3/5 over a built-in corpus.

#### [langgraph-tool-agent](https://github.com/shu0819-sjy/langgraph-tool-agent)

A minimal tool-calling agent on a LangGraph StateGraph with bounded failure handling: one retry under a fixed policy, then a graceful fallback instead of crashing the run.
