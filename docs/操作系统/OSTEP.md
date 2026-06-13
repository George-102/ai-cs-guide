# OSTEP: Operating Systems: Three Easy Pieces

## 教材简介

- 来源：University of Wisconsin-Madison（Remzi Arpaci-Dusseau）
- 先修要求：C 语言基础、计算机体系结构基础
- 课程难度：🌟🌟🌟
- 预计学时：60 小时 +

OSTEP（Operating Systems: Three Easy Pieces）是全球最受欢迎的操作系统教材之一，完全免费在线阅读。书名中的"三块"指的是操作系统的三大核心主题：**虚拟化（Virtualization）、并发（Concurrency）、持久化（Persistence）**。

这本书最大的特点是**讲解极其清晰**。作者 Remzi Arpaci-Dusseau 是威斯康星大学的教授，也是操作系统领域的顶级研究者。他用通俗的语言和生动的类比把复杂的概念讲得明明白白。

## 教材资源

- 官方网站：[pages.cs.wisc.edu/~remzi/OSTEP/](https://pages.cs.wisc.edu/~remzi/OSTEP/)
- 在线阅读：完全免费，支持 PDF 下载
- 配套项目：[OSTEP Projects](https://pages.cs.wisc.edu/~remzi/OSTEP/projects/)（编程作业）
- 中文翻译：[OSTEP 中文版](https://github.com/remzi-arpacidusseau/ostep-translations/tree/master/chinese)（社区翻译）

## 内容结构

### 第一部分：虚拟化（Virtualization）
- CPU 虚拟化：进程、进程 API、受限直接执行、进程调度
- 内存虚拟化：地址空间、内存 API、地址转换、分段、空闲空间管理

### 第二部分：并发（Concurrency）
- 线程和锁
- 条件变量
- 信号量
- 并发 bug
- 基于事件的并发

### 第三部分：持久化（Persistence）
- I/O 设备
- 磁盘驱动器
- RAID
- 文件系统实现
- FSCK 和日志
- 分布式系统简介

## 自学建议

**按顺序阅读，不要跳章。** 这本书的章节之间有很强的依赖关系。前面的概念是后面的基础。

**做书后的编程项目。** 每个章节都有配套的编程作业（用 C 语言实现），这些项目能帮你把理论转化为实践。

**配合 MIT 6.S081 使用。** OSTEP 讲理论，6.S081 做实验。两者结合，理论和实践都不落下。

**不要只看中文翻译。** 英文原版写得非常流畅，建议直接读英文。遇到不懂的术语再参考中文版。

## 备注

这本书是操作系统入门的最佳教材之一。如果你时间有限，只读这本书 + 做 MIT 6.S081 实验，就足以建立扎实的操作系统基础。
