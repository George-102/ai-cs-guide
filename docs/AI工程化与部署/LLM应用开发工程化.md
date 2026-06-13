# LLM 应用开发工程化

## 简介

- 来源：[OpenAI Cookbook](https://cookbook.openai.com/)、[Anthropic Building with the Claude API](https://www.anthropic.com/engineering/building-effective-agents)、[Full Stack LLM Bootcamp](https://fullstackdeeplearning.com/llm-bootcamp/)
- 先修要求：Python 基础、了解 LLM API 调用、了解基本的 Web 开发
- 编程语言：Python
- 课程难度：🌟🌟🌟
- 预计学时：20 小时 +

调用 LLM API 写个 demo 很简单，但把 LLM 应用做到**生产可用**完全是另一回事。本课程覆盖 LLM 应用开发中的工程化实践：如何设计可靠的 API 调用层、如何处理流式输出、如何做错误处理和重试、如何控制成本、如何评估输出质量。

这些知识是从"玩具项目"到"真实产品"的关键跨越。吴恩达在 Buildathon 上反复强调：AI 工程师的核心能力不是调模型，而是**构建可靠的 AI 系统**。

## 课程资源

- 文档：[OpenAI Cookbook](https://cookbook.openai.com/) — OpenAI 官方代码示例集合，覆盖各种使用场景
- 文档：[Anthropic API Documentation](https://docs.anthropic.com/) — Claude API 官方文档，工程化实践丰富
- 课程：[Full Stack LLM Bootcamp (Stanford)](https://fullstackdeeplearning.com/llm-bootcamp/) — 斯坦福免费课程，覆盖 LLM 应用全栈开发

## 资源汇总

**API 调用工程化：**

- [OpenAI Cookbook - API 调用最佳实践](https://cookbook.openai.com/examples/) — 流式输出、错误处理、重试策略、并发请求
- [Anthropic - Streaming Messages](https://docs.anthropic.com/en/docs/build-with-claude/streaming) — 流式输出实现指南
- [tenacity (Python 重试库)](https://github.com/jd/tenacity) — 给 API 调用加指数退避重试
- [LiteLLM](https://github.com/BerriAI/litellm) — 统一 100+ LLM 提供商的 API 接口，避免供应商锁定

**成本管理：**

- [OpenAI Cookbook - Managing Costs](https://cookbook.openai.com/examples/how_to_handle_rate_limits) — 限流、预算控制、token 计数
- [tiktoken (OpenAI Token 计数)](https://github.com/openai/tiktoken) — 在调用 API 前精确计算 token 用量
- [Token 成本计算器](https://github.com/AgentOps-AI/tokencost) — 统一计算各模型 token 成本

**输出质量保障：**

- [Structured Output (OpenAI)](https://platform.openai.com/docs/guides/structured-outputs) — 强制模型输出指定 JSON 格式
- [Instructor (Python)](https://github.com/instructor-ai/instructor) — 基于 Pydantic 的结构化输出库
- [Guardrails AI](https://github.com/guardrails-ai/guardrails) — 验证和过滤 LLM 输出的框架
- [LMQL](https://lmql.ai/) — 在提示词中嵌入约束和逻辑

**评估与监控：**

- [LangSmith (LangChain)](https://www.langchain.com/langsmith) — LLM 应用的调试、测试、监控平台
- [Braintrust](https://www.braintrust.dev/) — LLM 评估平台，支持自动化测试
- [OpenEvals (LangChain)](https://github.com/langchain-ai/openevals) — 开源 LLM 评估框架
- [DeepEval](https://github.com/confident-ai/deepeval) — 类似 pytest 的 LLM 测试框架

**Web 框架集成：**

- [FastAPI](https://fastapi.tiangolo.com/) — 构建 LLM 后端服务的首选 Python 框架
- [Streamlit](https://streamlit.io/) — 快速搭建 LLM 应用的前端界面
- [Gradio](https://www.gradio.app/) — 快速创建 ML/AI 模型的交互式演示
- [Next.js + Vercel AI SDK](https://sdk.vercel.ai/) — 前端全栈 LLM 应用开发

## 备注

工程化能力是区分"会用 AI"和"AI 工程师"的关键。建议路线：先用 FastAPI + OpenAI API 搭一个简单的后端 → 加入流式输出 → 加入错误处理和重试 → 加入成本监控 → 加入评估体系。每加一个环节，你对生产级 AI 系统的理解就深一层。

不要忽视评估——没有评估的 LLM 应用就像没有测试的软件，上线后你永远不知道它什么时候会出问题。
