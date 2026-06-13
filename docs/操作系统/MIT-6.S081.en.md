# MIT 6.S081: Operating System Engineering

## Descriptions

- Offered by: MIT
- Prerequisites: Computer architecture basics, C programming
- Programming Language: C
- Difficulty: 🌟🌟🌟🌟
- Class Hour: 80+

MIT 6.S081 (formerly 6.828) is MIT's operating system course, built around the xv6 teaching OS. It's widely regarded as one of the best OS courses in the world — not because it covers the most material, but because it has you **actually implement an operating system**.

The course centers on 7 labs, each requiring you to add a core feature to the xv6 kernel: process management, memory management, file systems, networking, and more. After completing these labs, your understanding of operating systems will surpass 90% of CS graduates.

## Course Resources

- Website: [pdos.csail.mit.edu/6.828](https://pdos.csail.mit.edu/6.828/2023/)
- Lectures: [YouTube 2020](https://www.youtube.com/playlist?list=PLf3u8NhoEikhTC5radGrmmqdkOK-xMDoO)
- Textbook: [xv6 Book](https://pdos.csail.mit.edu/6.828/2023/xv6/book-riscv-rev3.pdf) (free PDF)
- Lab code: [xv6-riscv](https://github.com/mit-pdos/xv6-riscv)

## Lab List

| Lab | Content | Difficulty |
|-----|---------|------------|
| Lab 1: Unix utilities | Implement xarg, sleep, etc. | 🌟 |
| Lab 2: System calls | Add system calls, understand kernel mode | 🌟🌟 |
| Lab 3: Page tables | Implement page tables, understand virtual memory | 🌟🌟🌟 |
| Lab 4: Traps | Implement interrupt and exception handling | 🌟🌟🌟 |
| Lab 5: Copy-on-write fork | Implement copy-on-write | 🌟🌟🌟 |
| Lab 6: Multithreading | Implement threading and locks | 🌟🌟🌟🌟 |
| Lab 7: Network driver | Implement network driver | 🌟🌟🌟🌟 |
| Lab 8: File system | Implement file system | 🌟🌟🌟🌟🌟 |
| Lab 9: mmap | Implement memory mapping | 🌟🌟🌟🌟 |

## Self-Study Tips

**Read the first 3 chapters of the xv6 Book first.** Don't jump straight into labs. Understand xv6's basic architecture (process, memory, file system implementation) before writing code.

**Allocate 1-2 weeks per lab.** Labs increase in difficulty; later ones (file system, mmap) may take 2+ weeks. Don't rush.

**Master GDB debugging.** Debugging OS code is different from normal programs. Learning to debug kernel code with GDB is one of the most important skills from this course.

**Reference, don't copy.** Many reference implementations are available online, but copying them means you learn nothing. Think first, then look at references when stuck.

## Notes

This course has a massive workload, but the rewards are equally huge. If you can complete all labs independently, any OS interview question will be within your reach.

The 2023+ version switched from x86 to RISC-V architecture with cleaner lab code. The new version is recommended.
