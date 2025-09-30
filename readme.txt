Black-Scholes Model and Greeks Analyzer
Project Overview
This repository contains a comprehensive implementation of the Black-Scholes-Merton (BSM) Model in Python, designed for the theoretical pricing of financial options and the calculation of their associated Greeks.
The project uses real-time financial data, integrated via the yfinance library, to provide accurate model inputs and allow for comparison between theoretical prices and current market quotes. It is an essential tool for quantitative finance students, traders, and analysts looking to understand the mechanics of option valuation and risk management.
Key Features
The Jupyter Notebook (Modelo_Black_Scholes_y_Griegas.ipynb) provides the following functionalities:
* Black-Scholes-Merton (BSM) Pricing: Calculates the fair value for European-style Call and Put options based on five input variables: underlying price (  ), strike price (  ), time to expiration (  ), risk-free rate (  ), and volatility (  ).
* Option Greeks Calculation: Computes the "Greeks," which measure the sensitivity of the option's price to changes in input parameters:
   * Delta (  ): Sensitivity to the underlying asset's price.
   * Gamma (  ): Sensitivity of Delta to the underlying asset's price.
   * Theta (  ): Sensitivity to the passage of time (time decay).
   * Vega (V): Sensitivity to volatility.
   * Rho (  ): Sensitivity to the risk-free interest rate.
      * Implied Volatility (IV) Solver: Uses numerical optimization (scipy.optimize.brentq) to calculate the volatility implied by the market price of an option.
      * Market Data Integration: Automatically fetches up-to-date stock information, historical volatility, and option chain data using the yfinance library.
      * Model Comparison (Inferred): Includes calculations and comparisons, potentially against the Binomial Option Pricing Model (as suggested by notebook output), to validate and contrast different valuation methodologies.
Requirements
To run this project, you will need Python 3.x and the following libraries:
Library
	Description
	numpy
	For high-level mathematical operations and array processing.
	scipy
	For scientific computing, particularly the norm distribution and the brentq solver for IV.
	yfinance
	To download market data from Yahoo! Finance.
	matplotlib
	For plotting and data visualization (e.g., visualizing Greeks vs. time/price).
	Installation
      1. Clone the repository:
git clone [https://github.com/pmonsivaisrivera08/your-repo-name.git](https://github.com/pmonsivaisrivera08/your-repo-name.git)
cd your-repo-name

      2. Install dependencies:
pip install numpy scipy yfinance matplotlib jupyter

      3. Run the notebook:
jupyter notebook Modelo_Black_Scholes_y_Griegas.ipynb

Usage
Open and run the cells within the Modelo_Black_Scholes_y_Griegas.ipynb notebook. The code is structured to:
         1. Define the BlackScholesModel class containing all necessary functions.
         2. Fetch a stock ticker's data (e.g., TSLA).
         3. Calculate historical volatility for use as the model's   .
         4. Input current options parameters (Strike, Expiration, Mid Price).
         5. Output theoretical price, Greeks, and Implied Volatility for the selected options contract.
Author
This project was created by:
pmonsivaisrivera08
Feel free to connect or contribute!