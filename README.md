<div align="center">

# FHRouter — Free LLM API

**Frontier AI models. Free for everyone.**

[![Website](https://img.shields.io/badge/fhrouter.com-free_LLM_API-10b981?style=flat-square)](https://fhrouter.com)
[![Free tier](https://img.shields.io/badge/free_tier-no_credit_card-10b981?style=flat-square)](https://fhrouter.com/free-llm-api)
[![OpenAI compatible](https://img.shields.io/badge/API-OpenAI_compatible-6366f1?style=flat-square)](https://fhrouter.com/docs/api-reference)

[Website](https://fhrouter.com) · [Free LLM API](https://fhrouter.com/free-llm-api) · [Pricing](https://fhrouter.com/pricing) · [Docs](https://fhrouter.com/docs) · [Blog](https://fhrouter.com/blog)

</div>

---

FHRouter is a **free LLM API and AI gateway** that puts frontier-class AI models — Grok, DeepSeek, and GLM families — **free on every account**, behind one [OpenAI-compatible](https://fhrouter.com/docs/api-reference) endpoint. No credit card, no expiring trial, no per-provider signup: create an account, generate one API key, and call any model on the gateway.

If you can use the OpenAI SDK, you can use FHRouter — change the base URL and key, and everything else works: streaming, tool calls, embeddings, error shapes.

## What you get for free

The [free LLM API tier](https://fhrouter.com/free-llm-api) includes frontier-class models on every account:

| Model | Family | Free |
|---|---|---|
| `grok-4.6` | xAI Grok | ✅ |
| `deepseek-v4-flash` | DeepSeek V4 | ✅ |
| `glm-5.3-flash` | GLM / Zhipu | ✅ |

The free set rotates over time — the [live catalog](https://fhrouter.com/free-llm-api) always shows the current list. Free usage is subject to fair-use limits; every other model on the gateway runs pay-as-you-go at **up to 50% below list prices**.

## Quickstart

**curl:**

```bash
curl https://fhrouter.com/v1/chat/completions \
  -H "Authorization: Bearer $FHROUTER_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model":"grok-4.6","messages":[{"role":"user","content":"Hello"}]}'
```

**Python (OpenAI SDK):**

```python
from openai import OpenAI

client = OpenAI(
    base_url="https://fhrouter.com/v1",
    api_key="fh-...",
)

response = client.chat.completions.create(
    model="deepseek-v4-flash",
    messages=[{"role": "user", "content": "Hello"}],
)
```

## Works with the tools you already use

FHRouter speaks the native protocols of the major AI CLIs and agents:

- [Claude Code setup](https://fhrouter.com/docs/guides/claude-code) — point it at FHRouter with one settings file
- [Codex CLI setup](https://fhrouter.com/docs/guides/codex) — OpenAI-compatible out of the box
- [Gemini CLI setup](https://fhrouter.com/docs/guides/gemini) — via the Gemini-native endpoint
- [Zed](https://fhrouter.com/docs/advanced/zed), [OpenCode](https://fhrouter.com/docs/advanced/opencode), [Kilo Code](https://fhrouter.com/docs/advanced/kilo-code), [Claude Desktop](https://fhrouter.com/docs/advanced/claude-desktop), [OpenClaw](https://fhrouter.com/docs/advanced/openclaw), [curl examples](https://fhrouter.com/docs/advanced/curl)

## Why a free LLM API gateway?

Most free tiers hand you small open-weight models and tight rate limits. FHRouter's bet is different: a **rotating set of frontier-class models that are simply free**, one key for the whole gateway, and honest pay-as-you-go pricing (up to 50% below list) for everything else.

Read the comparison: [Free LLM API providers in 2026: what's actually free](https://fhrouter.com/blog/free-llm-api-providers-2026) — an honest look at Google AI Studio, Groq, Cerebras, OpenRouter, Cloudflare, Mistral, GitHub Models, and where FHRouter fits.

## FAQ

**Is there a completely free LLM API?**
Yes — FHRouter includes frontier-class models free on every account, no credit card. See [how free models work](https://fhrouter.com/docs/free-models).

**Can I use a free LLM API with Claude Code or Codex CLI?**
Yes — [Claude Code](https://fhrouter.com/docs/guides/claude-code), [Codex](https://fhrouter.com/docs/guides/codex), and [Gemini CLI](https://fhrouter.com/docs/guides/gemini) setup guides take about three minutes.

**Is FHRouter OpenAI SDK compatible?**
Fully — base URL `https://fhrouter.com/v1`, streaming, tool calls, and OpenAI-shaped errors. [API reference](https://fhrouter.com/docs/api-reference).

**What's the catch with the free tier?**
Fair-use limits and a rotating free set. No expiring trial credits, and your credit balance is never touched by free models.

## Links

- [fhrouter.com](https://fhrouter.com) — the gateway
- [Free LLM API](https://fhrouter.com/free-llm-api) — the free tier, explained
- [Model pricing](https://fhrouter.com/pricing) — every model, up to 50% below list
- [Docs](https://fhrouter.com/docs) — setup, troubleshooting, API reference
- [Benchmarks](https://fhrouter.com/benchmarks) · [Rankings](https://fhrouter.com/rankings) · [Status](https://fhrouter.com/status)
- [Blog](https://fhrouter.com/blog) — guides and honest comparisons

---

<div align="center">
<sub>This repository is the public presence of <a href="https://fhrouter.com">FHRouter</a>. The service runs at fhrouter.com — sign up and start calling frontier models for free in minutes.</sub>
</div>
