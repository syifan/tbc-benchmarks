# Machine Learning Reproducibility Study

## What do you want to build?

Write a research paper documenting an attempt to reproduce results from 10 recent machine learning papers using only their published code and data. The study should systematically analyze reproducibility challenges, success rates, and factors that facilitate or hinder reproduction.

The research should:
- Select 10 ML papers from recent conferences (NeurIPS, ICML, ICLR 2022-2024) that claim to provide code/data
- Attempt to reproduce key results (accuracy, loss curves, performance metrics) following published methodology
- Document reproduction attempts: success/failure, time required, issues encountered, workarounds needed
- Categorize reproducibility barriers: missing dependencies, unclear hyperparameters, computational requirements, dataset issues, code bugs
- Analyze correlation between reproducibility and factors like: code quality, documentation completeness, venue, research area
- Use only publicly available papers, code repositories (GitHub), and datasets — no private compute clusters required

The final deliverable is a conference-quality research paper (8-12 pages) in LaTeX suitable for submission to ML conferences or reproducibility workshops.

## How do you consider the project is success?

1. LaTeX paper compiles without errors and produces a properly formatted PDF (8-12 pages, conference format)
2. Paper includes all required sections: abstract, introduction, related work (prior reproducibility studies), methodology, results, discussion, conclusion, references
3. Study covers exactly 10 papers with documented selection criteria and systematic reproduction protocol
4. Results section includes a reproducibility matrix: for each paper, report success/partial/failure, time spent, and primary barriers encountered
5. Paper includes 6-8 figures/tables: reproducibility success rates by venue/year/domain, barrier frequency analysis, time-to-reproduce distributions, before/after result comparisons
6. Quantitative analysis reports: overall reproducibility rate, correlation between documentation quality and success, computational cost distribution
7. Discussion provides 5-7 actionable recommendations for researchers and venues to improve reproducibility
8. References section contains 25+ citations to original papers, reproducibility studies, and ML methodology papers
