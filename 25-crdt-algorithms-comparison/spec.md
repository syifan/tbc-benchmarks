# CRDT Algorithms Comparative Study

## What do you want to build?

Write a research paper presenting a comparative study of Conflict-free Replicated Data Type (CRDT) algorithms. The study should implement 5 major CRDT variants from scratch, benchmark their performance under various workloads, and analyze trade-offs in convergence time, memory overhead, and operational latency.

The research should:
- Implement 5 CRDT algorithms: OR-Set, LWW-Element-Set, RGA (Replicated Growable Array), Logoot, and YATA/Yjs-style sequence CRDT
- Create a simulation framework for distributed editing scenarios with configurable network delays, partition rates, and concurrent operation rates
- Benchmark performance metrics: convergence time (time until all replicas agree), memory usage (tombstones, version vectors), operation latency, and conflict resolution overhead
- Vary workloads: document size, edit frequency, number of replicas (2-10), network conditions
- Analyze theoretical properties vs. empirical behavior
- Use standard programming languages (Python, Rust, Go) and no specialized hardware

The final deliverable is a conference-quality research paper (8-12 pages) in LaTeX suitable for submission to distributed systems or PL venues like PODC, DISC, or OOPSLA.

## How do you consider the project is success?

1. LaTeX paper compiles without errors and produces a properly formatted PDF (8-12 pages, conference format)
2. Paper includes all required sections: abstract, introduction, background (CRDT theory), methodology (implementation details, benchmark setup), results, discussion, related work, conclusion, references
3. All 5 CRDT algorithms are implemented and pass correctness tests: eventual consistency, commutativity, associativity
4. Benchmark suite includes 20+ experiment configurations varying replica count, workload type, and network conditions
5. Paper includes 10-12 figures/tables: convergence time comparisons, memory usage plots, latency distributions, scaling behavior graphs, trade-off scatter plots
6. Results section reports quantitative comparisons: median convergence times, memory overhead ratios, throughput measurements with confidence intervals
7. Discussion analyzes trade-offs and provides recommendations for choosing CRDTs based on use-case requirements
8. References section contains 25+ citations to CRDT papers, distributed systems research, and consistency models
