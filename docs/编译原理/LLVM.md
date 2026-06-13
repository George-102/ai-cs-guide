# LLVM: 现代编译器基础设施

## 项目简介

- 来源：Chris Lattner（Swift 语言创始人，前 Apple/Tesla/Modular）
- 先修要求：C++ 基础、编译原理基础
- 编程语言：C++
- 课程难度：🌟🌟🌟🌟
- 预计学时：60 小时 +

LLVM 是现代编译器基础设施的事实标准。Clang（C/C++ 编译器）、Swift 编译器、Rust 编译器、Julia 编译器——都建立在 LLVM 之上。

学习 LLVM 的价值在于：**你不再只是编译原理的理论学习者，而是能真正参与现代编译器的开发**。LLVM 的模块化设计让你可以为现有语言添加新的优化 pass，甚至为自定义硬件生成代码。

## 项目资源

- 官方网站：[llvm.org](https://llvm.org/)
- 官方教程：[LLVM Tutorial](https://llvm.org/docs/tutorial/)
- 官方文档：[LLVM Documentation](https://llvm.org/docs/)
- GitHub：[llvm/llvm-project](https://github.com/llvm/llvm-project)

## 核心概念

### LLVM IR
- LLVM 的中间表示（IR）是 LLVM 的核心
- 三地址码形式，SSA（静态单赋值）表示
- 可以在 IR 层面做各种优化

### Pass 架构
- LLVM 的优化通过 Pass 实现
- 每个 Pass 做一件事（如常量折叠、循环展开）
- Pass 之间可以组合和复用

### 后端
- LLVM 支持几乎所有主流 CPU 架构（x86、ARM、RISC-V、GPU）
- TableGen 用于描述目标架构

## 自学建议

**先学编译原理基础。** 不理解 IR、优化、代码生成，学 LLVM 会很吃力。

**跟着官方教程走。** LLVM 官方提供了一个完整的教程，教你实现一个简单的语言（Kaleidoscope）并编译到 LLVM IR。

**阅读 Clang 源码。** Clang 是 LLVM 的 C/C++ 前端，代码质量很高，是学习编译器实现的最佳参考。

## 备注

LLVM 是工业级编译器开发的基础设施。如果你想从事编译器、编程语言、AI 编译器（如 TVM、MLIR）相关的工作，LLVM 是必须掌握的。

Chris Lattner 在 2022 年创立了 Modular AI，正在用 LLVM/MLIR 技术栈构建 AI 编译器基础设施。
