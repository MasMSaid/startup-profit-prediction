# Startup Profit Prediction (Supervised Regression)

## 📌 Project Overview
This project predicts company profit based on R&D spend, marketing spend, administration costs, and geographic location using supervised regression techniques. The goal is to identify key drivers of profitability and compare the performance of different regression models on a small, structured dataset.

⚠️ This project is for educational purposes and does not represent production-level deployment.

## 📂 Dataset
- **Source:** 50_Startups.csv  
- **Observations:** 50  
- **Features:**
  - R&D Spend  
  - Administration  
  - Marketing Spend  
  - State (categorical)  
  - Profit (target variable)  

## ⚙️ Methods
- Data preprocessing and one-hot encoding
- Exploratory Data Analysis (EDA)
- Multiple regression models
- Hyperparameter tuning
- Model evaluation and comparison

## 📊 Models Implemented
- Decision Tree Regression  
- Polynomial Regression  
- Random Forest Regression  
- Support Vector Regression (SVR)  

## 🏆 Results & Insights

### Final Model Comparison

| Model                      | MAE      | MSE           | RMSE     | R² Score |
|---------------------------|----------|---------------|----------|----------|
| Decision Tree Regression  | 13,406.59 | 2.78 × 10⁸ | 16,688.26 | 0.8415 |
| Polynomial Regression     | **7,109.74** | **8.17 × 10⁷** | **9,036.48** | **0.9535** |
| Random Forest Regression  | 10,098.17 | 2.01 × 10⁸ | 14,166.05 | 0.8858 |
| Support Vector Regression | 9,004.44 | 1.33 × 10⁸ | 11,547.94 | 0.9241 |

### Key Observations
- **Polynomial Regression** achieved the best overall performance, with the **lowest MAE (7,109)** and **highest R² (0.9535)**. It captures strong linear relationships—particularly **R&D Spend**—while modeling mild non-linearity and maintaining low variance.
- **Support Vector Regression (SVR)** also performed well (**MAE = 9,004, R² = 0.9241**) due to its smooth function approximation and built-in regularisation.
- **Random Forest** and **Decision Tree Regression** underperformed relative to Polynomial Regression and SVR, likely due to higher sensitivity to individual data points and increased overfitting risk on a small dataset.
- **R&D Spend** consistently emerged as the most influential predictor of company profit across all models.
- Given the limited dataset size, **MAE was prioritised over R²** as it provides a more intuitive measure of average prediction error in monetary terms.

## 🛠️ Tools
- Python  
- Scikit-learn  
- Pandas, NumPy  
- Matplotlib, Seaborn  

## 🚀 How to Run
```bash
pip install -r requirements.txt

jupyter notebook Supervised_Machine_Learning_Regression.ipynb
