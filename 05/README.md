# Day 5: Classification - Titanic Survival Prediction

## Objective

The objective of this project is to predict whether a passenger survived the Titanic disaster using classification algorithms. The project covers data preprocessing, model training, evaluation, and comparison of different classification models.

---

## Dataset

The Titanic dataset contains passenger information such as:

- Passenger class
- Sex
- Age
- Number of siblings/spouses aboard
- Number of parents/children aboard
- Fare
- Embarkation port
- Survival status

### Target Variable

- `Survived = 1` → Passenger survived
- `Survived = 0` → Passenger did not survive

---

## Topics Covered

### Classification Algorithms

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree

### Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

---

## Project Workflow

1. Load the dataset.
2. Explore the dataset.
3. Handle missing values.
4. Drop unnecessary columns.
5. Encode categorical features.
6. Split the dataset into training and testing sets.
7. Scale the features where required.
8. Train classification models.
9. Evaluate model performance.
10. Compare the results.

---

## Data Preprocessing

### Removed Columns

- `PassengerId`
- `Name`
- `Ticket`
- `Cabin`

### Missing Value Handling

- Filled missing values in `Age` using the median.
- Filled missing values in `Embarked` using the mode.

### Encoding

Applied One-Hot Encoding on:

- `Sex`
- `Embarked`

### Feature Scaling

Used `StandardScaler` for:

- Logistic Regression
- KNN

Decision Tree was trained on unscaled data.

---

## Models Used

### Logistic Regression

A linear classification algorithm that predicts probabilities using the sigmoid function.

### K-Nearest Neighbors (KNN)

A distance-based algorithm that classifies samples based on the majority vote of the nearest neighbors.

### Decision Tree

A tree-based algorithm that learns decision rules by splitting the data into increasingly pure groups.

---

## Evaluation Results

| Metric | Logistic Regression | KNN | Decision Tree |
|----------|----------|----------|----------|
| Accuracy | 0.8101 | 0.8045 | 0.7989 |
| Precision | 0.7857 | 0.7826 | 0.8276 |
| Recall | 0.7432 | 0.7297 | 0.6486 |
| F1-Score | 0.7639 | 0.7552 | 0.7273 |
| ROC-AUC | 0.8820 | 0.8535 | Add your value |

---

## Observations

- Logistic Regression achieved the highest accuracy and ROC-AUC score.
- KNN performed similarly but slightly worse.
- Decision Tree achieved the highest precision.
- Decision Tree had lower recall, meaning it missed more passengers who survived.
- Logistic Regression provided the best overall balance among all metrics.

---

## Key Learnings

- Difference between regression and classification.
- Working of Logistic Regression, KNN, and Decision Trees.
- Importance of feature scaling in distance-based algorithms.
- Understanding the Confusion Matrix.
- Calculation and interpretation of Accuracy, Precision, Recall, F1-Score, and ROC-AUC.
- How hyperparameters affect model performance.

---

## Future Improvements

- Tune hyperparameters for KNN and Decision Tree.
- Perform feature engineering.
- Use ensemble methods such as Random Forest and XGBoost.
- Compare performance using cross-validation.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## Conclusion

Among the three models, Logistic Regression performed the best on the Titanic dataset by achieving the highest accuracy, F1-score, and ROC-AUC score.

This project provided hands-on experience with classification algorithms and evaluation metrics.