# MLPRegressor for Salary Prediction

## Overview
This project explores the implementation of a **Multi-layer Perceptron Regressor (MLPRegressor)** to predict salary based on various demographic and professional factors. The dataset used for this project comes from the **Adult Data Set** from the UCI Machine Learning Repository.

## Dataset
The dataset includes attributes such as:
- **Age**
- **Employer type**
- **Final sampling weight**
- **Education level**
- **Years of education**
- **Marital status**
- **Occupation**
- **Family relationship**
- **Race**
- **Gender**
- **Capital gain**
- **Capital loss**
- **Hours worked per week**
- **Country of origin**
- **Salary classification (>50K or ≤50K)**

After preprocessing, only **numeric features** were used for training the MLPRegressor.

## Implementation
The project consists of the following key steps:

### 1. Data Preprocessing
- **Conversion of categorical data**: String variables such as `marital status`, `race`, and `occupation` were converted into numerical values.
- **Feature selection**: Unnecessary columns were removed to improve model efficiency.
- **Data normalization**: Standardization techniques were applied to improve model training.

### 2. Model Definition: Multi-layer Perceptron Regressor
The base **MLPRegressor** model was configured with:
- **Hidden layers**: 1 layer with 2 neurons
- **Maximum iterations**: 300
- **Activation function**: ReLU
- **Solver**: Adam optimizer

Training was performed using **train-test split**.

### 3. Model Evaluation
The performance of the model was assessed using:
- **R-squared (R²)**: Measures how well the model explains the variability in salary.
- **Mean Squared Error (MSE)**: Evaluates the average squared differences between predicted and actual values.
- **Explained Variance Score**: Indicates how much of the dataset's variance is captured by the model.

### 4. Hyperparameter Optimization
A **grid search approach** was used to fine-tune the model, selecting the best configuration for:
- **Number of hidden layers**
- **Learning rate**
- **Number of iterations**

### 5. Results and Visualizations
- **Loss Curve**: Showed how the model's error decreased over epochs.
- **Scatter Plot**: Compared predicted vs actual values to analyze model performance.

## Key Findings
- The optimized **MLPRegressor model** showed improved **R² scores**, indicating a better fit.
- **Scatter plots** showed that predictions became more accurate after hyperparameter tuning.
- **Variance reduction** was observed after optimization.

## Requirements
To run this project, install the following dependencies:

```bash
pip install numpy pandas matplotlib scikit-learn
