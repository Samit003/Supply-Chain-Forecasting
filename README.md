# Supply Chain Forecasting with DeepAR and AWS SageMaker

This project showcases a forecasting pipeline for predicting retail inventory demand using time series modeling with Amazon SageMaker's DeepAR algorithm.

## Project Objective

To build an end-to-end machine learning pipeline that predicts the number of units sold per product per store for the next 30 days using historical sales data.

## Tools and Technologies

- Python (Pandas, Matplotlib, JSON)
- Amazon SageMaker (DeepAR Forecasting)
- AWS S3 for data storage
- Jupyter Notebook (hosted on SageMaker)
- Excel for final output reporting

## Project Structure

- `Supply-Chain-Forecasting.ipynb` — Full notebook with all steps
- `all_forecasts.xlsx` — Forecast output from DeepAR for all time series
- `series_mapping.xlsx` — Mapping of time series index to Store and Product IDs
- `final_forecast_output.xlsx` — Final merged output with readable Store/Product/Date and quantile predictions

## Workflow Overview

1. **Data Collection and Cleaning**  
   Loaded historical retail inventory data and grouped it by Store ID, Product ID, and Date.

2. **Data Preparation for DeepAR**  
   Transformed the dataset into DeepAR-compatible JSON format with features like prediction length, context length, and time frequency.

3. **Model Training using SageMaker**  
   Trained a DeepAR model on SageMaker with the prepared dataset using custom hyperparameters for forecasting accuracy.

4. **Model Deployment and Prediction**  
   Deployed the trained model as a SageMaker endpoint and performed real-time forecasting.

5. **Visualization**  
   Visualized actual sales vs forecast with median and 80% confidence interval bands.

6. **Postprocessing and Output**  
   Mapped the forecasts back to original Store/Product combinations and exported the results to Excel.

## Output Description

The final Excel file contains:
- Store ID
- Product ID
- Forecast Date
- Predicted quantiles: p10, p50 (median), p90

This format supports business decisions such as demand planning and stock optimization.

## Purpose of the Project

This project was developed as part of a hands-on initiative to demonstrate real-world data analysis and forecasting capabilities for a Supply Chain Analyst internship role. It highlights skills in AWS machine learning services, time series forecasting, and data-driven business decision support.
