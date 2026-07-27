# 🚗 Used Car Price Prediction using Machine Learning

## 📌 Business Objective

The objective of this project is to develop a machine learning model that predicts the selling price of used cars based on their specifications. Accurate price prediction helps buyers, sellers, and dealerships estimate fair market values and make informed decisions.

---

# 📂 Dataset Overview

- **Dataset:** CarDekho Used Car Dataset
- **Source:** https://www.kaggle.com/datasets/manishkr1754/cardekho-used-car-data
- **Shape:** 15,411 rows × 14 columns
- **Target Variable:** `selling_price`

---

# 🎯 Features and Target Variable

### Numerical Features
- vehicle_age
- km_driven
- mileage
- engine
- max_power
- seats

### Categorical Features
- brand
- model
- seller_type
- fuel_type
- transmission_type

### Target Variable
- selling_price

---

# 🛠 Data Preprocessing

The following preprocessing steps were performed:

- Removed missing values and duplicate records.
- Removed one unrealistic record with **3.8 million km** driven, treating it as a data entry error.
- Removed vehicles priced above **₹1 Crore** to reduce the influence of extreme luxury car outliers.
- Encoded categorical features using **Label Encoding**.
- Applied **StandardScaler** for Linear Regression.
- Split the dataset into training and testing sets (80:20).

---

# ⚙ Feature Engineering

The following features were created to improve prediction performance:

- **km_per_year** – Average kilometers driven per year.
- **power_per_cc** – Ratio of engine power to engine capacity.
- **is_premium** – Indicates whether the vehicle belongs to a premium brand.

---

# 🤖 Regression Models Implemented

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

---

# 📊 Performance Comparison

| Model | MAE | RMSE | R² Score |
|-------|---------:|---------:|---------:|
| Linear Regression | 223,897 | 427,158 | 0.704 |
| Decision Tree Regressor | 114,588 | 245,153 | 0.902 |
| **Random Forest Regressor** | **91,496** | **183,478** | **0.945** |

---

# 🏆 Best Performing Model

The **Random Forest Regressor** achieved the best overall performance.

### Justification

- **Highest R² Score:** **0.945**
- **Lowest MAE:** **91,496**
- **Lowest RMSE:** **183,478**
- Captured complex non-linear relationships between vehicle features.
- Combined multiple decision trees to improve prediction accuracy and reduce overfitting.

---

# 📌 Key Observations

- Vehicle age and kilometers driven significantly influence selling price.
- Premium brands generally have higher resale values.
- Feature engineering improved model performance.
- Removing unrealistic records and extreme luxury car outliers resulted in more stable predictions.
- Random Forest achieved the highest prediction accuracy with the lowest prediction errors among all models.

---

# 🚀 Future Improvements

- Perform hyperparameter tuning using GridSearchCV or RandomizedSearchCV.
- Experiment with advanced boosting algorithms such as XGBoost, LightGBM, and CatBoost.
- Apply K-Fold Cross Validation for more reliable model evaluation.
- Create additional domain-specific features to further improve prediction accuracy.

---

# 📜 Conclusion

This project successfully developed and compared three regression models for predicting used car prices. After preprocessing, feature engineering, and handling outliers, the **Random Forest Regressor** achieved the best performance with an **R² Score of 0.945**, making it the most suitable model for this dataset.
