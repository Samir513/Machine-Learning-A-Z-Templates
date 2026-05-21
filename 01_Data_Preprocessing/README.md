# Section 1: Data Preprocessing 🛠️

## Overview
Data Preprocessing is the most crucial step in any Machine Learning pipeline. Since Machine Learning models are essentially mathematical equations, they only understand numbers. This section contains a complete, reusable template to clean, handle, and prepare raw data before feeding it into any ML algorithm.

## Files in this Folder
* `Data.csv`: A simple dummy dataset containing missing values and categorical text used for practice.
* `data_preprocessing_template.py`: The clean, fully assembled Python script containing the standard preprocessing toolkit.
* `*.ipynb` files: Jupyter Notebooks containing step-by-step execution and explanations of the code.

## Key Steps Covered in the Template
This toolkit covers the standard 5-step preprocessing rhythm:

1. **Importing Libraries & Dataset:** Using `pandas` to load the dataset and separating it into the feature matrix (`X`) and the dependent variable vector (`y`).
2. **Taking Care of Missing Data:** Using `SimpleImputer` (strategy: mean) to replace missing numerical values so the model doesn't crash.
3. **Encoding Categorical Data:** 
   * **Independent Variables:** Using `OneHotEncoder` via `ColumnTransformer` to turn categories (like countries) into dummy variables. This prevents the model from assuming a false mathematical order.
   * **Dependent Variable:** Using `LabelEncoder` to turn Yes/No targets into 1s and 0s.
4. **Splitting the Dataset:** Using `train_test_split` to divide the data into a Training set (80%) and a Test set (20%).
5. **Feature Scaling:** Using `StandardScaler` to put all features on a level playing field, ensuring that variables with large numbers don't dominate the ML equations.

## ⚠️ Important Note
**Feature Scaling is ALWAYS applied AFTER splitting the dataset.** 
If we apply feature scaling before the split, the scaling formula will use the mean and variance of the *entire* dataset (including the test set). This causes **Data Leakage**, where information from the test set "leaks" into the training process, ruining the integrity of our model evaluation.

## How to Reuse This Template
To use this code on a new dataset:
1. Change `'Data.csv'` to your dataset's name.
2. Adjust the `.iloc[]` indices to match your dataset's feature and target columns.
3. Adjust the column indices in the `OneHotEncoder` and `SimpleImputer` if your missing data or categorical data are in different columns.
