# TBC Benchmarks

Benchmark suite for evaluating [TheBotCompany](https://github.com/syifan/thebotcompany) — a multi-agent autonomous software development orchestrator.

Each benchmark is a self-contained project specification. The goal is to give the spec to TBC and let the agents build it from scratch with no human intervention.

## Difficulty Level

Each benchmark requires:
- Multiple components working together
- Non-trivial algorithmic or architectural decisions
- Testing and validation
- Iterative refinement (accuracy targets, performance goals, or correctness criteria)

Comparable to building a cycle-accurate CPU simulator, writing a survey paper, or creating an ML prediction tool.

## Benchmarks

| # | Name | Domain | Language | Key Challenge |
|---|------|--------|----------|---------------|
| 1 | Distributed Key-Value Store | Systems | Go | Raft consensus, persistence, fault tolerance |
| 2 | Neural Network Framework | ML | Python | Autograd, GPU kernels, optimizer convergence |
| 3 | SQL Query Engine | Databases | Rust | Parser, planner, executor, B-tree indexes |
| 4 | Real-Time Ray Tracer | Graphics | C++ | BVH acceleration, materials, interactive FPS |
| 5 | Static Analysis Tool | PL/Compilers | Go | Control flow, data flow, taint analysis |
| 6 | Container Orchestrator | DevOps | Go | Scheduling, health checks, networking, CLI |
| 7 | Collaborative Text Editor | Distributed | TypeScript | CRDT, WebSocket sync, operational transform |
| 8 | Compiler Backend | Compilers | Rust | SSA IR, register allocation, x86-64 codegen |
| 9 | Packet Sniffer & Protocol Analyzer | Networking | Python | Raw sockets, protocol parsing, live dashboard |
| 10 | Automated Theorem Prover | Logic/Math | OCaml/Haskell | Unification, resolution, proof search |

## Usage

Each subdirectory contains a `spec.md` with:
- **What to build** — clear project description
- **Success criteria** — measurable goals
- Both are ready to paste into TBC's "Add Project" flow.

## Evaluation

A benchmark is considered **passed** if:
1. The project reaches a state where Athena declares `PROJECT_COMPLETE` with `success: true`
2. The success criteria in `spec.md` are verifiably met
3. No human intervention was needed during execution

Metrics to track:
- **Cycles to completion** — fewer is better
- **Total cost** — USD spent on API calls
- **Wall-clock time** — real time from start to completion
- **Success rate** — does it complete at all?
