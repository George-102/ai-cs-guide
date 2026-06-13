# Context Engineering 指南

## 简介

- 来源：[Context Engineering Github](https://github.com/davidkimai/Context-Engineering), [Philipp Schmid 指南](https://www.philschmid.de/context-engineering), [Simon Willison 分析](https://simonwillison.net/2025/Jun/27/context-engineering/)
- 先修要求：了解提示工程基础、能够调用大语言模型 API
- 课程难度：🌟🌟🌟🌟
- 预计学时：15 小时 +

**Context Engineering**（上下文工程）是一门系统化设计和构建动态上下文系统的学科，旨在为大语言模型提供完成任务所需的**一切信息**。它超越了传统提示工程中"写好一条指令"的范畴，转而关注如何在正确的时间、以正确的格式，为模型提供正确的信息和工具。

Shopify CEO Tobi Lutke 将其描述为一种核心技能——即"为任务提供所有上下文，使 LLM 能够合理地完成任务"的艺术。Andrej Karpathy 则将其定位为科学与艺术的结合：在工业级 LLM 应用中，核心挑战是"用恰到好处的信息填充上下文窗口，以支持下一步操作"。

**为什么学习 Context Engineering？** 因为在实际的 AI 应用开发中，单纯写好一条提示词远远不够。模型的表现不仅取决于你"说了什么"，更取决于它"看到了什么"——包括对话历史、检索到的文档、可用工具、记忆状态等。Context Engineering 正是解决"模型看到什么"这一问题的系统方法论。研究表明，大多数 Agent 的失败不再是模型能力不足，而是上下文设计质量低下。

> Context is the complete information payload provided to a LLM at inference time, encompassing all structured informational components that the model needs to plausibly accomplish a given task.
>
> ——引自 1400+ 篇论文的系统分析

**与 Prompt Engineering 的区别：** Prompt Engineering 关注的是"说什么"——用户发出的单条指令；Context Engineering 关注的是"模型看到什么"——包括指令、记忆、检索信息、工具、输出格式在内的完整信息系统。用一个简单的例子：当你问 AI"明天有什么安排？"时，Prompt Engineering 关注如何措辞这个问题；Context Engineering 关注的是在模型回答之前，应该为它提供哪些信息——日历数据、历史邮件、联系人列表、可用工具等。

## 课程内容大纲

### 模块一：基础概念

- **上下文的定义与构成**：理解上下文的七个层面——Instructions（系统提示）、User Prompt（用户输入）、短期记忆（对话历史）、长期记忆（跨对话知识）、检索信息（RAG）、可用工具、结构化输出
- **与 Prompt Engineering 的区别**：从"单一字符串"到"完整信息系统"的思维转变
- **上下文的核心原则**：上下文是一个系统而非单一字符串；动态生成而非静态模板；在正确时机提供正确的信息

### 模块二：核心技术

- **Token 预算优化**：在有限的上下文窗口中最大化信息密度，每个 token 都承载信息成本
- **Few-Shot 学习**：通过少量高质量示例教学，通常优于纯解释性方法
- **检索增强生成（RAG）**：注入相关文档以减少幻觉，关键是检索质量
- **记忆系统**：跨轮次的状态持久化，支持有状态交互；现代记忆系统实现记忆与推理的协同

### 模块三：高级主题

- **认知工具**：结构化的推理模式，如 Chain-of-Thought（思维链）、ReAct（推理+行动）等，研究表明可使 GPT-4.1 性能提升 16.6%
- **提示编程**：类代码的提示组合方式，包括函数式、过程式、面向对象等模式
- **动态上下文生成**：根据任务实时构建上下文，而非使用静态模板
- **神经场理论与量子语义学**：上下文作为动态场的前沿研究方向

### 模块四：实践应用

- **Agent 上下文设计**：为 AI Agent 构建完整的上下文系统
- **上下文质量评估**：如何衡量和改进上下文的有效性
- **实际案例分析**：日程安排 Agent 等场景的上下文对比（低质量 vs 高质量）
- **工具描述工程**：如何编写清晰的工具定义以提升模型调用能力

## 文档资源

- 网站：[Context Engineering Github](https://github.com/davidkimai/Context-Engineering)（含 12 周课程结构）, [Philipp Schmid 实践指南](https://www.philschmid.de/context-engineering), [Simon Willison 的分析](https://simonwillison.net/2025/Jun/27/context-engineering/)
- 论文：[Context Engineering Survey（1400+ 篇论文综述）](https://arxiv.org/pdf/2507.13334), [IBM Zurich 认知工具研究](https://arxiv.org/pdf/2506.12115), [MEM1 记忆-推理协同](https://arxiv.org/pdf/2506.15841), [LLM 吸引子动力学](https://arxiv.org/pdf/2502.15208)
- 补充：仓库提供 `minimal_context.yaml` 模板和 `00_toly_chatbot/` 完整实现示例，适合快速上手

## 资源汇总

Context Engineering 代表了 AI 应用开发的范式转变——从关注"说什么"到关注"模型看到什么"。对于计算机专业的学生而言，掌握这一技能意味着能够构建更可靠、更智能的 AI 系统。建议从理解上下文的构成要素入手，逐步深入到 RAG、记忆系统、认知工具等核心技术，最终形成自己的上下文工程方法论。
