# AI Safety and Alignment

## Introduction

- Source: [OWASP LLM Top 10](https://owasp.org/www-project-top-10-for-large-language-model-applications/)、[Lakera Gandalf](https://gandalf.lakera.ai/)、[Anthropic AI Safety](https://www.anthropic.com/research)
- Prerequisites: Basic understanding of LLM concepts and usage
- Course difficulty: 🌟�🌟🌟
- Estimated study hours: 15+

As AI becomes increasingly embedded in production systems, **security** is no longer something you can bolt on later. From Prompt Injection attacks to data leaks, from model bias to toxic output — AI system security issues are unique and require specialized knowledge and tools.

For AI engineers, security capability is not optional — it's a **core competency**. An insecure AI system might: leak user privacy, be hijacked by attackers to perform malicious operations, produce harmful content leading to legal risk, or harm specific groups due to bias.

## Course Resources

- Guide: [OWASP LLM Top 10](https://owasp.org/www-project-top-10-for-large-language-model-applications/) — The authoritative list of AI application security risks
- Article: [Anthropic - Challenges in Evaluating AI Systems](https://www.anthropic.com/research/evaluating-ai-systems) — Anthropic's AI safety evaluation methodology
- Article: [Anthropic - Measuring Progress on Scalable Oversight](https://www.anthropic.com/research/measuring-progress-on-scalable-oversight)

## Resource Summary

**Prompt Injection attack and defense:**

- [OWASP LLM01: Prompt Injection](https://genai.owasp.org/llmrisk/llm01-prompt-injection/) — The most dangerous AI attack vector
- [Lakera Gandalf](https://gandalf.lakera.ai/) — Interactive Prompt Injection challenge game, from Level 1 to Level 7, intuitively understand attack principles
- [Simon Willison - Prompt Injection](https://simonwillison.net/series/prompt-injection/) — The most comprehensive collection of Prompt Injection technical articles
- [PromptArmor](https://www.promptarmor.com/) — Tool for detecting Prompt Injection
- [Lakera Red](https://www.lakera.ai/) — Enterprise-grade AI security protection

**AI Alignment:**

- [Anthropic - Core Views on AI Safety](https://www.anthropic.com/news/core-views-on-ai-safety) — Anthropic's perspective on AI safety
- [OpenAI Safety](https://openai.com/safety) — OpenAI's safety research
- [Constitutional AI (Anthropic)](https://arxiv.org/abs/2212.08073) — Method for constraining model behavior with rules
- [RLHF (Reinforcement Learning from Human Feedback)](https://arxiv.org/abs/2204.05862) — How models are "trained" via human feedback

**AI bias and fairness:**

- [Google PAIR - Machine Learning Fairness](https://pair.withgoogle.com/guidebook/) — Google's ML fairness guide
- [IBM AI Fairness 360](https://aif360.mybluemix.net/) — Open-source AI bias detection toolkit
- [HuggingFace - Evaluating Bias](https://huggingface.co/blog/evaluating-llm-bias) — Practical guide to evaluating LLM bias

**Responsible AI frameworks:**

- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework) — NIST's AI risk management framework
- [EU AI Act](https://artificialintelligenceact.eu/) — EU AI Act, understand AI regulatory trends
- [Google AI Principles](https://ai.google/principles/) — Google's AI principles
- [Microsoft Responsible AI](https://www.microsoft.com/en-us/ai/responsible-ai) — Microsoft's responsible AI practices

**Data privacy:**

- [OpenAI Data Usage Policy](https://openai.com/policies/api-data-usage-policies) — Understand how data is used during API calls
- [Differential Privacy](https://en.wikipedia.org/wiki/Differential_privacy) — Mathematical method for protecting training data privacy
- [Presidio (Microsoft)](https://github.com/microsoft/presidio) — Data anonymization and PII detection tool

## Notes

You don't need to become a security expert, but you do need to build security awareness. Minimum requirements:
1. Understand Prompt Injection principles and defense methods
2. Know what sensitive data your AI system might leak
3. Understand basic AI bias detection methods
4. Know the contents of OWASP LLM Top 10

Lakera Gandalf game is the best starting point — spend 1-2 hours completing it, and you'll intuitively understand how attackers bypass AI safety guardrails.
