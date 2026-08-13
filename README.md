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

**How accurately can gestational diabetes be predicted using information available early in pregnancy, and how does predictive performance change once OGTT results become available?**

To address this question, the project evaluates two clinically distinct modeling scenarios:

- **Early Pregnancy Model:** Uses maternal characteristics, medical history, and clinical measurements available before routine gestational diabetes screening.
- **Post-OGTT Comparison Model:** Uses the same predictors with the addition of the Oral Glucose Tolerance Test (OGTT) result.

This design allows the project to evaluate both the feasibility of early risk assessment and the additional predictive information gained after routine glucose screening.

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

The project has completed the data understanding, exploratory analysis, feature engineering, and model preparation phases.

Completed work includes:

- Dataset audit and feature inventory
- Data quality and missingness assessment
- Documentation of preprocessing decisions
- Exploratory analysis of continuous and binary clinical variables
- Investigation of relationships with gestational diabetes
- Correlation and missingness analysis
- Definition of Early Pregnancy and Post-OGTT modeling scenarios
- Creation of a shared stratified train/test split
- Development of model-specific preprocessing pipelines
- Median imputation with missingness indicators for incomplete clinical measurements
- Feature standardization for Logistic Regression
- Validation of leakage-safe preprocessing workflows
- Creation of reusable preprocessing and split artifacts

The next phase will establish an interpretable Logistic Regression baseline for both modeling scenarios before comparing performance with tree-based models.

## Planned Modeling Approach

The modeling phase will compare two feature scenarios across multiple machine-learning algorithms.

The **Early Pregnancy** scenario will serve as the primary analysis and will exclude OGTT to approximate risk assessment before routine gestational diabetes screening. The **Post-OGTT** scenario will add OGTT to evaluate how predictive performance changes once glucose-testing information becomes available.

Both scenarios will use identical train/test observations and consistent evaluation procedures to support fair comparison.

Planned algorithms include:

- Logistic Regression
- Random Forest
- XGBoost

Model performance will be evaluated using metrics appropriate for binary clinical prediction, including ROC-AUC, recall/sensitivity, specificity, precision, F1-score, and calibration. Particular attention will be given to sensitivity because failure to identify a patient at elevated risk may have greater clinical consequences than a false-positive risk classification.

## Current Status

### Completed

- [x] Project proposal and clinical motivation
- [x] Repository setup and documentation
- [x] Dataset audit
- [x] Data quality assessment and preprocessing strategy
- [x] Exploratory data analysis
- [x] Feature engineering and model preparation

### Next

- [ ] Baseline Logistic Regression

### Planned

- [ ] Random Forest modeling
- [ ] XGBoost modeling
- [ ] Model comparison and hyperparameter tuning
- [ ] Final model evaluation
- [ ] Model explainability
- [ ] Clinical interpretation and limitations
- [ ] Final project documentation

## Repository Structure

```text
maternal-risk/
│
├── data/
│   ├── raw/                         # Original dataset
│   └── processed/                   # Cleaned data used for analysis and modeling
│
├── notebooks/
│   ├── 01_dataset_audit.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_exploratory_data_analysis.ipynb
│   └── 04_feature_engineering_and_model_preparation.ipynb
│
├── docs/                            # Supporting project documentation
├── reports/                         # Final reports and analytical summaries
├── figures/                         # Exported visualizations
├── models/                          # Generated preprocessing and model artifacts
├── src/                             # Reusable project source code
│
├── decision_log.md                  # Major analytical and modeling decisions
├── journal.md                       # Development notes and project reflections
├── requirements.txt                 # Python dependencies
└── README.md                        # Project overview and documentation
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