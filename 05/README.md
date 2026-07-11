# Day 5: Classification Algorithms

## Objective

The goal of Day 5 is to understand and implement fundamental classification algorithms and evaluate their performance on real-world datasets.

---

# Algorithms Covered

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree

---

# Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

---

# Concepts Learned

## Logistic Regression

- Difference between regression and classification.
- Sigmoid function.
- Log-odds and probability.
- Decision threshold.
- Binary classification.

## K-Nearest Neighbors (KNN)

- Distance-based learning.
- Euclidean distance.
- Choosing the value of `K`.
- Effect of feature scaling.
- Underfitting and overfitting.

## Decision Tree

- Tree structure:
  - Root node
  - Internal nodes
  - Leaf nodes
- Splitting criteria:
  - Gini Index
  - Entropy
- Hyperparameters:
  - `max_depth`
  - `min_samples_split`
  - `min_samples_leaf`
- Overfitting and pruning.

## Model Evaluation

- Confusion Matrix
- True Positive (TP)
- True Negative (TN)
- False Positive (FP)
- False Negative (FN)
- Accuracy
- Precision
- Recall
- F1-Score
- ROC Curve
- ROC-AUC

---

# Project 1: Titanic Survival Prediction

## Objective

Predict whether a passenger survived the Titanic disaster.

### Target Variable

- `1` → Survived
- `0` → Did not survive

---

## Data Preprocessing

### Removed Columns

- PassengerId
- Name
- Ticket
- Cabin

### Missing Value Handling

- Filled missing values in `Age` using the median.
- Filled missing values in `Embarked` using the mode.

### Feature Engineering

- Applied One-Hot Encoding to:
  - Sex
  - Embarked

### Feature Scaling

Used `StandardScaler` for:

- Logistic Regression
- KNN

Decision Tree was trained using unscaled data.

---

## Titanic Results

| Metric | Logistic Regression | KNN | Decision Tree |
|----------|----------|----------|----------|
| Accuracy | 0.8101 | 0.8045 | 0.7989 |
| Precision | 0.7857 | 0.7826 | 0.8276 |
| Recall | 0.7432 | 0.7297 | 0.6486 |
| F1-Score | 0.7639 | 0.7552 | 0.7273 |
| ROC-AUC | 0.8820 | 0.8535 | Add your value |

---

## Observations

- Logistic Regression achieved the best overall performance.
- KNN performed similarly but slightly worse.
- Decision Tree produced the highest precision.
- Decision Tree had lower recall, missing more passengers who survived.

---

# Project 2: Breast Cancer Classification

## Objective

Classify tumors as benign or malignant.

### Target Variable

- `0` → Malignant
- `1` → Benign

---

## Dataset Characteristics

- 569 samples.
- 30 numerical features.
- No missing values.
- No categorical columns.
- Slightly imbalanced dataset.

---

## Data Preprocessing

- No missing value handling required.
- No categorical encoding required.
- Applied `StandardScaler` before training Logistic Regression and KNN.
- Decision Tree was trained on unscaled data.

---

## Breast Cancer Results

| Metric | Logistic Regression | KNN | Decision Tree |
|----------|----------|----------|----------|
| Accuracy | 0.9737 | 0.9474 | 0.9386 |
| Precision | 0.9722 | 0.9577 | 0.9444 |
| Recall | 0.9859 | 0.9577 | 0.9577 |
| F1-Score | 0.9790 | 0.9577 | 0.9510 |
| ROC-AUC | 0.9974 | 0.9820 | 0.9291 |

---

## Observations

- Logistic Regression achieved the highest performance across all metrics.
- KNN performed well after feature scaling.
- Decision Tree performed reasonably well but had lower ROC-AUC.
- Recall is particularly important in medical datasets because false negatives can be dangerous.

---

# Comparison Between the Datasets

| Feature | Titanic | Breast Cancer |
|----------|----------|----------|
| Problem Type | Binary Classification | Binary Classification |
| Missing Values | Yes | No |
| Categorical Features | Yes | No |
| Scaling Required | Yes | Yes |
| Class Imbalance | Moderate | Moderate |
| Domain | Survival Prediction | Medical Diagnosis |

---

# Key Learnings

- Understood the difference between regression and classification.
- Learned how Logistic Regression converts scores into probabilities.
- Explored distance-based classification using KNN.
- Studied tree-based learning using Decision Trees.
- Learned why feature scaling is important.
- Understood overfitting and hyperparameter tuning.
- Learned how to interpret classification metrics.
- Compared models on two different datasets.

---

# Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

---

# Conclusion

Two classification projects were completed:

1. Titanic Survival Prediction.
2. Breast Cancer Classification.

Among the three algorithms, Logistic Regression achieved the best overall performance on both datasets. These projects provided practical experience in preprocessing, model training, evaluation, and comparison of classification algorithms.
