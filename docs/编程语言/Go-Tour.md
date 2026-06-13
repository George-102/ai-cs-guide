# A Tour of Go — Go 官方互动教程

## 简介

A Tour of Go 是 Go 语言的官方互动教程，在你的浏览器中直接编写和运行 Go 代码，无需安装任何软件。由 Go 团队编写，是入门 Go 语言最快的方式。

Go（又称 Golang）是 Google 开发的一种静态类型、编译型语言，以**简洁、高效、并发友好**著称。Go 的语法极简（只有 25 个关键字），编译速度极快，内置 goroutine 和 channel 支持并发编程，非常适合构建网络服务、微服务、命令行工具和云原生应用。

Docker 和 Kubernetes 都是用 Go 写的。如果你想做后端开发或云原生方向，Go 是必学语言之一。

## 先修要求

- **基本的编程概念**：了解变量、函数、循环等基本概念
- **不需要**：并发编程的前置知识（教程会从零讲起）

## 难度

🌟🌟（入门到中等）

Go 的语法非常简洁，入门门槛低。并发部分是难点，但对大多数应用来说，只用 goroutine 和 channel 就够了。

## 学时

约 10-15 小时（教程本身）+ 项目实践

- Tour of Go 教程：约 8-10 小时
- 基础练习：约 5-8 小时
- 项目实践：持续进行

## 课程资源

- 英文版：[go.dev/tour](https://go.dev/tour/)
- 中文版：[go.dev/tour/list](https://go.dev/tour/list)（切换语言）
- Go 官方文档：[go.dev/doc](https://go.dev/doc/)
- Go by Example：[gobyexample.com](https://gobyexample.com/) — 代码示例驱动的 Go 学习资源
- 练习：[Exercism Go Track](https://exercism.org/tracks/go)

## 自学建议

1. **Tour of Go 是入门的最快路径。** 直接在浏览器里写代码，即时看到结果，学习效率极高。

2. **重点掌握 goroutine 和 channel。** 这是 Go 的核心竞争力。学会用 goroutine 并发执行任务，用 channel 在 goroutine 之间安全通信。

3. **Go 的接口设计很特别。** Go 使用隐式接口（structural typing），不需要显式声明实现了哪个接口。这种设计比 Java/C# 的接口更灵活，也更难理解。多看几个例子才能掌握。

4. **不要陷入错误处理的Go 风格的讨论中。** Go 使用 `if err != nil` 处理错误，被很多人吐槽。它就是 Go 的风格，接受它。

5. **推荐书籍**：
   - *The Go Programming Language*（Donovan & Kernighan）— 权威的 Go 教材
   - *Go in Action* — 更实用的入门书

6. **学完后做一个小项目**：HTTP API 服务器、并发爬虫、命令行工具。Go 的标准库非常强大，很多功能不需要第三方库。
