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
