# House Price Prediction: Simple Linear Regression

## Overview
This repository contains a complete implementation of a **Simple Linear Regression** model to predict house prices based on their area (square footage). The project serves as a foundational exploration into machine learning modeling, focusing on understanding the mathematical relationship between a single independent variable (Area) and a dependent variable (Price), while accounting for inherent data noise.

## Problem Statement
The objective is to learn and model the linear relationship between house area (\(X\)) and price (\(y\)). By leveraging a synthetically generated dataset, the model attempts to discover the underlying parameters (slope and intercept) that govern this relationship.

## Methodology & Implementation
The project is structured into five sequential phases:

1. **Synthetic Data Generation:** 
   A dataset of 100 samples is generated using a uniform distribution for area (50 to 200 square meters). The target prices are calculated using the ground-truth formula: 
   \[
y = 50x + 1000 + \epsilon
\]
   where \(\epsilon\) represents Gaussian noise (\(\mu=0, \sigma=500\)). A random seed (`42`) is set to ensure absolute reproducibility.

2. **Exploratory Data Analysis (EDA):** 
   A scatter plot is utilized to visually verify the linear trend and observe the dispersion caused by the injected noise.

3. **Model Training (Dual Approach):** 
   To ensure robustness and validate the implementation, the model is trained using two independent methods:
   - *Analytical approach:* Manual implementation using the Ordinary Least Squares (OLS) formula via NumPy.
   - *Library approach:* Utilization of the optimized `LinearRegression` class from Scikit-learn.
   Both methods yielded identical results, confirming the mathematical correctness of the manual implementation.

4. **Evaluation & Metrics:** 
   The model's performance is rigorously evaluated using standard regression metrics: **MSE** (Mean Squared Error), **RMSE** (Root Mean Squared Error), **MAE** (Mean Absolute Error), and **R²** (Coefficient of Determination).

5. **Visual Validation:** 
   The fitted regression line is superimposed on the scatter plot to visually confirm the model's alignment with the data distribution.

## Results
The trained model successfully discovered the underlying linear relationship:
- **Discovered Equation:** \(y = 50.46x + 890.60\)
- **Ground Truth Equation:** \(y = 50x + 1000 + \epsilon\)
- **R² Score:** ~0.96 (The model explains approximately 96% of the variance in the data)
- **RMSE:** ~451 (The remaining error is strictly bounded by the standard deviation of the injected noise, indicating no overfitting or underfitting).

## How to Run
You can run the notebook directly in Google Colab. The required libraries are standard and can be installed via:
```bash
pip install numpy pandas matplotlib scikit-learn
```
**Acknowledgements**
Special thanks are extended to the following individuals for their invaluable guidance, academic support, and instruction throughout this project:
Project Supervisor & Instructor: **Dr. Mohammad Ali Javadzadeh**
Teaching Assistant: **Dr. Ali Jaleh Karimi**

**License**
This project is open-source and available for educational and academic purposes
