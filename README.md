# Hi, I'm [shu0819-sjy](https://github.com/shu0819-sjy)

I build small tools around LLM applications and spend a lot of time on the parts that are easy to skip: retries, failure handling, retrieval quality, and simple deployment setups.

Most of the repositories here are personal projects or learning builds. Some are rough around the edges, and the README is not always perfectly in sync with the latest code. That is part of the point: I keep the experiments public so I can come back to them, improve them, and see what I actually learned.

## What I'm working on

- Making tool-calling agents fail in predictable ways instead of getting stuck in loops.
- Keeping several model providers behind one small, OpenAI-compatible API.
- Rebuilding familiar infrastructure from scratch to understand the layers underneath.

## Tools I use most

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-18%2B-339933?logo=nodedotjs&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)

## Selected projects

### Agent tooling

#### [agent-loop-guard](https://github.com/shu0819-sjy/agent-loop-guard)

[![CI](https://github.com/shu0819-sjy/agent-loop-guard/actions/workflows/ci.yml/badge.svg)](https://github.com/shu0819-sjy/agent-loop-guard/actions/workflows/ci.yml)

A dependency-free TypeScript guard for repeated assistant text and identical tool calls. It is intentionally host-agnostic so it can sit in front of different agent runtimes.

#### [llm-router](https://github.com/shu0819-sjy/llm-router)

[![CI](https://github.com/shu0819-sjy/llm-router/actions/workflows/ci.yml/badge.svg)](https://github.com/shu0819-sjy/llm-router/actions/workflows/ci.yml)

An OpenAI-compatible FastAPI gateway for several providers, with failover, circuit breaking, rate limits, and a small SQLite usage ledger. The main goal is to keep the routing layer understandable.

#### [dsh-auto-continue](https://github.com/shu0819-sjy/dsh-auto-continue)

[![CI](https://github.com/shu0819-sjy/dsh-auto-continue/actions/workflows/ci.yml/badge.svg)](https://github.com/shu0819-sjy/dsh-auto-continue/actions/workflows/ci.yml)

A DeepSeek Harness plugin for resuming recoverable failures and stopping repeated turns. It includes retry limits and a human veto because automatic recovery should still have a clear stop condition.

### From-scratch builds

#### [mini-rag-from-scratch](https://github.com/shu0819-sjy/mini-rag-from-scratch)

[![CI](https://github.com/shu0819-sjy/mini-rag-from-scratch/actions/workflows/ci.yml/badge.svg)](https://github.com/shu0819-sjy/mini-rag-from-scratch/actions/workflows/ci.yml)

A small RAG implementation without a vector database: chunking, sentence-transformer embeddings, NumPy cosine retrieval, and recall checks over a built-in corpus.

#### [byo-redis](https://github.com/shu0819-sjy/byo-redis)

[![CI](https://github.com/shu0819-sjy/byo-redis/actions/workflows/ci.yml/badge.svg)](https://github.com/shu0819-sjy/byo-redis/actions/workflows/ci.yml)

A Python asyncio Redis-style server covering RESP, RDB snapshots, AOF persistence, and basic master/replica replication. It is a learning implementation, not a replacement for Redis.

#### [langgraph-tool-agent](https://github.com/shu0819-sjy/langgraph-tool-agent)

[![CI](https://github.com/shu0819-sjy/langgraph-tool-agent/actions/workflows/ci.yml/badge.svg)](https://github.com/shu0819-sjy/langgraph-tool-agent/actions/workflows/ci.yml)

A minimal LangGraph tool-calling example with one bounded retry and a fallback path. I keep this one small on purpose so the control flow is easy to inspect.

### Other experiments

- [guangyu-photo-lab](https://github.com/shu0819-sjy/guangyu-photo-lab) — a small browser-based photo retouching tool.
- [super-mario-audio](https://github.com/shu0819-sjy/super-mario-audio) — a Source Academy game build with an external audio pipeline.
- [codex-fusion](https://github.com/shu0819-sjy/codex-fusion) — a local companion for experimenting with Codex themes and effects.

## Notes

I prefer small, inspectable projects over a large demo repository. If a project looks unfinished, it probably is; the unfinished parts are usually more useful to me than a polished claim that hides the trade-offs.
