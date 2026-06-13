# Compiler Theory Overview

## What is Compiler Theory

Compiler theory studies **how to translate high-level programming languages into machine-executable instructions**. A compiler is the program that performs this translation. It typically divides into phases: lexical analysis, parsing, semantic analysis, intermediate code generation, optimization, and code generation.

## Why Learn Compiler Theory

**Understand the nature of programming languages.** You don't just "use" a language — you understand why it's designed the way it is.

**Foundation for AI code generation.** The AST (Abstract Syntax Tree) is the most fundamental data structure for AI-assisted programming.

**Write better code.** Understanding compiler optimizations helps you write compiler-friendly code.

**Train hardcore engineering thinking.** Compilers are among the most complex systems in software engineering.

## Core Knowledge Modules

### Lexical Analysis
- Regular expressions, finite automata (NFA/DFA)
- Lexer: converts source code character stream into token sequences

### Parsing
- Context-Free Grammars (CFG)
- Top-down parsing: recursive descent, LL(1)
- Bottom-up parsing: LR(0), SLR, LALR, LR(1)
- Abstract Syntax Tree (AST)

### Semantic Analysis
- Type systems: static vs. dynamic typing, type checking, type inference
- Symbol tables: managing scope and attributes of identifiers

### Intermediate Code and Optimization
- Intermediate Representation (IR): three-address code, SSA
- Optimization: constant folding, dead code elimination, loop optimization

### Code Generation
- Instruction selection, register allocation, instruction scheduling

### Runtime Environment
- Stack frame management, garbage collection, closure implementation

## How to Learn

**Start with hands-on work, then dive into theory.** Build a simple compiler first to build intuition.

**Start with Crafting Interpreters.** Build two programming languages from scratch, free online.

**Do the Stanford CS143 labs.** Implement a complete compiler (lexing, parsing, semantic analysis, code generation).

## Resources in This Module

| Resource | Type | Description |
|----------|------|-------------|
| [Stanford CS143](./Stanford-CS143.md) | Course | Stanford compiler course with complete labs |
| [Crafting Interpreters](./Crafting-Interpreters.md) | Tutorial | Build two languages from scratch, free online |
| [Engineering a Compiler](./Engineering-a-Compiler.md) | Textbook | Classic compiler design textbook |
| [LLVM](./LLVM.md) | Tool | Modern compiler infrastructure |
