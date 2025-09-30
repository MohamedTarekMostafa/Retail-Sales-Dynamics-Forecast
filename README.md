<p align="center">
  <img src="deployment.png" alt="SalesForeCast_Image.jpg" width="700">
</p>
💰 Retail Sales Dynamics Forecast

📌 Project Overview  
This is an End-to-End (E2E) Time Series Forecasting solution designed to predict the daily sales for a major retail chain (focusing on Store 1 of the Rossmann dataset). The project utilizes the Prophet model to analyze historical sales data, identify complex seasonal and trend patterns, and generate a stable 60-day sales forecast.  
The final deliverable is a functional, deployed web application using Streamlit.  

🎯 Business Goal & Value Proposition  
The primary objective of this project is to provide actionable intelligence to store managers and regional planners, enabling proactive operational decision-making.  

Objective | Business Impact  
- Inventory Management → Accurately predicts demand peaks and troughs, minimizing stockouts (lost sales) and reducing excess inventory (storage cost/waste).  
- Workforce Optimization → Forecasts busy periods, allowing for optimal staff scheduling to improve customer service and operational efficiency.  
- Financial Planning → Provides a reliable range of projected revenue (Confidence Interval) for accurate budgeting and cash flow management.  

⚙️ Technology Stack & Methodology  

Technology Stack:  
- Python → Core programming language.  
- Prophet → Primary forecasting model (used for its robust handling of seasonality and holidays).  
- Pandas / NumPy → Data ingestion, cleaning, and preparation for modeling.  
- Streamlit → Creating and deploying the interactive web interface.  
- Joblib → Serialization and persistence of the final production model.  

Key Methodology Notes:  
- Model Stabilization → The raw data for Store 1 exhibited high volatility. The final model was stabilized by diagnosing and correcting instability (which led to severe errors) through setting the seasonality mode to additive and constraining the number of changepoints.  
- Decomposition → The model captures underlying yearly and weekly seasonality along with the long-term sales trend.  

📈 Performance & Key Results  
- Metric: MAPE (Mean Absolute Percentage Error)  
- Result Achieved: 17.74%  
- Achievement: This result demonstrates a stable and commercially viable performance level for highly volatile retail time series data, validating the model's predictive reliability.  

📂 Project Structure  
- [Notebook_Name].ipynb → The main Jupyter/Colab notebook containing all E2E code (Data Prep, Training, Evaluation, Deployment setup).  
- app.py → The Streamlit code file for the front-end web application.  
- prophet_final_model_store_1.pkl → The final production model, trained on all historical data.  
- mape_score.pkl → File storing the final MAPE value for display in the application.  
- train.csv, store.csv → Original datasets required to run the project.  

🚀 How to Run the Project (Deployment)  

**Prerequisites**  
- Python 3.x  
- All required libraries installed (e.g., prophet, streamlit, pyngrok).  

**Execution Steps**  
1. Data & Model → Run the first three cells of the Jupyter/Colab notebook to install dependencies, clean data, train the model, and save the .pkl files.  
2. App File → Run Cell 4 to generate the app.py file.  
3. Deployment → Run Cell 5 (the pyngrok cell). Ensure your ngrok Authorization Token is correctly entered and uncommented.  
4. The output of the final cell will provide a Public URL (e.g., https://[...].ngrok-free.app) to access the live, interactive sales forecasting application.  
