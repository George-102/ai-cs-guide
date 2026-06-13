# Distributed Systems Overview

## What is a Distributed System

Distributed systems study **how multiple computers work together to accomplish tasks that a single computer cannot**. Virtually every large-scale internet service — search engines, social networks, e-commerce, cloud storage — is powered by distributed systems.

## Why Learn Distributed Systems

**Required for large-scale systems.** Modern AI training requires thousands of GPUs working in coordination; AI inference needs deployment across global data centers.

**Understand modern software architecture.** Microservices, Kubernetes, message queues, distributed databases — all built on distributed systems theory.

**Advanced interview topic.** System Design Interviews are fundamentally about distributed system design.

## Core Knowledge Modules

### Fundamentals
- Definition: resource sharing, concurrency, no global clock, independent failures
- Architecture: client-server, P2P, microservices

### Time and Clocks
- Clock synchronization, logical clocks (Lamport, vector clocks)

### Replication and Consistency
- Replication strategies, consistency models, CAP theorem, BASE theory

### Consensus Algorithms
- Paxos, Raft, ZAB, Two-Phase Commit

### Distributed Data Storage
- Sharding, distributed databases, distributed file systems

### Distributed Computing
- MapReduce, Spark, distributed training

## How to Learn

**Read classic papers first.** Start with Google's "big three" (GFS, MapReduce, Bigtable).

**Do the MIT 6.824 labs.** Implement Raft and a Raft-based KV store.

**Build a distributed cluster with Docker Compose.** Deploy a Redis Cluster or Kafka cluster.

## Resources in This Module

| Resource | Type | Description |
|----------|------|-------------|
| [MIT 6.824](./MIT-6.824.md) | Course | MIT distributed systems, implement Raft |
| [DDIA Distributed Chapters](./DDIA-Distributed.md) | Textbook | Designing Data-Intensive Applications - distributed chapters |
| [Google's Big Three](./Google-Papers.md) | Papers | Original GFS, MapReduce, Bigtable papers |
