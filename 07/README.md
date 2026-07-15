# Day 7: SVM, Naive Bayes, Hyperparameter Tuning and Spam Detection

## Overview

On Day 7, I learned advanced machine learning concepts for classification problems, including Support Vector Machines (SVM), Naive Bayes, Cross Validation, GridSearchCV, and RandomizedSearchCV.

To apply these concepts, I built an SMS Spam Detection system that classifies messages as either spam or ham.

---

## Topics Covered

### Support Vector Machine (SVM)

* Hyperplane and decision boundary
* Margin and support vectors
* Hard margin vs soft margin
* Kernel trick
* Linear kernel
* RBF kernel
* Effect of the C parameter
* Overfitting and underfitting

### Naive Bayes

* Bayes theorem intuition
* Multinomial Naive Bayes
* Probabilistic classification
* Text classification using word frequencies

### Text Vectorization

* CountVectorizer
* TF-IDF Vectorizer
* Sparse matrix representation
* Vocabulary generation

### Model Evaluation

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix
* Cross Validation

### Hyperparameter Tuning

* GridSearchCV
* RandomizedSearchCV
* Parameter tuning for SVM

---

## Mini Project: SMS Spam Detection

### Objective

Build a machine learning model that predicts whether an SMS message is spam or ham.

---

## Dataset

Dataset: SMS Spam Collection Dataset

Columns:

* `label`

  * ham
  * spam

* `message`

  * SMS text

---

## Project Workflow

### 1. Data Loading

* Loaded the dataset using Pandas.
* Used custom separators and column names.

### 2. Data Cleaning

* Checked for missing values.
* Removed duplicate messages.

### 3. Exploratory Data Analysis

* Analyzed class distribution.
* Observed that the dataset is imbalanced.

### 4. Text Preprocessing

* Converted text into numerical features using:

  * CountVectorizer
  * TF-IDF Vectorizer

### 5. Train-Test Split

* Used:

```python
train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42,
    stratify=y
)
```

### 6. Models Used

#### Multinomial Naive Bayes

* Suitable for text classification.
* Works on word frequencies.

#### Support Vector Machine (SVM)

* Used SVC from Scikit-Learn.
* Compared default and tuned models.

---

## Model Performance

### Multinomial Naive Bayes

| Metric    | Score   |
| --------- | ------- |
| Accuracy  | 95.26%  |
| Precision | 100.00% |
| Recall    | 62.60%  |
| F1-Score  | 76.99%  |

Confusion Matrix:

```text
[[903   0]
 [ 49  82]]
```

---

### Support Vector Machine (SVM)

| Metric    | Score  |
| --------- | ------ |
| Accuracy  | 97.29% |
| Precision | 97.25% |
| Recall    | 80.92% |
| F1-Score  | 88.33% |

---

## Cross Validation Results

### Naive Bayes

```text
[0.83928571, 0.72815534, 0.79816514, 0.78139535, 0.76190476]
```

Average F1-Score:

```text
0.7818
```

### SVM

```text
[0.90000000, 0.88034188, 0.88607595, 0.87553648, 0.86808511]
```

Average F1-Score:

```text
0.8820
```

---

## Hyperparameter Tuning

### GridSearchCV

Best Parameters:

```python
{
    'C': 1,
    'gamma': 'scale',
    'kernel': 'linear'
}
```

Best F1-Score:

```text
0.9212
```

---

### RandomizedSearchCV

Best Parameters:

```python
{
    'kernel': 'linear',
    'gamma': 'auto',
    'C': 100
}
```

Best F1-Score:

```text
0.9211
```

---

## Final Conclusion

* Naive Bayes performed well and was computationally efficient.
* SVM achieved better precision, recall, and F1-score.
* Hyperparameter tuning further improved SVM performance.
* The tuned SVM model was selected as the final model for spam detection.

---

## Libraries Used

* NumPy
* Pandas
* Scikit-Learn
* Matplotlib
* Seaborn

---

## Key Learnings

* SVM works effectively on high-dimensional text data.
* Naive Bayes is a strong baseline for NLP tasks.
* TF-IDF improves text representation.
* Cross Validation provides reliable model evaluation.
* GridSearchCV and RandomizedSearchCV help optimize model performance.
