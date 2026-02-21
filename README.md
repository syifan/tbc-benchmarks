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

### Hard Difficulty

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

### Medium Difficulty

| # | Name | Domain | Language | Key Challenge |
|---|------|--------|----------|---------------|
| 11 | Markdown Static Site Generator | Web | Go | Templates, live reload, RSS feed, file watching |
| 12 | Personal Finance Tracker | Web/Data | Python/Flask | Budgets, charts, CSV import, authentication |
| 13 | Git Implementation | VCS | Python | Object model, staging, branching, merging |
| 14 | Image Processing Pipeline | Graphics | Rust | Filters, resize algorithms, batch processing |
| 15 | Chat Application | Real-time | TypeScript/Node | WebSocket, rooms, file sharing, presence |
| 16 | Task Scheduler / Cron System | Systems | Go | Cron parsing, retries, persistence, web UI |
| 17 | Code Snippet Manager | Developer Tools | Rust | Syntax highlighting, TUI, search, Git sync |
| 18 | HTTP Load Tester | Performance | Go | Concurrency, metrics, percentiles, reports |
| 19 | Markdown Note-Taking App | Productivity | TypeScript | Backlinks, graph view, search, local storage |
| 20 | Log Aggregator & Alerting | Observability | Python | Ingestion, parsing, alerting, dashboard |

### Research Papers

| # | Name | Domain | Language | Key Challenge |
|---|------|--------|----------|---------------|
| 21 | LLM Evaluation Benchmarks Survey | ML/NLP | LaTeX | Taxonomy, meta-analysis, coverage analysis |
| 22 | Open-Source Project Sustainability Study | Software Engineering | Python/LaTeX | GitHub data mining, predictive modeling, contributor analysis |
| 23 | Machine Learning Reproducibility Study | ML | Python/LaTeX | Result reproduction, barrier analysis, systematic evaluation |
| 24 | Code Review Effectiveness Analysis | Software Engineering | Python/LaTeX | PR mining, statistical correlation, bug linkage |
| 25 | CRDT Algorithms Comparative Study | Distributed Systems | Rust/Python/LaTeX | Implementation, benchmarking, convergence analysis |
| 26 | Programming Language Adoption Study | Empirical CS | Python/LaTeX | Multi-source data, trend analysis, correlation studies |
| 27 | Technical Debt Empirical Analysis | Software Maintenance | Python/LaTeX | Metric extraction, temporal evolution, correlation analysis |
| 28 | LLM-Generated Code Quality Study | ML/SE | Python/LaTeX | Multi-model evaluation, error categorization, quality metrics |
| 29 | Package Dependency Network Analysis | Security/Networks | Python/LaTeX | Graph analysis, vulnerability propagation, topology metrics |
| 30 | Consensus Algorithms Comparative Study | Distributed Systems | Go/Rust/LaTeX | Implementation, simulation, performance benchmarking |

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
