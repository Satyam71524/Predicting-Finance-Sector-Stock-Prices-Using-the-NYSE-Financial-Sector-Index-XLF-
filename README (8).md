# Analyzing and Predicting Finance Sector Stock Prices Using the NYSE Financial Sector Index (XLF) via Regression Analysis with Python Implementation

## Project Duration
**Sep 2024 - Oct 2024**

## Institution
University at Buffalo School of Management, The State University of New York

## Project Overview

This project focuses on predicting stock prices of individual companies in the financial sector using the **NYSE Financial Sector Index (XLF)**. The XLF Index tracks the performance of financial companies in the U.S. stock market, providing a comprehensive representation of the financial sector. By applying **linear regression models**, we explore the relationship between stock returns of finance sector companies and the returns of the XLF index, taking into account lagged returns and volatility.

## Objectives
- **Predict Stock Prices**: Develop a predictive model for stock prices of individual companies based on the performance of the NYSE Financial Sector Index (XLF).
- **Examine Relationships**: Investigate how stock returns are correlated with the returns of the XLF, including lagged returns and volatility factors, to better understand the influence of the broader financial market.

## Methodology

### Data Collection:
- Download historical data for finance sector companies and the XLF index from **Yahoo Finance** using the `yfinance` library in Python.
- Calculate daily returns based on the closing price of stocks and the XLF index.

### Data Processing:
- **Volatility**: Compute the rolling volatility for both stock and XLF returns using a standard deviation calculation over a set window (e.g., 21 days).
- **Lagged Returns**: Include lagged returns for both stock and XLF data to capture delayed effects on stock prices.

### Regression Analysis:
- Apply **linear regression** to model the relationship between stock returns and XLF returns, using lagged returns and volatility as explanatory variables.
- The regression model will identify how changes in the financial sector (represented by XLF) influence individual stock returns.

### Prediction:
- Use the trained regression model to predict the next day's stock price for selected companies.

## Dependencies

This project uses the following Python libraries:
- `yfinance`: To download financial data.
- `pandas`: For data manipulation and cleaning.
- `numpy`: For numerical operations.
- `statsmodels`: To perform regression analysis.
- `matplotlib`: For plotting and visualizing data.



## Main Functions
 
 get_data(stock_ticker, start_date, end_date): Downloads the historical stock and XLF index data and calculates daily returns.
 
 calculate_volatility(data, window=21): Calculates the rolling volatility (standard deviation) for the given stock or XLF data.
 
 run_regression(stock_data, financial_index_data): Performs linear regression on the stock and XLF returns, including lagged returns and volatility as predictors.
 
 predict_next_day(stock_data, financial_index_data, model): Uses the regression model to predict the next day's stock price.
 
 main(stock_ticker, start_date, end_date): Runs the entire process of fetching data, training the model, and predicting the stock price.

## Usage
To run the program, simply call the main function with the desired stock ticker, start date, and end date.

Example:


if __name__ == '__main__':
    stock_ticker = 'GS'  # Example: Goldman Sachs stock
    start_date = '2020-01-01'
    end_date = '2025-03-01'
    
    main(stock_ticker, start_date, end_date)
This will download historical data for Goldman Sachs (GS), analyze the relationship between its stock price and the NYSE Financial Sector Index (XLF), and predict the next day's stock price.

## Results
The project outputs the predicted stock price for the selected company for the next trading day based on the regression model built from the historical returns and volatility data.

Example Output:

Predicted stock price for GS on the next day: $245.50.
Additionally, the project optionally plots a scatter plot showing the relationship between the stock returns and the XLF returns.

## Conclusion
This project demonstrates how regression analysis can be applied to predict stock prices in the financial sector. By using the NYSE Financial Sector Index (XLF) as a market proxy and incorporating lagged returns and volatility into the analysis, the model provides insights into how the broader financial market influences individual company stock prices.

## Author
Satyam
University at Buffalo
School of Management
MS in Business Analytics (Finance)
