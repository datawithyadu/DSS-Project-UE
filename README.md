🏠 House Price Prediction using Random Forest & XGBoost
📌 Project Overview

This project develops a supervised machine learning regression model to predict residential house prices using the Ames Housing dataset.

Unlike a basic modeling approach, this project emphasizes:

Structured preprocessing pipeline

Feature relevance analysis using Mutual Information

Cross-model feature importance comparison

Dimensionality reduction via zero-importance filtering

Hyperparameter optimization using GridSearchCV

Source Notebook: 

house_price_prediction_xg (6)

📊 Dataset

Dataset: Ames Housing (Kaggle Competition)

79 explanatory variables

Target variable: SalePrice

The dataset includes property attributes such as:

Construction quality

Living area

Basement area

Garage capacity

Neighborhood

Sale conditions

🧠 Machine Learning Pipeline
1️⃣ Data Preprocessing

Dropped ID column

Separated numerical & categorical features

Imputed:

Numerical → Mean strategy

Categorical → Most frequent strategy

Applied OneHotEncoding via ColumnTransformer

2️⃣ Feature Relevance Analysis

To reduce noise and improve model efficiency:

Applied Mutual Information Regression

Extracted:

Random Forest feature importance

XGBoost feature importance

Removed:

Features with XGBoost importance = 0

Features with RF importance = 0

Combined redundant feature lists

This reduced dimensionality while maintaining predictive power.

3️⃣ Model Comparison
🔹 Random Forest Regressor

n_estimators = 200

RMSE ≈ 33,107

🔹 XGBoost (Initial)

Default parameters

Validation RMSE ≈ 32,003

Training RMSE ≈ 1,400
→ Identified overfitting

4️⃣ Feature Filtering & Retraining

After removing zero-contributing features:

Random Forest RMSE ≈ 33,238

XGBoost improved performance

5️⃣ Hyperparameter Tuning

Used GridSearchCV:

Parameters tuned:

n_estimators

max_depth

learning_rate

Cross-validation: 3-fold
Scoring: Negative MSE

Final optimized model selected via best RMSE.

📈 Final Performance

Final optimized XGBoost model achieved:

RMSE ≈ 27,839

Improvement achieved through:

Feature elimination

Controlled model complexity

Cross-validated tuning

🏆 Key Technical Takeaways

Feature selection via model-based importance can reduce dimensionality without degrading performance.

XGBoost outperforms Random Forest for structured tabular regression tasks.

Hyperparameter tuning significantly reduces overfitting.

Proper preprocessing is critical in tabular ML pipelines.

🛠 Tech Stack

Python

Pandas

NumPy

Matplotlib / Seaborn

Scikit-learn

XGBoost

🔥 Now — Strategic LinkedIn Positioning

You SHOULD:

✅ Add under “Projects”
✅ Create a LinkedIn post
❌ Do NOT add as fake "Machine Learning Engineer Experience"

You're still transitioning — authenticity builds stronger trust.

🚀 LinkedIn Post Template (Authority Style)

You can post something like this:

📊 From Data to Decisions: Predicting House Prices with Machine Learning

I recently built an end-to-end regression pipeline to predict residential house prices using the Ames Housing dataset.

Instead of stopping at model training, I:

• Performed feature relevance analysis using Mutual Information
• Compared Random Forest and XGBoost
• Eliminated zero-contributing features
• Applied GridSearchCV for hyperparameter optimization
• Reduced RMSE to 27,839

This project strengthened my understanding of:

✔ Model interpretability
✔ Overfitting detection
✔ Feature importance comparison
✔ Performance optimization in structured datasets

GitHub link: [your link]

Excited to keep building in ML & AI 🚀

