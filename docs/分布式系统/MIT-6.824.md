# MIT 6.824: Distributed Systems

## 课程简介

- 来源：MIT
- 先修要求：操作系统基础、计算机网络基础、Go 语言基础
- 编程语言：Go
- 课程难度：🌟🌟🌟🌟
- 课程网站：[pdos.csail.mit.edu/6.824](https://pdos.csail.mit.edu/6.824/)

MIT 6.824 是 MIT 的分布式系统课程，被公认为全球最好的分布式系统课程。课程的核心是实现 Raft 共识算法和一个基于 Raft 的分布式 KV 存储。

## 课程资源

- 课程网站：[pdos.csail.mit.edu/6.824](https://pdos.csail.mit.edu/6.824/)
- 课程视频：[YouTube](https://www.youtube.com/playlist?list=PLrw6a1wE39_tb2fErI4-WkMbsvGQk9_UB)
- 实验代码：[MIT 6.824 Labs](https://pdos.csail.mit.edu/6.824/labs/)

## 实验列表

| 实验 | 内容 | 难度 |
|------|------|------|
| Lab 1: MapReduce | 实现 MapReduce 框架 | 🌟🌟 |
| Lab 2: Raft | 实现 Raft 共识算法 | 🌟🌟🌟🌟 |
| Lab 3: KV Server | 基于 Raft 实现 KV 存储 | 🌟🌟🌟🌟 |
| Lab 4: Sharded KV | 实现分片 KV 存储 | 🌟🌟🌟🌟🌟 |

## 自学建议

**Go 语言要扎实。** 课程用 Go 实现，需要熟悉 Go 的并发模型（goroutine、channel）。

**先读 Raft 论文。** Raft 论文是课程的核心，建议先读论文再做实验。

**每个实验预留 2-3 周。** Raft 实验尤其耗时，不要赶进度。

## 备注

6.824 是分布式系统课程中实验设计最好的。完成所有实验后，你对分布式系统的理解会超过大多数从业者。

Raft 是当今工业界最广泛使用的共识算法之一（etcd、TiKV、CockroachDB 都使用 Raft），掌握它是分布式系统工程师的基本功。
