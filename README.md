# 🚕 Sweet Lift Taxi – Time Series Forecasting for Airport Ride Demand

## 🔍 Project Functionality  
**Sweet Lift Taxi** wants to improve its operations by forecasting the number of taxi ride requests for the **next hour** at airports. This project builds a time series prediction model to assist the company in deploying drivers more effectively during peak times.

The **target performance metric** is an **RMSE under 48** on the test set.

## 🛠️ Technologies and Methods  
- **Python** (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, LightGBM, CatBoost, Statsmodels)  
- **Time Series Techniques**:
  - **Hourly resampling**
  - **Time-based features** (hour, day of week, weekend indicator)
  - **Lag features** (1 to 24 hours)
  - **Rolling means** (3, 6, and 12-hour windows)
  - **Seasonal decomposition** using `statsmodels`
- **Modeling and Evaluation**:
  - **Linear Regression** (baseline sanity check)
  - **Decision Tree** and **Random Forest**
  - **LightGBM** (primary model) and **CatBoost** for boosting performance
  - **RMSE** and **R² Score** used as evaluation metrics  
- **Hyperparameter tuning** with `GridSearchCV`

## 📈 Key Findings and Conclusion  
- The best-performing model was **LightGBM**, which achieved:
  - **RMSE < 48**, successfully meeting the project’s target
  - **R² = 0.489**, indicating solid explanatory power for variability in hourly demand  
- **Feature engineering** was crucial. Adding **lag variables**, **rolling means**, and **time-based features** significantly improved prediction accuracy:
  - RMSE reduced from **7.51**
