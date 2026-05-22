# Section 2: Simple Linear Regression 📈

## Overview
Simple Linear Regression is a fundamental Machine Learning algorithm used to predict a continuous dependent variable (y) based on a single independent variable (X). It works by finding the "best-fitting" straight line through the data points using a method called **Ordinary Least Squares (OLS)**, which minimizes the sum of the squared residuals (errors).

## Files in this Folder
* `Salary_Data.csv`: A dataset containing Years of Experience and Salary.
* `simple_linear_regression.py` / `*.ipynb`: The code template implementing the model.

## The Scikit-Learn 4-Step Rhythm
This section introduces the standard 4-step workflow used for almost all models in the `scikit-learn` library:
1. **Import:** `from sklearn.linear_model import LinearRegression`
2. **Instantiate:** `regressor = LinearRegression()`
3. **Fit (Train):** `regressor.fit(X_train, y_train)`
4. **Predict:** `y_pred = regressor.predict(X_test)`

## AI Pro-Tip 🤖
While standard tutorials only visualize the regression line on a graph, in real-world scenarios, we must prove the model's accuracy mathematically. In this template, I have included the use of `r2_score` from `sklearn.metrics` to calculate the exact percentage of accuracy for the model's predictions.

> **Note on Feature Scaling:** Simple Linear Regression does *not* require Feature Scaling. The algorithm includes a coefficient (the slope 'm' in y = mx + b) that automatically adapts to the scale of the independent variable.
