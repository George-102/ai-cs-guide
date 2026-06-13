# Harness Engineering 指南

## 简介

- 来源：[learn-harness-engineering](https://github.com/walkinglabs/learn-harness-engineering), [OpenAI Codex 指南](https://openai.com/index/introducing-codex/), [Anthropic 有效 harness 研究](https://www.anthropic.com/engineering/claude-code-best-practices)
- 先修要求：了解提示工程和 Context Engineering 基础、有编程经验、熟悉命令行操作
- 课程难度：🌟🌟🌟🌟
- 预计学时：20 小时 +

**Harness Engineering**（驾驭工程）是一门关于**为 AI 编程智能体构建完整工作环境**的学科。它的核心观点是：即使是最强大的 AI 模型，在没有适当环境支撑的情况下，也无法可靠地完成真实的工程任务。这个环境就是 **harness**（驾驭层）。

Anthropic 的一个对照实验生动地说明了这一点：同一个模型（Opus 4.5），在没有 harness 的情况下花费 $9/20 分钟产出无法运行的结果；而在完整 harness 的支撑下，花费 $200/6 小时构建出了可运行的软件。**模型没有改变，改变的是 harness。** OpenAI 在 Codex 中也报告了类似的结果——在良好 harness 管理的仓库中，AI 编程智能体的表现显著提升。

**为什么学习 Harness Engineering？** 因为 AI 辅助编程的瓶颈已经从"模型不够聪明"转变为"工作环境不够好"。没有 harness，智能体会写代码但破坏测试、过早宣布完成、丢失会话间状态，迫使人类反复修复。有 harness，智能体会读取指令、运行初始化、实现经过验证的功能、更新持久化状态，让人类专注于审查结果。掌握 Harness Engineering 意味着能够真正将 AI 智能体融入日常开发工作流。

> The strongest model in the world will still fail on real engineering tasks if you don't build a proper environment around it.
>
> ——learn-harness-engineering

**与 Prompt Engineering、Context Engineering 的区别：** Prompt Engineering 关注"说什么"——单条指令的措辞；Context Engineering 关注"模型看到什么"——完整的信息架构；Harness Engineering 关注"模型在什么环境中工作"——包含指令、状态、验证、范围、生命周期的完整系统。用一个比喻：Prompt Engineering 像是给工人一份清晰的指令；Context Engineering 像是给工人提供完整的图纸和材料；Harness Engineering 则是为工人搭建整个车间——包括工具架、质检流程、进度看板和交接班制度。

## 课程内容大纲

### 模块一：问题认知

- **为什么强大模型仍会失败**：理解"模型能力 ≠ 可靠执行"的核心矛盾，分析 Anthropic 对照实验的数据
- **Harness 的定义与本质**：什么是 harness，它如何将模型输出从不可预测变为可复现
- **三者的定位**：Prompt Engineering、Context Engineering、Harness Engineering 各自解决什么问题

### 模块二：五大子系统

- **Instructions（指令）**：定义智能体应该做什么以及按什么顺序做，采用渐进式披露而非单一巨型文件
- **State（状态）**：跟踪已完成的工作、进行中的任务和待办事项，状态必须持久化到磁盘
- **Verification（验证）**：通过的测试套件是完成工作的唯一有效证据，涵盖测试、lint、类型检查、端到端流水线
- **Scope（范围）**：约束智能体一次只做一个功能，功能列表作为机器可读的边界
- **Session Lifecycle（会话生命周期）**：管理开始前的初始化和结束后的清理，确保会话间可靠衔接

### 模块三：核心原则

- **仓库是唯一的事实来源**：所有上下文、约束和进度都必须编码在仓库文件中
- **测试驱动的验证**：智能体不能在没有可运行证明的情况下宣布胜利
- **会话生命周期管理**：每次会话都要留下干净的状态，确保下一个会话能顺利接手
- **一次只做一件事**：功能列表定义明确边界，防止过度扩展和不完整的多任务处理

### 模块四：实践应用

- **项目文件结构**：AGENTS.md、init.sh、feature_list.json、progress.md 等关键文件的组织方式
- **会话生命周期详解**：Start → Select → Execute → Wrap Up 的完整流程
- **有无 Harness 的对比**：智能体行为、会话间状态、人类角色、可靠性的系统对比
- **可观测性与调试**：如何让智能体行为可见，便于发现问题和改进

## 文档资源

- 网站：[learn-harness-engineering](https://walkinglabs.github.io/learn-harness-engineering/)（12 节课程 + 6 个项目）, [Github 仓库](https://github.com/walkinglabs/learn-harness-engineering)
- 参考文献：[OpenAI Codex harness 工程指南](https://openai.com/index/introducing-codex/), [Anthropic 有效 harness 研究](https://code.claude.com/docs/en/best-practices), [Thoughtworks/Martin Fowler harness 工程文章](https://martinfowler.com/articles/harness-engineering.html), [Cursor agent harness 博文](https://cursor.com/blog/continually-improving-agent-harness), [LangChain deep agents 研究](https://www.langchain.com/blog/deep-agents)
- 补充：仓库提供 harness-creator 技能，可快速搭建生产级 harness；所有项目围绕一个 Electron 知识库桌面应用逐步构建

## 资源汇总

Harness Engineering 代表了 AI 辅助编程的工程化成熟——从"会写提示词"到"能构建可靠系统"的跨越。对于计算机专业的学生而言，掌握这一技能意味着能够真正将 AI 智能体融入日常开发工作流，而不是在每次使用后手动修复。建议从理解问题开始，逐步学习五大子系统，通过项目实践建立 harness 思维，最终形成自己的工程化 AI 协作方法论。
