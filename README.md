# Algorithmic-Trading-Python-Pandas

### The Algorithmic Trading Process:

1. Collect Data (API calls)

2. Develop a hypothesis for a strategy (what your trading algorithms hopes to achieve)

3. Backtest that strategy 

	- Apply trading algorithm to every market possible going back as far as you can.
	
	- In other words, does the algorithm work on historical data?

4. Implement the strategy in production


### Project setup:

- Random Data from IEX Cloud datbase from IEX Cloud API
	
	- We will use GET requests to gather data from the IEX Cloud API 

		- Other API methods just for referece:
			- POST: Adds data to the database exposed by the API (create only)
			- PUT: Adds and overwrites data in the database exposed by the API (create or replace)
			- DELETE: Deletes data from the API's database

		- Free APIs to use for practice: https://github.com/public-apis/public-apis

- Python + Jupyter Notebook

- Excel

### Goal: 
	
	- We will pretend to hand over our results to traders that will execute trades based on what the algorithm suggests.
	
	- Output will be an excel file with the name of the companies to be purchased and how many shares of those companies to be purchased.

	- An example API call in Python:

		- symbol = 'APPL'
		  api_url = f'https://sandbox.iexapis.com/stable/stock/{symbol}/quote?token={IEX_CLOUD_API_TOKEN}'

		  data = request.get(api_url).json()
		  data


### Project-1

The S&P 500 is the world's most famous stock market index holding 500 of the largest companies in the US. Investment funds are benchmarked to this index to replicate its performance by buying all the stocks in S&P 500.

One of the most important characteristic of the S&P 500 is that it is market capitalization-weighted. This means that bigger companies in the index hold a larger weight.

We will build an alternative version of the S&P 500 Index where each company has the same weighting.
