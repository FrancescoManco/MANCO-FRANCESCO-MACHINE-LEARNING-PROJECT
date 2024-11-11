# Employee Productivity Prediction in the Garment Industry

This repository contains the implementation of a machine learning classification model to predict employee productivity levels in a garment factory. The project utilizes a dataset from the UCI Machine Learning Repository to classify productivity into two categories: `Low Productivity` and `High Productivity`. By applying pre-processing, feature selection, and various classification algorithms, the project identifies the most effective model for accurate productivity prediction.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Methodology](#methodology)
    - [Data Pre-processing](#data-pre-processing)
    - [Modeling and Hyperparameter Tuning](#modeling-and-hyperparameter-tuning)
6. [Results](#results)
7. [Conclusions](#conclusions)
8. [References](#references)

## Project Overview
In this project, we develop a classification system that predicts productivity levels of employees within the garment industry. The aim is to leverage machine learning to improve workforce management and operational efficiency by accurately categorizing employees into `Low Productivity` and `High Productivity` classes.

## Dataset
The dataset used comes from the UCI Machine Learning Repository and includes 1,197 samples representing different workdays and production lines in a garment factory. Key variables in the dataset include:
- **Production parameters**: date, day, quarter, department, team number, workers count, style changes, standard minute value (SMV), work-in-progress, and overtime.
- **Incentives and idle information**: financial incentives, idle time, and idle men.
- **Productivity metrics**: targeted and actual productivity rates.

The target variable is derived from the `actual_productivity` feature, which is divided into `Low Productivity` and `High Productivity` based on a threshold value of 0.72.

## Installation
To run this project locally, you will need Python and the following libraries:
- `numpy`
- `pandas`
- `scikit-learn`
- `matplotlib`

You can install the dependencies with:
```bash
pip install numpy pandas scikit-learn matplotlib

## Methodology

### Data Pre-processing
Data pre-processing steps include:
- **Cleaning and standardization**: Unifying categorical values and consolidating quarters.
- **Handling missing values**: Applying imputation to the `Work-in-Progress` variable.
- **Encoding**: One-Hot Encoding was applied to categorical variables.
- **Feature Engineering**: Transitioned from regression to binary classification by setting a productivity threshold.

### Modeling and Hyperparameter Tuning
The following models were evaluated:
1. K-Nearest Neighbors (KNN)
2. Logistic Regression
3. Decision Tree
4. Random Forest

To ensure robust performance, a nested cross-validation framework was employed:
- **Outer Cross-Validation**: 10-fold stratified cross-validation for unbiased performance estimation.
- **Inner Cross-Validation**: 5-fold cross-validation for hyperparameter optimization.

Each model underwent hyperparameter tuning, and the Random Forest model demonstrated the best performance with an accuracy of 85%.

## Results
| Model            | Accuracy | Precision | Recall | F1-score |
|------------------|----------|-----------|--------|----------|
| KNN              | 0.77     | 0.77      | 0.77   | 0.76     |
| Logistic Regression | 0.79  | 0.79      | 0.79   | 0.79     |
| Decision Tree    | 0.80     | 0.79      | 0.80   | 0.80     |
| **Random Forest** | **0.85** | **0.85**  | **0.85** | **0.85** |

The Random Forest model achieved the highest AUC of 0.92, highlighting its effectiveness in predicting employee productivity levels.

## Conclusions
This project demonstrates the utility of machine learning in classifying employee productivity in the garment sector. The optimized Random Forest model showed superior performance and reliability, making it suitable for real-world deployment in similar industrial settings.

## References
- Dataset source: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php)
- Manco, F. *Predicting Employee Productivity in the Garment Factory Using Machine Learning Techniques* (University of Bari Aldo Moro)

