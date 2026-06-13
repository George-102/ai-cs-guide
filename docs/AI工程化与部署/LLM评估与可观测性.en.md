# LLM Evaluation and Observability

## Introduction

- Source: [OpenEvals](https://github.com/langchain-ai/openevals)、[RAGAS](https://docs.ragas.io/)、[DeepEval](https://github.com/confident-ai/deepeval)
- Prerequisites: Python basics, understanding of LLM API calls
- Programming language: Python
- Course difficulty: 🌟🌟🌟🌟
- Estimated study hours: 15+

Traditional software testing has clear pass/fail criteria, but LLM output is natural language — how do you judge whether it's right? This is what **LLM evaluation** solves.

LLM evaluation is the most underestimated aspect of AI engineering. Without evaluation, you cannot:
- Know whether your prompt changes actually improved results
- Detect whether your RAG system is retrieving wrong documents
- Determine if the model is hallucinating in specific scenarios
- Prove to your team/users that your AI system is trustworthy

## Course Resources

- Documentation: [RAGAS Documentation](https://docs.ragas.io/) — Focused on RAG system evaluation
- Documentation: [DeepEval Documentation](https://docs.confident-ai.com/) — pytest-like LLM testing framework
- Paper: [Holistic Evaluation of Language Models (HELM)](https://arxiv.org/abs/2211.09110) — Stanford's comprehensive LLM evaluation framework

## Resource Summary

**Evaluation methodology:**

- [OpenEvals (LangChain)](https://github.com/langchain-ai/openevals) — Open-source evaluation framework with custom evaluator support
- [RAGAS](https://docs.ragas.io/) — Specifically evaluates RAG system quality (faithfulness, relevance, precision)
- [DeepEval](https://github.com/confident-ai/deepeval) — Write LLM tests like pytest
- [Promptfoo](https://www.promptfoo.dev/) — Command-line LLM evaluation tool, supports cross-model comparison

**Evaluation dimensions:**

| Dimension | Meaning | Tool |
|-----------|---------|------|
| **Faithfulness** | Whether the answer is based on retrieved documents, not fabricated | RAGAS |
| **Relevance** | Whether retrieved documents are relevant to the question | RAGAS |
| **Correctness** | Whether the answer is factually correct | LLM-as-Judge |
| **Safety** | Whether it contains harmful content | OpenAI Moderation API |
| **Fluency** | Whether the language is natural and fluent | Human evaluation |
| **Latency** | Whether response time is acceptable | Custom monitoring |

**LLM-as-Judge (using LLMs to evaluate LLMs):**

- [OpenAI Cookbook - LLM-as-Judge](https://cookbook.openai.com/examples/evaluation/use_llms_to_evaluate_llms) — Use strong models to evaluate weaker models' output
- [JudgeLM](https://github.com/baaivision/JudgeLM) — Purpose-built judge model
- Note: LLM-as-Judge itself has biases and requires human calibration

**Observability:**

- [LangSmith](https://www.langchain.com/langsmith) — Tracing, debugging, and monitoring for LLM applications
- [LangFuse](https://langfuse.com/) — Open-source LLM observability platform with tracing, evaluation, and prompt management
- [Weights & Biases (W&B)](https://wandb.ai/) — ML experiment tracking, also supports LLM evaluation tracking
- [OpenTelemetry for LLM](https://opentelemetry.io/) — Standardized telemetry data for LLM applications

**Evaluation datasets:**

- [MMLU](https://arxiv.org/abs/2009.03300) — Massive Multitask Language Understanding benchmark
- [HumanEval](https://arxiv.org/abs/2107.03374) — Code generation capability evaluation
- [MT-Bench](https://arxiv.org/abs/2306.05685) — Multi-turn conversation capability evaluation
- [AlpacaEval](https://github.com/tatsu-lab/alpaca_eval) — Instruction-following capability evaluation

## Notes

Evaluation is the foundation of iterative development. Without evaluation data, your improvements are "feels better" not "measurably better." Build the evaluation habit from the start: every time you change a prompt or switch models, run the evaluation suite and let data drive decisions.

Getting started: first use RAGAS to evaluate your RAG system (5 minutes to get started), then use DeepEval to write test cases for your LLM application. Together these two tools cover most evaluation needs.
