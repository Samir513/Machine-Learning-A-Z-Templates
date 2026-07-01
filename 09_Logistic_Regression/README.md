# Day 13: Logistic Regression

This folder contains the dataset, python script, and Jupyter Notebook for **Logistic Regression**, marking the transition from Regression models to **Classification** models.

## Dataset
- **File**: `Social_Network_Ads.csv`
- **Description**: Contains social network user data:
  *   **Age**: Independent Variable
  *   **EstimatedSalary**: Independent Variable
  *   **Purchased**: Target Variable (0 = No, 1 = Yes)

## Implementation Details
1. **Feature Scaling**: Applied `StandardScaler` since Logistic Regression relies on gradient descent optimization and is sensitive to the scale of input features.
2. **Model Training**: Trained the classifier using `LogisticRegression` from `sklearn.linear_model`.
3. **Evaluation**: Evaluated using a **Confusion Matrix** and **Accuracy Score** on the test set (25% split).

### Performance Output
- **Confusion Matrix**:
