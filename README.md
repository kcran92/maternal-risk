# MaternalRisk

![Status](https://img.shields.io/badge/status-in%20progress-blue)
![Python](https://img.shields.io/badge/Python-3.13-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## Table of Contents

- [Why this project?](#why-this-project)
- [Project Objective](#project-objective)
- [Research Question](#research-question)
- [Current Status](#current-status)
- [Repository Structure](#repository-structure)
- [Technologies](#technologies)
- [Disclaimer](#disclaimer)
- [Development Notes](#development-notes)

## Why this project?

During my first pregnancy, I was identified as being at increased risk for gestational diabetes during my very first prenatal appointment. Although I ultimately did not develop gestational diabetes, I underwent additional screening and experienced months of uncertainty while waiting for definitive testing.

That experience sparked a question:

> Could routinely collected information from the first prenatal visit be used to estimate gestational diabetes risk earlier using an explainable machine learning model?

This project explores that question by developing and evaluating interpretable predictive models using maternal demographic, clinical, and medical history data available during early prenatal care. The goal is not to replace clinical diagnosis, but to investigate whether machine learning can support earlier risk assessment and more informed clinical decision-making.

---

## Project Objective

The objective of this project is to investigate whether routinely collected clinical information available during the first prenatal visit can be used to predict gestational diabetes mellitus (GDM) before routine diagnostic screening.

The project emphasizes:

- Explainable machine learning
- Reproducible data science workflows
- Clinically meaningful model evaluation
- Transparent documentation of analytical decisions

## Research Question

> Can gestational diabetes be accurately predicted during early pregnancy using routinely collected maternal characteristics?

## Planned Modeling Approach

To evaluate whether gestational diabetes can be predicted using information available during the first prenatal visit, several machine learning models will be developed and compared.

The planned modeling pipeline includes:

- Logistic Regression (interpretable baseline)
- Decision Tree
- Random Forest
- XGBoost

Models will be evaluated using clinically meaningful performance metrics, including:

- ROC-AUC
- Recall (Sensitivity)
- Precision
- F1-score
- Calibration (Brier Score and calibration curves)

Model explainability techniques, including SHAP (SHapley Additive exPlanations), will be used to interpret predictions and identify the most influential clinical features.

Rather than selecting the model with the highest accuracy alone, this project emphasizes the trade-offs between predictive performance, interpretability, and potential clinical usefulness.

## Current Status

🚧 This project is currently in active development.

Completed:

- [x] Project proposal
- [x] Repository setup
- [x] Dataset audit
- [x] Documentation and project planning

In Progress:

- [ ] Data cleaning
- [ ] Exploratory data analysis

Planned:

- [ ] Feature engineering
- [ ] Baseline Logistic Regression
- [ ] Random Forest
- [ ] XGBoost
- [ ] Model explainability (SHAP)
- [ ] Calibration analysis
- [ ] Final report

## Repository Structure

```text
maternal-risk/
│
├── data/
├── notebooks/
├── src/
├── reports/
├── references/
├── figures/
├── models/
├── docs/
└── README.md
```

## Technologies

### Core Libraries

- pandas
- NumPy
- scikit-learn
- XGBoost
- SHAP

### Development Tools

- Jupyter Notebook
- Git
- GitHub
- VS Code / Cursor

### Visualization

- Matplotlib

## Disclaimer

This project is intended for educational and portfolio purposes only.

The predictive models developed in this repository are not intended for clinical use or medical decision-making.

## Development Notes

This repository documents the complete lifecycle of an applied healthcare data science project—from project planning and data auditing through model development, evaluation, and interpretation.

The goal is not only to build a predictive model, but also to demonstrate professional data science practices, including reproducibility, documentation, explainability, and thoughtful model evaluation.