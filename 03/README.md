# Day 3 – Data Preprocessing

## Objective

The goal of this project is to preprocess raw data and prepare it for machine learning models. The preprocessing steps include encoding categorical variables, scaling numerical features, splitting the dataset into training and testing sets, and creating a reusable preprocessing pipeline.

---

## Dataset

**Dataset:** Housing Prices Dataset

**Target Variable:** `Price`

---

## Steps Performed

### 1. Feature and Target Separation

* Separated the dataset into:

  * **Features (X)** – Input variables
  * **Target (y)** – Price

---

### 2. Categorical Feature Encoding

* Identified categorical columns automatically using pandas.
* Applied **One-Hot Encoding** using `pd.get_dummies()`.
* Used `drop_first=True` to avoid the dummy variable trap.

---

### 3. Numerical Feature Analysis

* Identified numerical columns.
* Examined the range and distribution of numerical features.
* Observed that features such as **Area** had much larger values than other numerical features, making scaling necessary.

---

### 4. Train-Test Split

* Split the dataset into:

  * **80% Training Data**
  * **20% Testing Data**
* Used `random_state=42` to ensure reproducible results.

---

### 5. Feature Scaling

* Applied **StandardScaler** to numerical features.
* Used:

  * `fit_transform()` on the training data.
  * `transform()` on the testing data.
* This prevents **data leakage** because the scaler learns statistics only from the training dataset.

---

### 6. Reusable Preprocessing Pipeline

Created a reusable preprocessing function that performs:

* One-Hot Encoding
* Train-Test Split
* Numerical Feature Scaling

The function returns:

* X_train
* X_test
* y_train
* y_test

---

## Key Concepts Learned

* Difference between **Label Encoding** and **One-Hot Encoding**
* When to use **StandardScaler** and **MinMaxScaler**
* Importance of **Train/Test Split**
* Understanding **fit()**, **transform()**, and **fit_transform()**
* Preventing **Data Leakage**
* Building a reusable preprocessing workflow

---

## Libraries Used

* pandas
* scikit-learn

---

## Outcome

Successfully prepared the dataset for machine learning by encoding categorical features, scaling numerical features, splitting the dataset correctly, and implementing a reusable preprocessing pipeline following standard machine learning practices.
