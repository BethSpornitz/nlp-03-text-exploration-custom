
# Analytics Job Description Text Exploration

Web Mining and Applied NLP | Project 03 | Custom Project Report

## Overview

This project explores how vocabulary and language patterns differ across three analytics-related job categories: Data Analyst, Business Analyst, and Data Governance.

The goal is to examine individual word frequencies and relationships between words, including co-occurrence patterns and recurring two-word phrases.

The project builds on the text exploration techniques demonstrated in the instructor's example.

## Phase 4: Technical Modification

### Original Corpus

The instructor's example corpus contains 22 short documents organized into four categories:

- Dogs: 6 documents
- Cats: 6 documents
- Cars: 6 documents
- Trucks: 4 documents

### Modification

The original context window of 2 tokens was increased to 3 tokens.

A context window determines how many words on either side of a target word are considered nearby.

The same corpus and tokenization method were used for both experiments.

### Results

| Target Word | Window 2 | Window 3 | Additional Entries |
|---|---:|---:|---:|
| dog | 7 | 9 | 2 |
| cat | 8 | 9 | 1 |
| car | 8 | 11 | 3 |
| truck | 7 | 9 | 2 |

Increasing the window captured additional context for every target word.

Examples included `kennel` near `dog`, `road` near `car`, and `engine` and `loads` near `truck`.

The larger window also captured additional common words such as `the`. This demonstrates that a larger context window provides more surrounding information but does not necessarily produce more meaningful results.

The underlying corpus remained unchanged, so global word frequencies and bigram counts were unaffected.

### Phase 4 Notebook

The notebook includes executable Python code, the original and modified experiments, a comparison table, a visualization, and observations.

[View the Phase 4 Context Window Comparison Notebook](../notebooks/phase4_context_window_comparison.ipynb)

## Phase 5: Custom Application

The custom application will analyze 12 paraphrased job descriptions across three categories:

| Category | Documents |
|---|---:|
| Data Analyst | 4 |
| Business Analyst | 4 |
| Data Governance | 4 |
| **Total** | **12** |

The planned analysis will examine:

- Global token frequencies.
- Vocabulary differences across job categories.
- Word co-occurrence patterns.
- Bigrams and recurring two-word skill phrases.
- Visualizations of the results.

The results, interpretation, and limitations will be added after the custom analysis is completed.

## Tools and Methods

- Python for text processing and analysis.
- Polars for frequency distributions and category comparisons.
- Context windows for word co-occurrence analysis.
- Bigrams for examining consecutive word pairs.
- Matplotlib for data visualization.
- Ruff, ty, and pytest for code verification.
- Zensical and GitHub Pages for published documentation.

## Documentation Index

- **Home** — This project report.
- [Project Instructions](project-instructions.md)
- [Glossary](glossary.md)

## Project Links

- [GitHub Repository](https://github.com/BethSpornitz/nlp-03-text-exploration-custom)
- [Python Analysis Script](https://github.com/BethSpornitz/nlp-03-text-exploration-custom/blob/main/src/nlp/nlp_corpus_explore.py)
- [Phase 4 Notebook](https://github.com/BethSpornitz/nlp-03-text-exploration-custom/blob/main/notebooks/phase4_context_window_comparison.ipynb)
- [Published Project Website](https://bethspornitz.github.io/nlp-03-text-exploration-custom/)

## Project Resources and Attribution

This project is adapted from the instructional example developed by Denise M. Case for Web Mining and Applied NLP.

- [Original Example Repository](https://github.com/denisecase/nlp-03-text-exploration)
- [Professional Python Guide](https://denisecase.github.io/pro-analytics-02/)
- [Professional Python Project Explainer](https://pup-pack.github.io/professional-python-project-explainer/)
