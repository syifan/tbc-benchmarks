# Code Review Effectiveness Analysis

## What do you want to build?

Write an empirical research paper analyzing the effectiveness of code review practices in large open-source projects. The study should mine pull request data to correlate review practices with post-merge bug rates, identify effective review patterns, and measure the impact of review thoroughness on code quality.

The research should:
- Collect PR and issue data from 10-20 large open-source projects (e.g., Linux, Kubernetes, React, VS Code) using GitHub/GitLab APIs
- Extract review metrics: number of reviewers, review duration, comment count, reviewer expertise, iteration rounds
- Link merged PRs to subsequent bug reports using issue trackers and git blame analysis
- Perform statistical analysis correlating review practices with bug introduction rates
- Identify review patterns associated with higher/lower defect rates
- Analyze the impact of reviewer expertise, review timing, and discussion quality on outcomes
- Use only publicly available repository data

The final deliverable is a conference-quality research paper (8-12 pages) in LaTeX suitable for submission to software engineering venues like ICSE, FSE, or ESEM.

## How do you consider the project is success?

1. LaTeX paper compiles without errors and produces a properly formatted PDF (8-12 pages, conference format)
2. Paper includes all required sections: abstract, introduction, background, methodology (data collection, metrics, linking PRs to bugs), results, discussion, threats to validity, conclusion, references
3. Dataset covers 10+ projects with 5,000+ merged pull requests and documented PR-to-bug linking methodology
4. Statistical analysis includes correlation coefficients, regression models, and significance tests (p-values) for at least 5 review metrics vs. bug rates
5. Paper includes 8-10 figures/tables: review practice distributions, bug rate comparisons, correlation heatmaps, regression results, time-series analysis
6. Results identify 3-5 review practices significantly correlated with lower bug rates with effect sizes and confidence intervals
7. Discussion provides actionable insights for practitioners: recommended review practices, trade-offs between thoroughness and velocity
8. References section contains 30+ citations to software engineering research, code review studies, and empirical methods papers
