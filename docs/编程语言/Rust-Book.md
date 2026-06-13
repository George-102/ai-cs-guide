# The Rust Programming Language — Rust 编程语言

## 简介

The Rust Programming Language（俗称 "The Rust Book"）是 Rust 语言的官方教程，由 Rust 社区编写，免费在线阅读。Rust 是一种系统级编程语言，由 Mozilla 开发，主打**内存安全和并发安全**，通过独特的所有权（Ownership）系统在编译时保证安全，无需垃圾回收器。

Rust 在 Stack Overflow 的"最受欢迎编程语言"调查中连续多年排名第一。它被广泛用于操作系统、Web 服务器、命令行工具、区块链、游戏引擎等领域。Linux 内核也开始接受 Rust 代码。

这本书是学习 Rust 的最佳起点，从零开始讲解 Rust 的所有核心概念：所有权、借用、生命周期、类型系统、泛型、trait、并发等。

## 先修要求

- **编程经验**：至少熟悉一门编程语言（C/C++ 背景有帮助但不是必须）
- **基本的命令行操作**：会用终端编译和运行程序
- **不需要**：系统编程或内存管理的前置知识

## 难度

🌟🌟🌟🌟（较高）

Rust 的所有权系统是其核心创新，也是最大的学习难点。很多程序员在这里卡住数周。但一旦理解了所有权，Rust 的其他概念就会变得自然。

## 学时

约 80-120 小时

- 阅读本书：约 40-60 小时
- 做练习和项目：约 40-60 小时

## 课程资源

- 英文原版：[doc.rust-lang.org/book](https://doc.rust-lang.org/book/)
- 中文翻译：[kaisery.github.io/trpl-zh-cn](https://kaisery.github.io/trpl-zh-cn/)
- Rust Playground（在线编译运行）：[play.rust-lang.org](https://play.rust-lang.org/)
- Rustlings（交互式练习）：[github.com/rust-lang/rustlings](https://github.com/rust-lang/rustlings/)

## 自学建议

1. **按顺序阅读，不要跳章。** 每一章都建立在前一章的基础上，特别是所有权相关的章节（第 4-10 章）。

2. **遇到编译器的错误信息时，不要沮丧。** Rust 编译器的错误信息是全国所有编译器中最友好的，它们通常会告诉你具体错在哪里以及怎么改。仔细阅读这些信息，它们是学习 Rust 的最好老师。

3. **用 Rustlings 做练习。** Rustlings 是一组交互式小练习，每个练习对应一个核心概念，非常适合巩固书中的知识。

4. **不要试图一次性理解生命周期。** 生命周期（Lifetime）是 Rust 中最难的概念。先理解基本用法，随着实践积累逐步深入。

5. **读完书后做一些小项目**：命令行工具、简单的 HTTP 解析器、文件处理工具。项目是最好的巩固方式。

6. **加入 Rust 社区。** Rust 社区以友好著称，在 Reddit、Discord 和 Rust 论坛上提问通常会得到耐心详细的回答。
