# Day 4 – Linear Models & House Price Prediction

## Objective

Learn and implement fundamental regression algorithms used for predicting continuous numerical values. Understand regularization techniques, polynomial regression, and evaluation metrics through a real-world House Price Prediction project.

---

## Topics Covered

### 1. Linear Regression
- Introduction to supervised regression
- Linear relationship between features and target
- Model training using `fit()`
- Prediction using `predict()`

### 2. Ridge Regression
- L2 Regularization
- Prevents overfitting by shrinking coefficients
- Effect of the `alpha` hyperparameter

### 3. Lasso Regression
- L1 Regularization
- Automatic feature selection
- Coefficients can become zero

### 4. Polynomial Regression
- Polynomial feature generation
- Higher-degree relationships
- Uses Linear Regression after feature transformation
- Understanding overfitting with higher polynomial degrees

---

## Evaluation Metrics

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

---

## Dataset

House Price Prediction Dataset

Target Variable:
- `price`

Input Features:
- Area
- Bedrooms
- Bathrooms
- Stories
- Parking
- Main Road
- Guest Room
- Basement
- Hot Water Heating
- Air Conditioning
- Preferred Area
- Furnishing Status

---

## Project Workflow

1. Load the dataset
2. Explore the data
3. Data preprocessing
   - Boolean encoding
   - One-Hot Encoding
4. Train-Test Split
5. Feature Scaling using StandardScaler
6. Train Linear Regression model
7. Train Ridge Regression model
8. Train Lasso Regression model
9. Train Polynomial Regression model
10. Compare model performance
11. Interpret results

---

## Model Performance

| Model | MAE | RMSE | R² Score |
|------|------:|------:|------:|
| Linear Regression | 970043 | 1324507 | **0.6529** |
| Ridge Regression | 969858 | 1324703 | 0.6528 |
| Lasso Regression | 970043 | 1324507 | 0.6529 |
| Polynomial Regression | 1034749 | 1379016 | 0.6238 |

---

## Key Learnings

- Linear Regression predicts continuous numerical values.
- Cost Function measures model error.
- Gradient Descent finds optimal weights.
- Ridge Regression reduces overfitting by shrinking coefficients.
- Lasso Regression performs feature selection by reducing some coefficients to zero.
- Polynomial Regression creates polynomial features while still using Linear Regression.
- Increasing model complexity does not always improve performance.
- Proper preprocessing significantly affects model performance.

---

## Conclusion

Linear Regression achieved the best overall performance on this dataset with an R² score of approximately **65%**. Ridge and Lasso Regression produced nearly identical results, indicating that the dataset did not suffer from significant overfitting. Polynomial Regression (degree = 2) introduced additional complexity but resulted in lower performance, demonstrating that a more complex model does not necessarily produce better predictions.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## Files

```
Day-04/
│
├── notebooks/
│   └── house_price_prediction.ipynb
│
├── README.md
│
└── requirements.txt
```

---

## What I Learned

- Implemented four regression models from scratch using Scikit-learn.
- Understood the importance of regularization.
- Learned how to evaluate regression models using multiple metrics.
- Compared different regression algorithms on the same dataset.
- Built an end-to-end machine learning regression pipeline from preprocessing to model evaluation.



## Personal Reflection

This project helped me understand the complete regression workflow—from preprocessing and feature scaling to training multiple regression models and evaluating them. I also learned that more complex models do not always perform better, and choosing the right model depends on the data rather than the algorithm's complexity.