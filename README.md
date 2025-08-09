# Time Series Event Study: NVDA & SFTBY (SoftBank as ARM Proxy)

## Project Overview

This project investigates the stock price behavior of NVIDIA (NVDA) and SoftBank (SFTBY, used as a proxy for ARM before its IPO in 2023), with AMD and Intel (INTC) as exogenous variables. The analysis is structured as an event study focusing on NVIDIA's attempted acquisition of ARM, detailing the impact of key announcements and regulatory events on the related equities.

## Objectives

- Analyze the impact of NVIDIA's ARM acquisition attempt on the stock prices of NVDA, SFTBY, AMD, and INTC.
- Compare price, returns, and volatility (squared returns) across the event window.
- Use yfinance to fetch historical data and perform time series analysis using Python.

## Data and Key Events

- **Stocks Analyzed:** NVDA, SFTBY, AMD, INTC
- **Time Period:** 2020-09-13 to 2022-02-14
- **Key Events:**
  - **Start**: 2020-09-13 — NVIDIA announces intent to acquire ARM
  - **Announcement 1**: 2021-07-20 — Regulatory concerns lead to investigation
  - **Announcement 2**: 2021-12-02 — FTC files lawsuit to block acquisition
  - **Scandal/Termination**: 2022-02-07 — Deal is terminated

## Methodology

1. **Data Collection:**  
   - Historical daily prices for all four tickers using `yfinance`.
   - Data cleaned, missing values filled, and business day frequency enforced.

2. **Feature Engineering:**  
   - Extract closing prices, returns, log returns, squared returns, squared log returns, and volumes for each ticker.
   - Remove unnecessary columns and handle missing values.

3. **Visualization:**  
   - Plot closing prices, returns, and squared returns for each ticker across the three key event periods.
   - Color-coded plots to highlight event windows.

4. **Analysis:**  
   - Examine how each announcement affected the volatility and returns of the involved stocks.

## Usage

1. **Install Dependencies:**
    ```bash
    pip install numpy pandas yfinance matplotlib seaborn statsmodels pmdarima arch scikit-learn
    ```

2. **Run the Notebook:**
    - Open `TS_NVDA_SFTBY.ipynb` in Jupyter Notebook or JupyterLab.
    - Execute each cell sequentially to reproduce the analysis and plots.

## Notable Libraries Used

- `numpy`, `pandas`: Data manipulation and computation
- `matplotlib`, `seaborn`: Visualization
- `statsmodels`, `arch`: Time series analysis and modeling
- `yfinance`: Data extraction from Yahoo! Finance
- `pmdarima`: Auto ARIMA modeling

## File Structure

- `TS_NVDA_SFTBY.ipynb`: Main analysis notebook (contains code, visualizations, and commentary)
- `README.md`: Project overview and instructions

## Results

- Plots comparing price and return movements for NVDA, SFTBY, AMD, and INTC across event periods.
- Insights into how major corporate events and regulatory actions influence stock behavior in the semiconductor sector.

## License

This project is for educational/research use. See repository license for more information.

## Author

- [Jon Cushman](https://github.com/Jcushman1116)

---

*For questions or suggestions, please open an issue or contact the author via GitHub.*
