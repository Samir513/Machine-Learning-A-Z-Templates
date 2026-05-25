# Section 3: Multiple Linear Regression 🌐

## Overview
Multiple Linear Regression expands on Simple Linear Regression by predicting a continuous dependent variable (y) based on **multiple** independent variables (X). Instead of drawing a 1D line, this model calculates a hyperplane through multidimensional space.

## Files in this Folder
* `50_Startups.csv`: A dataset of 50 companies containing R&D Spend, Administration Spend, Marketing Spend, State (categorical), and Profit (target).
* `multiple_linear_regression.py` / `*.ipynb`: The code template implementing the model.
* `MLR_Study_Guide.html`: Custom interactive study guide covering the 5-Question Schema and AI Pro-Tips.

## Key Concept: The Dummy Variable Trap
When dealing with categorical data (like "State"), we use `OneHotEncoder`. However, we must apply the **n-1 rule** (dropping one dummy column) to avoid perfect multicollinearity, which would break the underlying mathematics of the regression model. *Note: Scikit-learn's `LinearRegression` class handles this automatically behind the scenes!*

## Key Concept: Feature Selection (Backward Elimination)
Throwing every variable into a model is bad practice. To build a robust model, we use Stepwise Regression (specifically Backward Elimination) to systematically remove features with the highest P-values (usually > 0.05) until only statistically significant predictors remain.

## AI Pro-Tip 🤖 (Adjusted R-Squared)
In Multiple Linear Regression, standard R-Squared is flawed because it artificially increases whenever a new variable is added, even if that variable is garbage. To evaluate this model professionally, you must calculate **Adjusted R-Squared**, which penalizes the model for adding useless variables.
