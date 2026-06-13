# Context Engineering Guide

## Introduction

- Source: [Context Engineering Github](https://github.com/davidkimai/Context-Engineering), [Philipp Schmid's Guide](https://www.philschmid.de/context-engineering), [Simon Willison's Analysis](https://simonwillison.net/2025/Jun/27/context-engineering/)
- Prerequisites: Understanding of prompt engineering basics, ability to call LLM APIs
- Course difficulty: 🌟🌟🌟🌟
- Estimated study hours: 15+

**Context Engineering** is a systematic discipline for designing and building dynamic context systems that provide LLMs with **everything they need** to complete tasks. It goes beyond the traditional prompt engineering focus of "writing a good instruction" and instead addresses how to provide the right information and tools to the model at the right time, in the right format.

Shopify CEO Tobi Lutke describes it as a core skill — the art of "providing all the context for the task to be plausibly solvable by the LLM." Andrej Karpathy positions it as a combination of science and art: in industrial-grade LLM applications, the core challenge is "filling the context window with just the right information for the next step."

**Why study Context Engineering?** Because in real-world AI application development, simply writing a good prompt is far from sufficient. A model's performance depends not only on what you say, but on what it sees — including conversation history, retrieved documents, available tools, memory state, and more. Context Engineering is the systematic methodology for solving the "what the model sees" problem. Research shows that most agent failures are no longer due to insufficient model capability, but to poor context design quality.

> Context is the complete information payload provided to a LLM at inference time, encompassing all structured informational components that the model needs to plausibly accomplish a given task.
>
> ——from a systematic analysis of 1400+ research papers

**Difference from Prompt Engineering:** Prompt Engineering focuses on "what to say" — the single instruction from the user; Context Engineering focuses on "what the model sees" — the complete information system including instructions, memory, retrieved information, tools, and output formats. A simple example: when you ask an AI "What's on my schedule tomorrow?", Prompt Engineering focuses on how to phrase the question; Context Engineering focuses on what information should be provided before the model responds — calendar data, email history, contact list, available tools, and more.

## Course Content Outline

### Module 1: Foundational Concepts

- **Definition and components of context**: Understanding the seven layers of context — Instructions (system prompt), User Prompt, short-term memory (conversation history), long-term memory (cross-conversation knowledge), retrieved information (RAG), available tools, structured output
- **Difference from Prompt Engineering**: The mental shift from "single string" to "complete information system"
- **Core principles of context**: Context is a system, not a single string; dynamically generated, not static templates; providing the right information at the right time

### Module 2: Core Techniques

- **Token budget optimization**: Maximizing information density within the limited context window; every token carries information cost
- **Few-Shot learning**: Teaching through a small number of high-quality examples, often outperforming purely explanatory approaches
- **Retrieval-Augmented Generation (RAG)**: Injecting relevant documents to reduce hallucinations; the key is retrieval quality
- **Memory systems**: Cross-turn state persistence enabling stateful interactions; modern memory systems achieve memory-reasoning synergy

### Module 3: Advanced Topics

- **Cognitive tools**: Structured reasoning patterns such as Chain-of-Thought (CoT), ReAct (Reasoning + Acting), etc.; research shows GPT-4.1 performance improvement of 16.6%
- **Prompt programming**: Code-like prompt composition patterns, including functional, procedural, and object-oriented approaches
- **Dynamic context generation**: Real-time context construction based on tasks, rather than static templates
- **Neural field theory and quantum semantics**: Frontier research directions treating context as a dynamic field

### Module 4: Practical Applications

- **Agent context design**: Building complete context systems for AI agents
- **Context quality assessment**: How to measure and improve context effectiveness
- **Case study analysis**: Context comparison in scenarios like scheduling agents (low quality vs. high quality)
- **Tool description engineering**: Writing clear tool definitions to improve model invocation capability

## Document Resources

- Websites: [Context Engineering Github](https://github.com/davidkimai/Context-Engineering) (with 12-week curriculum), [Philipp Schmid's Practical Guide](https://www.philschmid.de/context-engineering), [Simon Willison's Analysis](https://simonwillison.net/2025/Jun/27/context-engineering/)
- Papers: [Context Engineering Survey (1400+ papers)](https://arxiv.org/pdf/2507.13334), [IBM Zurich Cognitive Tools](https://arxiv.org/pdf/2506.12115), [MEM1 Memory-Reasoning Synergy](https://arxiv.org/pdf/2506.15841), [LLM Attractors](https://arxiv.org/pdf/2502.15208)
- Supplementary: The repository provides `minimal_context.yaml` templates and `00_toy_chatbot/` complete implementation examples for quick start

## Resource Summary

Context Engineering represents a paradigm shift in AI application development — from focusing on "what to say" to focusing on "what the model sees." For computer science students, mastering this skill means being able to build more reliable and intelligent AI systems. Start with understanding the components of context, progressively explore core techniques like RAG, memory systems, and cognitive tools, and ultimately develop your own context engineering methodology.
