# Retail-Sales-Forecasting

# Retail Sales Forecasting Project

## Project Overview
This project predicts **weekly sales for retail stores** using historical sales, store information, promotions, holidays, and economic indicators. Accurate sales forecasting helps businesses manage inventory, plan promotions, and make informed operational decisions, reducing costs and increasing revenue.

---

## Problem Statement
Retail stores face challenges in predicting weekly sales due to seasonality, promotions, holidays, and store-specific characteristics. This project aims to build machine learning models that accurately forecast weekly sales for each store and department.

---

## Dataset Description
The project uses three datasets:

1. **Sales Data:** Weekly sales per store and department.  
2. **Store Data:** Store type, size, and characteristics.  
3. **Feature Data:** Promotions, holidays, markdowns, and economic indicators (CPI, Fuel Price, Unemployment).

---

## Variables
- **Target Variable:** `Weekly_Sales` (total sales per week).  
- **Features:** `Store`, `Dept`, `Date`, `IsHoliday`, `Promo`, `IsPromo2`, `Store_Type`, `Size`, `CPI`, `Fuel_Price`, `Unemployment`, `MarkDown1-5`  
- Derived features: `Month`, `WeekOfYear`, `Year`.

---

## Data Preprocessing
- Missing values handled using **SimpleImputer**.  
- Categorical variables encoded using **OneHotEncoder**.  
- Numeric features scaled using **StandardScaler** or **MinMaxScaler**.  
- Date column converted to datetime and additional features extracted.

---

## Exploratory Data Analysis (EDA)
- Visualized weekly, monthly, and yearly sales trends.  
- Correlation heatmaps to understand feature relationships.  
- Analyzed impact of holidays, promotions, and markdowns.  
- Explored store-wise and department-wise sales patterns.

---

## Machine Learning Models
Implemented three models:

1. **Linear Regression** – baseline model.  
2. **Random Forest Regressor** – ensemble model capturing non-linear patterns.  
3. **Gradient Boosting Regressor** – best-performing model.

**Evaluation Metrics:** R² Score, RMSE, MAE  
- Gradient Boosting Regressor achieved highest R² and lowest errors.

---

## Hyperparameter Tuning
- Technique: **GridSearchCV**  
- Optimized parameters: `n_estimators`, `max_depth`, `learning_rate`  
- Cross-validation ensured stable performance.  
- Improved R², RMSE, and MAE after tuning.

---

## Feature Importance
Most important features from Gradient Boosting:

- `Store_Type`, `Promotions`, `Holidays`, `Store Size`  
- Insights: Optimize inventory, schedule promotions, plan for holidays.

---

## Deployment
- Best model saved as `Retail_Sales_Model.pkl` using **pickle**.  
- Tested on unseen data for sanity check.  
- Ready for integration into retail systems for real-time forecasting.

---

## Future Work
- Add more features: weather, events, competitors.  
- Try advanced models: XGBoost, LightGBM.  
- Deploy as web app/dashboard for business use.

---

## How to Run
1. Clone the repository:  
```bash
git clone https://github.com/akhileshbhagat76/Retail-Sales-Forecasting.git

