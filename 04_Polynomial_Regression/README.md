# Section 4: Polynomial Regression 📐

## Overview
Polynomial Regression is a form of regression analysis in which the relationship between the independent variable (X) and the dependent variable (y) is modeled as an $n$-th degree polynomial. It is used when a visual check of the scatter plot shows a curved, wave-like, or exponential relationship that a rigid straight line cannot fit.

## Files in this Folder
* `Position_Salaries.csv`: A dataset of 10 job levels (from Business Analyst to CEO) and their corresponding salaries.
* `polynomial_regression.ipynb` / `*.py`: The code template implementing the model.
* `Polynomial_Regression_Guide.html`: Custom interactive study guide covering the 5-Question Schema and visualization hacks.

## Trick Question: Is it Linear or Non-Linear?
Even though the line on the graph curves, Polynomial Regression is mathematically classified as a **Linear Model**. In statistics, "linearity" refers to the **coefficients ($b_0, b_1, b_2...$)**, not the $x$ variables. Since the coefficients are all single-powered and added together, the math remains linear!

## The 2-Step Code Rhythm
Because `scikit-learn` does not have a native "PolynomialRegression" class, we build this model using a two-step process:
1. **Transform Features:** Use `PolynomialFeatures` to generate power columns ($X^2, X^3, X^4$) from our single column:
   `X_poly = PolynomialFeatures(degree=4).fit_transform(X)`
2. **Train Linear Model:** Fit a standard `LinearRegression` model using the newly created polynomial feature matrix:
   `LinearRegression().fit(X_poly, y)`

## AI Pro-Tip 🤖 (High-Resolution Plotting)
When plotting polynomial curves, using standard discrete data points results in a jagged, blocky line. To solve this, this template uses a high-resolution grid using `np.arange` with a step size of `0.1` to generate a perfectly smooth, publication-ready curve.
