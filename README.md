# Stock Volatility Analysis & Forecasting with Machine Learning

This repository contains two Jupyter notebooks for analyzing and forecasting financial market volatility using PySpark and machine learning techniques.

## Notebooks

### 1. `volatility-analysis.ipynb`
- Performs exploratory volatility analysis on financial tick data.
- Key steps include:
  - Data ingestion with Spark DataFrames.
  - Lagging close prices to compute returns.
  - Calculating close-to-close log returns.
  - Computing rolling realised volatility over a 1-hour window.
  - Storing processed data in Databricks DBFS.

### 2. `forecasting-volatility-ml.ipynb`
- Focuses on building machine learning models for volatility forecasting.
- Main components:
  - **Data Cleaning**: Removing null values and preparing Spark DataFrames.
  - **Feature Engineering**: Creating lagged features and rolling window statistics.
  - **Model Training**: Random Forest Regressor used for forecasting realised volatility.
  - **Data Storage**: Saving processed features as Spark tables for reuse.

## Requirements

This project is designed to run in a **Databricks / PySpark environment**.  
Required Python packages include:

```bash
pyspark
scikit-learn
pandas
numpy
matplotlib
seaborn
```

## Repository Structure

```
.
├── volatility-analysis.ipynb         # Exploratory volatility analysis
├── forecasting-volatility-ml.ipynb   # ML models for volatility forecasting
├── README.md                         # Project documentation
```

## How to Run

1. Open the notebooks in a Databricks or local Jupyter environment with PySpark configured.
2. Run `volatility-analysis.ipynb` to compute realised volatility features.
3. Run `forecasting-volatility-ml.ipynb` to train ML models and generate forecasts.

## Results

- **Volatility Analysis**: Log returns and realised volatility computed from raw market data.
- **Forecasting Models**: Random Forest regression applied to predict realised volatility using engineered features.

## Next Steps

- Extend feature engineering to include macroeconomic indicators or alternative data sources.
- Compare different ML models (e.g., Gradient Boosting, Neural Networks).
- Deploy models for real-time volatility forecasting in trading strategies.
