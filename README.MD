# Portfolio Analysis and Market Data Collection

This project consists of two Jupyter notebooks that work together to collect, analyze, and visualize financial market data. The goal is to gather historical stock data for a personal portfolio as well as major market indices, and then perform a variety of analyses including return statistics, risk metrics, beta calculation, and portfolio optimization.

## Project Structure

```
├── data
│   ├── Portfolio.csv                  # Portfolio file with ticker and weight information
│   ├── Portfolio_prices.csv           # Collected historical price data for portfolio stocks
│   ├── SP500.csv                      # Historical data for the S&P 500 index
│   ├── NASDAQ.csv                     # Historical data for the NASDAQ index
│   └── Dow_Jones.csv                  # Historical data for the Dow Jones index
├── data-collection-for-portfolio-analysis-and-market.ipynb
│                                       # Notebook for collecting data from Yahoo Finance
└── personal-portfolio-analysis.ipynb  # Notebook for portfolio analysis and risk metrics
```

## Notebooks Overview

### 1. `data-collection-for-portfolio-analysis-and-market.ipynb`

This notebook is responsible for:

- **Data Collection**:  
  - Loading portfolio tickers from `data/Portfolio.csv`.
  - Downloading historical price data for each portfolio stock using the `yfinance` library.
  - Downloading historical data for market indices (S&P 500, NASDAQ, Dow Jones).
  
- **Data Preparation**:  
  - Calculating daily returns for stocks and indices.
  - Saving the collected data to CSV files within the `data` directory for further analysis.

### 2. `personal-portfolio-analysis.ipynb`

This notebook performs various portfolio analyses including:

- **Data Visualization**:  
  - Plotting average adjusted stock prices.
  - Visualizing the distribution of daily returns.
  - Displaying trading volume statistics and persistence.

- **Risk Metrics Calculation**:  
  - Calculating portfolio return, volatility, Sharpe ratio, and Sortino ratio.
  - Computing Value-at-Risk (VaR) and Conditional Value-at-Risk (CVaR) using both historical and parametric methods.

- **Beta Calculation**:  
  - Calculating the beta of individual stocks relative to a market index.

- **Portfolio Optimization**:  
  - Finding optimal portfolio weights to achieve a target return using mean-variance optimization.

## Setup Instructions

1. **Clone the Repository**  
   Clone this repository to your local machine:
   ```bash
   git clone https://github.com/yourusername/portfolio-analysis.git
   cd portfolio-analysis
   ```

2. **Create a Virtual Environment (Optional but Recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. **Install Dependencies**  
   Install the required Python packages using pip:
   ```bash
   pip install numpy pandas yfinance matplotlib plotnine statsmodels scipy
   ```
   > **Note:** This project uses `yfinance` to fetch market data and `plotnine` (a ggplot2-like library for Python) for plotting.

4. **Portfolio Data**  
   Ensure that the `data/Portfolio.csv` file exists in the `data` folder. This file should contain your portfolio tickers and corresponding weights.

## Running the Notebooks

1. **Data Collection Notebook**  
   Open and run `data-collection-for-portfolio-analysis-and-market.ipynb` first. This notebook will:
   - Create the `data` folder if it does not exist.
   - Download historical data for the portfolio tickers and market indices.
   - Save the collected data as CSV files within the `data` folder.

2. **Portfolio Analysis Notebook**  
   Once the data collection notebook has run successfully, open and run `personal-portfolio-analysis.ipynb` to:
   - Load the CSV files generated in the previous step.
   - Perform various analyses (plotting, risk metrics, beta calculation, optimization).
   - Visualize the results of your portfolio analysis.

## License
This project is open-source and available under the GNU General Public License (GPL-3.0).
## Contributing

Contributions and feedback are welcome! Please open an issue or submit a pull request for any improvements.

