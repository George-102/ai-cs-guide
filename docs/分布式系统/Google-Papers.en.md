# Google's Big Three: GFS, MapReduce, Bigtable

## Descriptions

- Source: Google (Sanjay Ghemawat, Jeff Dean, et al.)
- Prerequisites: OS fundamentals, networking fundamentals
- Difficulty: 🌟🌟🌟🌟
- Class Hour: 20+

Google's three classic papers — GFS, MapReduce, Bigtable — laid the foundation for modern distributed systems. Hadoop, HBase, Spark, and other open-source projects were directly influenced by these papers.

Reading these papers, you'll understand core distributed systems design principles and see how industry solves real distributed problems.

## Paper Resources

### GFS: The Google File System
- Paper: [GFS Paper](https://research.google/pubs/pub62/) (SOSP 2003)
- Core idea: Distributed file system with data sharding and replication for high availability

### MapReduce: Simplified Data Processing on Large Clusters
- Paper: [MapReduce Paper](https://research.google/pubs/pub62/) (OSDI 2004)
- Core idea: Programming model for large-scale data processing with automatic parallelization and fault tolerance

### Bigtable: A Distributed Storage System for Structured Data
- Paper: [Bigtable Paper](https://research.google/pubs/pub27897/) (OSDI 2006)
- Core idea: Distributed structured data storage built on GFS and SSTable

## Self-Study Tips

**Read in order.** GFS → MapReduce → Bigtable; the latter builds on the former.

**Focus on design trade-offs.** Each paper makes many engineering trade-offs. Understanding these trade-offs matters more than memorizing design details.

**Pair with MIT 6.824.** Papers cover design principles; 6.824 gives you hands-on implementation.

## Notes

These three papers are the "bible" of distributed systems. Even if you have time for no other distributed systems papers, these three are essential.

Later open-source projects (Hadoop, HBase, Cassandra, Spark) were directly influenced by these papers.
