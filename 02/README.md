# Day 2 - Exploratory Data Analysis (EDA) & Visualization

## Objective

The goal of this project is to perform Exploratory Data Analysis (EDA) on the Titanic dataset using Pandas, Matplotlib, and Seaborn. The notebook focuses on understanding the dataset through statistical summaries and visualizations before applying any machine learning algorithms.

---

## Dataset

- Titanic Dataset
- Source: Kaggle / Seaborn

---

## Topics Covered

### Data Exploration

- Dataset overview
- Shape of the dataset
- Data types
- Statistical summary
- Missing value analysis

### Univariate Analysis

- Histogram
- Boxplot
- Count Plot

### Bivariate Analysis

- Survival vs Gender
- Survival vs Passenger Class
- Scatter Plot (Age vs Fare)

### Correlation Analysis

- Correlation Matrix
- Heatmap

### Optional Visualization

- Pair Plot

---

## Libraries Used

- Pandas
- NumPy
- Matplotlib
- Seaborn

---

## Key Insights

- Most passengers were between 20 and 30 years old.
- Fare distribution is highly right-skewed.
- Several high-fare outliers are valid observations.
- Female passengers had a much higher survival rate than male passengers.
- First-class passengers had the highest survival rate.
- Passenger Class and Fare show a moderate negative correlation.
- Age has very little correlation with the other numerical features.

---

## Learning Outcomes

After completing this notebook, I learned how to:

- Perform Exploratory Data Analysis (EDA)
- Identify missing values
- Analyze numerical and categorical features
- Detect outliers using boxplots
- Visualize data using Matplotlib and Seaborn
- Interpret histograms, scatter plots, and count plots
- Understand feature relationships using correlation and heatmaps
- Extract meaningful insights from data before building machine learning models

---

## Files

```
Day2_EDA/
│
├── Titanic_EDA.ipynb
├── README.md
└── titanic.csv
```

---

## Next Step

Day 3 - Data Preprocessing

- Handling Missing Values
- Encoding Categorical Variables
- Feature Scaling
- Train-Test Split