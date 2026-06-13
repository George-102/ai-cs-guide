# LLVM: Modern Compiler Infrastructure

## Descriptions

- Source: Chris Lattner (creator of Swift, formerly Apple/Tesla/Modular)
- Prerequisites: C++ basics, compiler theory basics
- Programming Language: C++
- Difficulty: 🌟🌟🌟🌟
- Class Hour: 60+

LLVM is the de facto standard for modern compiler infrastructure. Clang, Swift, Rust, and Julia compilers are all built on LLVM.

Learning LLVM means: **you're no longer just a compiler theory student — you can actually participate in modern compiler development.** LLVM's modular design lets you add new optimization passes for existing languages or generate code for custom hardware.

## Resources

- Official site: [llvm.org](https://llvm.org/)
- Official tutorial: [LLVM Tutorial](https://llvm.org/docs/tutorial/)
- Documentation: [LLVM Documentation](https://llvm.org/docs/)
- GitHub: [llvm/llvm-project](https://github.com/llvm/llvm-project)

## Core Concepts

### LLVM IR
- LLVM's Intermediate Representation (IR) is its core
- Three-address code in SSA (Static Single Assignment) form
- Various optimizations can be performed at the IR level

### Pass Architecture
- LLVM optimizations are implemented as Passes
- Each Pass does one thing (e.g., constant folding, loop unrolling)
- Passes can be composed and reused

### Backend
- LLVM supports virtually all major CPU architectures (x86, ARM, RISC-V, GPU)
- TableGen is used to describe target architectures

## Self-Study Tips

**Learn compiler theory first.** Without understanding IR, optimization, and code generation, LLVM will be overwhelming.

**Follow the official tutorial.** LLVM provides a complete tutorial implementing a simple language (Kaleidoscope) and compiling to LLVM IR.

**Read the Clang source code.** Clang is LLVM's C/C++ frontend with excellent code quality — the best reference for learning compiler implementation.

## Notes

LLVM is the infrastructure for industrial-grade compiler development. If you want to work on compilers, programming languages, or AI compilers (like TVM, MLIR), LLVM is essential.

Chris Lattner founded Modular AI in 2022, building AI compiler infrastructure using the LLVM/MLIR technology stack.
