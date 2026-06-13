# Building RAG Systems

## Introduction

- Source: [LangChain RAG Course](https://www.langchain.com/learn/retrieval-augmented-generation)、[LlamaIndex Documentation](https://docs.llamaindex.ai/)、[Harrison Chase — Building Advanced RAG](https://www.youtube.com/watch?v=sVcwVQRHlDo)
- Prerequisites: Python basics, basic understanding of LLM concepts, basic understanding of vector databases
- Programming language: Python
- Course difficulty: 🌟🌟🌟🌟
- Estimated study hours: 25+

**RAG (Retrieval-Augmented Generation)** is currently the most mainstream LLM application technique. The core idea is simple: **don't stuff all knowledge into the prompt — instead, "retrieve" relevant knowledge snippets when needed, then let the model generate based on that knowledge.**

This addresses several fundamental LLM problems:
- **Hallucinations**: Let the model answer based on retrieved real documents, not fabrication
- **Knowledge freshness**: Training data has a cutoff date; RAG can connect to the latest external data
- **Domain knowledge**: No fine-tuning needed to make the model "understand" your domain
- **Traceability**: Answers can cite sources for user verification

Many "knowledge base Q&A" products you use today — customer service bots, document assistants, enterprise search — are essentially RAG under the hood. In Andrew Ng's Buildathon demo, RAG was the most frequently appearing building block.

## Course Resources

- Course: [LangChain RAG Course (LangChain Academy)](https://academy.langchain.com/courses/intro-to-rag) — Free, covers the complete RAG pipeline, highly recommended
- Documentation: [LlamaIndex Documentation](https://docs.llamaindex.ai/) — Another mainstream RAG framework with excellent documentation
- Course videos: [Andrew Ng - LangChain: Chat With Your Data](https://learn.deeplearning.ai/courses/langchain-chat-with-your-data) — Short course, quick to get started

## Resource Summary

**Beginner (understanding the full RAG pipeline):**

- [Andrew Ng - LangChain for LLM Application Development](https://learn.deeplearning.ai/courses/langchain) — 3 hours, covers RAG basics (chunking, embedding, retrieval, generation)
- [Jay Alammar - RAG from Scratch](https://www.youtube.com/watch?v=sVcwVQRHlDo) — Build a RAG system from scratch, understand what each component does
- [Full Stack LLM Bootcamp - RAG Lecture](https://fullstackdeeplearning.com/llm-bootcamp/) — Stanford's free LLM bootcamp RAG section, excellent quality

**Advanced (engineering-grade RAG):**

- [LangChain RAG from Scratch (YouTube Series)](https://www.youtube.com/playlist?list=PLfaIDFEXuae2LXbO1_PKyVJiQ23ZztA0x) — Harrison Chase walks you through building RAG from scratch, covering advanced retrieval strategies
- [LlamaIndex - Advanced RAG Techniques](https://docs.llamaindex.ai/en/stable/examples/) — Covers HyDE, RAPTOR, Self-RAG, and other advanced techniques
- [RAG Survey Paper](https://arxiv.org/abs/2312.10997) — Survey paper covering the academic frontier

**Deep dive into retrieval quality (RAG bottlenecks are usually in retrieval, not generation):**

- [ColBERT: Efficient and Effective Passage Search](https://arxiv.org/abs/2004.12832) — Classic fine-grained retrieval method
- [HyDE: Hypothetical Document Embeddings](https://arxiv.org/abs/2212.10496) — Use model-generated "hypothetical answers" to improve retrieval
- [Parent-Child Chunking Strategy](https://www.youtube.com/watch?v=cDa2M2VfQ7Q) — Practical technique for balancing retrieval granularity
- [Lost in the Middle: How Language Models Use Long Contexts](https://arxiv.org/abs/2307.03172) — Research showing models tend to lose information in the middle of long contexts, important for RAG chunk design

**Hands-on project:**

Build a "personal knowledge base Q&A system" from scratch:
1. Pick a domain you're familiar with (course notes, technical docs, novel setting bibles)
2. Use LangChain or LlamaIndex for document loading and chunking
3. Choose an Embedding model (recommend `text-embedding-ada-002` or open-source `bge-large-zh`)
4. Store in a vector database (recommend Qdrant or Chroma)
5. Connect to an LLM for Q&A
6. Evaluate results, iterate on retrieval strategy

## Notes

The hard part of RAG isn't "stuffing documents in" — it's **retrieval quality**. 90% of RAG effectiveness problems come from chunking strategy, Embedding selection, or retrieval algorithms. Start by building the simplest possible RAG pipeline (can be done in ~50 lines of code), then spend time evaluating and improving retrieval quality. Both LangChain and LlamaIndex are great for learning, but production environments usually require custom components.
