# Sleep Quality Prediction with Machine Learning

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-orange?logo=ai)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.0%2B-red?logo=scikitlearn)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

A machine learning project that predicts sleep quality and classifies sleep disorders using various regression and classification algorithms.

## ✨ Features

- **Sleep Quality Prediction**: Regression models to predict sleep quality scores
- **Sleep Disorder Classification**: Multiple classifiers to identify sleep disorders
- **Comprehensive Dataset**: 400 samples with 13 features related to sleep health and lifestyle
- **Multiple Algorithms**: Implementation of various regression and classification techniques

## 📊 Dataset

The Sleep Health and Lifestyle Dataset contains 400 rows and 13 columns with features including:
- Demographic information (Gender, Age, Occupation)
- Sleep metrics (Sleep Duration, Quality of Sleep)
- Lifestyle factors (Physical Activity Level, Stress Levels, Daily Steps)
- Health indicators (BMI Category, Blood Pressure, Heart Rate)
- Sleep Disorders (presence or absence)

## 🛠️ Data Preprocessing

### Steps Performed:
1. **Blood Pressure Processing**: Split into systolic and diastolic values
2. **Categorical Encoding**: Label encoding for:
   - Gender
   - Occupation 
   - BMI Category
   - Sleep Disorder
3. **Feature Scaling**: Min-max scaling for "Daily Steps" feature
4. **Target Variable Preparation**:
   - Regression: Sleep quality score
   - Classification: Sleep disorder categories (0: Insomnia, 1: None, 2: Sleep Apnea)

## 📈 Regression Models

### Linear Regression
- Baseline model for predicting sleep quality scores
- Simple implementation with all features

### Ridge Regression
- Effective for handling multicollinearity in data
- Shrinks coefficients without setting them to zero
- Helps prevent overfitting

### Lasso Regression
- Performs automatic feature selection
- Sets coefficients of irrelevant features to zero
- Useful for datasets with redundant features

## 🔍 Classification Models

### Support Vector Machine (SVM)
- **Linear Kernel**: Finds optimal hyperplane for linear separation
- **RBF Kernel**: Handles non-linear classification using radial basis function
- **Polynomial Kernel**: Non-linear classification with polynomial function
- **Parameter Tuning**: Regularization parameter (C) controls complexity-accuracy tradeoff

### Random Forest Classifier
- Ensemble learning with multiple decision trees
- Reduces overfitting through random feature subsets
- **Parameters**: 
  - n_estimators: Number of trees
  - max_depth: Controls model complexity (higher values increase overfitting risk)

### K-Neighbors Classifier
- Instance-based learning using nearest neighbors
- Handles both linear and non-linear data
- **Parameters**:
  - n_neighbors: Number of neighbors (smaller values may cause overfitting)

### Gradient Boosting Classifier
- Sequential building of weak learners (decision trees)
- Each tree corrects errors of previous ones
- **Parameters**:
  - learning_rate: Contribution of each tree (higher values increase overfitting risk)

### Decision Tree Classifier
- Tree-based model with feature splits
- Handles both numerical and categorical features
- Prone to overfitting without proper regularization
