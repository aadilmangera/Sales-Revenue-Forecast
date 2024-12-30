# Sales and Revenue Forecasting Project

## Project Overview
This project focuses on predicting weekly sales for Walmart stores using historical sales data and various economic and seasonal factors. Additionally, it includes a comprehensive data analysis and visualization dashboard built using Power BI to provide insights into sales trends and contributing factors. You can view the [Live Dashboard](https://app.powerbi.com/groups/me/reports/13d5e6fe-2da9-4f8a-8718-10c2eee4d377/e17ec0dda954fdee9222?experience=power-bi)


## Key Objectives
- Build a machine learning model to predict weekly sales.
- Analyze key economic and seasonal factors affecting sales.
- Create interactive dashboards in Power BI for better insights and storytelling.

---

## Tools and Technologies
- **Python Libraries**: Pandas, NumPy, Matplotlib, Scikit-learn, Seaborn
- **Visualization**: Power BI
- **Dataset**: [Walmart Sales Forecast Dataset](https://www.kaggle.com/datasets/aslanahmedov/walmart-sales-forecast)
- **Environment**: Jupyter Notebooks in VS Code

---

## Dataset Overview
The project utilizes four main datasets:
1. **train.csv**: Contains historical sales data by store and department.
2. **features.csv**: Includes economic and seasonal data such as CPI, fuel prices, and holiday indicators.
3. **stores.csv**: Details about the size and type of Walmart stores.
4. **sales_forecasting_results.csv**: Contains predicted sales output from the machine learning model.

### Key Features:
- **Weekly_Sales**: Target variable for forecasting.
- **IsHoliday**: Boolean flag indicating whether the week included a holiday.
- **CPI**: Consumer Price Index.
- **Fuel_Price**: Weekly fuel prices.
- **MarkDowns**: Promotional markdown data.
- **Store Size**: Size of the store.
- **Temperature**: Regional temperatures.

---

## Steps to Reproduce

### 1. Data Preparation
- Loaded, merged, and cleaned datasets to address missing values and ensure consistency.
- Extracted time-based features (Year, Month, Week).

### 2. Exploratory Data Analysis (EDA)
- Visualized trends in sales over time.
- Identified patterns and relationships between variables.

### 3. Feature Engineering
- Created additional features to improve model accuracy, such as:
  - Holiday season indicator
  - One-hot encoding for categorical variables.

### 4. Machine Learning Model
- Trained Linear Regression and Decision Tree Regressor models to predict weekly sales.
- Evaluated models using metrics such as MAE, RMSE, and R².

### 5. Visualization and Dashboard
- Built an interactive Power BI report featuring:
  - **Historical Analysis**: Trends and patterns of weekly sales.
  - **Predicted Sales**: Visualized forecasted sales.
  - **Economic Factors Analysis**: Correlations between CPI, fuel prices, markdowns, and sales.

---

## Project Highlights

### Machine Learning Results
Both models were evaluated for performance. The Decision Tree Regressor captured non-linear relationships better with an an RMSE of **21960.77**, making it the preferred model for forecasting.

### Power BI Dashboard
- **Overview Page**: Showcases key metrics and trends.
- **Historical Analysis**: Displays sales trends by year and store.
- **Predicted Sales**: Visualizes the forecasted values alongside actual sales.
- **Economic Factors Analysis**:
  - Impact of CPI, fuel price, and markdowns on sales.
  - Correlation between temperature and weekly sales.
    
---

## Data Model in Power BI
The data model includes relationships between the following tables:
- `features` (connected by `Date` and `Store` columns).
- `train` (connected by `Date`, `Store`, and `Dept` columns).
- `stores` (connected by `Store` column).
- `sales_forecasting_results` (connected by `Date`, `Store`, and `Dept` columns).

---

## Installation and Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/aadilmangera/sales-revenur-forecast.git
   ```
2. Install required Python packages:
   ```bash
   pip install -r requirements.txt
   ```
3. Open the Power BI file (`Sales Dashboard.pbix`) to explore the visualizations.

---

## Files in the Repository
- **Jupyter Notebook**: `sales_forecasting.ipynb` (contains data preparation, modeling, and evaluation).
- **Python File**: `sales_forecasting.py`
- **Power BI Dashboard**: `Sales Dashboard.pbix`
- **Datasets**: `train.csv`, `test.csv`, `features.csv`, `stores.csv`, `sales_forecasting_results.csv`

---

## Future Work
- Implement advanced machine learning models like Random Forest or XGBoost for improved accuracy.
- Include external datasets (e.g., regional economic data or weather patterns) for better feature engineering.
- Add more detailed insights in Power BI using DAX calculations.
