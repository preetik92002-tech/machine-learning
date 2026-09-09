 # Machine Learning - Salary Prediction Project

Welcome to the **Salary Prediction** project repository! This project demonstrates how to build, evaluate, and interpret a Simple Linear Regression model to predict salaries based on years of experience.

---

## 🛠️ Step 1: Python Libraries & Imports Explained

Before building the model, we import essential libraries for data handling, visualization, and machine learning. Here is a line-by-line breakdown of why each import is required:

### 1. `import numpy as np`
* **Numerical Python (`numpy`):** The foundation for fast mathematical operations on multi-dimensional arrays.
* **Alias:** `np` *(Standard community convention)*
* **Why we need it:** Machine learning algorithms operate on numerical arrays and matrices rather than standard Python lists. `numpy` provides fast vectorized operations like sums, means, and array reshaping.

---

### 2. `import pandas as pd`
* **Pandas:** The primary Python library for working with structured tabular data (rows and columns).
* **Alias:** `pd` *(Standard community convention)*
* **Why we need it:** Datasets are represented in table formats (e.g., `Experience`, `Salary`). Pandas provides the `DataFrame` object to easily load, clean, inspect, and filter tabular data.

---

### 3. `import matplotlib.pyplot as plt`
* **Matplotlib (`pyplot`):** Python's core plotting library providing interactive MATLAB-like plotting functions.
* **Alias:** `plt`
* **Why we need it:** Used to visualize relationships in data, such as drawing scatter plots (*Salary vs. Experience*), plotting the regression line, and visualizing residuals.

---

### 4. `from sklearn.model_selection import train_test_split`
* **`scikit-learn` (`sklearn`):** The standard machine learning toolkit in Python.
* **`train_test_split`:** A utility function used to partition data into separate training and testing subsets.
* **Why we need it:** Evaluating a model on the same data used for training leads to overfitting (memorization). Splitting ensures an unbiased evaluation of how well the model generalizes to unseen data.

---

### 5. `from sklearn.linear_model import LinearRegression`
* **`LinearRegression`:** The core model class implementing Ordinary Least Squares (OLS) Linear Regression.
* **Why we need it:** Fits a straight line to the training data to learn the linear mathematical relationship:
  
  $$\text{Salary} = m \times \text{Experience} + c$$

---

### 6. `from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score`
* **Evaluation Metrics:** Three key metrics used to evaluate model accuracy:
  * **Mean Absolute Error (MAE):** Measures the average magnitude of absolute errors in predictions. Easy to interpret directly in target units (e.g., *"off by ₹0.6 LPA on average"*).
  * **Mean Squared Error (MSE):** Squares the prediction errors before averaging. Heavily penalizes larger errors. (Taking the square root gives **RMSE**).
  * **$R^2$ Score (Coefficient of Determination):** Measures the proportion of variance in the target variable explained by the feature. Scale ranges from $0$ to $1$ ($1.0$ indicating a perfect fit).

---

## 🔄 Project Flow & Lifecycle

The standard execution lifecycle followed in this project:

```text
[ Load Data ] ──> [ Data Exploration ] ──> [ Train/Test Split ] ──> [ Fit Linear Regression ] ──> [ Predict & Evaluate ]
   (pandas)            (matplotlib)            (train_test_split)           (LinearRegression)           (sklearn.metrics)
