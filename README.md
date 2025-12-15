# Pharmacy Daily Sales Prediction
### Project Overview
This project aims to predict daily sales for a pharmacy using historical sales data. The goal is to provide accurate forecasts to improve inventory management, reduce stockouts, and optimize operational planning.
Multiple predictive models were built and evaluated, including:
* Decision Tree Regression
* Linear Regression with various feature sets
* PCA-based Regression for dimensionality reduction
Models were evaluated using RMSE, MAE, and R² metrics to identify the best-performing approach.

### Dataset
The dataset consists of daily sales records for multiple drug categories. Key characteristics:
* Time-series data including weekdays, dates, and sales volumes
* Multiple drug categories, each with potential seasonal or promotional variations
* No missing values, with outliers identified and analyzed
Data preprocessing included:
* Feature encoding (e.g., weekdays → 1–7)
* Standardization of continuous features
* PCA transformation for dimensionality reduction

### Exploratory Data Analysis (EDA)
EDA revealed:
* Seasonal and cyclical patterns, particularly for drug R06
* Outliers in sales data likely caused by promotions or demand spikes, not data errors
* Correlations between drug categories, visualized via heatmaps
Interactive dashboards were created for:
* Sales overview & summary
* Trend analysis
* Seasonality & cycle analysis

### Models & Evaluation
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Model</th>
      <th>RMSE</th>
      <th>MAE</th>
      <th>R^2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>DecisionTree_v1</td>
      <td>2.749417</td>
      <td>2.113194</td>
      <td>-0.099194</td>
    </tr>
    <tr>
      <th>1</th>
      <td>DecisionTree_v2</td>
      <td>3.197650</td>
      <td>2.468703</td>
      <td>-0.486808</td>
    </tr>
    <tr>
      <th>2</th>
      <td>LinearRegression_v1</td>
      <td>2.217586</td>
      <td>1.699001</td>
      <td>0.098691</td>
    </tr>
    <tr>
      <th>3</th>
      <td>LinearRegression_v2</td>
      <td>2.243616</td>
      <td>1.734510</td>
      <td>0.077407</td>
    </tr>
    <tr>
      <th>4</th>
      <td>LinearRegression_v3</td>
      <td>2.243972</td>
      <td>1.736503</td>
      <td>0.077114</td>
    </tr>
    <tr>
      <th>5</th>
      <td>LinearRegression_v4</td>
      <td>1.920963</td>
      <td>1.426363</td>
      <td>0.407981</td>
    </tr>
    <tr>
      <th>6</th>
      <td>PCA_Regression</td>
      <td>2.074156</td>
      <td>1.542044</td>
      <td>0.309791</td>
    </tr>
  </tbody>
</table>
</div>
Key insights:
* LinearRegression_v4 achieved the best performance and is most suitable for forecasting
* PCA regression reduces dimensionality while maintaining reasonable predictive power
* Decision trees struggled with high variability and outliers

### How to Use
1. Clone the repository:
```
git clone <repo_url>
```
2. Install required Python packages
3. Load preprocessed data and models using joblib for predictions
4. Evaluate models or generate forecasts with new data
5. 
