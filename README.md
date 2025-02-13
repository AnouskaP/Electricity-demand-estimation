# Electricity Consumption Forecasting

## Project Overview
This project focuses on analyzing and forecasting electricity consumption using **time series analysis** and **machine learning techniques**. The goal is to transform the dataset into a stationary time series and apply **ARIMA** to make future predictions.

## Dataset
- The dataset contains **electricity consumption data** over time.
- It has two columns:
  - `Date`: Timestamp of the recorded consumption
  - `Consumption`: Electricity usage in kWh

## Project Workflow
1. **Data Preprocessing**
   - Handle missing values
   - Convert date column to `datetime` format
   - Set `Date` as the index

2. **Exploratory Data Analysis (EDA)**
   - Visualizing raw time series data
   - Identifying trends, seasonality, and noise
   - Checking for stationarity using the **Augmented Dickey-Fuller (ADF) test**

3. **Making the Time Series Stationary**
   - Log transformation to reduce variance
   - Rolling mean subtraction
   - Differencing to remove trends and seasonality
   - Exponential moving average (EMA) smoothing

4. **Time Series Decomposition**
   - Separating **Trend, Seasonality, and Residuals** using `statsmodels`

5. **Model Selection and Forecasting**
   - **Autocorrelation Function (ACF) & Partial Autocorrelation Function (PACF)** to determine ARIMA parameters
   - Building and training the **ARIMA (AutoRegressive Integrated Moving Average) model**
   - Making future predictions and visualizing results

## Installation & Dependencies
To run this project, install the required Python libraries:

```bash
pip install numpy pandas matplotlib statsmodels seaborn
```

## Usage
Clone the repository and run the Jupyter Notebook:

```bash
git clone https://github.com/AnouskaP/Electricity-demand-estimation
cd Electricity-demand-estimation
jupyter notebook
```

## Results & Findings
- The model effectively captures seasonal patterns in electricity consumption.
- Forecasting extends to **2040**, with trends showing increasing consumption.
- The **ARIMA (3,1,3)** model performed well with low residual error.

## Future Work
- Experimenting with **LSTM & Prophet** for better accuracy.
- Adding **weather and economic factors** to enhance predictions.

