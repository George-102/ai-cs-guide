# MIT 6.S081: Operating System Engineering

## 课程简介

- 来源：MIT
- 先修要求：计算机体系结构基础、C 语言
- 编程语言：C
- 课程难度：🌟🌟🌟🌟
- 预计学时：80 小时 +

MIT 6.S081（原 6.828）是 MIT 的操作系统课程，基于 xv6 教学操作系统。这门课被公认为全球最好的操作系统入门课程之一——不是因为它讲得最全面，而是因为它让你**真正动手实现一个操作系统**。

课程的核心是 7 个实验（lab），每个实验要求你为 xv6 内核添加一个核心功能：进程管理、内存管理、文件系统、网络等。做完这些实验，你对操作系统的理解会超过 90% 的 CS 毕业生。

## 课程资源

- 课程网站：[pdos.csail.mit.edu/6.828](https://pdos.csail.mit.edu/6.828/2023/)
- 课程视频：[YouTube 2020 年版](https://www.youtube.com/playlist?list=PLf3u8NhoEikhTC5radGrmmqdkOK-xMDoO)
- 教材：[xv6 Book](https://pdos.csail.mit.edu/6.828/2023/xv6/book-riscv-rev3.pdf)（免费 PDF）
- 实验代码：[xv6-riscv](https://github.com/mit-pdos/xv6-riscv)

## 实验列表

| 实验 | 内容 | 难度 |
|------|------|------|
| Lab 1: Unix utilities | 实现 xarg、sleep 等基础命令 | 🌟 |
| Lab 2: System calls | 添加系统调用，理解内核态切换 | 🌟🌟 |
| Lab 3: Page tables | 实现页表，理解虚拟内存 | 🌟🌟🌟 |
| Lab 4: Traps | 实现中断和异常处理 | 🌟🌟🌟 |
| Lab 5: Copy-on-write fork | 实现写时复制 | 🌟🌟🌟 |
| Lab 6: Multithreading | 实现多线程和锁 | 🌟🌟🌟🌟 |
| Lab 7: Network driver | 实现网卡驱动 | 🌟🌟🌟🌟 |
| Lab 8: File system | 实现文件系统 | 🌟🌟🌟🌟🌟 |
| Lab 9: mmap | 实现内存映射 | 🌟🌟🌟🌟 |

## 自学建议

**先读 xv6 Book 前 3 章。** 不要一上来就做实验。先理解 xv6 的基本架构（进程、内存、文件系统的实现），再开始写代码。

**每个实验预留 1-2 周。** 实验难度递增，后面的实验（文件系统、mmap）可能需要 2 周以上。不要赶进度。

**善用 GDB 调试。** 操作系统代码的调试和普通程序不同。学会用 GDB 调试内核代码是这门课最重要的技能之一。

**参考但不照抄。** 网上有很多实验的参考实现，但直接照抄等于没学。先自己思考，卡住了再看参考。

## 备注

这门课的工作量很大，但收获也是巨大的。如果你能独立完成所有实验，操作系统面试中的任何问题都不在话下。

2023 年后的版本从 x86 切换到了 RISC-V 架构，实验代码更简洁，推荐学习新版。
