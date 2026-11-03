# nlp-03-text-exploration-custom

[![Python 3.14](https://img.shields.io/badge/python-3.14%2B-blue?logo=python)](pyproject.toml)
[![CI](https://github.com/BethSpornitz/nlp-03-text-exploration-custom/actions/workflows/ci-python-zensical.yml/badge.svg)](https://github.com/BethSpornitz/nlp-03-text-exploration-custom/actions/workflows/ci-python-zensical.yml)
[![Documentation](https://img.shields.io/badge/docs-site-blue?logo=github)](https://bethspornitz.github.io/nlp-03-text-exploration-custom/)

[![uv managed](https://img.shields.io/badge/uv-managed-DE5FE9)](https://docs.astral.sh/uv/)
[![ty type checked](https://img.shields.io/badge/ty-type_checked-2F80ED)](https://docs.astral.sh/ty/)
[![Zensical docs](https://img.shields.io/badge/Zensical-docs-purple)](https://zensical.org/)
[![MIT](https://img.shields.io/badge/license-MIT-yellow.svg)](LICENSE)

> Exploring language, technical skills, and common phrases across analytics job descriptions.

## Project Overview

Author: Beth Spornitz

Date: 2026 November

Third project in the Web Mining and Applied NLP course.

This project explores patterns in job descriptions for three analytics career categories: Data Analyst, Business Analyst, and Data Governance.

The analysis explores token frequencies, category comparisons, word co-occurrence, and bigrams. Particular attention will be given to multi-word combinations such as "Power BI," "data quality," and "business requirements."

The goal is to investigate which technical skills and terminology appear across these career categories and identify patterns that individual word frequencies may not reveal.

The project is configured in [pyproject.toml](pyproject.toml).

## Data

This project uses 12 job descriptions from a previous Module 2 project, divided into three categories:

- Data Analyst: 4 job descriptions
- Business Analyst: 4 job descriptions
- Data Governance: 4 job descriptions

Each job description includes the job title, employer, source link, and a summarized description of the position.

The descriptions are used to compare the language and skills mentioned in different types of analytics jobs. The analysis will also look at phrases like "Power BI," "data quality," and "business requirements" to see what can be learned by examining words together rather than individually.

Because the dataset includes only 12 job descriptions, the results will be used to explore patterns rather than draw conclusions about the entire job market.

## Approach

This project uses Python and Polars to explore how language and job requirements differ across three types of analytics positions.

The analysis includes:

- Preparing the job descriptions for analysis.
- Identifying the most frequently used words.
- Comparing commonly used words across job categories.
- Looking at which words tend to appear near each other.
- Identifying common two-word phrases.
- Creating charts to show patterns and differences between job categories.
- Reviewing the results to better understand the skills and responsibilities associated with each type of position.

The goal is to see what can be learned by looking at words together, rather than just counting how often individual words appear.

### Project Components

- [pyproject.toml](pyproject.toml) - Project settings and dependencies.
- [src/nlp/nlp_corpus_explore.py](src/nlp/nlp_corpus_explore.py) - Python script used for text analysis.
- [tests/](tests/) - Automated tests.
- [.github/workflows/](.github/workflows/) - Automated checks and documentation publishing.
- [docs/](docs/) - Project documentation.
- [zensical.toml](zensical.toml) - Documentation settings.
- [data/job_descriptions.csv](data/job_descriptions.csv) - Custom job description dataset.
- [src/nlp/job_description_explore.py](src/nlp/job_description_explore.py) - Custom job description analysis.
- [notebooks/phase4_context_window_comparison.ipynb](notebooks/phase4_context_window_comparison.ipynb) - Phase 4 context window comparison.
- [notebooks/phase5_job_description_exploration.ipynb](notebooks/phase5_job_description_exploration.ipynb) - Phase 5 job description analysis.

## Run the Project

Follow the [Professional Python Workflow Guide](https://denisecase.github.io/pro-analytics-02/)
to set up your machine and project environment.

From a VS Code terminal in the project root:

```shell
uv run python -m nlp.job_description_explore
```

Close each visualization window after viewing
so the script can continue executing.

## Results

The job descriptions showed some differences in the words used for each career category. Data Analyst descriptions included terms like dashboards and SQL, while Business Analyst descriptions focused more on users and requirements. Data Governance descriptions included terms like quality and metadata. I also found that the original code removed "BI" from "Power BI" because it was only two characters long. After changing the code to keep "BI," the analysis identified the phrase "Power BI" three times.

Successful execution produces:

```shell
========================
Pipeline executed successfully!
========================
```

A `project.log` file is created in the project root.

This confirms that the Python analysis executes
and the logging system works.

## Verification

Run the automated tests:

```shell
uv run python -m pytest
```

## Project Documentation

The [hosted documentation site](https://bethspornitz.github.io/nlp-03-text-exploration-custom/)
is published using Zensical and GitHub Pages.

The documentation site is used to present the project report,
covering such sections as data, methods, results, visualizations,
interpretation, and conclusions.

## CI/CD and GitHub Actions

This project includes continuous integration and continuous deployment (CI/CD)
to check project files and publish the docs.

GitHub Actions include:

- [CI: Python and Documentation Checks](https://github.com/BethSpornitz/nlp-03-text-exploration-custom/actions/workflows/ci-python-zensical.yml)
- [CD: Documentation Deployment](https://github.com/BethSpornitz/nlp-03-text-exploration-custom/actions/workflows/deploy-zensical.yml)

## Developer Reference

Follow the
[Professional Python Workflow Guide](https://denisecase.github.io/pro-analytics-02/)
for **detailed instructions and troubleshooting**.

### Initialize and Update the Python Environment

With the project open in VS Code, open a VS Code terminal.
Paste each command and hit Enter or Return after to run it.

```shell
uvx pup-clean --delete
uv self update
uv python pin 3.14
uv python install
uv lock --upgrade
uv sync
uv audit
```

### Set Up and Run Git Hooks

Set up and run the git hooks to perform
basic checks automatically before
any changes get pushed to GitHub.

In the VS Code terminal,
paste each command and hit Enter or Return after to run it.

```shell
uvx prek install --force
uvx prek update --freeze --cooldown-days 7

git add -A
uvx prek run --all-files
# repeat if changes were made
uvx prek run --all-files
```

### Run Common Chores

Run linters, formatters, type checks, tests, and
build the documentation.

```shell
uv run ruff check . --fix
uv run ruff format .

uv run ty check
uv run python -m pytest
uv run python -m zensical build
```

### Git add-commit-push to GitHub

After making useful changes, save your work to GitHub.

```shell
git add -A
git commit -m "describe your changes in quotes"
git push -u origin main
```

## Developer Notes

- Use the **UP ARROW** and **DOWN ARROW** in the terminal to scroll through past commands.
- Use `CTRL+f` to find (and replace) text within a file.

## Developer Tools

This project uses professional Python tools to support development,
testing, documentation, and code quality.

- [uv](https://docs.astral.sh/uv/) - Python environments and dependencies.
- [Ruff](https://docs.astral.sh/ruff/) - Python linting and formatting, configured in [.ruff.toml](.ruff.toml).
- [ty](https://docs.astral.sh/ty/) - Python type checking.
- [pytest](https://docs.pytest.org/) - automated Python testing, configured in [.pytest.toml](.pytest.toml).
- [prek](https://prek.j178.dev/) - Git hooks and automated checks, configured in [prek.toml](prek.toml).
- [Zensical](https://zensical.org/) - project documentation, configured in [zensical.toml](zensical.toml).

## Links

- [Hosted Documentation](https://bethspornitz.github.io/nlp-03-text-exploration-custom/)
- [Professional Python Workflow Guide](https://denisecase.github.io/pro-analytics-02/)
- [Citation](CITATION.cff)
- [License](LICENSE)
