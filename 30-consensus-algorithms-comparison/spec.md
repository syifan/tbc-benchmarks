# Consensus Algorithms Comparative Study

## What do you want to build?

Write a research paper presenting a comparative study of distributed consensus algorithms. The study should implement Raft, Multi-Paxos, and PBFT (Practical Byzantine Fault Tolerance) from scratch, benchmark their performance under various network conditions and fault scenarios, and analyze trade-offs in latency, throughput, fault tolerance, and complexity.

The research should:
- Implement three consensus algorithms: Raft, Multi-Paxos, and PBFT (simplified PBFT suitable for research prototype)
- Build a network simulation framework that models message delays, packet loss, network partitions, and node crashes/Byzantine failures
- Benchmark performance metrics: commit latency (time from proposal to commit), throughput (transactions/sec), recovery time after failures, message overhead
- Test various configurations: cluster sizes (3, 5, 7, 9 nodes), workload intensities, network latency profiles (LAN, WAN), fault injection scenarios
- Compare theoretical properties vs. empirical behavior: leader election overhead, log replication efficiency, Byzantine resilience
- Use standard programming language (Go, Rust, or Python) with simulated network, no distributed infrastructure needed

The final deliverable is a conference-quality research paper (8-12 pages) in LaTeX suitable for submission to distributed systems venues like SOSP, OSDI, NSDI, or EuroSys.

## How do you consider the project is success?

1. LaTeX paper compiles without errors and produces a properly formatted PDF (8-12 pages, conference format)
2. Paper includes all required sections: abstract, introduction, background (consensus problem, algorithm descriptions), methodology (implementation details, simulation environment, metrics), results, discussion, related work, conclusion, references
3. All three algorithms correctly implement consensus: pass safety tests (agreement, validity, termination) with automated test suites
4. Benchmark suite includes 30+ experiment configurations varying cluster size, network conditions, fault types, and workload patterns
5. Paper includes 12-15 figures/tables: latency-throughput curves, scaling behavior graphs, fault tolerance comparisons, message overhead analysis, recovery time measurements, trade-off scatter plots
6. Results report quantitative comparisons: median commit latency, maximum throughput, 95th/99th percentile latencies, message complexity (messages per commit), with confidence intervals
7. Discussion analyzes algorithm trade-offs: when to use each algorithm, performance vs. fault tolerance vs. simplicity, practical deployment considerations
8. References section contains 35+ citations to distributed systems papers, consensus algorithm research, Byzantine fault tolerance work, and empirical evaluation studies
