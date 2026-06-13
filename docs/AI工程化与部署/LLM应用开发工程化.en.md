# Engineering LLM Applications

## Introduction

- Source: [OpenAI Cookbook](https://cookbook.openai.com/)、[Anthropic Building with the Claude API](https://www.anthropic.com/engineering/building-effective-agents)、[Full Stack LLM Bootcamp](https://fullstackdeeplearning.com/llm-bootcamp/)
- Prerequisites: Python basics, understanding of LLM API calls, basic web development knowledge
- Programming language: Python
- Course difficulty: 🌟🌟🌟
- Estimated study hours: 20+

Calling an LLM API to build a demo is easy, but making an LLM application **production-ready** is a completely different story. This course covers engineering practices for LLM application development: how to design reliable API call layers, handle streaming output, implement error handling and retries, control costs, and evaluate output quality.

These skills are the key leap from "toy project" to "real product." Andrew Ng repeatedly emphasized at Buildathon: the core capability of an AI engineer isn't tuning models — it's **building reliable AI systems**.

## Course Resources

- Documentation: [OpenAI Cookbook](https://cookbook.openai.com/) — OpenAI's official code example collection covering various use cases
- Documentation: [Anthropic API Documentation](https://docs.anthropic.com/) — Claude API official docs with rich engineering practices
- Course: [Full Stack LLM Bootcamp (Stanford)](https://fullstackdeeplearning.com/llm-bootcamp/) — Stanford's free course covering full-stack LLM application development

## Resource Summary

**API call engineering:**

- [OpenAI Cookbook - API best practices](https://cookbook.openai.com/examples/) — Streaming output, error handling, retry strategies, concurrent requests
- [Anthropic - Streaming Messages](https://docs.anthropic.com/en/docs/build-with-claude/streaming) — Streaming output implementation guide
- [tenacity (Python retry library)](https://github.com/jd/tenacity) — Add exponential backoff retries to API calls
- [LiteLLM](https://github.com/BerriAI/litellm) — Unified API interface for 100+ LLM providers, avoid vendor lock-in

**Cost management:**

- [OpenAI Cookbook - Managing Costs](https://cookbook.openai.com/examples/how_to_handle_rate_limits) — Rate limiting, budget control, token counting
- [tiktoken (OpenAI Token Counter)](https://github.com/openai/tiktoken) — Precisely calculate token usage before API calls
- [Token cost calculator](https://github.com/AgentOps-AI/tokencost) — Unified token cost calculation across models

**Output quality assurance:**

- [Structured Output (OpenAI)](https://platform.openai.com/docs/guides/structured-outputs) — Enforce specific JSON format from model output
- [Instructor (Python)](https://github.com/instructor-ai/instructor) — Pydantic-based structured output library
- [Guardrails AI](https://github.com/guardrails-ai/guardrails) — Framework for validating and filtering LLM output
- [LMQL](https://lmql.ai/) — Embed constraints and logic directly in prompts

**Evaluation and monitoring:**

- [LangSmith (LangChain)](https://www.langchain.com/langsmith) — Debugging, testing, and monitoring platform for LLM applications
- [Braintrust](https://www.braintrust.dev/) — LLM evaluation platform with automated testing support
- [OpenEvals (LangChain)](https://github.com/langchain-ai/openevals) — Open-source LLM evaluation framework
- [DeepEval](https://github.com/confident-ai/deepeval) — pytest-like testing framework for LLMs

**Web framework integration:**

- [FastAPI](https://fastapi.tiangolo.com/) — The go-to Python framework for building LLM backend services
- [Streamlit](https://streamlit.io/) — Quickly build front-end interfaces for LLM applications
- [Gradio](https://www.gradio.app/) — Quickly create interactive demos for ML/AI models
- [Next.js + Vercel AI SDK](https://sdk.vercel.ai/) — Full-stack LLM application development

## Notes

Engineering capability is the key differentiator between "can use AI" and "AI engineer." Recommended path: first build a simple backend with FastAPI + OpenAI API → add streaming output → add error handling and retries → add cost monitoring → add evaluation. With each addition, your understanding of production-grade AI systems deepens.

Don't neglect evaluation — an LLM application without evaluation is like software without tests. You'll never know when it breaks in production.
