# Software Engineering

## What is Software Engineering

Software Engineering is the discipline of **systematically building high-quality software**. It's not just "writing code" — it covers the entire software lifecycle: requirements analysis, design, implementation, testing, deployment, and maintenance.

When you're working on a course assignment alone, you don't need software engineering. But as projects grow larger, teams get bigger, and maintenance periods get longer, without engineering methods things fall apart — messy code, frequent bugs, and changes that break everything. Software engineering solves these problems.

## Why Learn Software Engineering

**Write maintainable code.** You can write code, but will you understand it six months later? Can someone else take it over? Software engineering teaches you to write readable, maintainable, and testable code.

**Learn team collaboration.** Real-world software is built by teams. Version control, code reviews, task division — these collaboration skills are fundamental for software engineers.

**Understand what "good software" means.** It's not enough for code to run. Good software should be correct, reliable, efficient, maintainable, and scalable. Software engineering builds this quality awareness.

**Interviews and career development.** Software engineering skills (code quality, system design, engineering habits) are core evaluation criteria in technical interviews and daily work.

## Core Knowledge Areas

### Code Quality

- **Code readability**: naming conventions, comments, code style
- **Code Review**: how to give feedback on others' code, how to receive feedback
- **Static checking and testing**: type checking, lint tools, unit testing, integration testing
- **Technical debt**: balancing short-term compromises with long-term costs

### Specifications and Design

- **Specifications**: preconditions, postconditions, behavioral equivalence
- **Abstract Data Types (ADTs)**: encapsulation, representation independence, abstraction functions and representation invariants
- **Interface design**: what good interfaces look like, how to design reusable components
- **Immutability**: why immutable objects are safer, when to use mutability

### Version Control and Collaboration

- **Git workflows**: branching strategies, merge vs rebase, PR/MR workflows
- **Team version control**: Git practices for multi-person collaboration
- **Continuous Integration (CI)**: automated builds and testing

### Software Design Principles

- **Single Responsibility Principle**: a class should do one thing
- **Open/Closed Principle**: open for extension, closed for modification
- **Dependency Inversion**: depend on abstractions, not concrete implementations
- **DRY Principle**: Don't Repeat Yourself

### Concurrency and Safety

- **Thread safety**: the risks of shared mutable state
- **Locks and synchronization**: synchronized, Lock, deadlocks
- **Message passing**: using message queues instead of shared memory

## How to Learn

**Start with a good course.** Software engineering can't be learned just from books — it requires practice in real projects. MIT 6.031 Software Construction is highly recommended — it covers core software engineering concepts thoroughly with exercises for each topic.

**Practice in real projects.** Find a project with a few thousand lines of code (an open-source project or a large course assignment) and practice code review, writing tests, and refactoring. Theory without practice stays on paper.

**Build engineering habits.** Every time you write code, ask yourself: can others understand this? Is it tested? Is there a cleaner way? These habits are more important than any specific technology.

**Read excellent code.** GitHub has countless high-quality open-source projects. Reading their code structure, naming conventions, and test organization is more valuable than reading ten textbooks.

## Recommended Resources

### Courses

- [MIT 6.031: Software Construction](./MIT-6.031.md) — Highly recommended. 30 readings covering core topics, each with exercises
- [Berkeley CS169: Software Engineering](./Berkeley-CS169.md) — Focuses on agile development and SaaS architecture
- [CMU 17-313: Foundations of Software Engineering](./CMU-17-313.md) — CMU's software engineering foundations course

### Books

- *Clean Code* (Robert Martin) — How to write readable, maintainable code
- *Refactoring* (Martin Fowler) — Systematic approaches to code refactoring
- *Design Patterns* (GoF) — Classic design pattern reference

### Tools

- [GitHub](https://github.com/) — Version control and collaboration platform
- [SonarQube](https://www.sonarqube.org/) — Code quality and security analysis tool
- [JUnit](https://junit.org/junit5/) / [pytest](https://pytest.org/) — Java / Python testing frameworks
