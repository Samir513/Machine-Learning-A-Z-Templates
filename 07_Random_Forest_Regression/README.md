This folder contains the dataset, code implementation, and interactive study guides for **Random Forest Regression**, an ensemble learning method used for robust non-linear regression.

## Folder Contents
*   `Position_Salaries.csv`: The classic non-linear dataset mapping job levels to typical salaries.
*   `random_forest_regression_guide.html`: A comprehensive Jupyter notebook export documenting the implementation step-by-step with output cell logs.
*   `RFR_StudyGuide.html`: An interactive, beautifully styled HTML study guide designed to explain the core mechanics of bagging, ensemble aggregation, and model optimization.

## Key Takeaways
1. **Ensemble Concept**: Unlike a single Decision Tree, Random Forest reduces variance by training multiple trees on random bootstrap samples and averaging their predictions.
2. **Feature Scaling**: No feature scaling is required for this model as splits are based on tree-based relative order comparisons rather than coordinate distances.
3. **Out-of-Bag (OOB) Evaluation**: We used OOB metrics to evaluate the generalization performance of the forest natively during the training loop.
