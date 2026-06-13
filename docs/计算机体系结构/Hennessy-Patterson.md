# 计算机体系结构：量化研究方法

## 教材简介

- 来源：John Hennessy、David Patterson（2017 年图灵奖得主）
- 先修要求：计算机组成原理基础
- 课程难度：🌟🌟🌟🌟🌟
- 预计学时：100 小时 +

《计算机体系结构：量化研究方法》（Computer Architecture: A Quantitative Approach）是体系结构领域的"圣经"，作者是 2017 年图灵奖得主 John Hennessy 和 David Patterson。

这本书不是入门教材，而是**深入理解处理器设计和性能优化的权威参考书**。它用"量化"的方法——通过数据和实验来评估不同设计方案的优劣——来讲解体系结构的每一个决策。

## 教材资源

- 官方网站：[Hennessy & Patterson Books](https://www.elsevier.com/books/computer-architecture-a-quantitative-approach/hennessy/978-0-12-811905-1)
- 配套课程：[CMU 15-740](https://www.cs.cmu.edu/~calcm/15-740/)、[Stanford CS149](https://web.stanford.edu/class/cs149/)
- 姐妹书：《计算机组成与设计：硬件/软件接口》（入门版，RISC-V 版推荐）

## 核心内容

### 第一部分：基础
- 量化设计原则
- 存储器层次结构设计
- 指令级并行（ILP）

### 第二部分：数据级并行
- SIMD 和向量处理器
- GPU 架构
- 数据级并行编程

### 第三部分：线程级并行
- 多核处理器架构
- 缓存一致性协议（MESI、MOESI）
- 内存一致性模型

### 第四部分：大规模并行
- 仓库级计算机（Warehouse-Scale Computers）
- 数据中心架构
- 互连网络

## 自学建议

**先读《计算机组成与设计》。** 那是这本书的入门版，先打好基础再读这本。

**重点关注量化分析方法。** 这本书的核心不是记住各种架构，而是学会用数据和实验来评估设计决策。

**配合论文阅读。** 书中引用了大量经典论文，建议选读几篇感兴趣的。

## 备注

这本书适合想深入研究体系结构的人。如果你只是需要应付考试或面试，读《计算机组成与设计》就够了。

Hennessy 和 Patterson 在 2017 年因对 RISC 架构的贡献获得图灵奖，这本书是他们毕生研究的结晶。
