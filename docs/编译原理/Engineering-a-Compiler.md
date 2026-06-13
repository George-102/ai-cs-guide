# Engineering a Compiler: 编译器设计

## 教材简介

- 来源：Keith Cooper、Linda Torczon（Rice University）
- 先修要求：数据结构、计算机体系结构基础
- 课程难度：🌟🌟🌟🌟
- 预计学时：80 小时 +

《Engineering a Compiler》（编译器设计）是 Rice University 的 Keith Cooper 和 Linda Torczon 编写的编译器教材，与"龙书"（Compilers: Principles, Techniques, and Tools）齐名。

与龙书偏重理论不同，这本书更注重**工程实践**。它关注的是：如何在实际的编译器中实现各种优化？如何权衡编译时间和生成代码的质量？

## 教材资源

- 官方网站：[Elsevier](https://www.elsevier.com/books/engineering-a-compiler/cooper/978-0-12-088478-0)
- 配套课程：[Rice University COMP 412](https://www.cs.rice.edu/~keith/412/)

## 核心内容

### 第一部分：前端
- 词法分析、语法分析、语义分析
- 符号表管理
- 中间表示（IR）

### 第二部分：优化
- 局部优化：常量折叠、代数化简、死代码消除
- 全局优化：数据流分析、循环优化
- 过程间优化：内联、逃逸分析

### 第三部分：后端
- 指令选择、寄存器分配、指令调度
- 代码生成

## 自学建议

**先读龙书或上完 CS143。** 这本书适合有一定编译基础的人深入学习。

**重点关注优化部分。** 优化是编译器最复杂也最有价值的部分，也是这本书的精华。

## 备注

这本书是编译器进阶的最佳教材之一。如果你想深入理解 GCC、LLVM 等现代编译器的实现，这本书是必读的。
