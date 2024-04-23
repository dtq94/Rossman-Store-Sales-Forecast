# Rossmann Store Sales Prediction

## Overview
Rossmann operates over 3,000 drug stores across 7 European countries. This project aims to predict the daily sales for up to six weeks in advance for each store. Sales are influenced by various factors such as promotions, competition, holidays, seasonality, and locality. The goal is to develop a model that accurately forecasts sales to assist store managers in making informed decisions.

## Data Description
The dataset contains the following fields:
1. Id: Unique identifier for each (Store, Date) pair in the test set
2. Store: Unique identifier for each store
3. Sales: Turnover for a given day (prediction target)
4. Customers: Number of customers on a given day
5. Open: Indicator for whether the store was open (0 = closed, 1 = open)
6. StateHoliday: Indicates state holidays (a = public holiday, b = Easter holiday, c = Christmas, 0 = None)
7. SchoolHoliday: Indicates if the store was affected by the closure of public schools
8. StoreType: Differentiates between 4 store models (a, b, c, d)
9. Assortment: Describes assortment level (a = basic, b = extra, c = extended)
10. CompetitionDistance: Distance to the nearest competitor store (in meters)
11. CompetitionOpenSince[Month/Year]: Approximate year and month when the nearest competitor opened
12. Promo: Indicates if a store is running a promo on that day
13. Promo2: Indicates if a store is participating in a continuing promotion (0 = not participating, 1 = participating)
14. Promo2Since[Year/Week]: Year and calendar week when the store started participating in Promo2
15. PromoInterval: Months in which Promo2 is started anew (e.g., "Feb,May,Aug,Nov")

## Approach
1. Exploratory Data Analysis:
   - Identify unique users, popular platforms, correlations, and anomalies.
2. Imputation:
   - Fill missing values appropriately.
3. Outliers Detection and Removal:
   - Detect and eliminate outliers.
4. Further Exploratory Data Analysis:
   - Gain deeper insights into the data.
5. Label Encoding and One-Hot Encoding:
   - Convert non-numeric data to numeric format.
6. Model Building and Evaluation:
   - Apply regression algorithms:
     - Linear Regression
     - SGD Regression
     - Random Forest Regressor
     - Decision Tree Regressor
   - Select the best-performing model (Random Forest Regressor).
7. Feature Importance Analysis:
   - Determine which features contribute most or least to sales predictions.

## Project Structure
```
|-- InputFiles
    -- data.csv
|-- SourceFolder
    |-- ML_Pipeline
        -- Cat_to_nums.py
        -- Impute.py
        -- Train_model.py
        -- Utils.py
        -- Evaluate_results.py
        -- Feature_importance.py
    |-- Engine.py
