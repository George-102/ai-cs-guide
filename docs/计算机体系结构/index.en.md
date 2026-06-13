# Computer Architecture Overview

## What is Computer Architecture

Computer Architecture studies the organization of computer systems — how CPUs execute instructions, how memory stores and retrieves data, and how various components work together. The core question: how does a computer run the programs you write?

## Why Learn Computer Architecture

**Understand why programs are fast or slow.** Arrays are much faster than linked lists for the same algorithm — the reason is cache locality. With architecture knowledge, you can make informed optimization decisions.

**Understand "abstraction leaks."** Integer overflow, floating-point precision, concurrency races — the root causes are at the hardware level.

**Foundation for embedded and systems programming.** Essential for embedded development, device drivers, compilers, and performance optimization.

**Key topic for exams and interviews.** Instruction pipelines, cache principles, and bus arbitration are core exam and interview topics.

## Core Knowledge Areas

### Data Representation
- Binary and hexadecimal
- Integer representation: sign-magnitude, one's complement, two's complement
- Floating-point: IEEE 754
- Character encoding: ASCII, UTF-8

### Instruction Set Architecture
- ISA: CISC vs RISC
- Instruction types: arithmetic, logical, control flow, memory access
- Assembly language: x86 or RISC-V

### CPU Design
- Datapath: ALU, registers, buses
- Control unit: instructions to control signals
- Pipelining: fetch, decode, execute, memory access, write-back
- Pipeline hazards: data, control, structural

### Memory Hierarchy
- **Cache**: L1/L2/L3, mapping policies, replacement strategies
- **Main memory (DRAM)**: organization, bandwidth, latency
- **Virtual memory**: address translation, TLB, page replacement
- **Memory locality**: temporal and spatial

### Buses and I/O
- Bus types: data, address, control
- I/O methods: programmed I/O, interrupts, DMA

### Parallel Processing
- ILP: superscalar, out-of-order execution
- Data-Level Parallelism: SIMD, GPU
- Thread-Level Parallelism: multi-core, shared memory

## How to Learn

**Start with C and assembly.** Write simple C programs and use `gcc -S` to see generated assembly.

**Use simulation tools.** Use Ripes or Venus to simulate RISC-V processor execution.

**Draw datapath diagrams.** Draw data flow between components during instruction execution.

## Resources in This Module

| Resource | Type | Description |
|----------|------|-------------|
| [Berkeley CS61C](./CS61C.md) | Course | Berkeley architecture course with RISC-V labs |
| [Nand2Tetris](./Nand2Tetris.md) | Course | From NAND gates to a complete computer |
| [CS:APP](./CS-APP.md) | Textbook | Computer Systems: A Programmer's Perspective |
| [Computer Architecture: A Quantitative Approach](./Hennessy-Patterson.md) | Textbook | Classic architecture textbook |
