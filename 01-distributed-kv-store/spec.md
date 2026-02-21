# Distributed Key-Value Store

## What do you want to build?

Build a distributed key-value store in Go that uses the Raft consensus protocol for replication across a cluster of nodes. The system should support GET, PUT, and DELETE operations via an HTTP API, persist data to disk using a write-ahead log (WAL), and tolerate node failures (up to N/2-1 nodes in an N-node cluster).

The implementation must include:
- Raft consensus (leader election, log replication, safety) — implemented from scratch, not using an existing Raft library
- Write-ahead log with crash recovery
- HTTP API for client operations
- Cluster membership management (add/remove nodes)
- Snapshot and log compaction
- A test suite that validates correctness under simulated network partitions and node failures

## How do you consider the project is success?

1. A 3-node cluster correctly handles concurrent reads and writes with linearizable consistency
2. The cluster continues operating after killing any single node and recovers when the node restarts
3. Network partition simulation tests pass — split-brain scenarios are handled correctly
4. All Raft safety properties hold: election safety, leader append-only, log matching, leader completeness, state machine safety
5. Write-ahead log survives process crashes — no data loss after recovery
6. End-to-end test suite with at least 20 test cases covering normal operation, failures, and edge cases
7. Benchmarks show >1000 ops/sec on a single machine with 3 nodes
