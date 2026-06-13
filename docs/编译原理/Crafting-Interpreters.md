# Crafting Interpreters: 从零实现两门编程语言

## 教程简介

- 来源：Robert Nystrom
- 先修要求：至少掌握一门编程语言
- 编程语言：Java（第一部分）、C（第二部分）
- 课程难度：🌟🌟🌟
- 预计学时：60 小时 +

Crafting Interpreters 是 Robert Nystrom 编写的一本免费在线教程，教你从零实现两门编程语言（Lox）。第一部分用 Java 写一个树遍历解释器，第二部分用 C 写一个字节码编译器和虚拟机。

这本书的最大特点是**实践性极强**。每一章都有完整的代码实现，你可以跟着教程一步步写出一个能运行的解释器和编译器。

## 教程资源

- 官方网站：[craftinginterpreters.com](https://craftinginterpreters.com/)
- 在线阅读：完全免费
- GitHub：[craftinginterpreters](https://github.com/munificent/craftinginterpreters)（完整代码）

## 内容结构

### 第一部分：树遍历解释器（Java）
- 词法分析（Scanner）
- 语法分析（Parser）
- 表达式求值
- 语句和控制流
- 函数和闭包
- 类和继承

### 第二部分：字节码编译器（C）
- 字节码设计
- 编译器实现
- 虚拟机
- 垃圾回收
- 优化技术

## 自学建议

**跟着教程写代码，不要只读。** 这本书的价值在于动手实现。每写完一章，你就能运行一个功能更完整的解释器/编译器。

**先读第一部分，再读第二部分。** 第一部分用 Java 实现，更容易理解。第二部分用 C 实现，涉及内存管理和性能优化。

**参考但不照抄。** 先自己实现，遇到问题再参考作者的代码。

## 备注

Crafting Interpreters 是编译器入门的最佳实践教程。它不能替代正式的编译原理课程（如 Stanford CS143），但能给你最直观的感受——原来写一个编程语言并不难。

很多人认为这是他们读过的最好的编程书之一。
