# Section 5: Support Vector Regression (SVR) 📈

## Overview
Support Vector Regression (SVR) is a highly robust, non-parametric regression model. Instead of trying to minimize the error of a thin line (like standard Linear Regression), SVR aims to fit a "fat tube" (called the **$\epsilon$-insensitive tube**) around the data points. Errors within this tube are completely ignored, and the model's boundary is defined only by the points lying on or outside the tube, known as **Support Vectors**.

## Files in this Folder
* `Position_Salaries.csv`: The dataset containing 10 job levels and their corresponding salaries.
* `support_vector_regression.ipynb`: The Jupyter Notebook containing the code and model visualizations.
* `SVR_Study_Guide.html`: Custom interactive study guide covering the 6-Question Schema.

## Why Feature Scaling is 100% Mandatory ⚠️
This is the most critical concept of SVR: **You must apply Feature Scaling to both the independent variable (X) and the dependent variable (y).**

Unlike Linear Regression, the `SVR` class in `scikit-learn` does not have built-in scaling. Because SVR is a distance-based algorithm (it measures geometric distances between data points to fit the tube), having features on vastly different scales (e.g., Level `1-10` vs. Salary `$45k-$1M`) will completely break the distance calculations. Without `StandardScaler`, your SVR model will output a flat, useless line.

## The SVR Code Rhythm
Because scaling is mandatory, the preprocessing steps involve scaling both variables, fitting the model, and then reverse-scaling (inverse transforming) the predictions to get the real-world values back:

```python
# 1. Scale Features & Target (y must be reshaped to 2D)
from sklearn.preprocessing import StandardScaler
sc_X = StandardScaler()
sc_y = StandardScaler()
X_scaled = sc_X.fit_transform(X)
y_scaled = sc_y.fit_transform(y.reshape(-1, 1))

# 2. Fit the SVR Model (Using the non-linear RBF kernel)
from sklearn.svm import SVR
regressor = SVR(kernel='rbf')
regressor.fit(X_scaled, y_scaled.ravel())

# 3. Predict & Inverse Transform (To convert scaled outputs back to dollars)
y_pred = sc_y.inverse_transform(regressor.predict(sc_X.transform([[6.5]])).reshape(-1, 1))
