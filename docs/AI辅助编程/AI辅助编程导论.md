# AI 辅助编程导论

## 简介

- 来源：综合整理
- 先修要求：至少掌握一门编程语言（Python/Java/C++ 均可）
- 课程难度：🌟🌟
- 预计学时：10 小时 +

AI 辅助编程（AI-Assisted Programming）是指**利用 AI 工具来提升软件开发效率的一系列方法和实践**。它不是让 AI 替代你写代码，而是让 AI 成为你的编程搭档——你负责思考和决策，AI 负责执行和加速。

从 GitHub Copilot 的代码补全，到 Claude Code 的 Agentic 编程，再到 Cursor 的 IDE 集成——AI 编程工具正在快速进化。但工具只是手段，核心是你如何与 AI 协作。

## 为什么需要这门课

**AI 工具正在重塑编程方式。** 吴恩达在 Buildathon 上演示了 AI 辅助编程如何让独立开发者的原型开发速度提升 10 倍。这不是未来，而是现在正在发生的事。

**会用工具不等于会用好工具。** 很多人用 ChatGPT 写代码，但效果参差不齐。区别在于：你是否理解 AI 的能力边界？你是否知道如何清晰地表达需求？你是否能审查 AI 生成的代码？

**避免 Vibe Coding 的陷阱。** 不加审查地接受 AI 生成的代码，短期看起来很快，长期会积累大量技术债和安全漏洞。这门课教你正确的 AI 协作方式。

## 核心知识模块

### AI 编程工具的演进

- **代码补全时代**：Tabnine、GitHub Copilot —— 基于上下文的行/函数补全
- **对话编程时代**：ChatGPT、Claude —— 通过自然语言对话生成代码
- **Agentic 编程时代**：Claude Code、Cursor、Devin —— AI 能自主规划、执行多步骤任务
- **IDE 集成时代**：AI 深度集成到开发环境中，理解整个代码库

### 核心协作模式

- **你描述，AI 生成**：用自然语言描述需求，AI 生成代码草稿
- **AI 生成，你审查**：仔细阅读 AI 生成的代码，验证正确性
- **你写框架，AI 填细节**：你设计架构和接口，AI 实现具体函数
- **AI 辅助调试**：把错误信息交给 AI，让它帮助定位和修复问题
- **AI 辅助重构**：让 AI 改善代码结构、命名、性能

### 写好提示词的关键

- **明确上下文**：告诉 AI 项目使用的语言、框架、编码规范
- **分解复杂任务**：大任务拆成小任务，逐步完成
- **提供示例**：用 Few-Shot 示例让 AI 理解你想要的风格
- **指定输出格式**：明确函数签名、返回值、错误处理方式
- **迭代优化**：第一次不满意，补充信息重新生成

### 审查 AI 生成代码的检查清单

- 代码是否正确处理了边界条件？
- 是否有安全漏洞（SQL 注入、XSS、路径遍历等）？
- 是否有性能问题（不必要的循环、内存泄漏）？
- 命名是否清晰？逻辑是否可读？
- 是否有测试覆盖？

## 怎么学

**选一个工具深入使用。** 推荐从 Claude Code 或 Cursor 开始——它们代表了当前 AI 编程工具的最高水平。在实际项目中使用它，而不是只看教程。

**从简单任务开始。** 先让 AI 帮你写单元工具函数、写测试、重构小代码块。逐步建立对 AI 能力的准确预期。

**始终保持审查习惯。** 每一行 AI 生成的代码都要经过你的审查。这不是不信任 AI，而是对自己代码负责。

**结合 TDD 实践。** 先写测试，再让 AI 生成实现。测试是 AI 生成代码的"契约"，也是你验证代码正确性的安全网。

## 推荐资源

**工具**

- [Claude Code](https://claude.ai/code) —— Anthropic 官方 Agentic 编程工具，终端/IDE/Web 均支持
- [Cursor](https://cursor.com/) —— AI 原生 IDE，深度集成代码库理解
- [GitHub Copilot](https://github.com/features/copilot) —— 最早的 AI 代码补全工具，VS Code 集成
- [Windsurf](https://codeium.com/windsurf) —— Codeium 推出的 AI IDE
- [Devin](https://devin.ai/) —— Cognition 推出的自主 AI 编程 Agent

**课程与文章**

- [吴恩da - AI Agents in LangGraph](https://learn.deeplearning.ai/courses/ai-agents-langgraph) —— 理解 Agentic 编程的底层逻辑
- [Anthropic - Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) —— Agent 设计最佳实践
- [Simon Willison - AI Assisted Programming](https://simonwillison.net/series/ai-assisted-programming/) —— 大量实战经验分享

**相关课程**

- [Claude Code 指南](./Claude Code指南.md) —— 深入学习和配置 Claude Code
- [测试驱动开发](./测试驱动开发.md) —— TDD 是 AI 辅助编程的最佳搭档
