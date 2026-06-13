# xv6: A Simple, Unix-like Teaching Operating System

## Descriptions

- Source: MIT
- Prerequisites: C programming, computer architecture basics (RISC-V)
- Programming Language: C
- Difficulty: 🌟🌟🌟
- Class Hour: 40+

xv6 is a teaching operating system developed by MIT for its OS course (6.S081). It's a simplified Unix with only ~10,000 lines of code, yet contains all core concepts of a modern OS: process management, memory management, file systems, interrupt handling, and system calls.

xv6's value: **you can read the entire OS source code.** For a real OS kernel (Linux has 30 million lines), this is impossible. But xv6 lets you see real implementations of all core concepts in just tens of thousands of lines.

## Resources

- GitHub: [mit-pdos/xv6-riscv](https://github.com/mit-pdos/xv6-riscv) (RISC-V version, recommended)
- Documentation: [xv6 Book](https://pdos.csail.mit.edu/6.828/2023/xv6/book-riscv-rev3.pdf) (free PDF, covers each xv6 subsystem)
- MIT 6.S081: [xv6 is the lab platform for 6.S081](https://pdos.csail.mit.edu/6.828/2023/)

## xv6 Architecture

### Boot Process
- Starts from RISC-V reset vector
- Sets up page tables, interrupt vectors
- Initializes the first process

### Core Subsystems
- **Process management**: Process creation, scheduling, exit
- **Memory management**: Page tables, virtual memory mapping
- **File system**: Inodes, directories, file I/O
- **Interrupts and system calls**: Trap handling, user/kernel mode switching
- **Locks**: Spin locks, sleep locks

## Self-Study Tips

**Read the xv6 Book first.** It introduces xv6's implementation by subsystem, the best guide for reading the code.

**Start with boot code.** Understanding how xv6 goes from hardware reset to running the first process is key to understanding the whole system.

**Pair with MIT 6.S081 labs.** Each lab requires you to modify a specific xv6 subsystem — the best way to learn xv6.

**Debug with GDB.** Run xv6 in QEMU and use GDB to step through kernel code, observing each function's actual behavior.

## Notes

xv6 is the "minimum viable system" for learning OS implementation. After reading xv6's code, you'll have an inside-out understanding of operating systems.

Since 2023, xv6 has migrated from x86 to RISC-V with cleaner code. The RISC-V version is recommended.
