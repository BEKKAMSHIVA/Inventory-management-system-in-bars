# Inventory-management-system-in-bars
Hi, my name is Bekkam Shiva, and in this I’ll explain my project on Bar Inventory Forecasting and Optimization using the ARIMA model.
# Project Overview #
A hotel chain with multiple bars was facing inventory management issues, such as frequent stockouts of high-demand items and overstocking of slow-moving ones. These inefficiencies led to increased costs and poor customer satisfaction.

Our goal:
1. Analyze historical alcohol consumption data
2. Identify consumption patterns and seasonality
3. Forecast future demand
4. Recommend optimal inventory (par) levels for each bar

#  Dataset Details #
The dataset provided by the hotel includes 6,575 records and 8 columns:
Date Time Served, Bar Name, Alcohol Type, Brand Name
Opening Balance (ml), Purchase (ml), Consumed (ml), Closing Balance (ml)
All columns had correct data types
No nulls or duplicate rows

#  Feature Engineering #
Extracted Date, Hour, Day of Week, Weekend, Month, Week Number, and Season
Sorted timestamps for accurate time-series analysis

# EDA & Insights #
Focused on selected bars (e.g., Anderson’s Bar):
Total yearly consumption vs purchase
Alcohol type–wise and brand–wise trends
Monthly/Weekly/Daily consumption breakdowns
Stockout & overstock thresholds
Seasonality decomposition using statsmodels

 # Automation for Multiple Bars #
Manually analyzing each bar was inefficient.
I developed a reusable function that performs the above analysis for any bar, stores results in a structured dictionary format, and prepares data for forecasting.

# Forecasting with ARIMA #
Implemented ARIMA model:
AutoRegressive Integrated Moving Average
Trained separately for each bar using historical data
Forecasted future alcohol consumption and calculated optimal inventory levels per brand/type
Used BarInventoryForecastOptimizer class to modularize this step

# Results #
The model forecasts daily demand and recommends the par stock levels for each brand at each bar, helping managers make data-driven decisions and avoid both stockouts and overstocking
