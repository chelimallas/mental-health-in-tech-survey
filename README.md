# mental-health-in-tech-survey
#  Mental Health in Tech - Classification Project

This project analyzes a survey dataset on mental health in the tech workplace. Using machine learning classification techniques, we predict whether a person seeks mental health treatment based on personal, professional, and perception-based attributes.

##  Dataset Description

- **Source**: [Kaggle Mental Health in Tech Survey](https://www.kaggle.com/datasets/osmi/mental-health-in-tech-survey)
- **Target Variable**: `treatment` (Yes/No)
- **Features**:
  - Demographics: Age, Gender, Country
  - Work context: Remote work, Benefits, Company size
  - Mental health perceptions: Mental vs Physical importance, Awareness, Resources

## Preprocessing

- Removed irrelevant fields (e.g., timestamp, comments)
- Handled outliers in Age (<10 or >100 replaced with NaN → imputed)
- Encoded categorical variables using Label Encoding
- Scaled features with `StandardScaler`
- Imputed missing values using mode (categorical) and median (numerical)

##  Models Used

| Model                | Notes                                  |
|---------------------|----------------------------------------|
| Decision Tree        | Visual, interpretable                  |
| K-Nearest Neighbors  | Visual cluster formation               |
| Random Forest        | Best accuracy and generalization       |
| Naive Bayes          | Fast, probabilistic                    |
| Logistic Regression  | Strong ROC, interpretable coefficients |

All models were evaluated using **Stratified 5-Fold Cross-Validation** and metrics such as **Accuracy, Precision, Recall, F1-Score**.

## PCA & Visualization

- Applied **PCA (2 components)** to reduce dimensions for visualization
- Re-evaluated all models post-PCA
- Generated visualizations including:
  - Confusion matrices
  - ROC curves
  - PCA cluster scatter plots
  - Tree structure for Decision Tree

##  Results Summary

- **Random Forest** had the best performance before PCA
- PCA was useful for visualization but reduced model accuracy
- Logistic Regression had strong ROC performance even post-PCA
- KNN showed clear decision boundaries in PCA space

##  Key Takeaways

- Use tree-based models for high accuracy
- Use PCA + KNN for insightful visualizations
- Always cross-validate to ensure generalization
- Feature scaling and proper encoding significantly impact performance


