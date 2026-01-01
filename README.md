# 💰 Startup Profit Prediction (Supervised Regression)

**Tagline:** Predict startup profits and identify key drivers of profitability using regression models.

---

## 📌 Project Overview

This project uses **supervised regression** to predict company profit based on R&D spend, marketing spend, administration costs, and geographic location.  

The goal is to identify the most influential factors driving profitability and compare the performance of multiple regression models on a small, structured dataset.

> ⚠️ Note: This project is for **educational purposes** and does not represent production-level deployment.

---

## 📂 Dataset

- **Source:** `50_Startups.csv`  
- **Observations:** 50  
- **Features:**  
  - `R&D Spend` – Investment in research and development  
  - `Administration` – Administration costs  
  - `Marketing Spend` – Marketing expenditure  
  - `State` – Company location (categorical)  
  - `Profit` – Target variable  

---

## ⚙️ Methods & Workflow

1. **Data preprocessing:** Handle categorical variables via one-hot encoding, normalize if needed  
2. **Exploratory Data Analysis (EDA):** Understand distributions, relationships, and feature importance  
3. **Regression Models Implemented:**  
   - Decision Tree Regression  
   - Polynomial Regression  
   - Random Forest Regression  
   - Support Vector Regression (SVR)  
4. **Hyperparameter tuning** for optimal performance  
5. **Model evaluation:** Compare models using MAE, MSE, RMSE, and R²  
6. **Insights & key drivers:** Identify the most impactful features for profit prediction  

---

## 🏆 Results & Model Comparison

| Model                     | MAE        | MSE         | RMSE      | R² Score |
|---------------------------|------------|------------|-----------|----------|
| Decision Tree Regression   | 13,406.59 | 2.78×10⁸   | 16,688.26 | 0.8415   |
| Polynomial Regression      | 7,109.74  | 8.17×10⁷   | 9,036.48  | 0.9535   |
| Random Forest Regression   | 10,098.17 | 2.01×10⁸   | 14,166.05 | 0.8858   |
| Support Vector Regression  | 9,004.44  | 1.33×10⁸   | 11,547.94 | 0.9241   |

**Key Insights:**

- **Polynomial Regression** performed best, with the **lowest MAE** and **highest R²**, capturing both linear and mild non-linear relationships.  
- **Support Vector Regression (SVR)** also delivered strong results due to smooth function approximation and regularization.  
- Decision Tree and Random Forest were more sensitive to individual data points, which led to reduced performance on this small dataset.  
- **R&D Spend** emerged as the **most influential predictor** of profit.  
- MAE was prioritized over R² as it provides an intuitive measure of **average prediction error in monetary terms**.

---

## 🛠️ Tools & Libraries

- **Programming Language:** Python  
- **Libraries:** scikit-learn, Pandas, NumPy, Matplotlib, Seaborn  

---

## ✅ Summary

This project demonstrates how supervised regression can be applied to predict startup profits and identify key drivers of profitability.  
Polynomial Regression proved to be the most accurate model, highlighting the importance of R&D investment in driving profit.  

---

## 🚀 How to Run

1. Clone the repository  
2. Install dependencies:  
```bash
pip install -r requirements.txt
jupyter notebook startup_profit_regression.ipynb

