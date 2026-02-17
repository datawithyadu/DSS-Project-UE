# 🏠 House Price Prediction using Random Forest & XGBoost

## 📌 Project Overview

This project develops an end-to-end supervised machine learning regression model to predict residential house prices using the Ames Housing dataset (Kaggle Competition).

The objective is to build a robust predictive model capable of estimating **SalePrice** based on 79 structured property features such as construction quality, living area, basement size, garage capacity, and neighborhood.

Unlike a basic modeling approach, this project emphasizes:

- Structured preprocessing pipeline  
- Feature relevance analysis using Mutual Information  
- Cross-model feature importance comparison  
- Dimensionality reduction via zero-importance filtering  
- Hyperparameter optimization using GridSearchCV  

---

## 📊 Dataset

- Source: [Ames Housing Dataset - Kaggle](https://www.kaggle.com/competitions/home-data-for-ml-course/overview)
- Target Variable: `SalePrice`
- 79 explanatory variables

---

## 🔍 Machine Learning Pipeline

### 1️⃣ Data Preprocessing
- Removed ID column
- Separated numerical and categorical features
- Missing value treatment:
  - Numerical → Mean Imputation
  - Categorical → Most Frequent Imputation
- Applied OneHotEncoding using ColumnTransformer
- Verified absence of null values

---

### 2️⃣ Feature Relevance Analysis

- Applied **Mutual Information Regression**
- Extracted feature importance from:
  - Random Forest
  - XGBoost
- Removed zero-importance features
- Reduced dimensionality without degrading performance

---

### 3️⃣ Model Comparison

#### 🔹 Random Forest Regressor
- n_estimators = 200
- Validation RMSE ≈ 33,107

#### 🔹 XGBoost (Initial Model)
- Default configuration
- Validation RMSE ≈ 32,003
- Training RMSE ≈ 1,400 (Overfitting observed)

---

### 4️⃣ Hyperparameter Tuning

Used **GridSearchCV (3-fold cross-validation)**

Parameters tuned:
- n_estimators
- max_depth
- learning_rate

Scoring metric:
- Negative Mean Squared Error

---

## 📈 Final Performance

Final Optimized XGBoost Model:

**RMSE ≈ 27,839**

Performance improved through:
- Feature elimination
- Controlled model complexity
- Cross-validated hyperparameter tuning

---

## 🛠 Tech Stack

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- XGBoost  

---

## 📂 Source Notebook

[Open Notebook](house_price_prediction_xg.ipynb)

---

## 🚀 How to Run

1. Clone the repository  
   ```
   git clone https://github.com/yourusername/your-repo-name.git
   ```

2. Install dependencies  
   ```
   pip install -r requirements.txt
   ```

3. Run the notebook  
   ```
   jupyter notebook
   ```

---

## 📌 Author

**Yadukrishnan**  
Aspiring Data Scientist | Machine Learning & AI Enthusiast
