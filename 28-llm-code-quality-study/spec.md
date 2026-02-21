# LLM-Generated Code Quality Study

## What do you want to build?

Write a research paper comparing code quality across multiple large language models using standardized coding benchmarks. The study should evaluate LLM-generated code across dimensions like correctness, efficiency, maintainability, and security, and perform detailed error pattern analysis.

The research should:
- Evaluate 5-8 LLMs: GPT-4, Claude 3.5, Gemini, Llama 3, CodeLlama, StarCoder, DeepSeek-Coder, or similar publicly accessible models
- Use existing coding benchmarks: HumanEval, MBPP, CodeContests, plus custom problems covering diverse algorithmic patterns
- Test 100-200 programming problems across multiple languages (Python, JavaScript, Java)
- Analyze multiple quality dimensions: functional correctness (test pass rate), time/space complexity, code readability (cyclomatic complexity, naming quality), security vulnerabilities (using bandit, semgrep), and style adherence
- Categorize error patterns: logic errors, edge case handling, API misuse, off-by-one errors, type errors
- Compare model performance across problem difficulty, domain, and language
- Use only publicly accessible LLM APIs (free tier or standard pricing)

The final deliverable is a conference-quality research paper (8-12 pages) in LaTeX suitable for submission to ML/SE venues like ICSE, FSE, NeurIPS, or ICLR.

## How do you consider the project is success?

1. LaTeX paper compiles without errors and produces a properly formatted PDF (8-12 pages, conference format)
2. Paper includes all required sections: abstract, introduction, related work, methodology (models, benchmarks, evaluation metrics), results, error analysis, discussion, conclusion, references
3. Evaluation covers 5+ LLMs on 100+ problems with documented prompting strategy and temperature settings
4. Results report pass@1, pass@10 correctness rates, average cyclomatic complexity, vulnerability counts, and runtime efficiency comparisons
5. Paper includes 10-12 figures/tables: model comparison matrices, error type frequency distributions, difficulty-stratified performance, language-specific results, example code comparisons
6. Error analysis categorizes at least 100 failures into 6-8 error pattern categories with frequency counts and representative examples
7. Discussion identifies model strengths/weaknesses by problem type and provides insights into training data or architecture effects
8. References section contains 30+ citations to LLM papers, code generation research, software quality metrics, and benchmark papers
