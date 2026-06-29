# Day 12: Model Selection (Regression)

This folder focuses on **Model Selection**, comparing the performance of multiple regression models on the same dataset to identify the best-performing model using the R-squared ($R^2$) evaluation metric.

## Dataset
- **File**: `Data.csv`
- **Description**: A dataset from a Combined Cycle Power Plant, containing hourly average environmental variables:
  *   **AT**: Ambient Temperature
  *   **V**: Exhaust Vacuum
  *   **AP**: Ambient Pressure
  *   **RH**: Relative Humidity
  *   **PE**: Net hourly electrical energy output (Target Variable)

## Model Comparison & R-squared Results

We trained and evaluated five distinct regression models on this dataset (using an 80/20 train/test split). Below are the performance results based on the $R^2$ score:

| Regression Model | R-squared ($R^2$) Score | Feature Scaling Required? |
| :--- | :---: | :---: |
| **Random Forest Regression** | **~0.9615** | No |
| **Support Vector Regression (SVR)** | **~0.9480** | Yes |
| **Polynomial Regression (Degree 4)** | **~0.9458** | No |
| **Multiple Linear Regression** | **~0.9325** | No |
| **Decision Tree Regression** | **~0.9229** | No |

### Conclusion
On this specific dataset, the **Random Forest Regression** model yielded the highest $R^2$ score, making it the most suitable choice for predicting the electrical energy output under these environmental conditions.
