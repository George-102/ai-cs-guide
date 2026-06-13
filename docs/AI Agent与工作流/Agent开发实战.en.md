# Agent Development in Practice

## Introduction

- Source: [Andrew Ng Agentic AI Series](https://learn.deeplearning.ai/courses/ai-agents)、[LangGraph Official Documentation](https://langchain-ai.github.io/langgraph/)、[Anthropic Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents)
- Prerequisites: Python basics, understanding of LLM API calls, basic understanding of RAG concepts
- Programming language: Python
- Course difficulty: 🌟🌟🌟🌟
- Estimated study hours: 30+

**AI Agents** are the most central direction in AI application development today. If RAG solves "what the model knows," Agents solve "what the model does" — they can **autonomously plan, use tools, and execute multi-step tasks**, not just answer questions.

Core components of an Agent system:
- **LLM (brain)**: Responsible for reasoning and decision-making
- **Tools (hands)**: Search, code execution, API calls, file operations, etc.
- **Memory (notebook)**: Short-term (conversation history) + Long-term (persistent knowledge)
- **Planning (chain of thought)**: Decomposing complex tasks into executable steps

Andrew Ng repeatedly emphasized in his 2024-2025 course series: **Agentic workflows are the most important paradigm shift in AI application development**. Moving from simple single API calls to Agents that can autonomously complete multi-step tasks is a capability every AI engineer must master.

## Course Resources

- Course: [Andrew Ng - AI Agents in LangGraph](https://learn.deeplearning.ai/courses/ai-agents-langgraph) — Free short course, hands-on with the LangGraph framework
- Documentation: [LangGraph Documentation](https://langchain-ai.github.io/langgraph/) — The most mainstream multi-agent orchestration framework
- Article: [Anthropic - Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) — Anthropic's official Agent design guide, required reading

## Resource Summary

**Beginner (understanding core Agent concepts):**

- [Andrew Ng - Agentic Design Patterns (4 courses)](https://learn.deeplearning.ai/courses/ai-agents) — Covers Reflection, Tool Use, Planning, and Multi-Agent patterns, highly recommended
- [Lilian Weng - LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) — One of the most comprehensive Agent technical surveys
- [ReAct: Synergizing Reasoning and Acting in LLMs](https://arxiv.org/abs/2210.03629) — The original ReAct paper, understand the reasoning+action loop paradigm

**Framework practice (pick one to go deep):**

- [LangGraph](https://langchain-ai.github.io/langgraph/) — State-graph-based Agent orchestration framework, supports loops, conditional branches, human-in-the-loop, the most flexible framework available
- [CrewAI](https://www.crewai.com/) — Multi-agent collaboration framework with clear role division, quick to get started
- [AutoGen (Microsoft)](https://microsoft.github.io/autogen/) — Microsoft's open-source multi-agent conversation framework
- [OpenAI Agents SDK](https://openai.github.io/openai-agents-python/) — OpenAI's official Agent SDK, lightweight
- [smolagents (HuggingFace)](https://huggingface.co/docs/smolagents/) — Minimalist Agent framework, small codebase, great for learning principles

**Tool Use (Tool Use / Function Calling):**

- [OpenAI Function Calling Guide](https://platform.openai.com/docs/guides/function-calling) — Understand how LLMs call external tools
- [LangChain Tools & Toolkits](https://python.langchain.com/docs/modules/agents/tools/) — Rich collection of pre-built tools
- [MCP (Model Context Protocol)](https://modelcontextprotocol.io/) — Anthropic's standardized tool protocol, the most important Agent infrastructure of 2025

**Multi-Agent Systems:**

- [Andrew Ng - Multi-Agent Collaboration](https://learn.deeplearning.ai/courses/multi-ai-agent-systems-with-crewai) — CrewAI framework + multi-agent collaboration
- [AutoGen Agent Chat](https://microsoft.github.io/autogen/docs/tutorial/introduction) — Multi-agent conversation and collaboration
- [MetaGPT](https://github.com/geekan/MetaGPT) — Agent system simulating multi-role software company collaboration

**Memory Systems:**

- [LangMem (LangChain Memory)](https://langchain-ai.github.io/langmem/) — LangChain's official long-term memory solution
- [Mem0](https://mem0.ai/) — Intelligent memory layer designed specifically for AI Agents
- [Letta (MemGPT)](https://www.letta.com/) — Brings OS memory management concepts into Agent memory

## Notes

Agent development has a steep learning curve. Recommended path: first understand the ReAct paradigm (reasoning+action loop) → build a single Agent with LangGraph → add tool calls → add memory → try multi-agent collaboration.

Don't start with advanced frameworks. First hand-write a simple Agent with pure Python + OpenAI API (~100 lines of code) to understand what's happening at each step, then use frameworks to improve efficiency. This is the same principle as learning programming — write it by hand first, then use libraries.
