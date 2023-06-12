[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgit.uwaterloo.ca%2Fj22yi%2Fcfm301-financial-data-analytics&count_bg=%23FFBC93&title_bg=%238FC2FF&icon=&icon_color=%23E7E7E7&title=visits&edge_flat=false)](https://hits.seeyoufarm.com)

# Financial Data Analytics

## Preface

This repository is a collection of solutions for financial data analytics.

### Languages & Technologies used:

Python 3.10 with Pandas, Numpy, statsmodel, scikit-learn, Seaborn, Matplotlib

Data source from WRDS and CRSP.

### Topics

#### DA1

* Access Amazon stock data from WRDS and calculate the following:
    - Mean & SD
    - Annualized returns & Volatility
* Apply CAPM model to Amazon stock with value-weighted market returns
* Apply CAPM model for a rolling period of 60 month with alpha and beta estimates with t-stat for the period
* Apply CAPM model and rolling CAPM model to Amazon stock with Fama-French three-factor model
* Calculate monthly returns and SD using the given portfolio weights and stock returns from WRDS
* Calculate the portfolio's alpha and compare the result with the benchmark

#### DA2

* Using gvkey for Nasdaq 100 index stocks, pull quarterly financial information from Compustat
* Merge WRDS and Compustat data using pandassql aligned to stock months.
* Create additional variables (factors):
    - lnSize : Log size of a firm
    - bk2mkt : Book to market equity ratio
    - eP : Earnings-to-price ratio
* Descriptive statistics for three variables:
    - Mean, median, SD, percentiles
* Outliers
    - Winsorization : Replace any outlier values to +/- 3 SDs
    - Truncation : Invalidate any values outside of 3 SDs
* Cross-sectional z-scores

#### DA3

* Rolling CAPM for a rolling period of 36 months and report summary statistics of beta
* Estimate idiosyncratic volatiliy using Fama-French three factor model for daily returns and SD of the residuals from the model each month
* Estimate momentum using the past year cumulative monthly returns
* Apply winsorization to above three new factors.
* Show correlation between each factor using pairplot in python seaborn package
* Null hypothesis tests of no correlation between each pair of factors using correlation coefficient and p-values

#### DA4

* Constructing quintile portfolios for each factors provided
* Forming a hedge portfolios using quintile 1 and 5 of each factors to generate profit (or arbitrage)
* Calculate overall return, excess return from CAPM and FF-4 model, and sharpe ratio of the hedge portfolios
* Construct betting against beta strategy
    - apply above testing strategy and show differences
* Validating ETF strategy
    - Construct a long-single-factor ETF
    - Comparison with FF-4 model
    - Calculate the turnover ratio
* Multi-factor ETF with short selling
    - Construct ETF with hedge portfolios from multiple factors
    - Calculate FF-4 alpha and Sharpe ratio
    - Calculate FF-3 alpha and Sharpe ratio with a fee in ETF
* Conduct Fama-MacBeth monthly cross sectional test
* Construct quintile portfolio for all NYSE/Nasday stock
    - Data cleaning: remove stock price less than $5 or market cap less than $100 mil
