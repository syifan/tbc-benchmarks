# Open-Source Project Sustainability Study

## What do you want to build?

Write an empirical research paper analyzing the sustainability of open-source projects using GitHub data. The study should investigate contributor patterns, project abandonment predictors, and factors correlated with long-term project health.

The research should:
- Collect data from 500-1000 GitHub repositories across multiple languages and domains using the GitHub API
- Define sustainability metrics: commit frequency, contributor retention, issue resolution time, bus factor
- Analyze contributor lifecycle patterns: onboarding, active contribution period, dropout/burnout indicators
- Build predictive models for project abandonment using features like contributor diversity, documentation quality, governance structure, and community engagement
- Identify early warning signs of project decline
- Use only publicly available data from GitHub API, no proprietary sources

The final deliverable is a conference-quality research paper (8-12 pages) in LaTeX suitable for submission to venues like ICSE, FSE, or MSR (Mining Software Repositories).

## How do you consider the project is success?

1. LaTeX paper compiles without errors and produces a properly formatted PDF (8-12 pages, conference format)
2. Paper includes all required sections: abstract, introduction, methodology (data collection, metrics definition), results, discussion, threats to validity, conclusion, references
3. Dataset includes 500+ GitHub projects with documented selection criteria and data collection methodology
4. Analysis includes at least 5 sustainability metrics with statistical validation (mean, median, distribution plots)
5. Predictive model achieves >70% accuracy in identifying abandoned projects, with performance reported using precision, recall, F1-score, and ROC curves
6. Paper includes 8-10 figures/tables: data distribution plots, time-series graphs, correlation matrices, model performance comparisons
7. Discussion identifies 4-6 actionable insights for OSS maintainers or platforms to improve project sustainability
8. References section contains 30+ citations to software engineering research, OSS studies, and empirical methods papers
