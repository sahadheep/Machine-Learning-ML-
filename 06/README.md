# Day 6: Ensemble Models - Customer Churn Prediction

## Objective

The goal of this project is to predict customer churn using ensemble learning algorithms and compare their performance.

---

## Dataset

- Dataset: IBM Telco Customer Churn Dataset
- Rows: 7043
- Target Column: `Churn`

The dataset contains customer information such as:

- Gender
- Senior Citizen
- Tenure
- Internet Service
- Contract Type
- Payment Method
- Monthly Charges
- Total Charges

---

## Ensemble Models Implemented

1. Random Forest
2. AdaBoost
3. Gradient Boosting
4. XGBoost

---

## Project Workflow

### 1. Data Exploration

- Loaded the dataset using Pandas.
- Checked dataset shape and information.
- Identified categorical and numerical columns.
- Checked for missing values and duplicates.

### 2. Data Preprocessing

- Removed the `customerID` column.
- Converted `TotalCharges` from `object` to numeric.
- Handled missing values using the median.
- Encoded the target variable (`Churn`) using `LabelEncoder`.
- Applied one-hot encoding using `pd.get_dummies()`.
- Split the dataset into training and testing sets.

### 3. Model Training

The following ensemble models were trained:

- Random Forest Classifier
- AdaBoost Classifier
- Gradient Boosting Classifier
- XGBoost Classifier

### 4. Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC Score

---

## Evaluation Metrics

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|--------|--------|--------|--------|--------|--------|
| Random Forest | ... | ... | ... | ... | ... |
| AdaBoost | ... | ... | ... | ... | ... |
| Gradient Boosting | ... | ... | ... | ... | ... |
| XGBoost | ... | ... | ... | ... | ... |

---

## Key Concepts Learned

### Bagging

- Trains multiple models independently.
- Combines predictions using voting or averaging.
- Helps reduce variance.

Example:

- Random Forest

### Boosting

- Trains models sequentially.
- Each model learns from previous mistakes.
- Helps reduce bias.

Examples:

- AdaBoost
- Gradient Boosting
- XGBoost

---

## Model Comparison

### Random Forest

- Uses multiple decision trees.
- Applies bootstrap sampling and random feature selection.
- Reduces overfitting.

### AdaBoost

- Uses weak learners.
- Focuses on incorrectly classified samples.
- Combines predictions using weighted voting.

### Gradient Boosting

- Learns from residual errors.
- Builds trees sequentially.
- Improves predictions step by step.

### XGBoost

- Optimized version of Gradient Boosting.
- Includes regularization.
- Trains faster and handles missing values efficiently.

---

## Conclusion

- Implemented four ensemble learning algorithms.
- Compared bagging and boosting techniques.
- Understood how ensemble methods improve prediction performance.
- Learned the importance of hyperparameters such as:

  - `n_estimators`
  - `learning_rate`
  - `max_depth`

- Observed the strengths and weaknesses of different ensemble methods.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Jupyter Notebook

---

## Folder Structure

```text
Day-06-Ensemble-Models/

├── dataset/
│   └── Telco-Customer-Churn.csv
│
├── notebooks/
│   └── churn_prediction.ipynb
│
├── src/
│   ├── __init__.py
│   └── ensemble_models.py
│
└── README.md
```