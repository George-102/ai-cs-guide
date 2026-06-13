# Nand2Tetris: The Elements of Computing Systems

## 课程简介

- 来源：希伯来大学（Noam Nisan、Shimon Schocken）
- 先修要求：无，零基础友好
- 编程语言：HDL（硬件描述语言）、Jack（类 Java）、汇编
- 课程难度：🌟🌟🌟
- 预计学时：80 小时 +

Nand2Tetris 是一门传奇课程：**从与非门（NAND gate）开始，一步步构建出一个完整的计算机系统，最终在它上面运行一个俄罗斯方块游戏。**

这门课的理念是：计算机系统中没有"魔法"。从最底层的逻辑门到最高层的操作系统和编译器，每一层都可以从上一层的抽象中构建出来。当你亲手完成这个过程，你会对计算机系统有从内到外的理解。

## 课程资源

- 课程网站：[nand2tetris.org](https://www.nand2tetris.org/)
- 课程视频：[Coursera Part 1](https://www.coursera.org/learn/build-a-computer) | [Coursera Part 2](https://www.coursera.org/learn/nand2tetris2)
- 教材：《The Elements of Computing Systems》（免费 PDF 可下载）
- 软件工具：[下载页面](https://www.nand2tetris.org/software)（HDL 模拟器、汇编器、虚拟机模拟器等）

## 课程结构

### Part 1：从硬件到计算机（第 1-5 章）
1. **布尔逻辑**：用与非门构建基本逻辑门（AND、OR、NOT、XOR、MUX、DMUX）
2. **布尔运算**：构建 ALU（算术逻辑单元）
3. **时序逻辑**：构建寄存器和内存（RAM）
4. **机器语言**：设计指令集架构
5. **计算机架构**：将所有组件组合成一台完整的计算机（Hack 计算机）

### Part 2：从汇编到编译器（第 6-11 章）
6. **汇编器**：将汇编语言翻译为机器码
7. **虚拟机 I**：栈式虚拟机的实现
8. **虚拟机 II**：程序控制流
9. **高级语言**：Jack 语言（类似 Java）
10. **编译器 I**：语法分析
11. **编译器 II**：代码生成
12. **操作系统**：标准库（Math、String、Array、Output、Screen、Keyboard、Memory、Sys）

## 自学建议

**不要跳过任何一章。** 每一章都是下一章的基础。跳过了逻辑门，就无法理解 ALU；跳过了 ALU，就无法理解 CPU。

**动手做项目。** 课程的核心是 12 个项目——从设计一个与非门到实现一个俄罗斯方块游戏。每个项目都需要你亲自动手，不能用现成工具替代。

**配合 CS:APP 使用。** Nand2Tetris 侧重"从下到上"的视角，CS:APP 侧重"从上到下"的视角。两者互补，能给你完整的计算机系统理解。

## 备注

Nand2Tetris 是理解计算机系统的最佳入门课程。它不能替代专业课（体系结构、操作系统、编译原理），但能给你一个完整的全栈视角，让你理解计算机系统中每一层是如何构建的。

很多人认为这是他们上过的最好的 CS 课程。完成它之后，你会对计算机有全新的认识。
