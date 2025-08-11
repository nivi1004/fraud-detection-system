# fraud-detection-system
The Fraud Detection System uses machine learning to identify fraudulent financial transactions. It includes data cleaning, outlier handling with IQR, and EDA for insights. A Random Forest Classifier delivers high recall and accuracy, making it suitable for secure, reliable fraud detection in real-world scenarios.
# 💳 Fraud Detection System

## 📌 Overview
This project implements a **machine learning–based fraud detection system** using financial transaction data.  
The goal is to accurately identify fraudulent transactions while minimizing false negatives, ensuring maximum security in financial systems.

---

## 📂 Dataset
- **Source:** `Fraud.csv`
- Contains transaction details such as:
  - `amount`
  - `oldbalanceOrg`, `newbalanceOrig`
  - `oldbalanceDest`, `newbalanceDest`
  - Other transaction metadata
- **Missing Values:** None found in the dataset.

---

## 🛠 Data Preprocessing
1. **Outlier Detection & Handling**
   - Used **IQR (Interquartile Range)** method.
   - Columns capped:
     - `amount`
     - `oldbalanceOrg`
     - `newbalanceOrig`
     - `oldbalanceDest`
     - `newbalanceDest`
   - Formula:
     ```
     Lower Bound = Q1 − 1.5 × IQR
     Upper Bound = Q3 + 1.5 × IQR
     ```
   - Reduced impact of extreme values to improve model stability.

2. **Feature Engineering**
   - Removed original columns after capping.
   - Created clean, capped dataset for training.

---

## 📊 Exploratory Data Analysis (EDA)
- **Boxplots** for all numerical features to visualize outliers.
- Distribution checks for transaction amounts and balances.

---

## 🤖 Model Building
- **Algorithm:** Random Forest Classifier
- **Reason for Selection:** Handles high-dimensional data well, robust to outliers, and suitable for imbalanced datasets.

---

## 📈 Model Evaluation
- Metrics used: **Accuracy**, **Precision**, **Recall**, **F1-score**
- Emphasis on **Recall** to catch as many fraudulent transactions as possible.

---

## 🚀 Key Takeaways
- Effective preprocessing (especially outlier capping) significantly improved model stability.
- Random Forest provided high recall, making it suitable for real-world fraud detection scenarios.

