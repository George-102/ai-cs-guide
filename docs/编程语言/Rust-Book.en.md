# The Rust Programming Language

## Introduction

The Rust Programming Language (commonly known as "The Rust Book") is the official tutorial for the Rust programming language, written by the Rust community and available free online. Rust is a systems programming language developed by Mozilla, focused on **memory safety and concurrency safety**. It guarantees safety at compile time through its unique ownership system, without needing a garbage collector.

Rust has ranked #1 in Stack Overflow's "Most Loved Programming Language" survey for multiple consecutive years. It is widely used in operating systems, web servers, command-line tools, blockchain, game engines, and more. The Linux kernel has also started accepting Rust code.

This book is the best starting point for learning Rust, covering all core concepts from scratch: ownership, borrowing, lifetimes, type system, generics, traits, concurrency, and more.

## Prerequisites

- **Programming experience**: Familiar with at least one programming language (C/C++ background is helpful but not required)
- **Basic command-line skills**: Can compile and run programs from a terminal
- **No prior systems programming or memory management knowledge required**

## Difficulty

🌟🌟🌟🌟 (Challenging)

Rust's ownership system is its core innovation and also the biggest learning hurdle. Many programmers get stuck here for weeks. But once you understand ownership, the rest of Rust becomes much more natural.

## Estimated Study Hours

Approximately 80-120 hours

- Reading the book: ~40-60 hours
- Exercises and projects: ~40-60 hours

## Resources

- English original: [doc.rust-lang.org/book](https://doc.rust-lang.org/book/)
- Chinese translation: [kaisery.github.io/trpl-zh-cn](https://kaisery.github.io/trpl-zh-cn/)
- Rust Playground (online compiler): [play.rust-lang.org](https://play.rust-lang.org/)
- Rustlings (interactive exercises): [github.com/rust-lang/rustlings](https://github.com/rust-lang/rustlings/)

## Self-Study Tips

1. **Read in order, don't skip chapters.** Each chapter builds on the previous one, especially the ownership-related chapters (4-10).

2. **Don't get frustrated by compiler errors.** Rust's compiler error messages are among the friendliest of any compiler — they typically tell you exactly what's wrong and how to fix it. Read them carefully; they are the best teachers for learning Rust.

3. **Use Rustlings for practice.** Rustlings is a set of interactive small exercises, each targeting a core concept — perfect for reinforcing what you learned in the book.

4. **Don't try to understand lifetimes all at once.** Lifetimes are Rust's hardest concept. Learn the basic usage first, then deepen your understanding through practice.

5. **After reading the book, build some small projects**: a CLI tool, a simple HTTP parser, a file processing utility. Projects are the best way to solidify knowledge.

6. **Join the Rust community.** The Rust community is known for being exceptionally friendly. Asking questions on Reddit, Discord, or the Rust forum usually yields patient, detailed answers.
