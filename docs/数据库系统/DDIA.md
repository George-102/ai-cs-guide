# DDIA: 数据密集型应用系统设计

## 教材简介

- 来源：Martin Kleppmann（University of Cambridge）
- 先修要求：数据库基础、计算机网络基础、操作系统基础
- 课程难度：🌟🌟🌟🌟
- 预计学时：80 小时 +

《数据密集型应用系统设计》（Designing Data-Intensive Applications，简称 DDIA）是 Martin Kleppmann 编写的神书，被无数工程师誉为"后端开发的圣经"。

这本书的主题是：**如何设计和构建大规模、高可靠、可扩展的数据系统**。它不是某一种技术的入门教程，而是帮你建立对分布式数据系统的全面理解。

## 教材资源

- 官方资源：[dataintensive.net](https://dataintensive.net/)
- 中文翻译：《数据密集型应用系统设计》（中国电力出版社）
- 配套讲座：[Martin Kleppmann Lectures](https://www.youtube.com/playlist?list=PLmR rlAvgOH8RZUgMELdY270nxLMO8QGc)

## 核心内容

### 第一部分：数据系统的基石
- 数据模型与查询语言
- 存储与检索（B+ 树、LSM 树、列存储）
- 编码与演化（JSON、Protobuf、 Avro、Thrift）

### 第二部分：分布式数据系统
- 数据复制（主从复制、多主复制、无主复制）
- 数据分区（哈希分区、范围分区）
- 分布式事务与共识（2PC、Paxos、Raft）

### 第三部分：衍生数据
- 批处理（MapReduce、Spark）
- 流处理（Kafka、Flink）
- 数据系统的未来

## 自学建议

**先有数据库和网络基础。** 这本书假设你已经了解基本的数据库和网络概念。

**按主题阅读，不要按顺序。** 你可以根据自己的需要选读感兴趣的章节。

**做书后的思考题。** 每章都有思考题，能帮你检验理解程度。

## 备注

DDIA 是后端工程师必读的书。不理解它，你只能调 API；理解了它，你能设计系统。

这本书也是很多大公司系统设计面试的参考书。
