# Heart Disease Analysis and Machine Learning

## Overview

This portfolio project explores characteristics associated with recorded
heart disease and compares machine learning classification models.

## Objectives

- Inspect and clean the dataset.
- Explore patterns using statistics and visualisations.
- Compare Logistic Regression, Decision Tree, Random Forest and KNN.
- Evaluate models using cross-validation, precision, recall and ROC-AUC.
- Present findings in a Tableau dashboard.

## Tools

Python, pandas, NumPy, Matplotlib, seaborn, SciPy, scikit-learn,
Jupyter Notebook, Tableau and Git.

## Data source

UCI Machine Learning Repository — Heart Disease dataset.

https://archive.ics.uci.edu/dataset/45/heart+disease

## Scope

This is an educational project analysing recorded heart disease status.
It is not a clinical diagnostic tool or a prediction of future disease.

## Status

Data audit, exploratory analysis, model evaluation and Tableau dashboard completed.

## Interactive dashboard

[View the Heart Disease Model Evaluation dashboard on Tableau Public](https://public.tableau.com/app/profile/dafydd.jones2594/viz/HeartDiseaseClassificationModelEvaluation/HeartDiseaseModelEvaluation)

## Model comparison

Five-fold stratified cross-validation was performed on 242 training records.
Preprocessing was fitted separately within each training fold.

| Model | Accuracy | Recall | ROC-AUC |
|---|---:|---:|---:|
| Baseline | 0.541 | 0.000 | 0.500 |
| Logistic Regression | 0.847 | 0.784 | 0.906 |
| Decision Tree | 0.773 | 0.729 | 0.832 |
| Random Forest | 0.814 | 0.774 | 0.900 |
| KNN | 0.826 | 0.792 | 0.873 |

Logistic Regression was selected for its highest mean accuracy and
ROC-AUC, alongside relatively consistent scores across folds.

## Final test results

The selected model was evaluated on 61 reserved test records.

| Metric | Score |
|---|---:|
| Accuracy | 86.9% |
| Precision | 81.2% |
| Recall | 92.9% |
| ROC-AUC | 0.958 |

Confusion matrix: 27 true negatives, 6 false positives,
2 false negatives and 26 true positives.

## Limitations

- The dataset is small and historical.
- Results reflect one train/test split.
- Full-dataset exploratory analysis preceded modelling, so the test set
  is not a completely independent confirmation.
- Associations do not establish causation or population prevalence.
- External validation and probability calibration were not assessed.
- This is an educational project, not a clinical diagnostic tool.

## How to run the project

1. Clone this repository and open its folder.
2. Install packages: `python -m pip install -r requirements.txt`
3. Download the ZIP from https://archive.ics.uci.edu/dataset/45/heart+disease
4. Extract it and copy processed.cleveland.data into data/raw/.
5. Start JupyterLab: `jupyter lab`
6. Run notebooks 01, 02 and 03 in order.

Check relative paths against each notebook's working folder:
- From the project folder, use data/raw/ and data/processed/.
- From notebooks/, use ../data/raw/ and ../data/processed/.

Notebook 02 exports the results CSV files needed by Notebook 03.
Notebook 03 creates charts and additional Tableau tables.
Data files are excluded from Git and must be recreated locally.
The packaged Tableau workbook is in tableau/.
