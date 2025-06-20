# 🚢 Titanic Survival Prediction — Model Comparison & Benchmarking
This notebook aims to build a strong ML pipeline for the Titanic dataset, comparing classic and modern classifiers.
We go beyond accuracy to evaluate recall, precision, and F1 scores

---

##  Dataset Overview
- `train.csv`: contains labels (Survived)
- `test.csv`: no labels, used for submission
- Features include:
  - `Pclass`, `Sex`, `Age`, `SibSp`, `Parch`, `Fare`, `Embarked`, `Cabin`, `Ticket`, `Name`

---

##  Models Compared

| Model              | Accuracy | Precision (1) | Recall (1) | F1-Score (1) |
|-------------------|----------|---------------|------------|--------------|
| Logistic Regression | 0.7989 | 0.80 | 0.67 | 0.73 |
| Random Forest       | 0.7598 | 0.76 | 0.60 | 0.67 |
| SVM (RBF kernel)    | 0.6648 | 0.71 | 0.30 | 0.42 |
| XGBoost             | 0.7709 | 0.78 | 0.62 | 0.69 |
| LightGBM            | 0.7821 | 0.79 | 0.63 | 0.70 |
| CatBoost            | 0.8045 | 0.83 | 0.66 | 0.73 |
| Gradient Boosting   | **0.8101** | **0.87** | 0.63 | **0.73** |
| AdaBoost            | 0.7877 | 0.80 | 0.64 | 0.71 |

## Key Learnings

- **Sex, Pclass, Title, and FamilySize** are strong predictors of survival.
- Models like **SVM** underperform on this dataset due to non-linear patterns and lack of probability tuning.
- **Boosting models** consistently outperform bagging and linear methods.
- **Gradient Boosting** and **CatBoost** offered the highest performance out of the box.
- Ensemble or Voting classifiers can be explored for better generalisation.

---
