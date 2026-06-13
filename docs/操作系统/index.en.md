# Operating Systems Overview

## What is an Operating System

An Operating System (OS) is system software that manages computer hardware and software resources. It acts as an intermediary between applications and hardware, responsible for allowing multiple programs to share CPU, memory, disk, and network resources.

## Why Learn Operating Systems

**Understand what your programs actually do.** When you call `printf`, it involves system calls, user/kernel mode transitions, buffer management, and device drivers. Without understanding the OS, your programs are black boxes.

**Write more efficient programs.** Understanding process scheduling, memory paging, and caching helps you write system-friendly code.

**Essential for interviews and exams.** OS is a core subject for graduate school entrance exams and technical interviews.

**Foundation for advanced topics.** Computer networking, databases, and distributed systems all build on OS concepts.

## Core Knowledge Areas

### Processes and Threads
- A **process** is an instance of a program execution with its own address space
- A **thread** is an execution unit within a process; threads share the address space
- IPC: pipes, message queues, shared memory, semaphores
- Thread synchronization: mutexes, condition variables, read-write locks

### Memory Management
- **Virtual memory**: each process has its own virtual address space
- **Paging and segmentation**: two fundamental approaches
- **Page replacement algorithms**: LRU, FIFO, Clock
- **Memory allocation**: heap vs. stack, how malloc works

### File Systems
- File organization: directory tree structure
- Disk scheduling: SCAN, C-SCAN, SSTF
- File system implementation: inodes, journaling

### I/O and Device Management
- I/O models: blocking, non-blocking, multiplexing (select/poll/epoll)
- Device drivers
- Interrupt handling

### Concurrency and Synchronization
- Critical section problem
- Classic problems: producer-consumer, readers-writers, dining philosophers
- Deadlock conditions and prevention

## How to Learn

**Build the big picture first.** Understand core OS responsibilities (CPU, memory, disk, device management), then tackle each area.

**Learn by doing experiments.** The xv6 labs from MIT are highly recommended.

**Draw diagrams.** Process state transitions, memory mapping, disk scheduling — visualize them.

**Don't skip Linux commands.** Tools like `ps`, `top`, `strace`, and `lsof` let you observe OS behavior.

## Resources in This Module

| Resource | Type | Description |
|----------|------|-------------|
| [MIT 6.S081](./MIT-6.S081.md) | Course | MIT OS course based on xv6, with complete labs |
| [OSTEP](./OSTEP.md) | Textbook | Operating Systems: Three Easy Pieces, free online |
| [Berkeley CS162](./Berkeley-CS162.md) | Course | Berkeley OS course with videos and assignments |
| [xv6](./xv6.md) | Practice | MIT teaching OS, ~10,000 lines of code |
