# Portfolio Optimization for S&P 500 Stocks #

This project aims to perform portfolio optimization using historical stock data. Portfolio optimization is a crucial aspect of investment management, and this project demonstrates the process of constructing an optimal portfolio given a set of assets.

## Data Collection ##

8 years of historical data of S&P500 stocks is fetched using the Yahoo Finance API. The end date and start date can be modified according to requirements. The original data retrieved along with intermediate data is stored in the 'data' directory.

## Data Processing ##

After cleaning up the data and filtering the top 150 most liquid stocks, we calculate Garman-Klass Volatility, RSI, ATR, Bollinger Bands, and MACD and normalize them. Our model uses these indicators to make predictions.

## K-Means Clustering ##

Based on these metrics, we use K-Means Clustering model to divide the stocks into 4 groups at the end of each month. The best performing cluster containing 30-40 stocks will form our portfolio for the following month.

## Optimization ##

We then use the Max-Sharpe Optimization ratio to find the weights for the assets in our portfolio. 

