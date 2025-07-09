# 🩺 Diabetes Prediction using Linear Regression

This project predicts whether a patient has diabetes using **Linear Regression** based on the Pima Indians Diabetes dataset.

## 📌 Objective
Build a linear regression model that takes clinical data and predicts a binary diabetes outcome (0 or 1). Though linear regression is not typically used for classification, this project adapts it for binary prediction by rounding the predicted values.

---

## 📂 Dataset

The dataset contains 768 records with the following features:

- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age
- Outcome (target: 0 = non-diabetic, 1 = diabetic)

Source: [Pima Indians Diabetes Dataset (Kaggle)](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)

---

## ⚙️ Preprocessing Steps

1. Replace all zero values in key features (`Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, `BMI`) with the **mean** or **median** of the column.
2. Replace the **first row's Glucose** value with the **maximum Glucose** value in the dataset.
3. For all records with the **minimum age**, replace their Glucose values with the **minimum Glucose** value from the dataset.

---

## 🧠 Model

- Algorithm: **Linear Regression** (`sklearn.linear_model.LinearRegression`)
- Predictions were **rounded to 0 or 1** to simulate classification.
- Evaluated using standard classification metrics.

---

## 📊 Evaluation Metrics

- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**
- **Confusion Matrix**

These metrics are calculated using:
```python
from sklearn.metrics import accuracy_score, precision_score, recall_score, f1_score, confusion_matrix
