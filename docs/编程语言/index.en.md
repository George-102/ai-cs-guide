# Programming Languages

## What are Programming Languages

Programming languages are the bridge between humans and computers. Code you write in a programming language is ultimately translated into machine instructions that the CPU can execute. Different programming languages have different design philosophies, syntax, and use cases.

Learning a programming language isn't just about syntax. Each language embodies a philosophy about "how programs should be written." C lets you directly manipulate memory, emphasizing efficiency and control; Python manages memory for you, emphasizing simplicity and readability; Haskell uses pure functions and immutable data, emphasizing correctness and composability. Understanding these philosophies is far more important than memorizing syntax.

## Why Learn Programming Languages

**Different tasks need different languages.** There is no universal programming language. Operating systems are written in C/Rust, data science uses Python/R, frontend uses JavaScript/TypeScript, Android uses Kotlin, and iOS uses Swift. Mastering multiple languages lets you choose the best tool for each task.

**Understand programming paradigms.** Programming languages can be broadly categorized into paradigms: imperative (C, Java), functional (Haskell, Erlang), logic (Prolog), and object-oriented (Java, C++). Learning languages from different paradigms broadens your thinking and lets you view programming problems from different angles.

**Learning new languages gets faster.** The more languages you know, the easier it is to learn new ones. Most languages share fundamental concepts (variables, functions, loops, conditionals), with differences mainly in syntax and features. Once you understand multiple paradigms, learning a new language may take only days.

**Deepen computer science understanding.** Programming language design involves type systems, memory management, concurrency models, and compiler theory — core CS topics. Learning languages is also learning these underlying fundamentals.

## Core Knowledge Areas

### Programming Paradigms

- **Imperative/Procedural**: C, Go — change program state through a series of statements
- **Object-Oriented**: Java, C++, Python — organize code using objects and classes
- **Functional**: Haskell, Erlang, Scala — program with pure functions and immutable data
- **Multi-paradigm**: Python, JavaScript, Rust — support multiple programming styles

### Type Systems

- **Static vs dynamic typing**: compile-time checking vs runtime checking
- **Strong vs weak typing**: strictness of type conversions
- **Type inference**: compiler automatically deduces types (e.g., Rust, Haskell)
- **Generics/parametric types**: writing type-safe generic code

### Memory Management

- **Manual management**: C/C++ — you allocate and free memory yourself
- **Garbage Collection (GC)**: Java, Python, Go — runtime automatically reclaims unused memory
- **Ownership system**: Rust — guarantees memory safety at compile time without GC

### Concurrency Models

- **Threads and locks**: Java, C++ — traditional concurrency model
- **Actor model**: Erlang — concurrency through message passing
- **Coroutines**: Go (goroutines), Python (asyncio) — lightweight concurrency
- **Async/await**: JavaScript, Python, Rust — event-loop-based asynchronous programming

## How to Learn

**Master one language first, then learn others.** Don't try to learn many languages at once. Get one language to the point where you can solve real problems with it, then learn a second. Python is recommended as a first language — clean syntax, rich ecosystem, great for beginners.

**Learn through projects.** Don't just read syntax books. Set a small goal — build a web scraper, make a CLI tool, create a website — and learn the language's features and best practices through practice.

**Read excellent source code.** One of the best ways to learn a language is to read well-written code in that language. Python's standard library, Go's standard library, and Rust's crates are all great learning materials.

**Focus on language design philosophy.** Don't just learn "how to use it" — learn "why it was designed this way." Why does Rust have an ownership system? Why doesn't Go have inheritance? Why do functional languages emphasize immutability? Understanding design motivations is how you truly master a language.

**Compare languages.** Implement the same task (like a simple HTTP server) in different languages and compare the coding style, performance, and development experience. This comparison deepens your understanding of language features.

## Recommended Resources

### Language Introductions

- [Python Official Documentation](./Python-Official.md) — The go-to Python introduction
- [The Rust Programming Language](./Rust-Book.md) — The official Rust tutorial, free to read online
- [A Tour of Go](./Go-Tour.md) — Go's official interactive tutorial

### Programming Paradigms

- [UW Programming Languages](./UW-Programming-Languages.md) — UW course using SML, Racket, and Ruby to teach three paradigms
- *Concepts of Programming Languages* (Sebesta) — Systematic introduction to various programming paradigms
- [Learn You a Haskell for Great Good](http://learnyouahaskell.com/) — Classic introduction to functional programming

### Multi-Language Learning

- [Exercism](https://exercism.org/) — Practice platform supporting 60+ languages with mentor code review
- [Rosetta Code](https://rosettacode.org/) — Side-by-side comparisons of the same task implemented in different languages
