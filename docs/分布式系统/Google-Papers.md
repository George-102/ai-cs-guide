# Google 三驾马车：GFS、MapReduce、Bigtable

## 论文简介

- 来源：Google（Sanjay Ghemawat、Jeff Dean 等）
- 先修要求：操作系统基础、计算机网络基础
- 课程难度：🌟🌟🌟🌟
- 预计学时：20 小时 +

Google 的三篇经典论文——GFS（Google File System）、MapReduce、Bigtable——奠定了现代分布式系统的基础。Hadoop、HBase、Spark 等开源项目都直接受这些论文影响。

阅读这三篇论文，你不仅能理解分布式系统的核心设计思想，还能看到工业界如何解决真实的分布式问题。

## 论文资源

### GFS: The Google File System
- 论文：[GFS Paper](https://research.google/pubs/pub62/)（SOSP 2003）
- 核心思想：分布式文件系统，通过数据分片和副本实现高可用

### MapReduce: Simplified Data Processing on Large Clusters
- 论文：[MapReduce Paper](https://research.google/pubs/pub62/)（OSDI 2004）
- 核心思想：大规模数据处理的编程模型，自动并行化和容错

### Bigtable: A Distributed Storage System for Structured Data
- 论文：[Bigtable Paper](https://research.google/pubs/pub27897/)（OSDI 2006）
- 核心思想：分布式结构化数据存储，基于 GFS 和 SSTable

## 自学建议

**按顺序阅读。** GFS → MapReduce → Bigtable，后者依赖前者的技术。

**关注设计取舍。** 每篇论文都做了大量的工程权衡，理解这些权衡比记住设计细节更重要。

**配合 MIT 6.824 使用。** 论文讲设计思想，6.824 让你动手实现。

## 备注

这三篇论文是分布式系统的"圣经"。即使你没有时间读其他分布式系统论文，这三篇也必读。

后来的开源项目（Hadoop、HBase、Cassandra、Spark）都直接受这些论文影响。
