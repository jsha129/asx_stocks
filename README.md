(This is a project in progress)

# What is the problem?
The stock market could be a vehicle for wealth generation. This work aims to identify a selected few high-performance public companies from their business fundamental data (balance sheet, income and cashflow statements). 

Stock market is immensely complex and it is hoped that this analyses will reveal important financial numbers associated with stock price movement. 

**WARNING**: This work is not intended as financial advice. 

# Approach
## (1) Gather data
Historic data were provided by Yahoo Finance API and stored in an SQLite database (python, SQL). The database is updated as new data becomes available.

## (2) Calculate compound annual growth return (CAGR) 
Stock prices were retrieved from the database and log-transformed linear regression was performed to estimate growth rates and errors (python, scikit-learn)

## (3) Calculate ratios and other growth rates
Functions were implemented to calculate financial ratios. Some ratios were simple growth rates (eg, revenue growth) whereas other metrics were complex (eg, return on capital invested).

## (4) Identify features that correlate with high CAGR using machine learning
Two similar approaches were employed followed by feature selection. In the linear regression approach, we attempted to predict CAGR of a stock based on multiple financial ratios followed by model selection and feature selection. In the simpler **classification** style approach, companies were categorised as `high` or `low` CAGR if CAGR >= 15%. The cutoff value was based on CAGR quantiles and the observation that long term return of overall australian stock market is 10% per annum. 



Linear and logistic regression were used to identify financial ratios that could predict CAGR of stocks or .  

- Linear regression was to identify financial 

# Limitations
Due to changes in economic cycles and/or company governance, historic data may not be reliable as future predictors. Stock market is an example of second-order chaotic systems (https://danielmiessler.com/p/first-second-order-chaos/) because it responds to the prediction. A stock price (and market) is an aggregate of buyers' and sellers' sentiments that can be largely driven by emotions (fear, greed and so on) rather than logic.

