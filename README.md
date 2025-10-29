# Sales Forecasting

## 1. Project Overview
This project aims to forecast daily sales for a retail business using time-series analysis and machine learning models. The goal is to provide accurate sales predictions that can help with inventory management, resource allocation, and business planning.

The notebook implements and compares models such as **XGBoost Regressor** and **Random Forest Regressor**, leveraging engineered time-series features to capture short-term and seasonal patterns in sales data.

## 2. Dataset

### **Source:**
Synthetic or publicly available retail dataset (in CSV format).  
If using your own data, place it under:
data/raw/
├── train.csv
├── test.csv
├── stores.csv
└── features.csv

### **Description**
| File | Description |
|------|--------------|
| `train.csv` | Historical weekly sales by store and department |
| `test.csv` | Test data for which sales are to be predicted |
| `features.csv` | Supplementary information (e.g., holidays, markdowns, temperatures, fuel prices) |
| `stores.csv` | Metadata for each store (e.g., size, type, region) |


## 3. Repository Structure
│
├── data/
│   ├── raw/                 # Raw data files (train/test/features/stores)
│   └── processed/           # Intermediate data, if generated
│
├── sales_forecasting.ipynb  # Main notebook with full analysis & model training
├── requirements.txt         # Dependencies (optional)
├── README.md                # Project documentation

## 4. How to Run the Project
### **1. Clone the repository**
```bash
git clone https://github.com/mgill1009/sales_forecasting.git
cd sales_forecasting

Run the notebook:

jupyter notebook sales_forecasting.ipynb

## 5. Key Findings and Model Performance
	•	Feature Engineering:
Created lagged features, rolling means, and seasonal indicators to enhance time-series prediction accuracy.
This helped capture weekly and monthly trends in sales.
	•	Models Evaluated:
	•	Random Forest Regressor (baseline model)
	•	XGBoost Regressor (optimized model)
	•	Performance Summary:
	•	XGBoost outperformed Random Forest, achieving lower RMSE and better generalization on unseen data.
	•	Rolling mean of 4-week lag proved to be the most important predictor, confirming short-term seasonality in sales trends.
	•	Visualization Highlights:
	•	Actual vs. Predicted sales plots
	•	Feature importance rankings
	•	Error distribution analysis

## 6. Future Improvements
	•	Incorporate additional exogenous variables such as promotions, competitor pricing, or macroeconomic indicators.
	•	Implement cross-store forecasting using hierarchical models.
	•	Experiment with deep learning approaches (e.g., LSTM, Temporal Fusion Transformer).
	•	Automate data pipeline for continuous model retraining and dashboard integration.

