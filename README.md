# MaternalRisk

![Status](https://img.shields.io/badge/status-in%20progress-blue)
![Python](https://img.shields.io/badge/Python-3.13-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## Table of Contents

- [Why this project?](#why-this-project)
- [Project Objective](#project-objective)
- [Research Question](#research-question)
- [Project Workflow](#project-workflow)
- [Current Progress](#current-progress)
- [Planned Modeling Approach](#planned-modeling-approach)
- [Current Status](#current-status)
- [Repository Structure](#repository-structure)
- [Technologies](#technologies)
- [Disclaimer](#disclaimer)
- [Development Notes](#development-notes)
- [Future Enhancements](#future-enhancements)

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

## Project Workflow

This project follows a structured and reproducible analytical workflow.

1. Project Planning
2. Dataset Audit
3. Data Quality Assessment & Preprocessing
4. Exploratory Data Analysis
5. Feature Engineering
6. Baseline Modeling (Logistic Regression)
7. Ensemble Modeling (Random Forest & XGBoost)
8. Model Explainability (SHAP)
9. Calibration & Clinical Evaluation
10. Final Report

---

## Current Progress

The project is currently transitioning from data preparation to exploratory data analysis.

Completed work includes:

- Dataset auditing
- Missing data investigation
- Data quality assessment
- Documentation of preprocessing decisions
- Creation of a cleaned dataset for downstream analysis

The next phase focuses on identifying clinically meaningful relationships among predictors before model development.

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

Rather than selecting the model with the highest predictive performance alone, this project emphasizes the trade-offs between predictive performance, interpretability, calibration, and potential clinical usefulness.

## Current Status

🚧 This project is currently in active development.

Completed:

- [x] Project proposal
- [x] Repository setup
- [x] Dataset audit
- [x] Data quality assessment & preprocessing strategy
- [x] Documentation and project planning

In Progress:

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
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_dataset_audit.ipynb
│   ├── 02_data_cleaning.ipynb
│   └── ...
│
├── docs/
├── reports/
├── figures/
├── models/
├── src/
│
├── decision_log.md
├── journal.md
├── requirements.txt
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

## Future Enhancements

Potential extensions include:

- External dataset validation
- Hyperparameter optimization
- Streamlit dashboard
- Model deployment
- Additional explainability analyses