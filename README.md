# Algotrading multi-factor alpha & risk model
This is an algotrading multi-factor model, written in Python, and incorporating PCA for risk factors and alpha factors from academic literature for portfolio optimization. It works as follows:
- load market data using `zipline`
- computre daily returns over last 5 years
- create risk factors with `sklearn.decomposition.PCA`
- create alpha factors for 1 year momentum, mean reversion 5 days sector neutral, and overnight sentiment
- evaluate alpha factors with quantile analysis using `alphalens` and Sharpe ratio
- generate optimal portfolio weights incorporating constraints (risk factors, dollar neutral, unleveraged, etc.) and diversification parameter with `cvxpy`
