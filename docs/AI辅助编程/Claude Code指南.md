# Claude Code 指南

## 什么是 Claude Code

Claude Code 是 Anthropic 官方推出的 agentic 编程工具。它运行在你的终端、IDE 或浏览器中，能理解整个代码库，并通过自然语言对话帮你完成编程任务。

它和 GitHub Copilot 这类工具的本质区别在于：Copilot 是**补全工具**，在你打字时提供建议；Claude Code 是 **agent**，它能读懂你的项目结构、执行 shell 命令、读写文件、运行测试、管理 Git 工作流，甚至连接外部服务。

简单来说，Copilot 帮你写单行代码，Claude Code 帮你完成整个任务。

Claude Code 的核心特点：

- **对话式协作**：用自然语言描述需求，Claude Code 理解后执行
- **代码库理解**：它会先读懂你的项目，再动手修改
- **自主执行**：能运行命令、读写文件、处理错误，不需要你一步步指挥
- **多平台支持**：终端 CLI、VS Code 扩展、JetBrains 插件、Desktop 应用、Web 版（claude.ai/code）

## Vibe Coding 的问题

在讨论 Claude Code 之前，有必要先了解一种流行的但有问题的 AI 编程方式 — Vibe Coding。

### 什么是 Vibe Coding

2025 年 2 月，前特斯拉 AI 总监、OpenAI 联合创始人 Andrej Karpathy 发了一条推文，描述了一种他称为"Vibe Coding"的编程方式：

> "There's a new kind of coding I call 'vibe coding', where you fully give in to the vibes, embrace exponentials, and forget that the code even exists."

他的工作方式是：用 AI 工具生成代码，接受所有建议不看 diff，跑不起来就复制粘贴错误信息让 AI 修复，代码超出了自己的理解能力也无所谓。他承认这"对一次性周末项目还行"。

### Vibe Coding 的弊端

听起来很爽，但数据告诉我们事情没那么简单。

**安全漏洞激增**

CodeRabbit 在 2025 年 12 月分析了 470 个开源 GitHub PR，发现 AI 参与编写的代码包含的重大问题数量是人工代码的 1.7 倍，安全漏洞是 2.74 倍，配置错误多 75%。用 Vibe Coding 方式写出来的代码，安全问题更加严重 — 因为没人审查。

**代码质量急剧下降**

GitClear 在 2025 年初发布了一项纵向研究，分析了 2020-2024 年间 2.11 亿行代码变更。结果发现：重构占比从 25% 降到不足 10%，代码重复翻了四倍，代码流失率几乎翻倍。这些趋势都与 AI 辅助编码的普及相关。2025 年 9 月，资深工程师们开始报告在维护 AI 生成的代码库时陷入"开发地狱" — 这被称为"vibe coding 宿醉"。

**生产力是幻觉**

METR 在 2025 年 7 月进行了一项随机对照试验。经验丰富的开源开发者使用 AI 编程工具后，实际效率**降低了 19%**。但有意思的是，他们在事前预测自己会快 24%，事后仍然觉得自己快了 20%。这说明人对 AI 工具的效率感知存在严重的认知偏差。

**真实事故**

2025 年 7 月，Replit 的 AI agent 在明确被指示不要做任何更改的情况下，仍然删除了一个生产数据库，随后还提供了不准确的信息来掩盖发生了什么。CEO 公开道歉。

**能力退化**

长期使用 Vibe Coding 的开发者会逐渐丧失核心编程能力。不理解自己写的代码意味着：无法独立调试、无法进行架构决策、无法审查他人代码、无法维护自己的项目。你从"开发者"变成了"AI 操作员"。

### Simon Willison 的界定

Simon Willison（Django 联合创始人）对 Vibe Coding 做了一个重要区分：如果你仔细审查了 AI 生成的代码、进行了测试、确保自己理解了每一行，那就不叫 Vibe Coding — 那只是"用 LLM 作为打字助手"。

Vibe Coding 的核心特征是**放弃理解和控制**。这正是它与 AI 辅助编程的根本区别。

## AI 辅助编程的核心理念

### 人机协作，而非人机替代

Vibe Coding 的问题在于它把开发者变成了旁观者。AI 辅助编程的理念恰好相反：**你始终是决策者，AI 是执行者**。

你负责：

- 定义需求和验收标准
- 做架构决策
- 判断代码质量
- 控制项目方向

Claude Code 负责：

- 理解代码库
- 执行具体的编码任务
- 运行命令和测试
- 提供方案建议

这种分工让你保持对代码的理解和控制，同时大幅提升效率。

### 理解优先，而非生成优先

AI 辅助编程强调先理解再动手，而不是盲目生成代码。好的 AI 编程工具会先读懂相关的代码文件，理解现有的架构和模式，然后再做出符合项目风格的修改。

这和 Vibe Coding 的"生成了再说"形成鲜明对比。理解优先意味着生成的代码更可能与现有代码库保持一致，减少后续的整合成本。

### 渐进式信任

没有人建议你一开始就让 AI 处理核心业务逻辑。正确的做法是：

1. 从小任务开始 — 写个测试、修个小 bug、重构一个函数
2. 验证结果 — 跑测试、看 diff、读代码
3. 逐步扩展 — 当你对 AI 的能力有了准确的预期后，再扩大任务范围
4. 始终保持验证手段 — 测试、代码审查、手动验证

这种渐进式的方式让你既享受 AI 的效率，又不失去对代码的控制。

Claude Code 的设计体现了上述所有理念。接下来我们看看如何安装和使用它。

## 安装与配置

### 安装方法

**Windows（推荐）：**

```powershell
irm https://claude.ai/install.ps1 | iex
```

**macOS / Linux（推荐）：**

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

**Homebrew（macOS / Linux）：**

```bash
brew install --cask claude-code
```

**npm（仍可用但已弃用）：**

```bash
npm install -g @anthropic-ai/claude-code
```

**IDE 扩展：**

- VS Code：在 Marketplace 搜索 "Claude Code"，或运行 `code --install-extension anthropic.claude-code`
- JetBrains：在 JetBrains Marketplace 搜索 "Claude Code"

### 首次配置

安装完成后，验证安装并登录：

```bash
claude --version    # 确认安装成功
claude auth login   # 登录 Anthropic 账号
```

启动第一个会话：

```bash
claude              # 进入交互式会话
```

在会话中，你可以用 `/init` 让 Claude Code 分析你的项目并自动生成 `CLAUDE.md` 配置文件。这个文件记录了项目的架构、构建命令、编码规范等信息，帮助 Claude Code 更好地理解你的项目。

用 `/config` 可以打开设置界面，调整模型、权限模式等选项。

## 核心用法

### 交互式会话

Claude Code 最基本的使用方式是交互式会话。在项目目录下运行 `claude`，就能开始和 AI 对话：

```bash
# 启动新会话
claude

# 带初始提示启动
claude "帮我看看这个项目的测试覆盖率"

# 继续最近的对话
claude -c

# 恢复指定会话
claude -r "abc123"

# 非交互模式（适合脚本和 CI）
claude -p "运行所有测试并报告结果"
```

在会话中，你可以像和同事聊天一样描述需求。Claude Code 会阅读相关文件、执行命令、修改代码，整个过程你可以看到它在做什么，并在关键节点进行审查。

### 权限模式

Claude Code 有多种权限模式，控制它在执行操作前是否需要你批准：

| 模式 | 无需批准的操作 | 适用场景 |
|------|--------------|---------|
| `default` | 只读操作 | 敏感项目、初次使用 |
| `acceptEdits` | 读写文件、常用文件系统命令 | 日常开发 |
| `plan` | 只读操作 | 探索代码库 |
| `auto` | 所有操作（有安全分类器把关） | 长时间任务 |
| `bypassPermissions` | 所有操作（无安全检查） | 仅限隔离容器/VM |

在 CLI 中按 `Shift+Tab` 可以切换模式。建议日常使用 `acceptEdits`，在不确定的操作上保持审查习惯。

### 常用斜杠命令

Claude Code 提供了丰富的斜杠命令，按工作流分组：

**任务进行中：**

- `/plan` — 进入计划模式，先规划再执行
- `/model` — 切换模型（如从 Sonnet 切到 Opus 处理复杂任务）
- `/effort` — 调整努力级别（low/medium/high/max）
- `/compact` — 压缩对话上下文，释放 token 空间
- `/context` — 查看当前上下文使用情况

**提交代码前：**

- `/diff` — 查看未提交的变更
- `/code-review` — 审查当前 diff，发现 bug 和改进点
- `/security-review` — 分析变更中的安全漏洞

**会话管理：**

- `/clear` — 清空当前对话，开始新话题
- `/resume` — 恢复之前的会话
- `/branch` — 分支当前对话

**遇到问题时：**

- `/rewind` — 回滚代码和对话到上一个检查点
- `/doctor` — 诊断安装和配置问题
- `/debug` — 开启调试日志

**成本管理：**

- `/usage`（或 `/cost`）— 查看当前会话的 token 使用量和费用

### CLAUDE.md 配置系统

`CLAUDE.md` 是 Claude Code 的"项目记忆"文件。它在每次会话开始时自动加载，让 Claude Code 了解你的项目。

**文件位置层级：**

| 范围 | 位置 | 用途 |
|------|------|------|
| 用户级 | `~/.claude/CLAUDE.md` | 个人偏好，适用于所有项目 |
| 项目级 | `./CLAUDE.md` 或 `./.claude/CLAUDE.md` | 团队共享的项目说明 |
| 本地级 | `./CLAUDE.local.md` | 个人项目配置（应加入 .gitignore） |

**导入外部文件：**

```markdown
项目概述见 @README.md
npm 命令见 @package.json
```

**规则目录：**

`.claude/rules/` 下可以放模块化的、带路径范围的指令文件：

```markdown
---
paths:
  - "src/api/**/*.ts"
---
所有 API 端点必须包含输入验证。
```

用 `/init` 可以让 Claude Code 自动分析项目并生成初始的 `CLAUDE.md`。

### MCP 服务器集成

MCP（Model Context Protocol）让 Claude Code 连接外部工具和服务：

```bash
# 添加 GitHub MCP 服务器
claude mcp add --transport http github https://api.githubcopilot.com/mcp/ \
  --header "Authorization: Bearer YOUR_GITHUB_PAT"

# 添加 Sentry 错误追踪
claude mcp add --transport http sentry https://mcp.sentry.dev/mcp

# 添加 PostgreSQL 数据库
claude mcp add --transport stdio db -- npx -y @bytebase/dbhub \
  --dsn "postgresql://readonly:pass@localhost:5432/mydb"
```

管理命令：

```bash
claude mcp list          # 列出所有服务器
claude mcp get <name>    # 查看详情
claude mcp remove <name> # 移除服务器
```

在会话中用 `/mcp` 可以查看 MCP 服务器状态和管理连接。

项目级配置存储在 `.mcp.json` 文件中，可以提交到 Git 与团队共享。

### Hooks 系统

Hooks 让你在 Claude Code 的生命周期事件上执行自定义操作。比如在每次文件修改后自动运行 linter，或者在会话开始时加载特定配置。

常用事件：

- `PreToolUse` — 工具执行前触发（可用于拦截和验证）
- `PostToolUse` — 工具执行后触发（可用于后续处理）
- `SessionStart` — 会话开始时触发

配置位置在 `.claude/settings.json`：

```json
{
  "hooks": {
    "PostToolUse": [
      {
        "matcher": "Write|Edit",
        "type": "command",
        "command": "ruff check --fix $CLAUDE_FILE_PATH"
      }
    ]
  }
}
```

## 实战工作流

### 场景一：理解现有代码库

接手一个不熟悉的项目时，Claude Code 可以帮你快速建立理解：

```
> 这个项目是做什么的？帮我梳理一下整体架构。

> src/api/ 目录下的请求处理流程是怎样的？

> 这个函数的调用链是什么？哪些模块依赖它？
```

Claude Code 会阅读相关文件，分析依赖关系，用清晰的结构给你解释。这比你自己一个个文件翻要快得多。

### 场景二：实现新功能

从需求到实现的完整协作过程：

```
> 我想给用户注册功能添加邮箱验证。请先帮我看看现有的注册流程是怎样的。
```

Claude Code 会先阅读相关代码，理解现有架构，然后你继续：

```
> 好的，现在帮我设计邮箱验证的方案，包括数据库表结构和 API 端点。
```

审查方案后：

```
> 方案可以，请实现。记得写测试。
```

关键点：你在这个过程中做了三个决策 — 确认需求、审查设计、批准实现。Claude Code 负责了理解代码、设计方案、编写实现和测试。你保持了控制权。

### 场景三：修复 Bug

```
> 用户报告登录后 session 偶尔会丢失。错误日志在 logs/error.log，帮我定位问题。
```

Claude Code 会读取日志、分析代码、定位根因，然后给出修复方案。你可以要求它先写一个能复现问题的测试，再修复：

```
> 先写一个能复现这个问题的测试，然后修复它。
```

测试通过后，你就有了一个经过验证的修复，以及一个防止回归的测试。

### 场景四：代码重构

重构是 Claude Code 最擅长的场景之一，因为它需要理解代码的整体结构：

```
> src/utils/ 下的函数太乱了，帮我按功能重新组织，但不要改变任何外部行为。
```

Claude Code 会先分析现有的函数和它们的依赖关系，提出重构方案，然后在你的审查下执行。如果有测试套件，重构后跑一遍测试就能确认没有破坏任何东西。

这呼应了 TDD 那篇指南中的观点：测试是重构的安全网。

### 场景五：编写和运行测试

```
> 帮我给 src/services/payment.py 写单元测试，覆盖正常流程和边界情况。
```

Claude Code 会读取源文件，理解函数的输入输出，生成测试代码，然后运行：

```
> 测试写好了，我运行一下看看。

> 3 个测试通过，1 个失败。失败的那个是边界条件没处理好，我来修复。
```

这种"生成-运行-修复"的循环是 Claude Code 的自然工作方式，也是 TDD 理念在 AI 辅助编程中的体现。

## AI 辅助编程 vs Vibe Coding

| 维度 | Vibe Coding | AI 辅助编程 |
|------|-------------|-------------|
| 代码理解 | 不理解，"forget the code exists" | 先理解再修改 |
| 质量控制 | 无测试，无审查 | 支持 TDD、代码审查 |
| 安全性 | 漏洞率 2.74 倍于人工代码 | 内置安全审查 |
| 学习效果 | 能力退化 | 能力增长 |
| 长期价值 | 技术债累积 | 可维护的代码 |
| 开发者角色 | 旁观者 | 决策者 |

核心区别就一句话：**Vibe Coding 放弃控制，AI 辅助编程保持控制**。

用 Vibe Coding 的开发者短期内可能感觉很高效，但长期来看，他们正在丧失理解代码、调试问题、做架构决策的能力。当 AI 生成的代码出了问题 — 而它一定会出问题 — 他们将束手无策。

用 AI 辅助编程方式的开发者则在持续提升能力：他们学会了更好地描述需求、审查代码、设计架构，同时把重复性的编码工作交给 AI。AI 是放大器，不是替代品。

## 成本与效率管理

Claude Code 按 token 计费，合理管理成本很重要。

**查看花费：**

```
/usage    # 查看当前会话的 token 使用量和费用
```

**降低成本的策略：**

- **选择合适的模型**：日常任务用 Sonnet，复杂任务才用 Opus。用 `/model` 切换
- **压缩上下文**：对话变长后用 `/compact` 压缩，释放 token 空间
- **调整努力级别**：简单任务用 `/effort low`，减少不必要的推理
- **设置预算上限**：非交互模式下用 `--max-budget-usd` 限制花费
- **精简 CLAUDE.md**：保持在 200 行以内，避免每次会话都加载过多上下文
- **清理不相关对话**：开始新任务时用 `/clear` 清空上下文

## 总结

Claude Code 代表了一种正确的 AI 辅助编程方式：AI 负责执行，你负责判断。它不是让你"忘记代码的存在"，而是让你更高效地理解和控制代码。

对于大学学生来说，学会使用 Claude Code 这样的工具，核心不是学会某个命令或配置，而是培养一种协作思维：知道如何清晰地表达需求、如何审查生成的代码、如何在效率和质量之间做出平衡。这些能力在 AI 时代比以往任何时候都更重要 — 因为 AI 能帮你写代码，但只有你能决定代码应该做什么，以及它做得对不对。
