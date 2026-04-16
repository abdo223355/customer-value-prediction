# 🍫 Customer Value Prediction (Future-Based ML Project)

## 📌 Overview

This project focuses on predicting whether a customer will become a **high-value customer in the future** using historical transaction data from a retail chocolate sales dataset.

Unlike traditional approaches, this project avoids data leakage by using a **time-based split**, ensuring that only past data is used to predict future behavior.

---

## 🎯 Problem Statement

Predict if a customer will be a **high-value customer in the future** based on their past purchasing behavior.

---

## 🧠 Approach

### 1. Time-Based Splitting

* Past data → Feature Engineering
* Future data → Label Creation

This ensures a realistic machine learning setup and prevents leakage.

---

### 2. Feature Engineering

Customer-level features were created using past data only:

* **Recency** → Days since last purchase
* **Frequency** → Number of orders
* **Monetary (past)** → Total past spending
* **Avg Order Value**
* **Avg Quantity per Order**
* **Avg Discount Ratio**
* **Total Quantity**

---

### 3. Label Creation (Future-Based)

* Calculated total revenue per customer from future data
* Defined **high-value customers** as top 25%

---

### 4. Data Preprocessing

* Removed leakage features
* Dropped identifiers (e.g., customer_id)
* Applied stratified splitting

---

## ⚙️ Models Used

* Logistic Regression (with StandardScaler)
* Random Forest Classifier

---

## 📊 Results

| Metric                 | Value |
| ---------------------- | ----- |
| Accuracy               | 91%   |
| Recall (High Value)    | 84%   |
| Precision (High Value) | 80%   |
| F1-score               | 82%   |

---

## 🔥 Key Insights

* Behavioral features (Recency, Frequency) are strong predictors
* Removing leakage reduced accuracy but improved realism
* The model now predicts **future behavior**, not current value

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn

---

## 🚀 Future Improvements

* Hyperparameter tuning
* Feature importance visualization
* SHAP for model explainability
* Deployment (API or dashboard)

---

## 📂 Project Structure

```text
├── data/
├── notebook.ipynb
├── README.md
├── requirements.txt
```

---

## 💡 Conclusion

This project demonstrates how to build a **realistic machine learning pipeline** by:

* Avoiding data leakage
* Using time-based validation
* Focusing on meaningful business predictions

---

## 🤝 Author

Abdelrhman
