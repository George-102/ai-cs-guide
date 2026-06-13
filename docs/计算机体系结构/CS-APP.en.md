# CS:APP: Computer Systems: A Programmer's Perspective

## Descriptions

- Source: CMU (Randal Bryant, David O'Hallaron)
- Prerequisites: C programming basics
- Difficulty: 🌟🌟🌟🌟
- Class Hour: 80+

CS:APP (Computer Systems: A Programmer's Perspective) is CMU's classic textbook and one of the most popular computer systems books in the world. Its unique perspective: **understanding computer systems from a programmer's point of view**.

Unlike traditional architecture textbooks written for hardware designers, CS:APP focuses on: as a C programmer, what low-level knowledge do you need to write correct and efficient code?

The book covers the complete chain from data representation, assembly language, processor architecture, cache optimization, linking, virtual memory, system I/O, networking, to concurrency.

## Resources

- Official site: [csapp.cs.cmu.edu](http://csapp.cs.cmu.edu/)
- Course: [CMU 15-213](http://www.cs.cmu.edu/~213/) (complete videos and labs on course website)
- Lab code: [CS:APP Labs](http://csapp.cs.cmu.edu/3e/labs.html)
- Chinese translation: 《深入理解计算机系统》(3rd Edition)

## Core Content

### Part 1: Program Structure and Execution
- Data representation, assembly, processor architecture, performance optimization

### Part 2: Running Programs on a System
- Linking, exceptional control flow, virtual memory

### Part 3: Interaction and Communication Between Programs
- System-level I/O, network programming, concurrency

## Lab List

| Lab | Content | Difficulty |
|-----|---------|------------|
| Lab 1: Data Lab | Bit manipulation, integer/float representation | 🌟🌟 |
| Lab 2: Bomb Lab | Assembly reverse engineering | 🌟🌟🌟 |
| Lab 3: Attack Lab | Buffer overflow attacks | 🌟🌟🌟 |
| Lab 4: Architecture Lab | Y86-64 processor design | 🌟🌟🌟🌟 |
| Lab 5: Cache Lab | Cache optimization | 🌟🌟🌟 |
| Lab 6: Shell Lab | Implement a Unix shell | 🌟🌟🌟🌟 |
| Lab 7: Malloc Lab | Implement malloc/free | 🌟🌟🌟🌟🌟 |
| Lab 8: Proxy Lab | Implement a web proxy | 🌟🌟🌟🌟 |

## Self-Study Tips

**Do all the labs.** CS:APP's labs are the soul of the book. Bomb Lab and Attack Lab are particularly classic, giving you real understanding of assembly and memory safety.

**Watch the CMU 15-213 lectures.** The lecture quality is exceptional; Professor Bryant explains concepts thoroughly.

**Don't skip the assembly chapter.** Chapter 3 (Machine-Level Representation) is the hardest but most important. Understanding x86-64 assembly is key to understanding the machine.

## Notes

CS:APP bridges "programming" and "systems." After reading it, you'll understand the complete journey from C code to machine execution.

This book is also a reference for many tech company interviews. Bomb Lab and Attack Lab are among the most frequently asked-about project experiences in interviews.
