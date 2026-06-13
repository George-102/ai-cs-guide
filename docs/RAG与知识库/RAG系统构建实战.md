# RAG 系统构建实战

## 简介

- 来源：[LangChain RAG Course](https://www.langchain.com/learn/retrieval-augmented-generation)、[LlamaIndex 文档](https://docs.llamaindex.ai/)、[Harrison Chase — Building Advanced RAG](https://www.youtube.com/watch?v=sVcwVQRHlDo)
- 先修要求：Python 基础、了解大模型基本概念、了解向量数据库基本原理
- 编程语言：Python
- 课程难度：🌟🌟🌟🌟
- 预计学时：25 小时 +

**RAG（Retrieval-Augmented Generation，检索增强生成）** 是目前最主流的 LLM 应用技术。它的核心思路很简单：**不要把所有知识都塞进提示词里，而是在需要时去"检索"相关的知识片段，再让模型基于这些知识来回答。**

这解决了大模型的几个根本问题：
- **幻觉**：让模型基于检索到的真实文档回答，而不是凭空编造
- **知识时效性**：训练数据有截止日期，RAG 可以接入最新的外部数据
- **领域知识**：不需要微调就能让模型"懂"你的专业领域
- **可溯源**：回答可以标注来源，用户可以验证

你现在用的很多"知识库问答"产品——客服机器人、文档助手、企业搜索——本质上都是 RAG。吴恩达在 Buildathon 上演示的 AI 应用场景中，RAG 是最频繁出现的构建模块。

## 课程资源

- 课程：[LangChain Academy](https://academy.langchain.com/) — 免费课程，覆盖 RAG 完整流程，强烈推荐
- 文档：[LlamaIndex Documentation](https://docs.llamaindex.ai/) — 另一个主流 RAG 框架，文档质量很高
- 课程视频：[吴恩达 - LangChain: Chat With Your Data](https://learn.deeplearning.ai/courses/langchain-chat-with-your-data) — 短期课程，快速上手

## 资源汇总

**入门（理解 RAG 全流程）：**

- [吴恩达 - LangChain for LLM Application Development](https://learn.deeplearning.ai/courses/langchain) — 3小时，覆盖 RAG 基础（分块、嵌入、检索、生成）
- [Jay Alammar - RAG from Scratch](https://www.youtube.com/watch?v=sVcwVQRHlDo) — `Jay Alammar` 从零实现 RAG 系统，帮你理解每个环节的本质
- [Full Stack LLM Bootcamp - RAG Lecture](https://fullstackdeeplearning.com/llm-bootcamp/) — 斯坦福免费 LLM 训练营中的 RAG 部分，质量极高

**进阶（工程化 RAG）：**

- [LangChain RAG from Scratch (YouTube Series)](https://www.youtube.com/playlist?list=PLfaIDFEXuae2LXbO1_PKyVJiQ23ZztA0x) — Harrison Chase 亲自带你从零构建 RAG，涵盖高级检索策略
- [LlamaIndex - Advanced RAG Techniques](https://docs.llamaindax.ai/en/stable/examples/) — 涵盖了 HyDE、RAPTOR、Self-RAG 等高级技术
- [RAG Survey Paper](https://arxiv.org/abs/2312.10997) — 综述论文，了解学术前沿

**深入检索质量（RAG 的瓶颈往往在检索不在生成）：**

- [ColBERT: Efficient and Effective Passage Search](https://arxiv.org/abs/2004.12832) — 细粒度检索的经典方法
- [HyDE: Hypothetical Document Embeddings](https://arxiv.org/abs/2212.10496) — 用模型生成"假设答案"来改进检索
- [Parent-Child Chunking Strategy](https://www.youtube.com/watch?v=cDa2M2VfQ7Q) — 平衡检索粒度的实用技巧
- [Lost in the Middle: How Language Models Use Long Contexts](https://arxiv.org/abs/2307.03172) — 研究表明模型在长上下文中间容易丢失信息，这对 RAG 的 chunk 设计很重要

**动手实践项目：**

从零开始构建一个"个人知识库问答系统"：
1. 选一个你熟悉的领域（课程笔记、技术文档、小说设定集）
2. 用 LangChain 或 LlamaIndex 做文档加载和分块
3. 选一个 Embedding 模型（推荐 `text-embedding-ada-002` 或开源的 `bge-large-zh`）
4. 存入向量数据库（推荐 Qdrant 或 Chroma）
5. 接入 LLM 做问答
6. 评估效果，迭代改进检索策略

## 备注

RAG 的难点不在"把文档塞进去"，而在**检索质量**。90% 的 RAG 效果问题都出在分块策略、Embedding 选型或检索算法上。建议先搭一个最基础的 RAG pipeline（可以只用 50 行代码），然后花时间在评估和改进检索质量上。LangChain 和 LlamaIndex 都适合入门，但生产环境通常需要自研部分组件。
