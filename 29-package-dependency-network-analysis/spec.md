# Package Dependency Network Analysis

## What do you want to build?

Write a research paper analyzing the network topology of package dependency ecosystems (npm, PyPI, crates.io) with focus on vulnerability propagation, critical nodes, and ecosystem resilience. The study should apply graph theory and network analysis to understand dependency structures and their security implications.

The research should:
- Collect dependency graph data from npm (JavaScript), PyPI (Python), and crates.io (Rust) using public APIs and package registries
- Build directed dependency graphs for each ecosystem (100K-1M packages)
- Compute network topology metrics: degree distribution, clustering coefficient, centrality measures (PageRank, betweenness), connected components, average path length
- Identify critical packages: high-impact nodes whose compromise would affect many downstream packages
- Analyze vulnerability propagation: given a vulnerable package, calculate blast radius (transitive dependents)
- Compare ecosystem characteristics: centralization, fragility, evolution over time (2015-2024)
- Use publicly available package registry data and vulnerability databases (CVE, npm audit, GitHub Advisory Database)

The final deliverable is a conference-quality research paper (8-12 pages) in LaTeX suitable for submission to security or software engineering venues like IEEE S&P, USENIX Security, CCS, or ICSE.

## How do you consider the project is success?

1. LaTeX paper compiles without errors and produces a properly formatted PDF (8-12 pages, conference format)
2. Paper includes all required sections: abstract, introduction, background (dependency ecosystems, graph theory), methodology (data collection, metrics), results, discussion, related work, conclusion, references
3. Analysis covers all three ecosystems with graph construction methodology and dataset statistics (node count, edge count, data snapshot date)
4. Network metrics computed and reported: degree distributions (in-degree, out-degree), centrality rankings (top 50 packages), clustering coefficients, diameter/average path length
5. Paper includes 10-15 figures/tables: degree distribution plots, centrality heatmaps, dependency tree visualizations, vulnerability propagation simulations, ecosystem comparison matrices, temporal evolution graphs
6. Vulnerability analysis identifies top 20 critical packages per ecosystem and calculates blast radius for real CVEs or simulated compromises
7. Discussion compares ecosystem health, identifies structural risks, and proposes mitigation strategies for supply chain security
8. References section contains 30+ citations to software supply chain research, network science papers, security studies, and ecosystem analysis work
