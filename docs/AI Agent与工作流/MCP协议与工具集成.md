# MCP 协议与工具集成

## 简介

- 来源：[Model Context Protocol 官方文档](https://modelcontextprotocol.io/)、[Anthropic MCP 公告](https://www.anthropic.com/news/model-context-protocol)
- 先修要求：了解 LLM API 调用、了解 Agent 基本概念
- 编程语言：Python / TypeScript
- 课程难度：🌟🌟🌟
- 预计学时：15 小时 +

**MCP（Model Context Protocol）** 是 Anthropic 在 2024 年底推出的开放标准协议，用于让 AI 模型以统一方式连接外部工具和数据源。你可以把它理解为 **AI 世界的 USB 接口**——以前每个工具都要单独适配每个模型，现在只要工具支持 MCP，任何支持 MCP 的 AI 都能直接使用。

MCP 的核心价值：
- **标准化**：一次实现，处处可用
- **安全性**：明确的权限边界，工具只能暴露声明的功能
- **生态**：Claude Desktop、Cursor、Windsurf、VS Code 等主流工具都已支持 MCP

2025 年，MCP 已经成为 AI 工具集成的行业标准。理解和使用 MCP，是 AI 工程师的必备技能。

## 课程资源

- 官方文档：[modelcontextprotocol.io](https://modelcontextprotocol.io/) — 最权威的学习资源
- SDK：[MCP Python SDK](https://github.com/modelcontextprotocol/python-sdk)、[MCP TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk)
- 服务器集合：[MCP Servers (GitHub Awesome)](https://github.com/punkpeye/awesome-mcp-servers) — 社区维护的 MCP 服务器列表

## 资源汇总

**理解 MCP 协议：**

- [MCP 官方文档 - Overview](https://modelcontextprotocol.io/docs/getting-started/architecture) — 架构概览，必读
- [MCP 规范 (Specification)](https://spec.modelcontextprotocol.io/specification/) — 协议细节
- [What is MCP? (Anthropic Blog)](https://www.anthropic.com/news/modelcontextprotocol) — 官方公告，了解设计动机

**MCP 三大原语：**

1. **Tools（工具）**：AI 可以调用的函数，如搜索、计算、API 调用
2. **Resources（资源）**：AI 可以读取的数据，如文件、数据库记录
3. **Prompts（提示模板）**：预定义的提示模板，标准化常见任务

**使用现有 MCP 服务器：**

- [GitHub MCP Server](https://github.com/modelcontextprotocol/servers/tree/main/src/github) — 让 AI 操作 GitHub（PR、Issue、代码搜索）
- [Filesystem MCP Server](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem) — 让 AI 读写本地文件
- [PostgreSQL MCP Server](https://github.com/modelcontextprotocol/servers/tree/main/src/postgres) — 让 AI 查询数据库
- [Brave Search MCP Server](https://github.com/modelcontextprotocol/servers/tree/main/src/brave-search) — 让 AI 搜索网页
- [Slack MCP Server](https://github.com/modelcontextprotocol/servers/tree/main/src/slack) — 让 AI 操作 Slack

**开发自己的 MCP 服务器：**

- [MCP Python SDK Quickstart](https://github.com/modelcontextprotocol/python-sdk) — 从零构建 MCP 服务器
- [MCP Inspector](https://github.com/modelcontextprotocol/inspector) — 调试 MCP 服务器的可视化工具
- [Building MCP Servers (Tutorial)](https://modelcontextprotocol.io/docs/develop/build-server) — 官方教程

**MCP 客户端集成：**

- [Claude Desktop MCP 配置](https://modelcontextprotocol.io/docs/develop/connect-local) — 在 Claude Desktop 中使用 MCP
- [Cursor MCP 集成](https://cursor.com/docs/context/mcp) — 在 Cursor 中使用 MCP
- [在 LangGraph 中使用 MCP 工具](https://langchain-ai.github.io/langgraph/) — 将 MCP 工具集成到 Agent 工作流

## 备注

MCP 目前还在快速演进中，规范和 SDK 变化比较快。学习时以官方文档为准，第三方教程可能已经过时。

实践建议：先用现成的 MCP 服务器（如 GitHub MCP）感受一下 MCP 的能力边界，然后尝试用 Python SDK 写一个简单的 MCP 服务器（比如封装你自己项目的 API）。写一个 MCP 服务器大概只需要 50-100 行代码，是很好的练手项目。
