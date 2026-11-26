# Binary Classification Analysis — CIE 2 Activity 2 (Roll No: AD2127)

**A Supervised Binary Classification and Model Evaluation Project using Python**

## Overview

This repository contains the **CIE 2 Activity 2** submission focused on binary classification and model evaluation using Python. It covers exploratory data inspection, handling domain-invalid zeros, building leak-free preprocessing pipelines, training and cross-validating classification models, analyzing probability thresholds, and testing inference on new records.

## Project Objectives

- Inspect dataset structure, target class balance, and feature distributions.
- Identify missing values and domain-impossible zeros in clinical measurements.
- Build leak-free preprocessing pipelines (`SimpleImputer`, `StandardScaler`) and use fixed random seeds for reproducibility.
- Train and evaluate classification models (such as `LogisticRegression` and `RandomForestClassifier`) using stratified train/test splits and cross-validation.
- Evaluate classification performance across metrics (Accuracy, Precision, Recall/Sensitivity, Specificity, F1-Score, and ROC AUC) and compare probability thresholds (such as `0.50` vs. `0.35`).
- Test predictions on new records with range and validity checks.

## Technology Stack

| Category | Tools |
|---|---|
| Programming Language | Python |
| Data Manipulation | NumPy, Pandas |
| Data Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn |
| Development Environment | Jupyter Notebook / Google Colab |

## Dataset

- **Name:** Pima Indians Diabetes Dataset
- **Source:** `pima-indians-diabetes.csv` (768 rows, 8 features + target)
- **Domain:** Medical screening / binary classification
- **Target Column:** `Outcome` (`0` = No Diabetes, `1` = Diabetes)

## Workflow

### 1. Data Loading & Inspection
- Loaded the dataset using Pandas and recorded library versions and fixed random seeds for reproducibility.
- Inspected dataset shape, data types, missing values, duplicates, and target (`Outcome`) class counts and proportions.

### 2. Data Cleaning & Preprocessing
- Converted domain-impossible zeros in `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, and `BMI` to `NaN`.
- Built leak-free `Pipeline` objects with `SimpleImputer(strategy="median")` and `StandardScaler()` fit properly during training/validation.

### 3. Exploratory Data Analysis
- Visualized target class balance and feature distributions.
- Plotted ROC curves and reviewed model evaluation diagnostics.

### 4. Model Training & Evaluation
- Trained and evaluated classification models (such as `LogisticRegression` and `RandomForestClassifier`) on a stratified train/test split and via 5-fold stratified cross-validation.
- Compared models across Accuracy, Precision, Recall (Sensitivity), Specificity, F1-Score, and ROC AUC.

### 5. Threshold Tuning & Inference
- Converted predicted probabilities into class labels and compared classification thresholds (such as `0.50` vs. `0.35`) to examine false-negative vs. false-positive trade-offs.
- Generated sample predictions on new records alongside feature range and validity checks before interpreting outputs.

## Key Skills Demonstrated

- Binary Classification & ROC-AUC Evaluation
- Leak-Free Preprocessing Pipelines
- Stratified Cross-Validation & Threshold Tuning
- Data Visualization & Reproducible Python Workflows

## Repository Structure

```text
CIE2-Activity2-Classification-AD2127/
│
├── README.md
├── Activity 2.ipynb
└── pima-indians-diabetes.csv
