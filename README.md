# Cultural-Bias-Analyzer
## Cultural Bias Analysis in LLMs and bias auditing toolkit

## CultureBIAS Project Directory Structure

```
culturebias/
├── README.md
├── PLAN.md
├── requirements.txt
│
├── data/
│   ├── raw/
│   │   ├── templates/
│   │   │   ├── stereotype_elicitation.jsonl
│   │   │   ├── scenario_based.jsonl
│   │   │   ├── role_play.jsonl
│   │   │   └── comparative.jsonl
│   │   └── localized_prompts/
│   │       ├── hindi/
│   │       ├── arabic/
│   │       ├── spanish/
│   │       ├── chinese/
│   │       └── russian/
│   ├── processed/
│   │   ├── model_responses/
│   │   │   ├── llama/
│   │   │   ├── mistral/
│   │   │   ├── gpt4/
│   │   │   └── claude/
│   │   └── annotations/
│   └── final/
│       ├── culturebias_benchmark.jsonl
│       └── annotation_schema.json
│
├── src/
│   ├── data_pipeline/
│   │   ├── template_design.py
│   │   ├── localization.py
│   │   ├── prompt_expansion.py
│   │   └── quality_control.py
│   ├── model_interface/
│   │   ├── base_model.py
│   │   ├── openai_models.py
│   │   ├── huggingface_models.py
│   │   └── query_manager.py
│   ├── annotation/
│   │   ├── annotation_interface.py
│   │   ├── quality_metrics.py
│   │   └── agreement_calculator.py
│   ├── evaluation/
│   │   ├── automatic_metrics.py
│   │   ├── human_metrics.py
│   │   ├── statistical_analysis.py
│   │   └── benchmark_scorer.py
│   ├── mitigation/
│   │   ├── prompt_engineering.py
│   │   ├── fine_tuning.py
│   │   └── post_processing.py
│   └── visualization/
│       ├── bias_heatmaps.py
│       ├── distribution_plots.py
│       └── case_studies.py
│
├── experiments/
│   ├── exploratory_analysis.py
│   ├── quantitative_evaluation.py
│   ├── causal_analysis.py
│   ├── mitigation_experiments.py
│   └── human_studies.py
│
├── configs/
│   ├── models.yaml
│   ├── languages.yaml
│   └── annotation_schema.yaml
│
├── scripts/
│   ├── collect_responses.py
│   ├── run_annotation.py
│   ├── compute_metrics.py
│   ├── apply_mitigation.py
│   └── generate_report.py
│
├── notebooks/
│   ├── data_exploration.ipynb
│   ├── bias_analysis.ipynb
│   ├── mitigation_results.ipynb
│   └── visualization_dashboard.ipynb
│
├── results/
│   ├── figures/
│   ├── tables/
│   └── reports/
│
└── paper/
    ├── main.tex
    ├── sections/
    ├── figures/
    └── bibliography.bib
```

## Key Components

### Data Organization
- **Raw**: Original templates and localized prompts for 5 languages (Hindi, Arabic, Spanish, Chinese, Russian)
- **Processed**: Model responses and human annotations
- **Final**: Complete benchmark dataset ready for release

### Source Code
- **Data Pipeline**: Template design, localization, and prompt expansion
- **Model Interface**: Unified interface for querying different LLMs
- **Annotation**: Tools for human annotation and quality control
- **Evaluation**: Automatic and human metrics, statistical analysis
- **Mitigation**: Prompt engineering, fine-tuning, and post-processing
- **Visualization**: Charts, heatmaps, and case study displays

### Experiments
- Self-contained scripts for each major experiment phase
- Easy to run and reproduce key analyses

### Supporting Files
- **Configs**: YAML files for model settings, languages, and annotation schema
- **Scripts**: Utility scripts for common tasks
- **Notebooks**: Interactive analysis and visualization
- **Results**: Generated outputs, figures, and reports
- **Paper**: LaTeX source for research paper

# CultureBIAS Notebooks Overview

## 1. **Data Exploration Notebook** (`data_exploration.ipynb`)

- **Template analysis**: Distribution and statistics of different prompt types
- **Language coverage**: Analysis across Hindi, Arabic, Spanish, Chinese, Russian
- **Cultural dimensions**: Bias targets and cultural contexts
- **Prompt characteristics**: Length, word count, and linguistic features
- **Word clouds**: Visual representation of prompt content by language
- **Comprehensive summary**: Dataset statistics and coverage metrics

## 2. **Bias Analysis Notebook** (`bias_analysis.ipynb`)

- **Model comparison**: Bias patterns across different LLMs
- **Language-specific bias**: How bias varies by language/culture
- **Cultural bias patterns**: Stereotype directions, harm types, offense targets
- **Statistical significance**: Chi-square tests, ANOVA for model differences
- **Correlation analysis**: Relationships between bias measures
- **Comprehensive reporting**: Automated bias analysis reports

## 3. **Mitigation Results Notebook** (`mitigation_results.ipynb`)

- **Effectiveness analysis**: Compare prompt engineering, fine-tuning, post-processing
- **Bias reduction calculation**: Quantify percentage improvements
- **Quality trade-offs**: Helpfulness vs bias reduction analysis
- **Model-specific mitigation**: How different models respond to mitigation
- **Statistical validation**: Significance testing for mitigation effects
- **Comprehensive reporting**: Best strategies and recommendations

## 4. **Visualization Dashboard Notebook** (`visualization_dashboard.ipynb`)

- **Interactive dashboards**: Multi-panel overview with Plotly
- **Bias heatmaps**: Model vs language bias patterns
- **Stereotype networks**: Relationship visualization between cultures and bias
- **Temporal analysis**: Bias trends over time
- **Distribution analysis**: Detailed statistical distributions
- **Correlation dashboards**: Interactive correlation matrices
- **Cultural radar charts**: Multi-dimensional bias assessment
- **Export functionality**: Saves HTML dashboards for sharing

## Key Features:

- **Sample data generation** for testing when real data isn't available
- **Comprehensive statistical analysis** with proper significance testing
- **Interactive visualizations** using Plotly for better exploration
- **Automated reporting** with key insights and recommendations
- **Modular design** - each notebook can run independently
- **Export capabilities** for sharing results and dashboards

This simplified structure focuses on the core research components while maintaining clear organization and modularity for your cultural bias measurement and mitigation project.
