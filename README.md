# 🧠 Medical Insurance Charges Prediction

This project uses a dataset to predict medical insurance charges based on user attributes such as age, BMI, gender, smoking status, and region.

---

## 📌 Objectives

- Analyze features that affect medical insurance charges
- Select important features using:
  - Pearson correlation (for numeric variables)
  - Chi-Square test (for categorical variables)
- Train a linear regression model
- Evaluate model performance using R² score and MSE

---

## 🛠️ Technologies Used

| Tool/Library       | Purpose                            |
|--------------------|-------------------------------------|
| `pandas`           | Data manipulation                   |
| `numpy`            | Numerical operations                |
| `matplotlib.pyplot`| Data visualization                  |
| `seaborn`          | Correlation heatmap & plot styling  |
| `scikit-learn`     | Model training and evaluation       |
| `scipy.stats`      | Pearson and Chi-Square statistical tests |

---

## 📊 Data Analysis Steps

1. **Loading and Cleaning Data**
2. **Exploratory Data Analysis**
   - Correlation heatmaps
   - Feature distributions
3. **Feature Selection**
   - Pearson correlation for numeric features
   - Chi-square test for categorical features
4. **Final Feature Set**
   Selected features based on statistical tests:
   - `age`
   - `bmi`
   - `is_smoker`
   - `bmi_category_obese`
   - `region_southwest`
5. **Target Variable**
   - `charges`

---

## 🤖 Model Building

- Train-test split (80%-20%)
- Model: `LinearRegression()`
- Evaluation metrics:
  - R² Score
  - Mean Squared Error

```python
from sklearn.linear_model import LinearRegression
model = LinearRegression()
model.fit(X_train, y_train)
