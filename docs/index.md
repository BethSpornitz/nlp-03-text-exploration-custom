
# Analytics Job Description Text Exploration

Web Mining and Applied NLP | Project 03 | Custom Project Report

## Overview

This project explores how vocabulary and language patterns differ across three analytics-related job categories: Data Analyst, Business Analyst, and Data Governance.

The goal is to examine not only individual word frequencies but also the relationships between words. In particular, the project will explore whether co-occurrence and bigram analysis can help identify technical skills and multiword phrases that individual word counts may overlook.

The project builds on the text exploration techniques demonstrated in the course example.

## Project Progress

### Phase 4: Technical Modification

The instructor's example corpus contains 22 documents organized into four categories: dogs, cats, cars, and trucks.

The context window was increased from two words to three words to examine how this change affects co-occurrence results.

The larger window identified additional surrounding words, including "kennel" near "dog" and "engine" and "loads" near "truck." It also included additional common words, demonstrating that a larger context window does not necessarily produce more informative results.

### Phase 5: Custom Application

The custom application will analyze 12 paraphrased job descriptions organized into three categories:

| Category | Documents |
|---|---:|
| Data Analyst | 4 |
| Business Analyst | 4 |
| Data Governance | 4 |
| **Total** | **12** |

The planned analysis includes:

- Global token frequency analysis.
- Comparisons of word frequencies across job categories.
- Word co-occurrence analysis.
- Bigram analysis to identify recurring two-word phrases.
- Visualizations of vocabulary patterns.

The results and interpretations will be added after the custom analysis is completed.

## Tools and Methods

- Python for text processing and analysis.
- Polars for frequency distributions and category comparisons.
- Context windows for word co-occurrence analysis.
- Bigrams for examining consecutive word pairs.
- Matplotlib for visualizations.
- Ruff, ty, and pytest for code verification.
- Zensical and GitHub Pages for published documentation.

## Results and Interpretation

*This section will be completed after Phase 5.*

The final report will describe the most common words and phrases, differences between job categories, co-occurrence patterns, and the limitations of using a small collection of paraphrased job descriptions.

## Documentation Index

- **Home** — this project report.
- [Project Instructions](project-instructions.md)
- [Glossary](glossary.md)

## Project Links

- [GitHub Repository](https://github.com/BethSpornitz/nlp-03-text-exploration-custom)
- [Python Analysis Script](https://github.com/BethSpornitz/nlp-03-text-exploration-custom/blob/main/src/nlp/nlp_corpus_explore.py)
- [Published Project Website](https://bethspornitz.github.io/nlp-03-text-exploration-custom/)

## Project Resources and Attribution

This project is adapted from the instructional example developed by Denise M. Case for Web Mining and Applied NLP.

- [Original Example Repository](https://github.com/denisecase/nlp-03-text-exploration)
- [Professional Python Guide](https://denisecase.github.io/pro-analytics-02/)
- [Professional Python Project Explainer](https://pup-pack.github.io/professional-python-project-explainer/)
