# NVIDIA Stock Analysis

A Python project that evaluates and compares multiple predictive models for forecasting NVIDIA (NVDA) stock prices using historical market data collected from various financial APIs.

Originally developed as my International Baccalaureate (IB) Extended Essay, this repository contains the complete source code, data processing pipeline, model implementations, and documentation.

---

## Project Overview

The goal of this project was to investigate which predictive model provides the most accurate forecasts for NVIDIA stock prices.

The project includes:

- Historical market data collection
- Data cleaning and preprocessing
- Implementation of eight predictive models
- Model performance comparison
- Statistical analysis
- Result visualization

---

## Technologies

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Financial APIs (yfinence)
- Jupyter Notebook

---

## Models Evaluated

- Model 1 (Stocks of companies related to Nvidia. Nvidia's consumers and suppliers)
- Model 2 (Metal production)
- Model 3 (Metal futures prices)
- Model 4 (Metal ETFs)
- Model 5 (S&P 500)
- Model 6 (NDX 100)
- Model 7 (Small Modular Reactor (SMR) and Micro Modular Reactor (MMR) Companies)
- Model Composite (Synthesis of Optimal Parameters)

---

## Repository Structure

```
src/
data/
graphs/
docs/
README.md
requirements.txt
```

---

## Key Findings

Eight linear regression models were developed and evaluated using historical NVIDIA stock prices together with external market and economic indicators, including semiconductor stocks, commodity futures, ETFs, stock indices, and U.S. metal production data.

The main findings were:

- Models with high explanatory power (up to **R² = 0.932**) often suffered from strong autocorrelation, making them unreliable for forecasting without correction.
- After correcting for autocorrelation, the best-performing models retained a moderate explanatory power (**Adjusted R² ≈ 0.45**), indicating that linear regression can explain part—but not all—of NVIDIA's price movements.
- External variables such as the **NASDAQ-100**, **semiconductor industry stocks**, and **uranium-related ETFs** proved to be the most informative predictors among those tested.
- The results suggest that NVIDIA's stock price is influenced by a combination of broader technology market trends and AI infrastructure factors, but its behavior remains highly company-specific.
- The project also demonstrates the importance of validating regression assumptions rather than relying solely on goodness-of-fit metrics.

Overall, this investigation concluded that **ordinary least squares (OLS) regression is useful for analyzing relationships between market variables but is not the most appropriate method for forecasting financial time series**. Time-series models such as **ARIMA** would likely provide more reliable predictions.

For the complete methodology, statistical analysis, discussion, and conclusions, see the full technical report in [`docs/Extended_Essay.pdf`](docs/Extended_Essay.pdf).

---

## Future Improvements

- Test additional machine learning models.
- Incorporate macroeconomic indicators.
- Evaluate deep learning approaches.
- Automate data updates.

---

## Data Sources

This project uses publicly available data from:

- **Yahoo Finance** (via the `yfinance` Python package)
  - Historical stock prices
  - ETF prices
  - Futures prices

- **United States Geological Survey (USGS)**
  - Historical U.S. metal production statistics

--- 

## Documentation

The original IB Extended Essay is available in the `docs` folder.

---

## License

MIT License
