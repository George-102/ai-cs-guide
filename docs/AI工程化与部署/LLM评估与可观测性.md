# LLM 评估与可观测性

## 简介

- 来源：[OpenEvals](https://github.com/langchain-ai/openevals)、[RAGAS](https://docs.ragas.io/)、[DeepEval](https://github.com/confident-ai/deepeval)
- 先修要求：Python 基础、了解 LLM API 调用
- 编程语言：Python
- 课程难度：🌟🌟🌟🌟
- 预计学时：15 小时 +

传统软件测试有明确的 pass/fail，但 LLM 的输出是自然语言——怎么判断它对不对？这就是 **LLM 评估**要解决的问题。

LLM 评估是 AI 工程化中最被低估的环节。没有评估，你无法：
- 知道你的 prompt 改动是否真的提升了效果
- 发现 RAG 系统是否在检索错误的文档
- 判断模型是否在特定场景下产生幻觉
- 向团队/用户证明你的 AI 系统是可信赖的

## 课程资源

- 文档：[RAGAS Documentation](https://docs.ragas.io/) — 专注 RAG 系统评估
- 文档：[DeepEval Documentation](https://docs.confident-ai.com/) — 类 pytest 的 LLM 测试框架
- 论文：[Holistic Evaluation of Language Models (HELM)](https://arxiv.org/abs/2211.09110) — 斯坦福的 LLM 综合评估框架

## 资源汇总

**评估方法论：**

- [OpenEvals (LangChain)](https://github.com/langchain-ai/openevals) — 开源评估框架，支持自定义评估器
- [RAGAS](https://docs.ragas.io/) — 专门评估 RAG 系统的质量（忠实度、相关性、精确度）
- [DeepEval](https://github.com/confident-ai/deepeval) — 写起来像 pytest 的 LLM 测试框架
- [Promptfoo](https://www.promptfoo.dev/) — 命令行 LLM 评估工具，支持多模型横向对比

**评估维度：**

| 维度 | 含义 | 工具 |
|------|------|------|
| **忠实度 (Faithfulness)** | 回答是否基于检索到的文档，而非编造 | RAGAS |
| **相关性 (Relevance)** | 检索到的文档是否与问题相关 | RAGAS |
| **准确性 (Correctness)** | 回答是否事实正确 | LLM-as-Judge |
| **安全性 (Safety)** | 是否包含有害内容 | OpenAI Moderation API |
| **流畅度 (Fluency)** | 语言是否自然流畅 | 人工评估 |
| **延迟 (Latency)** | 响应时间是否可接受 | 自定义监控 |

**LLM-as-Judge（用 LLM 评估 LLM）：**

- [OpenAI Cookbook - LLM-as-Judge](https://cookbook.openai.com/examples/evaluation/use_llms_to_evaluate_llms) — 用强模型评估弱模型的输出
- [JudgeLM](https://github.com/baaivision/JudgeLM) — 专门训练的评判模型
- 注意：LLM-as-Judge 本身也有偏差，需要人工校准

**可观测性（Observability）：**

- [LangSmith](https://www.langchain.com/langsmith) — LLM 应用的 tracing、debugging、monitoring
- [LangFuse](https://langfuse.com/) — 开源 LLM 可观测性平台，支持 tracing、评估、提示管理
- [Weights & Biases (W&B)](https://wandb.ai/) — ML 实验追踪，也支持 LLM 评估追踪
- [OpenTelemetry for LLM](https://opentelemetry.io/) — 标准化 LLM 应用的遥测数据

**评估数据集：**

- [MMLU](https://arxiv.org/abs/2009.03300) — 大规模多任务语言理解基准
- [HumanEval](https://arxiv.org/abs/2107.03374) — 代码生成能力评估
- [MT-Bench](https://arxiv.org/abs/2306.05685) — 多轮对话能力评估
- [AlpacaEval](https://github.com/tatsu-lab/alpaca_eval) — 指令遵循能力评估

## 备注

评估是迭代开发的基础。没有评估数据，你的改进就是"感觉上好了"而不是"确实好了"。建议从一开始就建立评估习惯：每次改 prompt 或换模型，都跑一遍评估集，用数据说话。

入门建议：先用 RAGAS 评估你的 RAG 系统（5分钟上手），再用 DeepEval 为你的 LLM 应用写测试用例。这两个工具组合起来能覆盖大部分评估需求。
