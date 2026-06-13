# Engineering a Compiler

## Descriptions

- Source: Keith Cooper, Linda Torczon (Rice University)
- Prerequisites: Data structures, computer architecture basics
- Difficulty: 🌟🌟🌟🌟
- Class Hour: 80+

*Engineering a Compiler* by Keith Cooper and Linda Torczon of Rice University is a compiler textbook on par with the "Dragon Book."

Unlike the Dragon Book's theory-heavy approach, this book focuses on **engineering practice**: how to implement various optimizations in real compilers, and how to balance compilation time versus generated code quality.

## Resources

- Publisher: [Elsevier](https://www.elsevier.com/books/engineering-a-compiler/cooper/978-0-12-088478-0)
- Course: [Rice University COMP 412](https://www.cs.rice.edu/~keith/412/)

## Core Content

### Part 1: Frontend
- Lexical analysis, parsing, semantic analysis
- Symbol table management
- Intermediate Representation (IR)

### Part 2: Optimization
- Local: constant folding, algebraic simplification, dead code elimination
- Global: data flow analysis, loop optimization
- Interprocedural: inlining, escape analysis

### Part 3: Backend
- Instruction selection, register allocation, instruction scheduling
- Code generation

## Self-Study Tips

**Read the Dragon Book or complete CS143 first.** This book is for those with some compiler background.

**Focus on the optimization section.** Optimization is the most complex and valuable part of a compiler, and the heart of this book.

## Notes

This is one of the best textbooks for advanced compiler study. If you want to deeply understand modern compilers like GCC and LLVM, this book is essential reading.
