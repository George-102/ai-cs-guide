# Agent 开发实战

## 简介

- 来源：[Andrew Ng Agentic AI 系列](https://learn.deeplearning.ai/courses/ai-agents)、[LangGraph 官方文档](https://langchain-ai.github.io/langgraph/)、[Anthropic Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents)
- 先修要求：Python 基础、了解 LLM API 调用、了解 RAG 基本概念
- 编程语言：Python
- 课程难度：🌟🌟🌟🌟
- 预计学时：30 小时 +

**AI Agent** 是当前 AI 应用开发最核心的方向。如果说 RAG 解决了"让模型知道什么"，Agent 解决的是"让模型做什么"——它能**自主规划、使用工具、执行多步骤任务**，而不只是回答问题。

一个 Agent 系统的核心组件：
- **LLM（大脑）**：负责推理和决策
- **工具（手）**：搜索、代码执行、API 调用、文件操作等
- **记忆（笔记本）**：短期（对话历史）+ 长期（持久化知识）
- **规划（思维链）**：将复杂任务分解为可执行步骤

吴恩达在 2024-2025 年的系列课程中反复强调：**Agentic 工作流是 AI 应用开发最重要的范式转变**。从简单的单次 API 调用，到能自主完成多步骤任务的 Agent，这是 AI 工程师必须掌握的能力。

## 课程资源

- 课程：[吴恩达 - AI Agents in LangGraph](https://learn.deeplearning.ai/courses/ai-agents-langgraph) — 免费短期课程，LangGraph 框架实战
- 文档：[LangGraph Documentation](https://langchain-ai.github.io/langgraph/) — 最主流的多智能体编排框架
- 文章：[Anthropic - Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) — Anthropic 官方 Agent 设计指南，必读

## 资源汇总

**入门（理解 Agent 核心概念）：**

- [吴恩da - Agentic Design Patterns (4 个课程)](https://learn.deeplearning.ai/courses/ai-agents) — 覆盖 Reflection、Tool Use、Planning、Multi-Agent 四大模式，强烈推荐
- [Lilian Weng - LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) — 最全面的 Agent 技术综述之一
- [ReAct: Synergizing Reasoning and Acting in LLMs](https://arxiv.org/abs/2210.03629) — ReAct 原论文，理解 Agent 推理+行动的基本范式

**框架实战（选一个深入学习）：**

- [LangGraph](https://langchain-ai.github.io/langgraph/) — 基于状态图的 Agent 编排框架，支持循环、条件分支、人工介入，是目前最灵活的框架
- [CrewAI](https://www.crewai.com/) — 面向多智能体协作的框架，角色分工明确，上手快
- [AutoGen (Microsoft)](https://microsoft.github.io/autogen/) — 微软开源的多智能体对话框架
- [OpenAI Agents SDK](https://openai.github.io/openai-agents-python/) — OpenAI 官方 Agent SDK，轻量级
- [smolagents (HuggingFace)](https://huggingface.co/docs/smolagents/) — 极简 Agent 框架，代码量少，适合学习原理

**工具使用（Tool Use / Function Calling）：**

- [OpenAI Function Calling Guide](https://platform.openai.com/docs/guides/function-calling) — 理解 LLM 如何调用外部工具
- [LangChain Tools & Toolkits](https://python.langchain.com/docs/modules/agents/tools/) — 丰富的预置工具集合
- [MCP (Model Context Protocol)](https://modelcontextprotocol.io/) — Anthropic 推出的标准化工具协议，2025 年最重要的 Agent 基础设施

**多智能体系统：**

- [吴恩da - Multi-Agent Collaboration](https://learn.deeplearning.ai/courses/multi-ai-agent-systems-with-crewai) — CrewAI 框架 + 多智能体协作
- [AutoGen Agent Chat](https://microsoft.github.io/autogen/docs/tutorial/introduction) — 多智能体对话与协作
- [MetaGPT](https://github.com/geekan/MetaGPT) — 模拟软件公司多角色协作的 Agent 系统

**记忆系统：**

- [LangMem (LangChain Memory)](https://langchain-ai.github.io/langmem/) — LangChain 官方长期记忆解决方案
- [Mem0](https://mem0.ai/) — 专为 AI Agent 设计的智能记忆层
- [Letta (MemGPT)](https://www.letta.com/) — 将操作系统内存管理思想引入 Agent 记忆

## 备注

Agent 开发的学习曲线比较陡，建议路线：先理解 ReAct 范式（推理+行动循环）→ 用 LangGraph 搭一个单 Agent → 加入工具调用 → 加入记忆 → 尝试多智能体协作。

不要一上来就用高级框架。先用纯 Python + OpenAI API 手写一个简单的 Agent（100行代码），理解每一步在发生什么，再用框架提升效率。这和学编程时先手写再用车库是一个道理。
