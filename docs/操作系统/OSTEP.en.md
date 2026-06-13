# OSTEP: Operating Systems: Three Easy Pieces

## Descriptions

- Source: University of Wisconsin-Madison (Remzi Arpaci-Dusseau)
- Prerequisites: C programming basics, computer architecture basics
- Difficulty: 🌟🌟🌟
- Class Hour: 60+

OSTEP (Operating Systems: Three Easy Pieces) is one of the most popular OS textbooks in the world, completely free to read online. The "three easy pieces" in the title refer to the three core themes of operating systems: **Virtualization, Concurrency, and Persistence**.

The book's greatest strength is its **exceptional clarity**. Author Remzi Arpaci-Dusseau is a professor at UW-Madison and a top researcher in operating systems. He explains complex concepts in plain language with vivid analogies.

## Resources

- Official site: [pages.cs.wisc.edu/~remzi/OSTEP/](https://pages.cs.wisc.edu/~remzi/OSTEP/)
- Online reading: Completely free, PDF download available
- Projects: [OSTEP Projects](https://pages.cs.wisc.edu/~remzi/OSTEP/projects/) (programming assignments)
- Chinese translation: [OSTEP Chinese](https://github.com/remzi-arpacidusseau/ostep-translations/tree/master/chinese) (community translation)

## Content Structure

### Part 1: Virtualization
- CPU virtualization: processes, process API, restricted direct execution, scheduling
- Memory virtualization: address spaces, memory API, address translation, segmentation, free space management

### Part 2: Concurrency
- Threads and locks
- Condition variables
- Semaphores
- Concurrency bugs
- Event-based concurrency

### Part 3: Persistence
- I/O devices
- Disk drives
- RAID
- File system implementation
- FSCK and journaling
- Introduction to distributed systems

## Self-Study Tips

**Read in order, don't skip chapters.** The chapters have strong dependencies. Earlier concepts are the foundation for later ones.

**Do the programming projects.** Each chapter has accompanying programming assignments (in C) that transform theory into practice.

**Use alongside MIT 6.S081.** OSTEP covers theory; 6.S081 provides hands-on labs. Together, they cover both theory and practice.

**Don't rely solely on the Chinese translation.** The English original is written very fluently. Read English first, consult Chinese for unfamiliar terms.

## Notes

This is one of the best textbooks for OS beginners. If you're short on time, reading this book + doing MIT 6.S081 labs is sufficient to build a solid OS foundation.
