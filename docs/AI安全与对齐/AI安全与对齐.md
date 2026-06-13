# AI 安全与对齐

## 简介

- 来源：[OWASP LLM Top 10](https://owasp.org/www-project-top-10-for-large-language-model-applications/)、[Lakera Gandalf](https://gandalf.lakera.ai/)、[Anthropic AI Safety](https://www.anthropic.com/research)
- 先修要求：了解 LLM 基本概念和使用方法
- 课程难度：🌟🌟🌟
- 预计学时：15 小时 +

随着 AI 越来越深入生产系统，**安全**不再是可以事后补救的事情。从 Prompt Injection 攻击到数据泄露，从模型偏见到有毒输出——AI 系统的安全问题是独特的，需要专门的知识和工具来解决。

对 AI 工程师来说，安全能力不是可选的，而是**核心素养**。一个不安全的 AI 系统可能：泄露用户隐私、被攻击者劫持执行恶意操作、输出有害内容导致法律风险、或因为偏见损害特定群体。

## 课程资源

- 指南：[OWASP LLM Top 10](https://owasp.org/www-project-top-10-for-large-language-model-applications/) — AI 应用安全风险的权威清单
- 文章：[Anthropic - Challenges in Evaluating AI Systems](https://www.anthropic.com/research/evaluating-ai-systems) — Anthropic 的 AI 安全评估方法论
- 文章：[Anthropic - Measuring Progress on Scalable Oversight](https://www.anthropic.com/research/measuring-progress-on-scalable-oversight)

## 资源汇总

**Prompt Injection 攻防：**

- [OWASP LLM01: Prompt Injection](https://genai.owasp.org/llmrisk/llm01-prompt-injection/) — 最危险的 AI 攻击向量
- [Lakera Gandalf](https://gandalf.lakera.ai/) — 互动式 Prompt Injection 挑战游戏，从 Level 1 到 Level 7，非常直观地理解攻击原理
- [Simon Willison - Prompt Injection](https://simonwillison.net/series/prompt-injection/) — 最全面的 Prompt Injection 技术文章集合
- [PromptArmor](https://www.promptarmor.com/) — 检测 Prompt Injection 的工具
- [Lakera Red](https://www.lakera.ai/) — 企业级 AI 安全防护

**AI 对齐（Alignment）：**

- [Anthropic - Core Views on AI Safety](https://www.anthropic.com/news/core-views-on-ai-safety) — Anthropic 的 AI 安全观
- [OpenAI Safety](https://openai.com/safety) — OpenAI 的安全研究
- [Constitutional AI (Anthropic)](https://arxiv.org/abs/2212.08073) — 用规则约束模型行为的方法
- [RLHF (Reinforcement Learning from Human Feedback)](https://arxiv.org/abs/2204.05862) — 人类反馈强化学习，理解模型如何被"调教"

**AI 偏见与公平性：**

- [Google PAIR - Machine Learning Fairness](https://pair.withgoogle.com/guidebook/) — Google 的 ML 公平性指南
- [IBM AI Fairness 360](https://aif360.mybluemix.net/) — 开源 AI 偏见检测工具包
- [HuggingFace - Evaluating Bias](https://huggingface.co/blog/evaluating-llm-bias) — 评估 LLM 偏见的实践指南

**负责任 AI 框架：**

- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework) — 美国国家标准与技术研究院的 AI 风险管理框架
- [EU AI Act](https://artificialintelligenceact.eu/) — 欧盟 AI 法案，了解 AI 监管趋势
- [Google AI Principles](https://ai.google/principles/) — Google 的 AI 原则
- [Microsoft Responsible AI](https://www.microsoft.com/en-us/ai/responsible-ai) — 微软的负责任 AI 实践

**数据隐私：**

- [OpenAI Data Usage Policy](https://openai.com/policies/api-data-usage-policies) — 了解 API 调用时数据如何被使用
- [Differential Privacy](https://en.wikipedia.org/wiki/Differential_privacy) — 差分隐私，保护训练数据隐私的数学方法
- [Presidio (Microsoft)](https://github.com/microsoft/presidio) — 数据脱敏和 PII 检测工具

## 备注

AI 安全不需要你成为安全专家，但需要你建立安全意识。最低要求：
1. 理解 Prompt Injection 的原理和防御方法
2. 知道你的 AI 系统可能泄露哪些敏感数据
3. 了解基本的 AI 偏见检测方法
4. 知道 OWASP LLM Top 10 的内容

Lakera Gandalf 游戏是最佳入门方式——花 1-2 小时通关，你就能直观理解攻击者如何绕过 AI 的安全限制。
