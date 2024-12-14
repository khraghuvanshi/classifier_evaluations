# Classifier Comparison Project

## Overview
This project compares the performance of six supervised learning classifiers—Random Forest, Decision Tree, K-Nearest Neighbors (KNN), Naive Bayes, Support Vector Machine (SVM), and Logistic Regression—on binary classification tasks using three datasets from the UCI Machine Learning Repository. Inspired by the paper *“An Empirical Comparison of Supervised Learning Algorithms”* by Caruana et al. (2006), the project evaluates the classifiers using metrics like training, validation, and testing accuracy across different train-test splits (20/80, 50/50, 80/20).

## Objective
The goal is to determine the relative performance of the six classifiers and identify which performs best across datasets and data splits.

## Methodology
### Datasets
- **Dataset 1:** Breast Cancer dataset.
- **Dataset 2:** Heart Disease dataset.
- **Dataset 3:** Adult Income dataset.

### Preprocessing
- Missing values handled via imputation:
  - **Numerical features:** Filled with the mean.
  - **Categorical features:** Filled with the mode.
- Preprocessed using `ColumnTransformer`:
  - One-hot encoding for categorical features.
  - Standard scaling for numerical features.

### Evaluation
- **Hyperparameter Tuning:** Conducted using `GridSearchCV`.  
- **Metrics:** Training, validation, and testing accuracy, confusion matrices, and classification reports.

## Results
- **Best Performers:** SVM and Random Forest consistently achieved the highest accuracy across datasets.
- **Other Observations:**
  - Logistic Regression: Simple yet effective.
  - KNN: Sensitive to hyperparameters and data size.
  - Decision Tree: Prone to overfitting.
  - Naive Bayes: Performed poorly on correlated features.

