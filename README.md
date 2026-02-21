# LLM Gateway API

Unified LLM routing gateway with automatic fallbacks, semantic caching, and cost tracking.

## Providers
- OpenAI (GPT-4o, GPT-4o-mini)
- Anthropic (Claude 3.5 Sonnet, Haiku)
- Groq (Llama 3.1, Mixtral)
- Ollama (local models)

## Features
- Smart routing by cost/latency/capability
- Redis semantic caching (60-80% cost reduction)
- Automatic fallback chains
- Per-request cost tracking
- Rate limiting per API key

## Stack
FastAPI · Redis · PostgreSQL · Docker · Prometheus

```bash
docker-compose up -d
curl -X POST http://localhost:8000/v1/chat -d '{"model":"auto","messages":[...]}'
```