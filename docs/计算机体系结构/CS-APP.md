# CS:APP: Computer Systems: A Programmer's Perspective

## 教材简介

- 来源：CMU（Randal Bryant、David O'Hallaron）
- 先修要求：C 语言基础
- 课程难度：🌟🌟🌟🌟
- 预计学时：80 小时 +

CS:APP（Computer Systems: A Programmer's Perspective）是 CMU 的经典教材，也是全球最受欢迎的计算机系统教材之一。它的独特视角是：**从程序员的角度理解计算机系统**。

不同于传统的体系结构教材从硬件设计者出发，CS:APP 关注的是：作为一个写 C 程序的程序员，你需要理解计算机的哪些底层知识才能写出正确、高效的代码？

这本书覆盖了从数据表示、汇编语言、处理器架构、缓存优化、链接、虚拟内存、系统 I/O、网络编程到并发的完整知识链。

## 教材资源

- 官方网站：[csapp.cs.cmu.edu](http://csapp.cs.cmu.edu/)
- 配套课程：[CMU 15-213](http://www.cs.cmu.edu/~213/)（课程网站有完整视频和实验）
- 实验代码：[CS:APP Labs](http://csapp.cs.cmu.edu/3e/labs.html)（所有实验代码可下载）
- 中文翻译：《深入理解计算机系统》（第 3 版）

## 核心内容

### 第一部分：程序结构和执行
- 数据表示、汇编语言、处理器架构、优化程序性能

### 第二部分：在系统上运行程序
- 链接、异常控制流、虚拟内存

### 第三部分：程序间的交互和通信
- 系统级 I/O、网络编程、并发编程

## 实验列表

| 实验 | 内容 | 难度 |
|------|------|------|
| Lab 1: Data Lab | 位操作和整数/浮点数表示 | 🌟🌟 |
| Lab 2: Bomb Lab | 汇编语言逆向工程 | 🌟🌟🌟 |
| Lab 3: Attack Lab | 缓冲区溢出攻击 | 🌟🌟🌟 |
| Lab 4: Architecture Lab | Y86-64 处理器设计 | 🌟🌟🌟🌟 |
| Lab 5: Cache Lab | 缓存优化 | 🌟🌟🌟 |
| Lab 6: Shell Lab | 实现一个 Unix Shell | 🌟🌟🌟🌟 |
| Lab 7: Malloc Lab | 实现 malloc/free | 🌟🌟🌟🌟🌟 |
| Lab 8: Proxy Lab | 实现一个 Web 代理 | 🌟🌟🌟🌟 |

## 自学建议

**做所有的实验。** CS:APP 的实验是这本书的灵魂。Bomb Lab 和 Attack Lab 尤其经典，能让你真正理解汇编语言和内存安全。

**配合 CMU 15-213 课程视频。** 课程视频质量极高，Bryant 教授讲得非常透彻。

**不要跳过汇编部分。** 第 3 章（机器级表示）是最难但也是最重要的章节。理解 x86-64 汇编是理解计算机底层的关键。

## 备注

CS:APP 是连接"编程"和"系统"的桥梁。学完这本书，你会理解从 C 代码到机器执行的完整过程。

这本书也是很多大厂面试的参考书。Bomb Lab 和 Attack Lab 是面试官最喜欢问的项目经验之一。
