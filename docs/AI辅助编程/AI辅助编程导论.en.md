# Introduction to AI-Assisted Programming

## Introduction

- Source: Comprehensive compilation
- Prerequisites: Proficiency in at least one programming language (Python/Java/C++)
- Course difficulty: 🌟🌟
- Estimated study hours: 10+

AI-Assisted Programming refers to **a set of methods and practices that leverage AI tools to improve software development efficiency**. It's not about AI replacing you as a programmer — it's about AI becoming your programming partner: you think and decide, AI executes and accelerates.

From GitHub Copilot's code completion, to Claude Code's agentic programming, to Cursor's IDE integration — AI programming tools are evolving rapidly. But tools are just the means; the core is how you collaborate with AI.

## Why This Course

**AI tools are reshaping how we program.** Andrew Ng demonstrated at Buildathon how AI-assisted programming can accelerate independent developers' prototyping speed by 10x. This isn't the future — it's happening now.

**Knowing how to use a tool doesn't mean using it well.** Many people use ChatGPT to write code with mixed results. The difference: do you understand AI's capabilities and limitations? Do you know how to express requirements clearly? Can you review AI-generated code?

**Avoid the Vibe Coding trap.** Accepting AI-generated code without review looks fast in the short term but accumulates massive technical debt and security vulnerabilities over time. This course teaches the correct way to collaborate with AI.

## Core Knowledge Modules

### Evolution of AI Programming Tools

- **Code completion era**: Tabnine, GitHub Copilot — context-based line/function completion
- **Conversational programming era**: ChatGPT, Claude — generate code through natural language conversation
- **Agentic programming era**: Claude Code, Cursor, Devin — AI can autonomously plan and execute multi-step tasks
- **IDE integration era**: AI deeply integrated into development environments, understanding entire codebases

### Core Collaboration Patterns

- **You describe, AI generates**: Describe requirements in natural language, AI produces code drafts
- **AI generates, you review**: Carefully read AI-generated code, verify correctness
- **You write the framework, AI fills the details**: You design architecture and interfaces, AI implements specific functions
- **AI-assisted debugging**: Give error messages to AI for help locating and fixing issues
- **AI-assisted refactoring**: Let AI improve code structure, naming, and performance

### Keys to Writing Good Prompts

- **Provide clear context**: Tell AI the language, framework, and coding standards of your project
- **Decompose complex tasks**: Break large tasks into small ones, complete them incrementally
- **Provide examples**: Use Few-Shot examples to help AI understand your desired style
- **Specify output format**: Be explicit about function signatures, return values, error handling
- **Iterate and refine**: If the first result isn't satisfactory, add more information and regenerate

### Code Review Checklist for AI-Generated Code

- Does the code handle edge cases correctly?
- Are there security vulnerabilities (SQL injection, XSS, path traversal, etc.)?
- Are there performance issues (unnecessary loops, memory leaks)?
- Are names clear? Is the logic readable?
- Is there test coverage?

## How to Learn

**Pick one tool and use it deeply.** Recommended starting point: Claude Code or Cursor — they represent the current state of the art in AI programming tools. Use them in real projects, not just tutorials.

**Start with simple tasks.** Have AI help you write utility functions, write tests, and refactor small code blocks. Gradually build accurate expectations of AI capabilities.

**Always review.** Every line of AI-generated code should pass through your review. This isn't about distrusting AI — it's about taking responsibility for your own code.

**Combine with TDD practice.** Write tests first, then have AI generate the implementation. Tests are the "contract" for AI-generated code and your safety net for verifying correctness.

## Recommended Resources

**Tools**

- [Claude Code](https://claude.ai/code) — Anthropic's official agentic coding tool, available in terminal, IDE, and web
- [Cursor](https://cursor.com/) — AI-native IDE with deep codebase understanding
- [GitHub Copilot](https://github.com/features/copilot) — The original AI code completion tool, integrated with VS Code
- [Windsurf](https://codeium.com/windsurf) — AI IDE from Codeium
- [Devin](https://devin.ai/) — Autonomous AI programming agent from Cognition

**Courses and articles**

- [Andrew Ng - AI Agents in LangGraph](https://learn.deeplearning.ai/courses/ai-agents-langgraph) — Understand the underlying logic of agentic programming
- [Anthropic - Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) — Best practices for Agent design
- [Simon Willison - AI Assisted Programming](https://simonwillison.net/series/ai-assisted-programming/) — Extensive practical experience sharing

**Related courses**

- [Claude Code Guide](./Claude Code指南.md) — Deep dive into Claude Code configuration and usage
- [Test-Driven Development](./测试驱动开发.md) — TDD is the best companion to AI-assisted programming
