# MIT 6.824: Distributed Systems

## Descriptions

- Offered by: MIT
- Prerequisites: OS fundamentals, networking fundamentals, Go basics
- Programming Language: Go
- Difficulty: 🌟🌟🌟🌟
- Website: [pdos.csail.mit.edu/6.824](https://pdos.csail.mit.edu/6.824/)

MIT 6.824 is MIT's distributed systems course, widely regarded as the best in the world. The core of the course is implementing the Raft consensus algorithm and a Raft-based distributed KV store.

## Course Resources

- Website: [pdos.csail.mit.edu/6.824](https://pdos.csail.mit.edu/6.824/)
- Lectures: [YouTube](https://www.youtube.com/playlist?list=PLrw6a1wE39_tb2fErI4-WkMbsvGQk9_UB)
- Lab code: [MIT 6.824 Labs](https://pdos.csail.mit.edu/6.824/labs/)

## Lab List

| Lab | Content | Difficulty |
|-----|---------|------------|
| Lab 1: MapReduce | Implement MapReduce framework | 🌟🌟 |
| Lab 2: Raft | Implement Raft consensus algorithm | 🌟🌟🌟🌟 |
| Lab 3: KV Server | Implement Raft-based KV store | 🌟🌟🌟🌟 |
| Lab 4: Sharded KV | Implement sharded KV store | 🌟🌟🌟🌟🌟 |

## Self-Study Tips

**Solid Go skills required.** The course uses Go; familiarity with goroutines and channels is essential.

**Read the Raft paper first.** The Raft paper is the course's core. Read it before starting labs.

**Allocate 2-3 weeks per lab.** The Raft lab is especially time-consuming; don't rush.

## Notes

6.824 has the best lab design in distributed systems courses. After completing all labs, your understanding will surpass most practitioners.

Raft is one of the most widely used consensus algorithms in industry (etcd, TiKV, CockroachDB all use Raft). Mastering it is a fundamental skill for distributed systems engineers.
