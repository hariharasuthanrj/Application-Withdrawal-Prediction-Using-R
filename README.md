# Application Withdrawal Prediction Using R
A predictive analytics project developed in **R** to identify applicants who are likely to withdraw during the Teach For America (TFA) admissions process. The project applies advanced data preprocessing, feature engineering, class balancing through upsampling, and compares multiple machine learning models to recommend the best-performing solution.

## Project Overview

Recruitment teams often face challenges in identifying applicants who may drop out before completing the admissions process. This project builds predictive models that help:

- Predict applicant withdrawal risk
- Improve recruiter prioritization
- Reduce attrition through proactive intervention
- Support data-driven recruitment decisions

The workflow includes preprocessing, feature engineering, model training, evaluation, and comparison across multiple algorithms.

## Dataset

The dataset contains applicant demographic, academic, and behavioral information including:

- Sign-up dates
- Application start and submission dates
- University and major information
- Essay sentiment
- Event attendance
- Region preferences
- Application completion status

The target variable is:

- **Completed Admissions Process**
  - Completed
  - Withdrew

## Features Engineered

Several behavioral features were created to improve predictive performance:

- Days from signup to application start
- Days from application start to submission
- Days from signup to submission
- Days before application deadline
- Signup month and year
- Submission month
- Submitted early indicator
- Quick starter flag
- Quick completer flag

High-cardinality categorical variables were also reduced to improve generalization.

## Data Preprocessing

The pipeline includes:

- Missing value imputation
- High-cardinality category reduction
- Factor encoding
- Dummy variable creation
- Near-zero variance feature removal
- Train-test split (80/20)
- Cross-validation (5-fold)

To address class imbalance, the minority class was **upsampled** to match the majority class.

## Machine Learning Models

The project compares five supervised learning algorithms:

- Decision Tree (C5.0)
- k-Nearest Neighbors (kNN)
- Naive Bayes
- Support Vector Machine (SVM)
- Artificial Neural Network (ANN)

Each model is evaluated using:

- Accuracy
- Sensitivity
- Specificity
- Precision
- Recall
- F1 Score
- Kappa Statistic

## Packages Used
---
- R
- caret
- dplyr
- readxl
- lubridate
- C50
- e1071
- kernlab
- nnet
- class
- NeuralNetTools
- fastDummies
- partykit

## Results

The comparison demonstrates that **Decision Tree (C5.0) with upsampling** delivers the strongest overall performance by achieving high sensitivity and specificity while remaining highly interpretable for operational use.

Key observations:

- Upsampling significantly improves minority-class detection.
- Decision Tree provides the best balance between performance and interpretability.
- ANN and SVM achieve competitive results but are less explainable.
- Naive Bayes tends to overpredict the majority class.
- kNN performance is affected by high-dimensional feature spaces.


## Future Improvements

- Implement SMOTE for synthetic oversampling
- Hyperparameter optimization using grid/random search
- Ensemble methods such as Random Forest and XGBoost
- Model deployment through a Shiny dashboard
- Explainability using SHAP or LIME

---

