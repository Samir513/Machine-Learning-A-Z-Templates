# Machine Learning A-Z Templates

This repository contains code templates, datasets, and implementations from my Machine Learning journey.

## Day 10: Decision Tree Regression

On Day 10, the focus is on **Decision Tree Regression**, a non-linear regression model that splits the dataset into distinct segments (nodes) based on feature thresholds to make predictions.

### Dataset
- **File**: `Position_Salaries.csv`
- **Description**: A dataset containing 10 distinct job levels and their corresponding typical salaries. It is commonly used to model non-linear relationships, such as predicting the salary of an employee based on their position level (e.g., Level 6.5).

### Implementation Details
The implementation is completed in Python using `scikit-learn`. Key steps included:
1. **Data Preprocessing**: Importing the dataset and splitting it into features ($X$) and the target variable ($y$).
2. **Model Training**: Fitting the `DecisionTreeRegressor` model on the entire dataset.
3. **Prediction**: Predicting the salary for a specific position level (Level 6.5).
4. **Visualisation**: Plotting the results in a high-resolution format to properly capture the step-like prediction characteristic of decision trees.
5. **Model Evaluation**: Evaluating the performance using metrics such as $R^2$ and Adjusted $R^2$.

### Results Visualisation
The Decision Tree Regression model makes predictions by assigning the average value of the leaf node to any input falling within that partition. This results in a step-like visualization rather than a continuous curve.

---
*Follow along with my daily updates as I explore more Machine Learning models.*
