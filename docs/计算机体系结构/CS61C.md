# Berkeley CS61C: Great Ideas in Computer Architecture

## 课程简介

- 来源：UC Berkeley
- 先修要求：CS61A（Python 编程）、CS61B（数据结构）同等水平
- 编程语言：C、RISC-V 汇编
- 课程难度：🌟🌟🌟🌟
- 预计学时：80 小时 +

Berkeley CS61C 是 Berkeley 的计算机体系结构课程，也是全球最好的体系结构入门课之一。课程从高级语言（C）出发，逐步深入到机器层面（RISC-V 汇编、数字逻辑、CPU 设计）。

CS61C 最大的特点是**实验设计极其出色**。课程有 6 个实验，从 C 语言指针操作到 RISC-V CPU 设计，循序渐进。最终你会用 Logisim 设计出一个能运行 RISC-V 指令集的 CPU。

## 课程资源

- 课程网站：[cs61c.org](https://cs61c.org/)
- 课程视频：[YouTube](https://www.youtube.com/playlist?list=PLDoI6vnvwnMyDQOXD591VnEGDKAOm7lGY)
- 课程笔记：[cs61c.org/](https://cs61c.org/)（课程网站提供完整笔记）
- 配套教材：基于《计算机组成与设计：硬件/软件接口》（RISC-V 版）

## 实验列表

| 实验 | 内容 | 难度 |
|------|------|------|
| Lab 1: C 和指针 | C 语言基础、指针、内存操作 | 🌟🌟 |
| Lab 2: RISC-V 汇编 | 汇编语言、函数调用 | 🌟🌟 |
| Lab 3: 浮点数 | IEEE 754、浮点运算 | 🌟🌟 |
| Lab 4: CPU 设计 | 用 Logisim 设计 RISC-V CPU | 🌟🌟🌟🌟 |
| Lab 5: SIMD 优化 | 向量化计算优化 | 🌟🌟🌟 |
| Lab 6: 缓存优化 | 缓存友好的代码优化 | 🌟🌟🌟 |

## 自学建议

**先掌握 C 语言和指针。** CS61C 对 C 语言要求较高，特别是指针和内存管理。建议先完成 CS61A 或等效的 Python 课程，再学习 C 语言。

**认真做 CPU 设计实验。** Lab 4 是课程的高潮——你用 Logisim 从零设计一个 RISC-V CPU。这个实验能让你真正理解 CPU 的工作原理。

**画数据通路图。** CPU 的数据通路是课程的核心。画出每条指令在数据通路中的执行过程。

## 备注

CS61C 是体系结构入门的最佳课程之一。课程网站上的笔记和实验指南写得非常好，即使不注册课程也能自学。

课程使用的是 RISC-V 版本（而非 x86），RISC-V 更简洁，更容易理解。
