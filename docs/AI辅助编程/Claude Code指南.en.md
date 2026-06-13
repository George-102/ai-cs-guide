# Claude Code Guide

## What Is Claude Code

Claude Code is Anthropic's official agentic coding tool. It runs in your terminal, IDE, or browser, understands your entire codebase, and helps you complete programming tasks through natural language conversation.

The fundamental difference from tools like GitHub Copilot: Copilot is a **completion tool** that suggests code as you type; Claude Code is an **agent** that can read your project structure, execute shell commands, read and write files, run tests, manage Git workflows, and connect to external services.

Put simply, Copilot helps you write individual lines of code. Claude Code helps you complete entire tasks.

Core features:

- **Conversational collaboration**: Describe what you need in natural language, Claude Code understands and executes
- **Codebase understanding**: It reads your project before making changes
- **Autonomous execution**: Runs commands, reads/writes files, handles errors without step-by-step instructions
- **Multi-platform support**: Terminal CLI, VS Code extension, JetBrains plugin, Desktop app, Web (claude.ai/code)

## The Problem with Vibe Coding

Before discussing Claude Code, it's worth understanding a popular but problematic approach to AI programming — Vibe Coding.

### What Is Vibe Coding

In February 2025, former Tesla AI Director and OpenAI co-founder Andrej Karpathy posted a tweet describing a programming approach he called "Vibe Coding":

> "There's a new kind of coding I call 'vibe coding', where you fully give in to the vibes, embrace exponentials, and forget that the code even exists."

His workflow: use AI tools to generate code, accept all suggestions without reading diffs, copy-paste error messages to let AI fix them, and not worry that the code exceeds his own comprehension. He acknowledged this works "for throwaway weekend projects."

### The Drawbacks of Vibe Coding

Sounds appealing, but the data tells a different story.

**Security vulnerabilities skyrocket**

CodeRabbit analyzed 470 open-source GitHub pull requests in December 2025 and found that AI co-authored code contained 1.7x more major issues than human-written code, 2.74x more security vulnerabilities, and 75% more misconfigurations. Code written with Vibe Coding approaches has even worse security — because nobody reviews it.

**Code quality drops sharply**

GitClear published a longitudinal study in early 2025 analyzing 211 million lines of code changes from 2020-2024. Refactoring dropped from 25% to under 10% of changed lines, code duplication quadrupled, and code churn nearly doubled — all trends linked to AI-assisted coding. In September 2025, senior engineers began reporting "development hell" when maintaining AI-generated codebases — dubbed the "vibe coding hangover."

**Productivity is an illusion**

METR conducted a randomized controlled trial in July 2025. Experienced open-source developers were actually **19% slower** when using AI coding tools. But here's the interesting part: before the study, they predicted they'd be 24% faster, and afterward they still believed they'd been 20% faster. This reveals a significant cognitive bias in how people perceive AI tool efficiency.

**Real incidents**

In July 2025, Replit's AI agent deleted a production database despite explicit instructions not to make any changes, then provided inaccurate information about what happened. The CEO publicly apologized.

**Skill atrophy**

Developers who rely on Vibe Coding long-term gradually lose their core programming skills. Not understanding your own code means: unable to debug independently, unable to make architectural decisions, unable to review others' code, unable to maintain your own projects. You transform from a "developer" into an "AI operator."

### Simon Willison's Distinction

Simon Willison (Django co-founder) drew an important boundary: if you carefully review AI-generated code, test it, and ensure you understand every line, that's not Vibe Coding — that's simply "using an LLM as a typing assistant."

The defining characteristic of Vibe Coding is **giving up understanding and control**. This is precisely what distinguishes it from AI-assisted programming.

## Core Philosophy of AI-Assisted Programming

### Human-AI Collaboration, Not Human-AI Replacement

The problem with Vibe Coding is that it turns developers into bystanders. The AI-assisted programming philosophy is the opposite: **you are always the decision-maker, AI is the executor**.

You are responsible for:

- Defining requirements and acceptance criteria
- Making architectural decisions
- Judging code quality
- Directing the project

Claude Code is responsible for:

- Understanding the codebase
- Executing concrete coding tasks
- Running commands and tests
- Suggesting approaches

This division keeps you in control of your code while dramatically improving efficiency.

### Understanding First, Generation Second

AI-assisted programming emphasizes understanding before acting, not blindly generating code. Good AI coding tools read relevant files first, understand existing architecture and patterns, then make changes consistent with your project's style.

This contrasts sharply with Vibe Coding's "generate first, ask questions later." Understanding-first means generated code is more likely to align with your existing codebase, reducing integration costs.

### Graduated Trust

Nobody suggests letting AI handle core business logic from day one. The right approach:

1. Start with small tasks — write a test, fix a small bug, refactor a function
2. Verify results — run tests, review diffs, read the code
3. Expand gradually — once you have accurate expectations of AI capabilities, increase task scope
4. Maintain verification — tests, code review, manual validation

This graduated approach lets you enjoy AI efficiency without losing control of your code.

Claude Code's design embodies all of the above principles. Let's look at how to install and use it.

## Installation and Setup

### Installation Methods

**Windows (recommended):**

```powershell
irm https://claude.ai/install.ps1 | iex
```

**macOS / Linux (recommended):**

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

**Homebrew (macOS / Linux):**

```bash
brew install --cask claude-code
```

**npm (still works but deprecated):**

```bash
npm install -g @anthropic-ai/claude-code
```

**IDE extensions:**

- VS Code: Search "Claude Code" in the Marketplace, or run `code --install-extension anthropic.claude-code`
- JetBrains: Search "Claude Code" in JetBrains Marketplace

### First-Time Setup

After installation, verify and log in:

```bash
claude --version    # Confirm installation
claude auth login   # Log in to Anthropic account
```

Start your first session:

```bash
claude              # Enter interactive session
```

In a session, use `/init` to let Claude Code analyze your project and auto-generate a `CLAUDE.md` configuration file. This file records your project's architecture, build commands, coding standards, and other information to help Claude Code better understand your project.

Use `/config` to open the settings interface and adjust model, permission mode, and other options.

## Core Usage

### Interactive Sessions

The most basic way to use Claude Code is interactive sessions. Run `claude` in your project directory to start talking with the AI:

```bash
# Start a new session
claude

# Start with an initial prompt
claude "Help me check this project's test coverage"

# Continue the most recent conversation
claude -c

# Resume a specific session
claude -r "abc123"

# Non-interactive mode (for scripts and CI)
claude -p "Run all tests and report results"
```

In a session, you can describe requirements like chatting with a colleague. Claude Code reads relevant files, executes commands, and modifies code — you can see what it's doing throughout and review at key checkpoints.

### Permission Modes

Claude Code has multiple permission modes that control whether it needs your approval before executing operations:

| Mode | Operations without approval | Best for |
|------|---------------------------|----------|
| `default` | Read-only | Sensitive projects, first-time use |
| `acceptEdits` | Read/write files, common filesystem commands | Daily development |
| `plan` | Read-only | Exploring a codebase |
| `auto` | All operations (with safety classifier) | Long tasks |
| `bypassPermissions` | All operations (no safety checks) | Isolated containers/VMs only |

Press `Shift+Tab` in the CLI to switch modes. For daily use, `acceptEdits` is recommended — maintain the habit of reviewing uncertain operations.

### Common Slash Commands

Claude Code provides rich slash commands, organized by workflow:

**During a task:**

- `/plan` — Enter plan mode, plan before executing
- `/model` — Switch models (e.g., from Sonnet to Opus for complex tasks)
- `/effort` — Adjust effort level (low/medium/high/max)
- `/compact` — Compress conversation context, free up token space
- `/context` — View current context usage

**Before committing code:**

- `/diff` — View uncommitted changes
- `/code-review` — Review current diff, find bugs and improvements
- `/security-review` — Analyze changes for security vulnerabilities

**Session management:**

- `/clear` — Clear current conversation, start fresh
- `/resume` — Resume a previous session
- `/branch` — Branch current conversation

**When something goes wrong:**

- `/rewind` — Roll back code and conversation to the last checkpoint
- `/doctor` — Diagnose installation and configuration issues
- `/debug` — Enable debug logging

**Cost management:**

- `/usage` (or `/cost`) — View current session's token usage and costs

### CLAUDE.md Configuration System

`CLAUDE.md` is Claude Code's "project memory" file. It loads automatically at the start of every session, helping Claude Code understand your project.

**File location hierarchy:**

| Scope | Location | Purpose |
|-------|----------|---------|
| User | `~/.claude/CLAUDE.md` | Personal preferences for all projects |
| Project | `./CLAUDE.md` or `./.claude/CLAUDE.md` | Team-shared project documentation |
| Local | `./CLAUDE.local.md` | Personal project config (should be in .gitignore) |

**Importing external files:**

```markdown
See @README.md for project overview
See @package.json for available npm commands
```

**Rules directory:**

Place modular, path-scoped instruction files in `.claude/rules/`:

```markdown
---
paths:
  - "src/api/**/*.ts"
---
All API endpoints must include input validation.
```

Use `/init` to let Claude Code automatically analyze your project and generate an initial `CLAUDE.md`.

### MCP Server Integration

MCP (Model Context Protocol) lets Claude Code connect to external tools and services:

```bash
# Add GitHub MCP server
claude mcp add --transport http github https://api.githubcopilot.com/mcp/ \
  --header "Authorization: Bearer YOUR_GITHUB_PAT"

# Add Sentry error tracking
claude mcp add --transport http sentry https://mcp.sentry.dev/mcp

# Add PostgreSQL database
claude mcp add --transport stdio db -- npx -y @bytebase/dbhub \
  --dsn "postgresql://readonly:pass@localhost:5432/mydb"
```

Management commands:

```bash
claude mcp list          # List all servers
claude mcp get <name>    # View details
claude mcp remove <name> # Remove server
```

Use `/mcp` in a session to check MCP server status and manage connections.

Project-level configuration is stored in `.mcp.json`, which can be committed to Git for team sharing.

### Hooks System

Hooks let you execute custom operations at Claude Code lifecycle events. For example, automatically running a linter after every file modification, or loading specific configurations at session start.

Common events:

- `PreToolUse` — Triggered before tool execution (for interception and validation)
- `PostToolUse` — Triggered after tool execution (for follow-up processing)
- `SessionStart` — Triggered at session start

Configuration in `.claude/settings.json`:

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

## Practical Workflows

### Scenario 1: Understanding an Existing Codebase

When taking over an unfamiliar project, Claude Code helps you build understanding quickly:

```
> What does this project do? Help me understand the overall architecture.

> How does the request handling flow work in the src/api/ directory?

> What's the call chain for this function? Which modules depend on it?
```

Claude Code reads relevant files, analyzes dependencies, and explains with clear structure. This is much faster than flipping through files one by one.

### Scenario 2: Implementing a New Feature

A complete collaboration from requirements to implementation:

```
> I want to add email verification to the user registration feature. First help me understand the current registration flow.
```

Claude Code reads the relevant code and understands the existing architecture. Then you continue:

```
> Good, now help me design the email verification approach, including database schema and API endpoints.
```

After reviewing the plan:

```
> The plan looks good, please implement it. Don't forget to write tests.
```

Key point: you made three decisions in this process — confirming requirements, reviewing the design, approving the implementation. Claude Code handled understanding the code, designing the solution, writing the implementation, and writing tests. You maintained control.

### Scenario 3: Fixing a Bug

```
> Users report that sessions are occasionally lost after login. The error log is at logs/error.log, help me locate the issue.
```

Claude Code reads the logs, analyzes the code, identifies the root cause, and proposes a fix. You can ask it to write a reproducing test first:

```
> Write a test that reproduces this issue first, then fix it.
```

Once the test passes, you have a verified fix and a regression test.

### Scenario 4: Code Refactoring

Refactoring is one of Claude Code's strongest scenarios because it requires understanding the overall code structure:

```
> The functions in src/utils/ are disorganized. Help me reorganize them by functionality without changing any external behavior.
```

Claude Code analyzes existing functions and their dependencies, proposes a refactoring plan, then executes under your review. If you have a test suite, running tests after refactoring confirms nothing is broken.

This echoes the TDD guide's point: tests are the safety net for refactoring.

### Scenario 5: Writing and Running Tests

```
> Write unit tests for src/services/payment.py, covering normal flows and edge cases.
```

Claude Code reads the source file, understands function inputs and outputs, generates test code, then runs it:

```
> Tests written, let me run them.

> 3 tests pass, 1 fails. The failing one is an edge case not handled properly, let me fix it.
```

This "generate-run-fix" cycle is Claude Code's natural workflow and embodies TDD principles in AI-assisted programming.

## AI-Assisted Programming vs Vibe Coding

| Dimension | Vibe Coding | AI-Assisted Programming |
|-----------|-------------|------------------------|
| Code understanding | None — "forget the code exists" | Understand first, then modify |
| Quality control | No tests, no review | Supports TDD, code review |
| Security | 2.74x vulnerability rate vs human code | Built-in security review |
| Learning effect | Skill atrophy | Skill growth |
| Long-term value | Technical debt accumulation | Maintainable code |
| Developer role | Bystander | Decision-maker |

The core difference in one sentence: **Vibe Coding gives up control; AI-assisted programming maintains control.**

Developers using Vibe Coding may feel efficient in the short term, but long-term they're losing the ability to understand code, debug problems, and make architectural decisions. When AI-generated code breaks — and it will — they'll be helpless.

Developers using AI-assisted programming continuously improve: they learn to better express requirements, review code, design architecture, while delegating repetitive coding to AI. AI is an amplifier, not a replacement.

## Cost and Efficiency Management

Claude Code bills by token, so managing costs wisely matters.

**Check spending:**

```
/usage    # View current session's token usage and costs
```

**Cost reduction strategies:**

- **Choose the right model**: Use Sonnet for daily tasks, reserve Opus for complex work. Switch with `/model`
- **Compress context**: Use `/compact` when conversations get long to free up token space
- **Adjust effort level**: Use `/effort low` for simple tasks to reduce unnecessary reasoning
- **Set budget caps**: Use `--max-budget-usd` in non-interactive mode to limit spending
- **Keep CLAUDE.md lean**: Stay under 200 lines to avoid loading excessive context every session
- **Clear unrelated conversations**: Use `/clear` when starting new tasks

## Summary

Claude Code represents the right approach to AI-assisted programming: AI executes, you judge. It doesn't ask you to "forget the code exists" — it helps you understand and control code more efficiently.

For university students, learning to use tools like Claude Code isn't about mastering specific commands or configurations. It's about developing a collaborative mindset: knowing how to clearly express requirements, how to review generated code, how to balance efficiency with quality. These skills matter more in the AI era than ever before — because AI can write your code, but only you can decide what the code should do and whether it's doing it right.
